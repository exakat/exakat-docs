.. _php-password55:


.. _use-password\_hash():

Use password_hash()
+++++++++++++++++++


.. meta::

	:description:

		Use password_hash(): password_hash() and password_check() are a better choice to replace the use of crypt() to check password.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Use password_hash()

	:twitter:description: Use password_hash(): password_hash() and password_check() are a better choice to replace the use of crypt() to check password

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Use password_hash()

	:og:type: article

	:og:description: password_hash() and password_check() are a better choice to replace the use of crypt() to check password

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use password_hash().html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Password55.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Password55.html","name":"Use password_hash()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"password_hash() and password_check() are a better choice to replace the use of crypt() to check password","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use password_hash().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`password_hash() <https://www.php.net/password_hash>`_ and password_check() are a better choice to replace the use of `crypt() <https://www.php.net/crypt>`_ to check password.

PHP 5.5 introduced these functions.

.. code-block:: php
   
   <?php
   
   $password = 'rasmuslerdorf';
   $hash = '$2y$10$YCFsG6elYca568hBi2pZ0.3LDL5wjgxct1N8w/oLR/jfHsiQwCqTS';
   
   // The cost parameter can change over time as hardware improves
   $options = array('cost' => 11);
   
   // Verify stored hash against plain-text password
   if (password_verify($password, $hash)) {
       // Check if a newer hashing algorithm is available
       // or the cost has changed
       if (password_needs_rehash($hash, PASSWORD_DEFAULT, $options)) {
           // If so, create a new hash, and replace the old one
           $newHash = password_hash($password, PASSWORD_DEFAULT, $options);
       }
   
       // Log user in
   }
   ?>

See also `Password hashing <https://www.php.net/manual/en/book.password.php>`_.


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Password55                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


