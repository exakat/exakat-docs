.. _structures-unpreprocessed:


.. _unpreprocessed-values:

Unpreprocessed Values
+++++++++++++++++++++

.. meta::
	:description:
		Unpreprocessed Values: Preprocessing values is the preparation of values before PHP executes the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unpreprocessed Values
	:twitter:description: Unpreprocessed Values: Preprocessing values is the preparation of values before PHP executes the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unpreprocessed Values
	:og:type: article
	:og:description: Preprocessing values is the preparation of values before PHP executes the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unpreprocessed Values.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Unpreprocessed.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Unpreprocessed.html","name":"Unpreprocessed Values","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Preprocessing values is the preparation of values before PHP executes the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unpreprocessed Values.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Preprocessing values is the preparation of values before PHP executes the code. 

There is no macro language in PHP, that prepares the code before compilation, bringing some comfort and short syntax. Most of the time, one uses PHP itself to preprocess data. 

For example : 
could be written 
and avoid preprocessing the string into an array first. 

Preprocessing could be done anytime the script includes all the needed values to process the expression. 

This is a micro-optimisation, in particular when the expression is used once.

.. code-block:: php
   
   <?php
       $days_en = 'monday,tuesday,wednesday,thursday,friday,saturday,sunday';
       $days_zh = '星期－,星期二,星期三,星期四,星期五,星期六,星期日';
   
       $days = explode(',', $lang === 'en' ? $days_en : $days_zh); 
   ?>
Connex PHP features
-------------------

  + `Preprocessing <https://php-dictionary.readthedocs.io/en/latest/dictionary/preprocess.ini.html>`_
  + `Micro-optimisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/micro-optimisation.ini.html>`_


Suggestions
___________

* Preprocess the values and hardcode them in PHP. Do not use PHP to calculate something at the last moment.
* Use already processed values, or cache to avoid calculating the value each hit.
* Create a class that export the data in the right format for every situation, including the developer's comfort.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/Unpreprocessed                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `always-preprocess <https://github.com/dseguy/clearPHP/tree/master/rules/always-preprocess.md>`__                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zurmo-structures-unpreprocessed`, :ref:`case-piwigo-structures-unpreprocessed`                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


