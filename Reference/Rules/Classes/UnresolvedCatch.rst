.. _classes-unresolvedcatch:


.. _unresolved-catch:

Unresolved Catch
++++++++++++++++


.. meta::

	:description:

		Unresolved Catch: Catch clauses do not check for Exception existence.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Unresolved Catch

	:twitter:description: Unresolved Catch: Catch clauses do not check for Exception existence

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Unresolved Catch

	:og:type: article

	:og:description: Catch clauses do not check for Exception existence

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unresolved Catch.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnresolvedCatch.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UnresolvedCatch.html","name":"Unresolved Catch","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Catch clauses do not check for Exception existence","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unresolved Catch.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Catch clauses do not check for `Exception <https://www.php.net/exception>`_ existence. 

Catch clauses check that the emitted expression is of the requested Class, but if that class doesn't exist in the code, the catch clause is always false. This is dead code.

.. code-block:: php
   
   <?php
   
   try {
       // doSomething()
   } catch {TypoedExxeption $e) { // Do not exist Exception
       // Fix this exception
   } catch {Stdclass $e) {        // Exists, but is not an exception
       // Fix this exception
   } catch {Exception $e) {        // Actual and effective catch
       // Fix this exception
   }
   ?>

See also `PHP Try Catch: Basics & Advanced PHP Exception Handling Tutorial <https://stackify.com/php-try-catch-php-exception-tutorial/>`_ and `Silent failure to catch exceptions in PHP <http://yakhairsurplus.com/silent-filure-to-catch-exceptions-in-php/>`_.

Connex PHP features
-------------------

  + `try-catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/try-catch.ini.html>`_


Suggestions
___________

* Fix the name of the exception
* Remove the catch clause
* Add a use expression with a valid name
* Create/import the missing exception




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnresolvedCatch                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-unresolved-catch <https://github.com/dseguy/clearPHP/tree/master/rules/no-unresolved-catch.md>`__                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


