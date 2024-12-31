.. _enums-nomagicmethod:

.. _no-magic-method-for-enum:

No Magic Method For Enum
++++++++++++++++++++++++

.. meta\:\:
	:description:
		No Magic Method For Enum: Enumeration cannot have magic methods, nor a constructor.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Magic Method For Enum
	:twitter:description: No Magic Method For Enum: Enumeration cannot have magic methods, nor a constructor
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Magic Method For Enum
	:og:type: article
	:og:description: Enumeration cannot have magic methods, nor a constructor
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Enums/NoMagicMethod.html
	:og:locale: en
  Enumeration cannot have magic methods, nor a constructor. Enumeration cases are created as needed, and magic methods are interfering with the default behavior of enumerations.

.. code-block:: php
   
   <?php
   
   enum a {
       function __construct($a) {}
   }
   
   ?>

See also `Enumeration Methods <https://www.php.net/manual/en/language.enumerations.methods.php>`_.

Related PHP errors 
-------------------

  + `Enum may not include __construct <https://php-errors.readthedocs.io/en/latest/messages/enum-%25s-cannot-include-magic-method-%25s.html>`_
  + `Enum may not include __isset <https://php-errors.readthedocs.io/en/latest/messages/enum-%25s-cannot-include-magic-method-%25s.html>`_



Connex PHP features
-------------------

  + `enumeration <https://php-dictionary.readthedocs.io/en/latest/dictionary/enumeration.ini.html>`_
  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Remove the method




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Enums/NoMagicMethod                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


