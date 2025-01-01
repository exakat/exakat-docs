.. _classes-unusedconstant:

.. _unused-class-constant:

Unused Class Constant
+++++++++++++++++++++

.. meta::
	:description:
		Unused Class Constant: The class constant is unused.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Class Constant
	:twitter:description: Unused Class Constant: The class constant is unused
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Class Constant
	:og:type: article
	:og:description: The class constant is unused
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UnusedConstant.html
	:og:locale: en
The class constant is unused. Consider removing it or using it.

Class constants may be used in expressions, in `static <https://www.php.net/manual/en/language.oop5.static.php>`_ expressions, when building other constants, or in default values.

.. code-block:: php
   
   <?php
   
   class foo {
       public const UNUSED = 1; // No mention in the code
       
       private const USED = 2;  // used constant
       
       function bar() {
           echo self::USED;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `class-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_


Suggestions
___________

* Remove the class constant
* Use the class constant




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnusedConstant                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


