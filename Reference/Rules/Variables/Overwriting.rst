.. _variables-overwriting:


.. _overwriting-variable:

Overwriting Variable
++++++++++++++++++++

.. meta::
	:description:
		Overwriting Variable: Replacing the content of a variable by something entirely different is prone to errors.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwriting Variable
	:twitter:description: Overwriting Variable: Replacing the content of a variable by something entirely different is prone to errors
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwriting Variable
	:og:type: article
	:og:description: Replacing the content of a variable by something entirely different is prone to errors
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Overwriting Variable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/Overwriting.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/Overwriting.html","name":"Overwriting Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 02 Apr 2025 16:35:34 +0000","dateModified":"Wed, 02 Apr 2025 16:35:34 +0000","description":"Replacing the content of a variable by something entirely different is prone to errors","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Overwriting Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Replacing the content of a variable by something entirely different is prone to errors. 

For example, it is not obvious if the ``$text`` variable is plain text or HTML text. 

Generally, it is possible that the source will be needed later, for extra processing. 

Note that accumulators, like ``+=``, ``.=``, ``[]``, etc., that are meant to collect lots of values with consistent type are not reported by this rule.

.. code-block:: php
   
   <?php
   
   // variable replacement
   $text = htmlentities($text);
   
   // Recommended syntax
   $textHTML = htmlentities($text);
   
   // here, $g is actually undefined, as it is used before being defined.
   // first usage is in use ($g)
   $g = function() use ($g) { echo $g; }; 
   
   ?>
Connex PHP features
-------------------

  + `Variables <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/Overwriting                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


