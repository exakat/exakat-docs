.. _complete-enumcasevalues:

.. _enum-case-values:

Enum Case Values
++++++++++++++++

.. meta\:\:
	:description:
		Enum Case Values: Adds a `DEFINITION`link between a static Enumeration case and its actual defined value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Enum Case Values
	:twitter:description: Enum Case Values: Adds a `DEFINITION`link between a static Enumeration case and its actual defined value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Enum Case Values
	:og:type: article
	:og:description: Adds a `DEFINITION`link between a static Enumeration case and its actual defined value
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/EnumCaseValues.html
	:og:locale: en
  Adds a `DEFINITION`link between a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ Enumeration case and its actual defined value. 

No link is added when no value is defined.

.. code-block:: php
   
   <?php
   
   enum E: string {
      case Foo = 'foo';
   }
   
   // Constants
   const C = E::Foo->name;  
   
   ?>
Connex PHP features
-------------------

  + `enum <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum.ini.html>`_
  + `enum-backed <https://php-dictionary.readthedocs.io/en/latest/dictionary/enum-backed.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/EnumCaseValues                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


