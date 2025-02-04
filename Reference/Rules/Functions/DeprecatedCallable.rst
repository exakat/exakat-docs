.. _functions-deprecatedcallable:


.. _deprecated-callable:

Deprecated Callable
+++++++++++++++++++

.. meta::
	:description:
		Deprecated Callable: Callable functions that are supported by ``call_user_func($callable)``, but not with the ``$callable()`` syntax are deprecated.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Deprecated Callable
	:twitter:description: Deprecated Callable: Callable functions that are supported by ``call_user_func($callable)``, but not with the ``$callable()`` syntax are deprecated
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Deprecated Callable
	:og:type: article
	:og:description: Callable functions that are supported by ``call_user_func($callable)``, but not with the ``$callable()`` syntax are deprecated
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Deprecated Callable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/DeprecatedCallable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/DeprecatedCallable.html","name":"Deprecated Callable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Callable functions that are supported by ``call_user_func($callable)``, but not with the ``$callable()`` syntax are deprecated","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Deprecated Callable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Callable functions that are supported by ``call_user_func($callable)``, but not with the ``$callable()`` syntax are deprecated. 

One important aspect is the loss of context : 'self\:\:method' may be created anywhere in the code, while `self\:\:class` can only be used inside a class, and, in that case, inside the target class. 
It is recommended to update the code with any PHP version, to prepare for the future removal of the feature.

.. code-block:: php
   
   <?php
   
   class x {
       // This will fail 
       function foo(callable $callable) {
           $callable();
       }
       
       function method() {
       
       }
   }
   
   $x = new x;
   $x->foo('self::method');
   ?>

See also `PHP RFC: Deprecate partially supported callables <https://wiki.php.net/rfc/deprecate_partially_supported_callables>`_.

Related PHP errors 
-------------------

  + `Use of "self" in callables is deprecated <https://php-errors.readthedocs.io/en/latest/messages/use-of-%22self%22-in-callables-is-deprecated.html>`_
  + `Use of "static" in callables is deprecated <https://php-errors.readthedocs.io/en/latest/messages/use-of-%22static%22-in-callables-is-deprecated.html>`_
  + `Use of "parent" in callables is deprecated <https://php-errors.readthedocs.io/en/latest/messages/use-of-%22parent%22-in-callables-is-deprecated.html>`_



Connex PHP features
-------------------

  + `Callables <https://php-dictionary.readthedocs.io/en/latest/dictionary/callable.ini.html>`_


Suggestions
___________

* Replace the keyword (such as self) by the full class name, with self::class.
* Use a variable and the $s(...) syntax.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/DeprecatedCallable                                                                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and older                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


