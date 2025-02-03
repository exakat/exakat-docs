.. _classes-couldbeprivateconstante:

.. _could-be-private-class-constant:

Could Be Private Class Constant
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Could Be Private Class Constant: Class constant may use ``private`` visibility.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Private Class Constant
	:twitter:description: Could Be Private Class Constant: Class constant may use ``private`` visibility
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Private Class Constant
	:og:type: article
	:og:description: Class constant may use ``private`` visibility
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Private Class Constant.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBePrivateConstante.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBePrivateConstante.html","name":"Could Be Private Class Constant","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Class constant may use ``private`` visibility","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Private Class Constant.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Class constant may use ``private`` visibility. 

Since PHP 7.1, constants may also have a public/protected/private visibility. This restrict their usage to anywhere, class and children or class. 

As a general rule, it is recommended to make constant ``private`` by default, and to relax this restriction as needed. PHP makes them public by default.
Constant shall stay ``public`` when the code has to be compatible with PHP 7.0 and older. 

They also have to be public in the case of component : some of those constants have to be used by external actors, in order to configure the component.

.. code-block:: php
   
   <?php
   
   class foo {
       // pre-7.1 style
       const PRE_71_CONSTANT = 1;
       
       // post-7.1 style
       private const PRIVATE_CONSTANT = 2;
       public const PUBLIC_CONSTANT = 3;
       
       function bar() {
           // PRIVATE CONSTANT may only be used in its class
           echo self::PRIVATE_CONSTANT;
       }
   }
   
   // Other constants may be used anywhere
   function x($a = foo::PUBLIC_CONSTANT) {
       echo $a.' '.foo:PRE_71_CONSTANT;
   }
   
   ?>

See also `Class Constants <https://www.php.net/manual/en/language.oop5.constants.php>`_.

Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBePrivateConstante                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.10                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phinx-classes-couldbeprivateconstante`                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


