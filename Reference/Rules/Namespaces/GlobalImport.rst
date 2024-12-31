.. _namespaces-globalimport:

.. _global-import:

Global Import
+++++++++++++

.. meta\:\:
	:description:
		Global Import: This rule marks a ``use`` statement that imports a global class in the current file.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Global Import
	:twitter:description: Global Import: This rule marks a ``use`` statement that imports a global class in the current file
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Global Import
	:og:type: article
	:og:description: This rule marks a ``use`` statement that imports a global class in the current file
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Namespaces/GlobalImport.html
	:og:locale: en
  This rule marks a ``use`` statement that imports a global class in the current file.

.. code-block:: php
   
   <?php
   
   namespace Foo {
       // This is a global import
       use Stdclass;
   }
   ?>
Connex PHP features
-------------------

  + `namespace <https://php-dictionary.readthedocs.io/en/latest/dictionary/namespace.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/GlobalImport                                                                                                 |
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


