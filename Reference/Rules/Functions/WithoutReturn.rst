.. _functions-withoutreturn:


.. _methods-without-return:

Methods Without Return
++++++++++++++++++++++

.. meta::
	:description:
		Methods Without Return: List of all the functions, closures, methods that have no explicit return.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Methods Without Return
	:twitter:description: Methods Without Return: List of all the functions, closures, methods that have no explicit return
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Methods Without Return
	:og:type: article
	:og:description: List of all the functions, closures, methods that have no explicit return
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Methods Without Return.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WithoutReturn.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WithoutReturn.html","name":"Methods Without Return","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of all the functions, closures, methods that have no explicit return","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Methods Without Return.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of all the functions, closures, methods that have no explicit return. 

Functions with the ``void`` or ``never`` return types, are omitted.

.. code-block:: php
   
   <?php
   
   // With return null : Explicitly not returning
   function withExplicitReturn($a = 1) {
       $a++;
       return null;
   }
   
   // Without indication
   function withoutExplicitReturn($a = 1) {
       $a++;
   }
   
   // With return type void : Explicitly not returning
   function withExplicitReturnType($a = 1) : void {
       $a++;
   }
   
   ?>

See also `return <https://www.php.net/manual/en/function.return.php>`_.

Connex PHP features
-------------------

  + `Return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_
  + `Never Type <https://php-dictionary.readthedocs.io/en/latest/dictionary/never.ini.html>`_


Suggestions
___________

* Add the returntype 'void' to make this explicit behavior




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WithoutReturn                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


