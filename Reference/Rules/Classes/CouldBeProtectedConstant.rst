.. _classes-couldbeprotectedconstant:

.. _could-be-protected-class-constant:

Could Be Protected Class Constant
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Could Be Protected Class Constant: Class constant may use 'protected' visibility.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Protected Class Constant
	:twitter:description: Could Be Protected Class Constant: Class constant may use 'protected' visibility
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Protected Class Constant
	:og:type: article
	:og:description: Class constant may use 'protected' visibility
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Protected Class Constant.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeProtectedConstant.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeProtectedConstant.html","name":"Could Be Protected Class Constant","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Class constant may use 'protected' visibility","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Protected Class Constant.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Class constant may use 'protected' visibility. 

Since PHP 7.1, constants may also have a public/protected/private visibility. This restrict their usage to anywhere, class and children or class. 

As a general rule, it is recommended to make constant 'private' by default, and to relax this restriction as needed. PHP makes them public by default.

.. code-block:: php
   
   <?php
   
   class foo {
       // pre-7.1 style
       const PRE_71_CONSTANT = 1;
       
       // post-7.1 style
       protected const PROTECTED_CONSTANT = 2;
       public const PUBLIC_CONSTANT = 3;
   }
   
   class foo2 extends foo {
       function bar() {
           // PROTECTED_CONSTANT may only be used in its class or its children
           echo self::PROTECTED_CONSTANT;
       }
   }
   
   class foo3 extends foo {
       function bar() {
           // PROTECTED_CONSTANT may only be used in its class or any of its children
           echo self::PROTECTED_CONSTANT;
       }
   }
   
   // Other constants may be used anywhere
   function x($a = foo::PUBLIC_CONSTANT) {
       echo $a.' '.foo:PRE_71_CONSTANT;
   }
   
   ?>
Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_
  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_


Suggestions
___________

* Use protected visibility with the reported constants.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeProtectedConstant                                                                                         |
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


