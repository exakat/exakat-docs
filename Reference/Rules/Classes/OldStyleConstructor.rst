.. _classes-oldstyleconstructor:

.. _old-style-constructor:

Old Style Constructor
+++++++++++++++++++++

.. meta::
	:description:
		Old Style Constructor: PHP classes used to have the method bearing the same name as the class acts as the constructor.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Old Style Constructor
	:twitter:description: Old Style Constructor: PHP classes used to have the method bearing the same name as the class acts as the constructor
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Old Style Constructor
	:og:type: article
	:og:description: PHP classes used to have the method bearing the same name as the class acts as the constructor
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Old Style Constructor.html
	:og:locale: en
PHP classes used to have the method bearing the same name as the class acts as the constructor. That was PHP 4, and early PHP 5. 

The manual issues a warning about this syntax : ``Old style constructors are DEPRECATED in PHP 7.0, and will be removed in a future version. You should always use `__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_ in new code.``
This is no more the case in PHP 5, which relies on ``__construct()`` to do so. Having this old style constructor may bring in confusion, unless you are also supporting old time PHP 4.

Note that classes with methods bearing the class name, but inside a namespace are not following this convention, as this is not breaking backward compatibility. Those are excluded from the analyze.

.. code-block:: php
   
   <?php
   
   namespace {
       // Global namespace is important
       class foo {
           function foo() {
               // This acts as the old-style constructor, and is reported by PHP
           }
       }
   
       class bar {
           function __construct() { }
           function bar() {
               // This doesn't act as constructor, as bar has a __construct() method
           }
       }
   }
   
   namespace Foo\Bar{
       class foo {
           function foo() {
               // This doesn't act as constructor, as bar is not in the global namespace
           }
       }
   }
   
   ?>

See also  `Constructors and Destructors <https://www.php.net/manual/en/language.oop5.decon.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Old+style+constructors+are+DEPRECATED+in+PHP+7.0%2C+and+will+be+removed+in+a+future+version.+You+should+always+use+%60%60__construct%28%29%60%60+in+new+code..html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Methods+with+the+same+name+as+their+class+will+not+be+constructors+in+a+future+version+of+PHP%3B+%25s+has+a+deprecated+constructor.html>`_



Connex PHP features
-------------------

  + `constructor <https://php-dictionary.readthedocs.io/en/latest/dictionary/constructor.ini.html>`_


Suggestions
___________

* Remove old style constructor and make it ``__construct()``
* Remove old libraries and use a modern component




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/OldStyleConstructor                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-php4-class-syntax <https://github.com/dseguy/clearPHP/tree/master/rules/no-php4-class-syntax.md>`__                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


