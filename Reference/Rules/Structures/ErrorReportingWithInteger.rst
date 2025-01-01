.. _structures-errorreportingwithinteger:

.. _error\_reporting()-with-integers:

error_reporting() With Integers
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		error_reporting() With Integers: Using named constants with error_reporting is strongly encouraged to ensure compatibility for future versions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: error_reporting() With Integers
	:twitter:description: error_reporting() With Integers: Using named constants with error_reporting is strongly encouraged to ensure compatibility for future versions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: error_reporting() With Integers
	:og:type: article
	:og:description: Using named constants with error_reporting is strongly encouraged to ensure compatibility for future versions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ErrorReportingWithInteger.html
	:og:locale: en
Using named constants with error_reporting is strongly encouraged to ensure compatibility for future versions. As `error <https://www.php.net/error>`_ levels are added, the range of integers increases, so older integer-based `error <https://www.php.net/error>`_ levels will not always behave as expected. (Adapted from the documentation).

.. code-block:: php
   
   <?php
   
   // This is ready for PHP next version
   error_reporting(E_ALL & ~E_DEPRECATED & ~E_STRICT & ~E_NOTICE & ~E_WARNING);
   
   // This is not ready for PHP next version
   error_reporting(2047);
   
   // -1 and 0 are omitted, as they will be valid even is constants changes.
   error_reporting(-1);
   error_reporting(0);
   
   ?>

See also `directive error_reporting <https://www.php.net/manual/en/errorfunc.configuration.php#ini.error-reporting>`_ and `error_reporting <https://www.php.net/manual/en/function.error-reporting.php>`_.


Suggestions
___________

* Always use the constant combination when configuring error_reporting or any PHP native function




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ErrorReportingWithInteger                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-sugarcrm-structures-errorreportingwithinteger`                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


