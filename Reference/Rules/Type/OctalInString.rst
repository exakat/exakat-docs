.. _type-octalinstring:


.. _invalid-octal-in-string:

Invalid Octal In String
+++++++++++++++++++++++

.. meta::
	:description:
		Invalid Octal In String: Any octal sequence inside a string can't be go \377.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Invalid Octal In String
	:twitter:description: Invalid Octal In String: Any octal sequence inside a string can't be go \377
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Invalid Octal In String
	:og:type: article
	:og:description: Any octal sequence inside a string can't be go \377
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Invalid Octal In String.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/OctalInString.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/OctalInString.html","name":"Invalid Octal In String","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Any octal sequence inside a string can't be go \\377","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Invalid Octal In String.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Any octal sequence inside a string can't be go \377. Those will be a fatal `error <https://www.php.net/error>`_ at parsing time. 

The check is applied to the string, starting with PHP 7.1. In PHP 7.0 and older, those sequences were silently adapted (modulo/% \400).

.. code-block:: php
   
   <?php
   
   // A valid octal in a PHP string
   echo "\100"; // @
   
   // Emit a warning in PHP 7.1
   //Octal escape sequence overflow \500 is greater than \377
   echo "\500"; // @
   
   // Silent conversion
   echo "\478"; // 8
   
   ?>

See also `Integers <https://www.php.net/manual/en/language.types.integer.php>`_.

Related PHP errors 
-------------------

  + `Octal escape sequence overflow \500 is greater than \377 <https://php-errors.readthedocs.io/en/latest/messages/octal-escape-sequence-overflow-%5C%5C%25s-is-greater-than-%5C%5C377.html>`_




Suggestions
___________

* Use a double slash to avoid the sequence to be an octal sequence
* Use a function call, such as decoct() to convert larger number to octal notation




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/OctalInString                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`Inventory <ruleset-Inventory>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.1                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.1 and older                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


