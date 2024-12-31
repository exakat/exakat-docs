.. _structures-evalwithouttry:

.. _eval()-without-try:

eval() Without Try
++++++++++++++++++

.. meta\:\:
	:description:
		eval() Without Try: ``eval()`` emits a ``ParseError`` exception with PHP 7 and later.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: eval() Without Try
	:twitter:description: eval() Without Try: ``eval()`` emits a ``ParseError`` exception with PHP 7 and later
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: eval() Without Try
	:og:type: article
	:og:description: ``eval()`` emits a ``ParseError`` exception with PHP 7 and later
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/EvalWithoutTry.html
	:og:locale: en
  ``eval()`` emits a ``ParseError`` `exception <https://www.php.net/exception>`_ with PHP 7 and later. Catching this `exception <https://www.php.net/exception>`_ is the recommended way to handle errors when using the ``eval()`` function.
Note that it will catch situations where ``eval()`` is provided with code that can't be used, but it will not catch security problems. Avoid using ``eval()`` with incoming data.

.. code-block:: php
   
   <?php
   
   $code = 'This is no PHP code.';
   
   //PHP 5 style
   eval($code);
   // Ends up with a Fatal error, at execution time
   
   //PHP 7 style
   try {
       eval($code);
   } catch (ParseError $e) {
       cleanUpAfterEval();
   }
   
   ?>
Connex PHP features
-------------------

  + `eval <https://php-dictionary.readthedocs.io/en/latest/dictionary/eval.ini.html>`_


Suggestions
___________

* Always add a try/catch block around eval() call




Specs
_____

+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/EvalWithoutTry                                                                                                                                                                                        |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>` |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                                            |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and more recent                                                                                                                                                                                     |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Critical                                                                                                                                                                                                         |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                                                  |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/EvalWithouTry.html>`__                                                                                                          |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                        |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples         | :ref:`case-fuelcms-structures-evalwithouttry`, :ref:`case-expressionengine-structures-evalwithouttry`                                                                                                            |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule     | :ref:`could-use-try`                                                                                                                                                                                             |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                          |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


