.. _structures-reusevariable:

.. _reuse-existing-variable:

Reuse Existing Variable
+++++++++++++++++++++++

.. meta::
	:description:
		Reuse Existing Variable: A variable is already holding the content that is calculated again : it could be used again.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Reuse Existing Variable
	:twitter:description: Reuse Existing Variable: A variable is already holding the content that is calculated again : it could be used again
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Reuse Existing Variable
	:og:type: article
	:og:description: A variable is already holding the content that is calculated again : it could be used again
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Reuse Existing Variable.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ReuseVariable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ReuseVariable.html","name":"Reuse Existing Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A variable is already holding the content that is calculated again : it could be used again","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Reuse Existing Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>A variable is already holding the content that is calculated again : it could be used again. 

It is recommended to use the cached value. This saves some computation, in particular when used in a loop, and speeds up the process. This is called memoization.
Some expressions are not idempotent, and should not be cached. For example, calls to `time() <https://www.php.net/time>`_ or `fgets() <https://www.php.net/fgets>`_ return different values with the same parameters.

This may be a micro-optimisation.

.. code-block:: php
   
   <?php
   
   function foo($a) {
       $b = strtolower($a);
       
       // strtolower($a) is already calculated in $b. Just reuse the value.
       if (strtolower($a) === 'c') {
           doSomething();
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `memoization <https://php-dictionary.readthedocs.io/en/latest/dictionary/memoization.ini.html>`_


Suggestions
___________

* Reuse the existing variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ReuseVariable                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


