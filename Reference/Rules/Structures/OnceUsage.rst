.. _structures-onceusage:

.. _include\_once()-usage:

include_once() Usage
++++++++++++++++++++

.. meta::
	:description:
		include_once() Usage: This rules reports sage of ``include_once()`` and ``require_once()``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: include_once() Usage
	:twitter:description: include_once() Usage: This rules reports sage of ``include_once()`` and ``require_once()``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: include_once() Usage
	:og:type: article
	:og:description: This rules reports sage of ``include_once()`` and ``require_once()``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/OnceUsage.html
	:og:locale: en
This rules reports sage of ``include_once()`` and ``require_once()``. Those functions should be avoided for performances reasons.

Try using autoload for loading classes, or use include() or require() and make it possible to include several times the same file without errors.

.. code-block:: php
   
   <?php
   
   // Including a library. 
   include 'lib/helpers.inc';
   
   // Including a library, and avoiding double inclusion
   include_once 'lib/helpers.inc';
   
   ?>
Connex PHP features
-------------------

  + `include <https://php-dictionary.readthedocs.io/en/latest/dictionary/include.ini.html>`_
  + `include_once <https://php-dictionary.readthedocs.io/en/latest/dictionary/include_once.ini.html>`_


Suggestions
___________

* Avoid using include_once() whenever possible 
* Use autoload() to load classes, and avoid loading them with include




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OnceUsage                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xoops-structures-onceusage`, :ref:`case-tikiwiki-structures-onceusage`                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


