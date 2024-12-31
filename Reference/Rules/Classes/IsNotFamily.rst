.. _classes-isnotfamily:

.. _is-not-class-family:

Is Not Class Family
+++++++++++++++++++

.. meta\:\:
	:description:
		Is Not Class Family: Mark a static method call as inside the family of classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is Not Class Family
	:twitter:description: Is Not Class Family: Mark a static method call as inside the family of classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is Not Class Family
	:og:type: article
	:og:description: Mark a static method call as inside the family of classes
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/IsNotFamily.html
	:og:locale: en
  Mark a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method call as inside the family of classes. Children are not considered here.

.. code-block:: php
   
   <?php
   
   class a {
       function familyMethod() {}
   }
   
   classs b {
       function foo() {
           self::familyMethod(); // This is a call to a family method
           b::notAFamilyMethod(); // This is a call to a method of a class outside the family
       }
   }
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IsNotFamily                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


