.. _patterns-dependencyinjection:

.. _dependency-injection:

Dependency Injection
++++++++++++++++++++

  A dependency injection is a typehinted argument, that is stored in a property by the constructor.

.. code-block:: php
   
   <?php
   
   // Classic dependency injection 
   class foo {
       private $bar;
   
       public function __construct(Bar $bar) {
           $this->bar = $bar;
       }
   
       public function doSomething($args) {
           return $this->bar->barbar($args);
       }
   }
   
   // Without typehint, this is not a dependency injection
   class foo {
       private $bar;
   
       public function __construct($bar) {
           $this->bar = $bar;
       }
   }
   
   ?>

See also `Understanding Dependency Injection <http://php-di.org/doc/understanding-di.html>`_.

Connex PHP features
-------------------

  + `dependency-injection <https://php-dictionary.readthedocs.io/en/latest/dictionary/dependency-injection.ini.html>`_
  + `pattern <https://php-dictionary.readthedocs.io/en/latest/dictionary/pattern.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Patterns/DependencyInjection                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


