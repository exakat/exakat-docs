.. _php-noclassinglobal:

.. _no-class-in-global:

No Class In Global
++++++++++++++++++

.. meta\:\:
	:description:
		No Class In Global: Avoid defining structures in Global namespace.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Class In Global
	:twitter:description: No Class In Global: Avoid defining structures in Global namespace
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Class In Global
	:og:type: article
	:og:description: Avoid defining structures in Global namespace
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/NoClassInGlobal.html
	:og:locale: en
  Avoid defining structures in Global namespace. Always prefer using a namespace. This will come handy later, either when publishing the code, or when importing a library, or even if PHP reclaims that name.

.. code-block:: php
   
   <?php
   
   // Code prepared for later
   namespace Foo {
       class Bar {}
   }
   
   // Code that may conflict with other names.
   namespace {
       class Bar {}
   }
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `global-scope <https://php-dictionary.readthedocs.io/en/latest/dictionary/global-scope.ini.html>`_


Suggestions
___________

* Use a specific namespace for your classes




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoClassInGlobal                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.9                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-php-noclassinglobal`                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


