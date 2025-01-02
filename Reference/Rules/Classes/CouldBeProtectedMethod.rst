.. _classes-couldbeprotectedmethod:

.. _could-be-protected-method:

Could Be Protected Method
+++++++++++++++++++++++++

.. meta::
	:description:
		Could Be Protected Method: Those methods are declared 'public', but are never used publicly.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Protected Method
	:twitter:description: Could Be Protected Method: Those methods are declared 'public', but are never used publicly
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Protected Method
	:og:type: article
	:og:description: Those methods are declared 'public', but are never used publicly
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Protected Method.html
	:og:locale: en
Those methods are declared 'public', but are never used publicly. They may be made 'protected'. 

These properties may even be made private.

.. code-block:: php
   
   <?php
   
   class foo {
       // Public, and used publicly
       public publicMethod() {}
   
       // Public, but never used outside the class or its children
       public protectedMethod() {}
       
       private function bar() {
           $this->protectedMethod();
       }
   }
   
   $foo = new Foo();
   $foo->publicMethod();
   
   ?>
Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_
  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Use protected visibility with these methods.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeProtectedMethod                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.11                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


