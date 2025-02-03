.. _functions-multiplesamearguments:

.. _multiple-definition-of-the-same-argument:

Multiple Definition Of The Same Argument
++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Definition Of The Same Argument: A method's signature is holding twice (or more) the same argument.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Definition Of The Same Argument
	:twitter:description: Multiple Definition Of The Same Argument: A method's signature is holding twice (or more) the same argument
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Definition Of The Same Argument
	:og:type: article
	:og:description: A method's signature is holding twice (or more) the same argument
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Definition Of The Same Argument.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MultipleSameArguments.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/MultipleSameArguments.html","name":"Multiple Definition Of The Same Argument","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"A method's signature is holding twice (or more) the same argument","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiple Definition Of The Same Argument.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>A method's signature is holding twice (or more) the same argument. For example, function x ($a, $a) { `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ }. 

This is accepted as is by PHP 5, and the last parameter's value will be assigned to the variable. PHP 7.0 and more recent has dropped this feature, and reports a fatal `error <https://www.php.net/error>`_ when linting the code.
However, this is not common programming practise : all arguments should be named differently.

.. code-block:: php
   
   <?php
     function x ($a, $a) { print $a; };
     x(1,2); => display 2
   
       // special case with a closure : 
     function ($a) use ($a) { print $a; };
     x(1,2); => display 2
   
   ?>

See also `Prepare for PHP 7 error messages (part 3) <https://www.exakat.io/prepare-for-php-7-error-messages-part-3/>`_.

Related PHP errors 
-------------------

  + `Cannot use lexical variable $b as a parameter name <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-lexical-variable-%25s-as-a-parameter-name.html>`_
  + `Redefinition of parameter $b <https://php-errors.readthedocs.io/en/latest/messages/redefinition-of-parameter-%24%25s.html>`_



Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Give different names to different parameters




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MultipleSameArguments                                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `all-unique-arguments <https://github.com/dseguy/clearPHP/tree/master/rules/all-unique-arguments.md>`__                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


