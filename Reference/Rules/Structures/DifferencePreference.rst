.. _structures-differencepreference:


.. _difference-consistence:

Difference Consistence
++++++++++++++++++++++

.. meta::
	:description:
		Difference Consistence: There are two operators to check a difference : <> and !=.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Difference Consistence
	:twitter:description: Difference Consistence: There are two operators to check a difference : <> and !=
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Difference Consistence
	:og:type: article
	:og:description: There are two operators to check a difference : <> and !=
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Difference Consistence.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DifferencePreference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DifferencePreference.html","name":"Difference Consistence","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"There are two operators to check a difference : <> and !=","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Difference Consistence.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

There are two operators to check a difference : <> and !=.

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It happens that != and <> are used depending on coding style and files. One file may be consistently using <>, while the others are all using !=. 
<> and != are the two only comparison operators that are identical.

.. code-block:: php
   
   <?php
   
   // Both != and <> are used in the code
   // When one of them is used less than 10%, it is reported as a consistence issue.
   if ($a != $b) {
   
   } elseif ($c <> $d) {
   
   }
   
   ?>

See also `Comparison Operators <https://www.php.net/manual/en/language.operators.comparison.php>`_.

Connex PHP features
-------------------

  + `Operators <https://php-dictionary.readthedocs.io/en/latest/dictionary/operator.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DifferencePreference                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.1                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


