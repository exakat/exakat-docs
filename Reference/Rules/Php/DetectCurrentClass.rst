.. _php-detectcurrentclass:

.. _detect-current-class:

Detect Current Class
++++++++++++++++++++

  Detecting the current class should be done with `self\:\:class` or `static\:\:class` operator.

`__CLASS__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ may be replaced by ``self\:\:class``. 
`get_called_class() <https://www.php.net/get_called_class>`_ may be replaced by ``static\:\:class``. 

`__CLASS__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ and `get_called_class() <https://www.php.net/get_called_class>`_ are set to be deprecated in PHP 7.4. 


.. code-block:: php
   
   <?php
   
   class X {
       function foo() {
           echo __CLASS__."\n";          // X
           echo self::class."\n";        // X
           
           echo get_called_class()."\n";  // Y
           echo static::class."\n";       // Y
       }
   }
   
   class Y extends X {}
   
   $y = new Y();
   $y->foo();
   
   ?>

See also `PHP RFC: Deprecations for PHP 7.4 <https://wiki.php.net/rfc/deprecations_php_7_4>`_.


Suggestions
___________

* Use the self::class operator to detect the current class name, instead of __CLASS__ and get_class().
* Use the static::class operator to detect the current called class name, instead of get_called_class().




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DetectCurrentClass                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`, :ref:`Suggestions <ruleset-Suggestions>`                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.8                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | class                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


