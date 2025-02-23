.. _structures-checkdivision:


.. _check-division-by-zero:

Check Division By Zero
++++++++++++++++++++++

.. meta::
	:description:
		Check Division By Zero: Always check before dividing by a value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Check Division By Zero
	:twitter:description: Check Division By Zero: Always check before dividing by a value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Check Division By Zero
	:og:type: article
	:og:description: Always check before dividing by a value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Check Division By Zero.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CheckDivision.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CheckDivision.html","name":"Check Division By Zero","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Always check before dividing by a value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Check Division By Zero.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Always check before dividing by a value. If that value is cast to 0, PHP might stop the processing with an `exception <https://www.php.net/exception>`_, or keep processing it with 0 as a `result <https://www.php.net/result>`_. Both will raise problems. 

The best practise is to check the incoming value before attempting the division. On possible alternative is to catch the `DivisionByZeroError <https://www.php.net/manual/en/class.`divisionbyzeroerror <https://www.php.net/divisionbyzeroerror>`_.php>`_ `exception <https://www.php.net/exception>`_, that PHP 8.0 and more recent will raise.

.. code-block:: php
   
   <?php
   
   // Check the value before usage
   function foo($a = 1) {
       if ($a !== 0) {
           return 42 / $a;
       } else {
           // process an error
       }
   }
   
   // Check the value after usage (worse than the above)
   function foo($a = 1) {
       try {
           return 42 / $a;
       } catch (DivisionByZero) {
           // fix the situation now
       }
   }
   
   // This might fails with a division by 0
   function foo($a = 1) {
       return 42 / $a;
   }
   
   ?>

See also `DivisionByZeroError <https://www.php.net/manual/fr/class.divisionbyzeroerror.php>`_.

Connex PHP features
-------------------

  + `Exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_
  + `ArithmeticError Error <https://php-dictionary.readthedocs.io/en/latest/dictionary/arithmeticerror.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CheckDivision                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`could-use-try`                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


