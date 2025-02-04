.. _functions-unusedarguments:


.. _unused-parameter:

Unused Parameter
++++++++++++++++

.. meta::
	:description:
		Unused Parameter: Those parameters are not used inside the method or function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Parameter
	:twitter:description: Unused Parameter: Those parameters are not used inside the method or function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Parameter
	:og:type: article
	:og:description: Those parameters are not used inside the method or function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unused Parameter.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnusedArguments.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UnusedArguments.html","name":"Unused Parameter","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Those parameters are not used inside the method or function","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unused Parameter.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those parameters are not used inside the method or function. 

Unused parameters should be removed in functions : they are dead code, and seem to offer features that they do not deliver.

Some parameters are unused, due to the signature compatibility: for example, if an interface or a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class defines that parameter, but it is not useful in the current method. Then, it must stay.

This is a silent error: no `error <https://www.php.net/error>`_ message is emitted when doing so.


.. code-block:: php
   
   <?php
   
   // $unused is in the signature, but not used. 
   function foo($unused, $b, $c) {
       return $b + $c;
   }
   
   interface i {
       function goo($a);
   }
   
   class a implements i {
       // goo signature comes from the interface
       function goo($a) {
           return 3;
       }
   }
   ?>
Connex PHP features
-------------------

  + `Parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_


Suggestions
___________

* Drop the argument from the signature
* Actually use that argument in the body of the method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnusedArguments                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
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
| Examples     | :ref:`case-thinkphp-functions-unusedarguments`, :ref:`case-phpmyadmin-functions-unusedarguments`                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`never-called-parameter`, :ref:`could-be-class-constant`                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


