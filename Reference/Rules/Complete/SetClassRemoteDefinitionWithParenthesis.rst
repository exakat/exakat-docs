.. _complete-setclassremotedefinitionwithparenthesis:

.. _set-class-remote-definition-with-parenthesis:

Set Class Remote Definition With Parenthesis
++++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Set Class Remote Definition With Parenthesis: Links methodcall, properties and constants to its definition, based to the new in the parenthesis.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Class Remote Definition With Parenthesis
	:twitter:description: Set Class Remote Definition With Parenthesis: Links methodcall, properties and constants to its definition, based to the new in the parenthesis
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Class Remote Definition With Parenthesis
	:og:type: article
	:og:description: Links methodcall, properties and constants to its definition, based to the new in the parenthesis
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Set Class Remote Definition With Parenthesis.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SetClassRemoteDefinitionWithParenthesis.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SetClassRemoteDefinitionWithParenthesis.html","name":"Set Class Remote Definition With Parenthesis","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Links methodcall, properties and constants to its definition, based to the new in the parenthesis","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Set Class Remote Definition With Parenthesis.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Links methodcall, properties and constants to its definition, based to the new in the parenthesis. The link is ``DEFINITION``.

.. code-block:: php
   
   <?php
   
   class x {
       public function bar() {    }
   }
   
   function foo() {
       // This links to class x, method bar(), thanks to the new.
       return (new x)->bar();
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetClassRemoteDefinitionWithParenthesis                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`NoDoc <ruleset-NoDoc>`                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                   |
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


