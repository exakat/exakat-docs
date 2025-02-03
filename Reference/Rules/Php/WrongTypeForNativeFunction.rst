.. _php-wrongtypefornativefunction:

.. _wrong-type-for-native-php-function:

Wrong Type For Native PHP Function
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Wrong Type For Native PHP Function: This rule reports calls to a PHP native function with values of the wrong type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Type For Native PHP Function
	:twitter:description: Wrong Type For Native PHP Function: This rule reports calls to a PHP native function with values of the wrong type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Type For Native PHP Function
	:og:type: article
	:og:description: This rule reports calls to a PHP native function with values of the wrong type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Type For Native PHP Function.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/WrongTypeForNativeFunction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/WrongTypeForNativeFunction.html","name":"Wrong Type For Native PHP Function","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This rule reports calls to a PHP native function with values of the wrong type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Type For Native PHP Function.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This rule reports calls to a PHP native function with values of the wrong type. With modern PHP versions and strict_typing, it generates a Fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // valid calls
   echo exp(1);
   echo exp(2.5);
   
   // invalid calls
   echo exp("1");  // OK without strict types
   echo exp(array(2.5)); // always a fatal error
   
   // valid call, but invalid math
   // -1 is not a valid value for log(), but -1 is a valid type (int) : it is not reported by this analysis.
   echo log(-1);
   ?>

See also `PHP 7.1 no longer converts string to arrays the first time a value is assigned with square bracket notation <https://www.drupal.org/project/adaptivetheme/issues/2832900>`_.

Related PHP errors 
-------------------

  + `Argument #1 must be of type float, string given <https://php-errors.readthedocs.io/en/latest/messages/argument-%23%25d-%28%24%25s%29-must-be-of-type-%25s%2C-%25s-given.html>`_




Suggestions
___________

* Set the code to the valid type, when calling a PHP native function




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/WrongTypeForNativeFunction                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


