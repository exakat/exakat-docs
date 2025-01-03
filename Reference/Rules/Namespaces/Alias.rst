.. _namespaces-alias:

.. _aliases:

Aliases
+++++++

.. meta::
	:description:
		Aliases: This rule lists all aliases.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Aliases
	:twitter:description: Aliases: This rule lists all aliases
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Aliases
	:og:type: article
	:og:description: This rule lists all aliases
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Aliases.html
	:og:locale: en
This rule lists all aliases. Aliases are used file by file, although some classes may have different aliases depending on the context.

.. code-block:: php
   
   <?php
   
   // This is an alias
   use stdClass as aClass;
   
   // This is not an alias : it is not explicit
   use stdClass;
   
   trait t {
       // This is not an alias, it's a trait usage
       use otherTrait;
   }
   
   ?>

See also `Using namespaces: Aliasing/Importing <https://www.php.net/manual/en/language.namespaces.importing.php>`_ and `A Complete Guide to PHP Namespaces <https://www.thoughtfulcode.com/a-complete-guide-to-php-namespaces/>`_.

Connex PHP features
-------------------

  + `namespace <https://php-dictionary.readthedocs.io/en/latest/dictionary/namespace.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/Alias                                                                                                                                                                        |
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


