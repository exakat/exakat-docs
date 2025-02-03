.. _constants-conditionedconstants:


.. _conditioned-constants:

Conditioned Constants
+++++++++++++++++++++

.. meta::
	:description:
		Conditioned Constants: This rule indicates when a constant is defined if a condition is met.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Conditioned Constants
	:twitter:description: Conditioned Constants: This rule indicates when a constant is defined if a condition is met
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Conditioned Constants
	:og:type: article
	:og:description: This rule indicates when a constant is defined if a condition is met
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Conditioned Constants.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/ConditionedConstants.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/ConditionedConstants.html","name":"Conditioned Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rule indicates when a constant is defined if a condition is met","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Conditioned Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule indicates when a constant is defined if a condition is met. Several definitions of a global constant are possible in the code: using conditions, it is possible to have only one defined during execution.

.. code-block:: php
   
   <?php
   
   if (time() > 1519629617) {
       define('MY_CONST', false);
   } else {
       define('MY_CONST', time() - 1519629617);
   }
   
   ?>
Connex PHP features
-------------------

  + `conditioned <https://php-dictionary.readthedocs.io/en/latest/dictionary/conditioned.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/ConditionedConstants                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


