.. _functions-neverusedparameter:


.. _never-called-parameter:

Never Called Parameter
++++++++++++++++++++++

.. meta::
	:description:
		Never Called Parameter: This analysis reports when a parameter is never used at calltime.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Never Called Parameter
	:twitter:description: Never Called Parameter: This analysis reports when a parameter is never used at calltime
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Never Called Parameter
	:og:type: article
	:og:description: This analysis reports when a parameter is never used at calltime
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Never Called Parameter.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NeverUsedParameter.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NeverUsedParameter.html","name":"Never Called Parameter","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This analysis reports when a parameter is never used at calltime","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Never Called Parameter.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis reports when a parameter is never used at calltime. 

Such parameter has a default value, and always falls back to it. As such, it may be turned into a local variable.

A never called parameter is often planned for future use, though, so far, the code base doesn't make use of it. It also happens that the code use it, but is not part of the analyzed code base, such as a plugin system.

This issue is silent: it doesn't yield any `error <https://www.php.net/error>`_. It is also difficult to identify, as it requires checking all the usage of the method.

This analysis checks for actual usage of the parameter, from the outside of the method. This is different from checking if the parameter is used inside the method.


.. code-block:: php
   
   <?php
   
   // $b may be turned into a local var, it is unused
   function foo($a, $b = 1) {
       return $a + $b;
   }
   
   // whenever foo is called, the 2nd arg is not mentioned
   foo($a);
   foo(3);
   foo('a');
   foo($c);
   
   ?>

See also :ref:`Unused Parameter <unused-parameter>`, :ref:`Cancelled Parameter <cancelled-parameter>` and :ref:`Parameter Hiding <parameter-hiding>`.

Connex PHP features
-------------------

  + `Silent Behavior <https://php-dictionary.readthedocs.io/en/latest/dictionary/silent.ini.html>`_


Suggestions
___________

* Drop the unused argument in the method definition
* Actually use the argument when calling the method
* Drop the default value, and check warnings that mention usage of this parameter




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NeverUsedParameter                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Rector <ruleset-Rector>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.6                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-piwigo-functions-neverusedparameter`                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`could-be-class-constant`, :ref:`unused-parameter`                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


