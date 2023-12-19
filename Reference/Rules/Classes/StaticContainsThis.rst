.. _classes-staticcontainsthis:

.. _static-methods-can't-contain-$this:

Static Methods Can't Contain $this
++++++++++++++++++++++++++++++++++

  `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods are also called ``class methods`` : they may be called even if the class has no instantiated object. Thus, the local variable ``$this`` won't exist, PHP will set it to `NULL <https://www.php.net/manual/en/language.types.null.php>`_ as usual. 


.. code-block:: php
   
   <?php
   
   class foo {
       // Static method may access other static methods, or property, or none. 
       static function staticBar() {
           // This is not possible in a static method
           return self::otherStaticBar() . static::$staticProperty;
       }
   
       static function bar() {
           // This is not possible in a static method
           return $this->property;
       }
   }
   
   ?>


Either this is not a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, which is fixed by removing the ``static`` keyword, or replace all `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ mention by `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties ``Class\:\:$property``.

See also `Static Keyword <https://www.php.net/manual/en/language.oop5.static.php>``Static Keyword <https://www.php.net/manual/en/language.oop5.static.php>`_.


Suggestions
___________

* Remove any $this usage
* Turn any $this usage into a static call : $this->foo() => self::foo()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/StaticContainsThis                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | $this, static                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-static-this <https://github.com/dseguy/clearPHP/tree/master/rules/no-static-this.md>`__                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-classes-staticcontainsthis`, :ref:`case-sugarcrm-classes-staticcontainsthis`                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


