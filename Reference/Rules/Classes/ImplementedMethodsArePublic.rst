.. _classes-implementedmethodsarepublic:

.. _implemented-methods-must-be-public:

Implemented Methods Must Be Public
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Implemented Methods Must Be Public: Class methods that are defined in an interface must be public.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Implemented Methods Must Be Public
	:twitter:description: Implemented Methods Must Be Public: Class methods that are defined in an interface must be public
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Implemented Methods Must Be Public
	:og:type: article
	:og:description: Class methods that are defined in an interface must be public
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/ImplementedMethodsArePublic.html
	:og:locale: en
Class methods that are defined in an interface must be public. They cannot be either private, nor protected.
This `error <https://www.php.net/error>`_ is not reported by lint, and is reported at execution time.

.. code-block:: php
   
   <?php
   
   interface i {
       function foo();
   }
   
   class X {
       // This method is defined in the interface : it must be public
       protected function foo() {}
       
       // other methods may be private
       private function bar() {}
   }
   
   ?>

See also `Interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_ and `Interfaces - the next level of abstraction <https://phpenthusiast.com/object-oriented-php-tutorials/interfaces>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Access+level+to+x%3A%3Afoo%28%29+must+be+public+%28as+in+class+i%29.html>`_



Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_
  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Make the implemented method public




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ImplementedMethodsArePublic                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.5                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


