.. _structures-randomwithouttry:

.. _random-without-try:

Random Without Try
++++++++++++++++++

  `random_int() <https://www.php.net/random_int>`_ and `random_bytes() <https://www.php.net/random_bytes>`_ require a try/catch structure around them.

`random_int() <https://www.php.net/random_int>`_ and `random_bytes() <https://www.php.net/random_bytes>`_ emit Exceptions if they meet a problem. This way, failure can't be mistaken with returning an empty value, which leads to lower security. 
Since PHP 7.4, `openssl_random_pseudo_bytes() <https://www.php.net/openssl_random_pseudo_bytes>`_ has adopted the same behavior. It is included in this analysis : check your PHP version for actual application.

.. code-block:: php
   
   <?php
   
   try {
       $salt = random_bytes($length);
   } catch (TypeError $e) {
       // Error while reading the provided parameter
   } catch (Exception $e) {
       // Insufficient random data generated
   } catch (Error $e) {
       // Error with the provided parameter : <= 0
   }
   
   ?>
Connex PHP features
-------------------

  + `random <https://php-dictionary.readthedocs.io/en/latest/dictionary/random.ini.html>`_


Suggestions
___________

* Add a try/catch structure around calls to random_int() and random_bytes().




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/RandomWithoutTry                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


