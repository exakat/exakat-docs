.. _exceptions-unusedexceptionvariable:


.. _unused-exception-variable:

Unused Exception Variable
+++++++++++++++++++++++++

.. meta::
	:description:
		Unused Exception Variable: The variable from a catch clause is not used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Exception Variable
	:twitter:description: Unused Exception Variable: The variable from a catch clause is not used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Exception Variable
	:og:type: article
	:og:description: The variable from a catch clause is not used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Exception Variable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/UnusedExceptionVariable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/UnusedExceptionVariable.html","name":"Unused Exception Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The variable from a catch clause is not used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Exception Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The variable from a catch clause is not used. It is expected to be used, either by chaining the `exception <https://www.php.net/exception>`_, or logging the message.

In PHP 8.0, this variable may be omitted.

.. code-block:: php
   
   <?php
   
   try{
       doSomething();
   } catch (A $a) {
       // $a is caught, but not used here
   } catch (B $b) {
       // $b is caught, and used
       log($b->getMessage());
   } catch (C) {
       // Caught and ignored (PHP 8.0 +)
   }
   
   ?>
Connex PHP features
-------------------

  + `Exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Drop the variable in the clause expression (PHP 8.0 and more recent)
* Chain the exception
* Log the exception message




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/UnusedExceptionVariable                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
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


