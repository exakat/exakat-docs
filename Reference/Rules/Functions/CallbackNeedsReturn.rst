.. _functions-callbackneedsreturn:


.. _callback-function-needs-return:

Callback Function Needs Return
++++++++++++++++++++++++++++++


.. meta::

	:description:

		Callback Function Needs Return: When used with array_map() functions, the callback must return something.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Callback Function Needs Return

	:twitter:description: Callback Function Needs Return: When used with array_map() functions, the callback must return something

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Callback Function Needs Return

	:og:type: article

	:og:description: When used with array_map() functions, the callback must return something

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Callback Function Needs Return.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CallbackNeedsReturn.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/CallbackNeedsReturn.html","name":"Callback Function Needs Return","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When used with array_map() functions, the callback must return something","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Callback Function Needs Return.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When used with `array_map() <https://www.php.net/array_map>`_ functions, the callback must return something. This return may be in the form of a ``return`` statement, a global variable or a parameter with a reference. All those solutions extract information from the callback. 



The following functions are omitted, as they don't require the return : 

+ `forward_static_call_array() <https://www.php.net/forward_static_call_array>`_
+ `forward_static_call() <https://www.php.net/forward_static_call>`_
+ `register_shutdown_function() <https://www.php.net/register_shutdown_function>`_
+ `register_tick_function() <https://www.php.net/register_tick_function>`_

.. code-block:: php
   
   <?php
   
   // This filters each element
   $filtered = array_filter($array, function ($x) {return $x == 2; });
   
   // This return void for every element
   $filtered = array_filter($array, function ($x) {return ; });
   
   // costly array_sum()
   $sum = 0;
   $filtered = array_filter($array, function ($x) use (&$sum) {$sum += $x; });
   
   // costly array_sum()
   global $sum = 0;
   $filtered = array_filter($array, function () {global $sum; $sum += $x; });
   
   // register_shutown_function() doesn't require any return
   register_shutown_function("my_shutdown");
   
   ?>

See also `array_map <https://www.php.net/array_map>`_.

Connex PHP features
-------------------

  + `callback <https://php-dictionary.readthedocs.io/en/latest/dictionary/callback.ini.html>`_


Suggestions
___________

* Add an explicit return to the callback
* Use `null` to unset elements in an array without destroying the index




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CallbackNeedsReturn                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-functions-callbackneedsreturn`, :ref:`case-phpdocumentor-functions-callbackneedsreturn`                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


