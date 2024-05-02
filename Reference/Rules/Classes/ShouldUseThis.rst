.. _classes-shouldusethis:

.. _should-use-local-class:

Should Use Local Class
++++++++++++++++++++++

  Methods should use the defining class, or be functions.

Methods should use ``$this`` with another method or a property, or call ``parent\:\:``. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods should call another `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, or a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property. 
Methods which are overwritten by a child class are omitted : the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class act as a default value for the children class, and this is correct.
Note that a method using a class constant is not considered as using the local class, for this analyzer.

.. code-block:: php
   
   <?php
   
   class foo {
       public function __construct() {
           // This method should do something locally, or be removed.
       }
   }
   
   class bar extends foo {
       private $a = 1;
       
       public function __construct() {
           // Calling parent:: is sufficient
           parent::__construct();
       }
   
       public function barbar() {
           // This is acting on the local object
           $this->a++;
       }
   
       public function barfoo($b) {
           // This has no action on the local object. It could be a function or a closure where needed
           return 3 + $b;
       }
   }
   
   ?>

Suggestions
___________

* Make this method a function
* Actually use $this, or any related attributes of the class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ShouldUseThis                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | $this, self                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `not-a-method <https://github.com/dseguy/clearPHP/tree/master/rules/not-a-method.md>`__                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


