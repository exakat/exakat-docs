.. _structures-opensslrandompseudobytesecondarg:

.. _openssl\_random\_pseudo\_byte()-second-argument:

openssl_random_pseudo_byte() Second Argument
++++++++++++++++++++++++++++++++++++++++++++

  openssl_random_pseudo_byte() uses exceptions to signal an `error <https://www.php.net/error>`_. Since PHP 7.4, there is no need to use the second argument.

On the other hand, it is important to catch the `exception <https://www.php.net/exception>`_ that openssl_random_pseudo_byte() may emit.

.. code-block:: php
   
   <?php
       // PHP 7.4 way to check on random number generation
       try {
           $bytes = openssl_random_pseudo_bytes($i);
       } catch(\Exception $e) {
           die("Error while loading random number");
       }
   
       // Old way to check on random number generation
       $bytes = openssl_random_pseudo_bytes($i, $cstrong);
       if ($cstrong === false) {
           die("Error while loading random number");
       }
   ?>

See also `openssl_random_pseudo_byte <https://www.php.net/openssl_random_pseudo_bytes>`_ and `PHP RFC: Improve openssl_random_pseudo_bytes() <https://wiki.php.net/rfc/improve-openssl-random-pseudo-bytes>`_.

Connex PHP features
-------------------

  + `openssl <https://php-dictionary.readthedocs.io/en/latest/dictionary/openssl.ini.html>`_


Suggestions
___________

* Skip the second argument, add a try/catch around the call to openssl_random_pseudo_bytes()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OpensslRandomPseudoByteSecondArg                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


