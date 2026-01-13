.. _classes-uselesstypehint:

.. _useless-typehint:

Useless Typehint
++++++++++++++++

  `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_ magic methods won't enforce any typehint. The name of the magic property is always cast to string.

`__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_

.. code-block:: php
   
   <?php
   
   class x {
       // typehint is set and ignored
       function __set(float $name, string $value) {
           $this->$name = $value;
       }
   
       // typehint is set and ignored
       function __get(integer $name) {
           $this->$name = $value;
       }
   
       // typehint is checked by PHP 8.0 linting
       // typehint is enforced by PHP 7.x
       function __call(integer $name) {
           $this->$name = $value;
       }
   }
   
   $o = new x;
   $b = array();
   // Property will be called 'Array'
   $o->{$b} = 2;
   
   // type of $m is check at calling time. It must be string.
   $o->{$m}();
   
   ?>

See also `__set <https://www.php.net/manual/en/language.oop5.overloading.php#object.set>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Method+name+must+be+a+string.html>`_



Connex PHP features
-------------------

  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Use `string` for the `$name` parameter
* Use no typehint for the `$name` parameter




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UselessTypehint                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


