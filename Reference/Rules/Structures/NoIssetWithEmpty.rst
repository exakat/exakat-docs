.. _structures-noissetwithempty:


.. _no-isset()-with-empty():

No isset() With empty()
+++++++++++++++++++++++

.. meta::
	:description:
		No isset() With empty(): empty() actually does the job of isset() too.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No isset() With empty()
	:twitter:description: No isset() With empty(): empty() actually does the job of isset() too
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No isset() With empty()
	:og:type: article
	:og:description: empty() actually does the job of isset() too
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No isset() With empty().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoIssetWithEmpty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoIssetWithEmpty.html","name":"No isset() With empty()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"empty() actually does the job of isset() too","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No isset() With empty().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

empty() actually does the job of `isset() <https://www.www.php.net/isset>`_ too. 

From the manual : ``No warning is generated if the variable does not exist. That means empty() is essentially the concise equivalent to !`isset( <https://www.www.php.net/isset>`_$var) || $var == `false <https://www.php.net/false>`_.`` The main difference is that `isset() <https://www.www.php.net/isset>`_ only works with variables, while empty() works with other structures, such as constants.

.. code-block:: php
   
   <?php
   
   
   // Enough validation
   if (!empty($a)) {
       doSomething();
   }
   
   // Too many tests
   if (isset($a) && !empty($a)) {
       doSomething();
   }
   
   ?>

See also `Isset <http://www.php.net/isset>`_ and `empty <http://www.php.net/empty>`_.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Only use isset(), just drop the empty()
* Only use empty(), just drop the empty()
* Use a null value, so the variable is always set




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoIssetWithEmpty                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.7                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xoops-structures-noissetwithempty`                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


