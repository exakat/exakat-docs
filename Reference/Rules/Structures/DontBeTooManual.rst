.. _structures-dontbetoomanual:

.. _don't-be-too-manual:

Don't Be Too Manual
+++++++++++++++++++

.. meta::
	:description:
		Don't Be Too Manual: Adapt the examples from the PHP manual to the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Don't Be Too Manual
	:twitter:description: Don't Be Too Manual: Adapt the examples from the PHP manual to the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Don't Be Too Manual
	:og:type: article
	:og:description: Adapt the examples from the PHP manual to the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Don't Be Too Manual.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DontBeTooManual.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DontBeTooManual.html","name":"Don't Be Too Manual","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Adapt the examples from the PHP manual to the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Don't Be Too Manual.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Adapt the examples from the PHP manual to the code. Don't reuse directly the same names in the source: be more specific about what to expect in those variables.

Here are the variables names that are classic with specific functions: 

+ ``for($i = 0; $i < 10; ++$i) {}``, ``$j``, ``$k```
+ ``catch(`Exception <https://www.php.net/exception>`_ $e)``
+ ``$fp = fopen(`...) <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_``, ``$fh``
+ ``$conn = new `PDO( <https://www.php.net/pdo>`_...):``, ``$dbh``, ``$fh``, ``$conn``, ``$link``
+ ``$stmt = mysql_prepare(`...) <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_``, ``$sth``
+ ``$row = $`pdo <https://www.php.net/pdo>`_->fetchArray(`...) <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_``, ``$`result <https://www.php.net/result>`_``, ``$line``, ``$record``
+ ``preg_match(`... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_, `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_, $r)``, ``$matches```
+ ``str_contains($haystack, $needle)`` and ``strpos``



.. code-block:: php
   
   <?php
   
   // Search for phone numbers in a text
   preg_match_all('/((\d{3})-(\d{3})-(\d{4}))/', $string, $phoneNumber);
   
   // Search for phone numbers in a text
   preg_match_all('/(\d{3})-(\d{3})-(\d{4})/', $string, $matches);
   
   ?>

Suggestions
___________

* Use precise and adapted name with your variables




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontBeTooManual                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


