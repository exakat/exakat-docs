.. _classes-variableclasses:


.. _dynamically-called-classes:

Dynamically Called Classes
++++++++++++++++++++++++++

.. meta::
	:description:
		Dynamically Called Classes: This rule reports when a class is called dynamically.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamically Called Classes
	:twitter:description: Dynamically Called Classes: This rule reports when a class is called dynamically
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamically Called Classes
	:og:type: article
	:og:description: This rule reports when a class is called dynamically
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dynamically Called Classes.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/VariableClasses.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/VariableClasses.html","name":"Dynamically Called Classes","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rule reports when a class is called dynamically","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dynamically Called Classes.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports when a class is called dynamically. To call dynamically a class, one must use a variable at instantiation time, or with the objects syntaxes.

.. code-block:: php
   
   <?php
   
   // This class is called dynamically
   class X {
       const CONSTANTE = 1;
   }
   
   $classe = 'X';
   
   $x = new $classe();
   
   echo $x::CONSTANTE;
   
   ?>
Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `Dynamic Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-class.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/VariableClasses                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


