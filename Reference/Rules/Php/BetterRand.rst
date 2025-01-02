.. _php-betterrand:

.. _use-random\_int():

Use random_int()
++++++++++++++++

.. meta::
	:description:
		Use random_int(): rand() and mt_rand() should be replaced with random_int().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use random_int()
	:twitter:description: Use random_int(): rand() and mt_rand() should be replaced with random_int()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use random_int()
	:og:type: article
	:og:description: rand() and mt_rand() should be replaced with random_int()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use random_int().html
	:og:locale: en
`rand() <https://www.php.net/rand>`_ and `mt_rand() <https://www.php.net/mt_rand>`_ should be replaced with `random_int() <https://www.php.net/random_int>`_.

At worse, `rand() <https://www.php.net/rand>`_ should be replaced with `mt_rand() <https://www.php.net/mt_rand>`_, which is a drop-in replacement and `srand() <https://www.php.net/srand>`_ by `mt_srand() <https://www.php.net/mt_srand>`_. 

`random_int() <https://www.php.net/random_int>`_ replaces `rand() <https://www.php.net/rand>`_, and has no seeding function like `srand() <https://www.php.net/srand>`_.

Other sources of entropy that should be replaced by `random_int() <https://www.php.net/random_int>`_ : `microtime() <https://www.php.net/microtime>`_, `uniqid() <https://www.php.net/uniqid>`_, `time() <https://www.php.net/time>`_. Those a often combined with hashing functions and mixed with other sources of entropy, such as a salt.
Since PHP 7, `random_int() <https://www.php.net/random_int>`_ along with `random_bytes() <https://www.php.net/random_bytes>`_, provides cryptographically `secure <https://www.php.net/secure>`_ pseudo-random bytes, which are good to be used
when security is involved. `openssl_random_pseudo_bytes() <https://www.php.net/openssl_random_pseudo_bytes>`_ may be used when the ``OpenSSL`` extension is available.

.. code-block:: php
   
   <?php
   
   // Avoid using this
   $random = rand(0, 10);
   
   // Drop-in replacement
   $random = mt_rand(0, 10);
   
   // Even better but different : 
   // valid with PHP 7.0+
   try {
       $random = random_int(0, 10);
   } catch (\Exception $e) {
       // process case of not enoug random values
   }
   
   // This is also a source of entropy, based on srand()
   // random_int() is a drop-in replacement here
   $a = sha256(uniqid());
   
   ?>

See also `CSPRNG <https://www.php.net/manual/en/book.csprng.php>`_ and `OpenSSL <https://www.php.net/manual/en/book.openssl.php>`_.

Connex PHP features
-------------------

  + `random <https://php-dictionary.readthedocs.io/en/latest/dictionary/random.ini.html>`_


Suggestions
___________

* Use random_bytes() and randon_int(). At least, use them as a base for random data, and then add extra prefix and suffix, and a hash call on top.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/BetterRand                                                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`Security <ruleset-Security>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thelia-php-betterrand`, :ref:`case-fuelcms-php-betterrand`                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


