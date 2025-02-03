.. _functions-nodefaultforreference:

.. _no-default-for-referenced-parameter:

No Default For Referenced Parameter
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Default For Referenced Parameter: Parameters with reference should not have a default value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Default For Referenced Parameter
	:twitter:description: No Default For Referenced Parameter: Parameters with reference should not have a default value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Default For Referenced Parameter
	:og:type: article
	:og:description: Parameters with reference should not have a default value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Default For Referenced Parameter.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoDefaultForReference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/NoDefaultForReference.html","name":"No Default For Referenced Parameter","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Parameters with reference should not have a default value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Default For Referenced Parameter.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Parameters with reference should not have a default value. 

When they have a default value, that default value is not a reference, and it will not have impact on the calling context. 

Then, the parameter behaves like a reference when the argument is provided, and not as a reference when the parameter is not provided. This makes sense : no parameter in, no parameter out.

.. code-block:: php
   
   <?php
   
   function foo(&$i = 1) {
   	++$i;
   }
   
   // $i is 1, but it is not available in the calling context
   foo(); 
   
   // $i is 1, but it is not available in the calling context
   $i = 1;
   foo($i); 
   
   echo $i; // $i is now 2
   
   ?>
Connex PHP features
-------------------

  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Suggestions
___________

* Remove the reference
* Make that parameter a local variable
* Remove the default value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NoDefaultForReference                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
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


