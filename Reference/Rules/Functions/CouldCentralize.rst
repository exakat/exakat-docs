.. _functions-couldcentralize:


.. _could-make-a-function:

Could Make A Function
+++++++++++++++++++++

.. meta::
	:description:
		Could Make A Function: When a function is called across the code with the same arguments often enough, it should be turned into a local API.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Make A Function
	:twitter:description: Could Make A Function: When a function is called across the code with the same arguments often enough, it should be turned into a local API
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Make A Function
	:og:type: article
	:og:description: When a function is called across the code with the same arguments often enough, it should be turned into a local API
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Make A Function.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CouldCentralize.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CouldCentralize.html","name":"Could Make A Function","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When a function is called across the code with the same arguments often enough, it should be turned into a local API","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Make A Function.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When a function is called across the code with the same arguments often enough, it should be turned into a local API. 

This approach is similar to turning literals into constants : it centralize the value, it helps refactoring by updating it. It also makes the code more readable. Moreover, it often highlight common grounds between remote code locations. 

The analysis looks for functions calls, and checks the arguments. When the calls occurs more than 4 times, it is reported.

.. code-block:: php
   
   <?php
   
   // str_replace is used to clean '&' from strings. 
   // It should be upgraded to a central function
   function foo($arg ) {
       $arg = str_replace('&', '', $arg);
       // do something with $arg
   }
   
   class y {
       function bar($database ) {
           $value = $database->queryName();
           $value = str_replace('&', '', $value);
           // $value = removeAmpersand($value);
           // do something with $arg2
       }
   }
   
   // helper function
   function removeAmpersand($string) {
       return str_replace('&', '', $string);
   }
   
   ?>

+---------------------+---------+---------+-------------------------------------------------------------------+
| Name                | Default | Type    | Description                                                       |
+---------------------+---------+---------+-------------------------------------------------------------------+
| centralizeThreshold | 8       | integer | Minimal number of calls of the function with one common argument. |
+---------------------+---------+---------+-------------------------------------------------------------------+



See also `Don't repeat yourself (DRY) <https://en.wikipedia.org/wiki/Don%27t_repeat_yourself>`_.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Create a constant for common pieces of data
* Create a function based on context-free repeated elements
* Create a class based on repeated elements with dependent values




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CouldCentralize                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


