.. _php-reservedkeywords7:

.. _reserved-keywords-in-php-7:

Reserved Keywords In PHP 7
++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Reserved Keywords In PHP 7: PHP reserved names for class/trait/interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Reserved Keywords In PHP 7
	:twitter:description: Reserved Keywords In PHP 7: PHP reserved names for class/trait/interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Reserved Keywords In PHP 7
	:og:type: article
	:og:description: PHP reserved names for class/trait/interface
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/ReservedKeywords7.html
	:og:locale: en
  PHP reserved names for class/trait/interface. They won't be available anymore in user space starting with PHP 7.

For example, string, float, false, true, null, resource,`... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ are not acceptable as class name.

.. code-block:: php
   
   <?php
   
   // This doesn't compile in PHP 7.0 and more recent
   class null { }
   
   ?>

See also `List of other reserved words <https://www.php.net/manual/en/reserved.other-reserved-words.php>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Avoid using PHP reserved keywords as names for structures such as class, functions, etc.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ReservedKeywords7                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and older                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


