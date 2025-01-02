.. _classes-dynamicmethodcall:

.. _dynamic-methodcall:

Dynamic Methodcall
++++++++++++++++++

.. meta::
	:description:
		Dynamic Methodcall: Dynamic calls to class methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Methodcall
	:twitter:description: Dynamic Methodcall: Dynamic calls to class methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Methodcall
	:og:type: article
	:og:description: Dynamic calls to class methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dynamic Methodcall.html
	:og:locale: en
Dynamic calls to class methods.

.. code-block:: php
   
   <?php
   
   class x {
       static public function foo() {}
              public function bar() {}
   }
   
   $staticmethod = 'foo';
   // dynamic static method call to x::foo()
   x::$staticmethod();
   
   $method = 'bar';
   // dynamic method call to bar()
   $object = new x();
   $object->$method();
   
   ?>
Connex PHP features
-------------------

  + `dynamic-call <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-call.ini.html>`_
  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DynamicMethodCall                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


