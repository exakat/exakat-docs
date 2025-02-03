.. _interfaces-isnotimplemented:


.. _interfaces-is-not-implemented:

Interfaces Is Not Implemented
+++++++++++++++++++++++++++++


.. meta::

	:description:

		Interfaces Is Not Implemented: Classes that implements interfaces, must implements each of the interface's methods.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Interfaces Is Not Implemented

	:twitter:description: Interfaces Is Not Implemented: Classes that implements interfaces, must implements each of the interface's methods

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Interfaces Is Not Implemented

	:og:type: article

	:og:description: Classes that implements interfaces, must implements each of the interface's methods

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Interfaces Is Not Implemented.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/IsNotImplemented.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/IsNotImplemented.html","name":"Interfaces Is Not Implemented","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Classes that implements interfaces, must implements each of the interface's methods","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Interfaces Is Not Implemented.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Classes that implements interfaces, must implements each of the interface's methods. Otherwise, the class shall be marked as ``abstract``.
This problem tends to occur in code that splits interfaces and classes by file. This means that PHP's linting will skip the definitions and not find the problem. At execution time, the definitions will be checked, and a Fatal `error <https://www.php.net/error>`_ will occur.

This situation usually detects code that was forgotten during a refactorisation of the interface or the class and its siblings.

.. code-block:: php
   
   <?php
   
   class x implements i {
       // This method implements the foo method from the i interface
       function foo() {}
   
       // The method bar is missing, yet is requested by interface i
       function foo() {}
   }
   
   interface i {
       function foo();
       function bar(); 
   }
   
   ?>

See also `Interfaces <https://www.php.net/manual/en/language.oop5.interfaces.php>`_.

Related PHP errors 
-------------------

  + `Class %s contains %d abstract method%s and must therefore be declared abstract or implement the remaining methods <https://php-errors.readthedocs.io/en/latest/messages/class-%25s-contains-%25d-abstract-method%25s-and-must-therefore-be-declared-abstract-or-implement-the-remaining-methods.html>`_



Connex PHP features
-------------------

  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_
  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_
  + `implements <https://php-dictionary.readthedocs.io/en/latest/dictionary/implements.ini.html>`_


Suggestions
___________

* Implements all the methods from the interfaces
* Remove the class
* Make the class abstract
* Make the missing methods abstract




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/IsNotImplemented                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.5                                                                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


