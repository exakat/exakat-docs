.. _structures-includeusage:

.. _inclusions:

Inclusions
++++++++++

.. meta::
	:description:
		Inclusions: List of all inclusions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Inclusions
	:twitter:description: Inclusions: List of all inclusions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Inclusions
	:og:type: article
	:og:description: List of all inclusions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/IncludeUsage.html
	:og:locale: en
List of all inclusions. Inclusions are made with include(), include_once(), require() and require_once().

.. code-block:: php
   
   <?php
   
   include 'library.php';
   
   // display is a function defined in 'library.php';
   display('Message');
   
   ?>

See also `Include <https://www.php.net/manual/en/function.include.php>`_ and `Require <https://www.php.net/manual/en/function.require.php>`_.

Connex PHP features
-------------------

  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/IncludeUsage                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


