.. _php-coulduseiscountable:

.. _use-is\_countable:

Use is_countable
++++++++++++++++

  `is_countable() <https://www.php.net/is_countable>`_ checks if a variables holds a value that can be counted. It is recommended to use it before calling `count() <https://www.php.net/count>`_.

`is_countable() <https://www.php.net/is_countable>`_ accepts arrays and object whose class implements \`countable <https://www.php.net/countable>`_.

.. code-block:: php
   
   <?php
   
   function foo($arg) {
       if (!is_countable($arg)) {
           // $arg cannot be passed to count()
           return 0
       }
       return count($arg);
   }
   
   function bar($arg) {
       if (!is_array($arg) and !$x instanceof \Countable) {
           // $arg cannot be passed to count()
           return 0
       }
   
       return count($arg);
   }
   
   ?>

See also `PHP RFC: is_countable <https://wiki.php.net/rfc/is-countable>`_.


Suggestions
___________

* Use is_countable()
* Create a compatibility function that replaces is_countable() until the code is ready for PHP 7.3




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CouldUseIsCountable                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.3 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | array, countable                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


