.. _php-declarestricttype:

.. _declare-strict\_types-usage:

Declare strict_types Usage
++++++++++++++++++++++++++

.. meta::
	:description:
		Declare strict_types Usage: Usage of ``strict_types``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Declare strict_types Usage
	:twitter:description: Declare strict_types Usage: Usage of ``strict_types``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Declare strict_types Usage
	:og:type: article
	:og:description: Usage of ``strict_types``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/DeclareStrictType.html
	:og:locale: en
Usage of ``strict_types``. By default, PHP attempts to change the original type to match the type specified by the type-declaration. With an explicit ``strict_types`` declaration, PHP ensures that the incoming argument has the exact type. 

``strict_types`` were introduced in PHP 7.0.

.. code-block:: php
   
   <?php
   
   // Setting strict_types;
       declare(strict_types = 1);
   
       function foo(int $i) {
           echo $i;
       }
   
       // Always valid : displays 1
       foo(1);
       // with strict types, this emits an error
       // without strict types, this displays 1
       foo(1.7);
   
   ?>

See also `declare <https://www.php.net/manual/en/control-structures.declare.php>`_.

Connex PHP features
-------------------

  + `declare <https://php-dictionary.readthedocs.io/en/latest/dictionary/declare.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DeclareStrictType                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.1                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


