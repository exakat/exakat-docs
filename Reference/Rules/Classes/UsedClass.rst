.. _classes-usedclass:

.. _used-classes:

Used Classes
++++++++++++

.. meta::
	:description:
		Used Classes: The following classes are used in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Classes
	:twitter:description: Used Classes: The following classes are used in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Classes
	:og:type: article
	:og:description: The following classes are used in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Used Classes.html
	:og:locale: en
The following classes are used in the code.

Classes may be use when they are instantiated, or with `static <https://www.php.net/manual/en/language.oop5.static.php>`_ calls

.. code-block:: php
   
   <?php
   
   class unusedClasss { const X = 1;}
   class usedClass {}
   
   $y = new usedClass(usedClass::X);
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UsedClass                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


