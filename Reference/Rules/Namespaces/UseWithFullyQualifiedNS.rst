.. _namespaces-usewithfullyqualifiedns:

.. _use-with-fully-qualified-name:

Use With Fully Qualified Name
+++++++++++++++++++++++++++++

.. meta::
	:description:
		Use With Fully Qualified Name: Use statement doesn't require a fully qualified name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use With Fully Qualified Name
	:twitter:description: Use With Fully Qualified Name: Use statement doesn't require a fully qualified name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use With Fully Qualified Name
	:og:type: article
	:og:description: Use statement doesn't require a fully qualified name
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Namespaces/UseWithFullyQualifiedNS.html
	:og:locale: en
Use statement doesn't require a fully qualified name.

PHP manual recommends not to use fully qualified name (starting with \) when using the 'use' statement : they are "the leading backslash is unnecessary and not recommended, as import names must be fully qualified, and are not processed relative to the current namespace".

.. code-block:: php
   
   <?php
   
   // Recommended way to write a use statement.
   use  A\B\C\D as E;
   
   // No need to use the initial \
   use \A\B\C\D as F;
   
   ?>

Suggestions
___________

* Remove the initial \ in use expressions.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/UseWithFullyQualifiedNS                                                                                                                                                                                               |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


