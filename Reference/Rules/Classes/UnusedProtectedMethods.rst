.. _classes-unusedprotectedmethods:

.. _unused-protected-methods:

Unused Protected Methods
++++++++++++++++++++++++

.. meta\:\:
	:description:
		Unused Protected Methods: The following protected methods are unused in children class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Protected Methods
	:twitter:description: Unused Protected Methods: The following protected methods are unused in children class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Protected Methods
	:og:type: article
	:og:description: The following protected methods are unused in children class
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UnusedProtectedMethods.html
	:og:locale: en
  The following protected methods are unused in children class. As such, they may be considered for being private.

Methods reported by this analysis are not used by children, yet they are protected.
No usage of those methods were found. 

This analysis is impacted by dynamic method calls.

.. code-block:: php
   
   <?php
   
   class Foo {
       // This method is not used
       protected function unusedBar() {}
       protected function usedInFoo() {}
       protected function usedInFooFoo() {}
       
       public function bar2() {
           // some code
           $this->usedInFoo();
       }
   }
   
   class FooFoo extends Foo {
       protected function bar() {}
       
       public function bar2() {
           // some code
           $this->usedInFooFoo();
       }
   }
   
   class someOtherClass {
       protected function bar() {
           // This is not related to foo.
           $this->unusedbar();
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `unused <https://php-dictionary.readthedocs.io/en/latest/dictionary/unused.ini.html>`_


Suggestions
___________

* Make use of the protected method in the code
* Remove the method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnusedProtectedMethods                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`unused-public-methods`                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


