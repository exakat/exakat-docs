.. _security-comparehash:

.. _compare-hash:

Compare Hash
++++++++++++

  When comparing hash values, it is important to use the strict comparison : `hash_equals() <https://www.php.net/hash_equals>`_, ``===`` or ``!==``. 

In a number of situations, the hash value will start with ``0e``, and PHP will understand that the comparison involves integers : it will then convert the strings into numbers, and it may end up converting them to 0.

Here is an example : 


.. code-block:: php
   
   <?php
   
   // The two following passwords hashes matches, while they are not the same. 
   $hashed_password = 0e462097431906509000000000000;
   if (hash('md5','240610708',false) == $hashed_password) {
     print 'Matched.'.PHP_EOL;
   }
   
   // hash returns a string, that is mistaken with 0 by PHP
   // The strength of the hashing algorithm is not a problem
   if (hash('ripemd160','20583002034',false) == '0') {
     print 'Matched.'.PHP_EOL;
   }
   
   if (hash('md5','240610708',false) !== $hashed_password) {
     print 'NOT Matched.'.PHP_EOL;
   }
   
   // Display true
   var_dump(md5('240610708') == md5('QNKCDZO') );
   
   ?>


You may also use `password_hash() <https://www.php.net/password_hash>`_ and `password_verify() <https://www.php.net/password_verify>`_ : they work together without integer conversion problems, and they can't be confused with a number.

See also `Magic Hashes <https://blog.whitehatsec.com/magic-hashes/>`_ , `What is the best way to compare hashed strings? (PHP) <https://stackoverflow.com/questions/5211132/what-is-the-best-way-to-compare-hashed-strings-php/23959696#23959696>`_ and `md5('240610708') == md5('QNKCDZO') <https://news.ycombinator.com/item?id=9484757>`_.


Suggestions
___________

* Use dedicated functions for hash comparisons
* Use identity operators (===), and not equality operators (==) to compare hashes
* Compare hashes in the database (or external system), where such confusion is not possible




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/CompareHash                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Security <ruleset-Security>`                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | cryptography, hash                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `strict-comparisons <https://github.com/dseguy/clearPHP/tree/master/rules/strict-comparisons.md>`__                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-traq-security-comparehash`, :ref:`case-livezilla-security-comparehash`                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


