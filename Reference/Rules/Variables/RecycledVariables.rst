.. _variables-recycledvariables:


.. _recycled-variables:

Recycled Variables
++++++++++++++++++

.. meta::
	:description:
		Recycled Variables: A recycled variable is a variable used for two distinct missions in a method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Recycled Variables
	:twitter:description: Recycled Variables: A recycled variable is a variable used for two distinct missions in a method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Recycled Variables
	:og:type: article
	:og:description: A recycled variable is a variable used for two distinct missions in a method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Recycled Variables.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/RecycledVariables.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/RecycledVariables.html","name":"Recycled Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A recycled variable is a variable used for two distinct missions in a method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Recycled Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A recycled variable is a variable used for two distinct missions in a method. There is usually a first part, with its own initialization, then, later in the method, a second part with a new initialization and a distinct usage of the variable. 

Recycled variables leads to confusion: with the new initialization, the variable changes its purpose. Yet, with the same name, and with a bit of lost context, it is easy to confuse it later. 

.. code-block:: php
   
   <?php
   
   function foo() {
       $variable = "initial";      // first initialisation
       $variable = goo($variable);   // processing the variable
       hoo($variable);               // sending the variable to a final destination
       
       $variable = "second" ;      // second initialisation
       hoo2($variable);              // sending the variable to a different final destination
   }
   ?>

See also `Please Don’t Recycle Local Variables <https://daedtech.com/please-dont-recycle-local-variables/>`_.

Connex PHP features
-------------------

  + `Variables <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_
  + `Readability <https://php-dictionary.readthedocs.io/en/latest/dictionary/readability.ini.html>`_


Suggestions
___________

* Use distinct names for each variable
* Split the method into smaller methods and unique variable name usage




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/RecycledVariables                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


