.. _classes-unusedmethods:

.. _unused-methods:

Unused Methods
++++++++++++++

.. meta::
	:description:
		Unused Methods: Those methods are never called.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Methods
	:twitter:description: Unused Methods: Those methods are never called
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Methods
	:og:type: article
	:og:description: Those methods are never called
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Methods.html
	:og:locale: en
Those methods are never called. 

They are probably dead code, unless they are called dynamically.

This analysis omits methods which are in a class that makes dynamical `self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ calls : ``$this->$m()``. That way, any method may be called. 

This analysis omits methods which are overwritten by a child class. That way, they are considered to provide a default behavior.

.. code-block:: php
   
   <?php
   
   class foo {
       public function used() {
           $this->used();
       }
   
       public function unused() {
           $this->used();
       }
   }
   
   class bar extends foo {
       public function some() {
           $this->used();
       }
   }
   
   $a = new foo();
   $a->used();
   
   ?>

See also `Dead Code: Unused Method <https://vulncat.fortify.com/en/detail?id=desc.structural.java.dead_code_unused_method>`_.

Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Make use of the method
* Remove the method
* Move the method to another class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnusedMethods                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`unused-public-methods`                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


