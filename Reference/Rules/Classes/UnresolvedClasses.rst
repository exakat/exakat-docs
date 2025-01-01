.. _classes-unresolvedclasses:

.. _unresolved-classes:

Unresolved Classes
++++++++++++++++++

.. meta::
	:description:
		Unresolved Classes: The following classes are instantiated in the code, but their definition couldn't be found in that same code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unresolved Classes
	:twitter:description: Unresolved Classes: The following classes are instantiated in the code, but their definition couldn't be found in that same code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unresolved Classes
	:og:type: article
	:og:description: The following classes are instantiated in the code, but their definition couldn't be found in that same code
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UnresolvedClasses.html
	:og:locale: en
The following classes are instantiated in the code, but their definition couldn't be found in that same code. They might be defined in an extension or an external component.

.. code-block:: php
   
   <?php
   
   class Foo extends Bar {
       private function foobar() {
           // here, parent is not resolved, as Bar is not defined in the code.
           return parent::$prop;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Check for namespaces and aliases and make sure they are correctly configured.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnresolvedClasses                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


