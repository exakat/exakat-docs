.. _classes-readonlyusage:

.. _readonly-usage:

Readonly Usage
++++++++++++++

.. meta\:\:
	:description:
		Readonly Usage: Usage of the readonly option on classes and properties.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Readonly Usage
	:twitter:description: Readonly Usage: Usage of the readonly option on classes and properties
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Readonly Usage
	:og:type: article
	:og:description: Usage of the readonly option on classes and properties
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/ReadonlyUsage.html
	:og:locale: en
  Usage of the readonly option on classes and properties. Readonly is available on classes starting with PHP 8.2.

.. code-block:: php
   
   <?php
   
   class x {
   	private readonly int $property = 1;
   }
   
   readonly class y {
   	private int $property = 1;
   }
   
   ?>

See also `Readonly properties <https://www.php.net/manual/en/language.oop5.properties.php#language.oop5.properties.readonly-properties>`_.

Connex PHP features
-------------------

  + `readonly <https://php-dictionary.readthedocs.io/en/latest/dictionary/readonly.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ReadonlyUsage                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


