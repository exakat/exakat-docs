.. _structures-coalesceandconcat:


.. _coalesce-and-concat:

Coalesce And Concat
+++++++++++++++++++


.. meta::

	:description:

		Coalesce And Concat: The concatenation operator ``.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Coalesce And Concat

	:twitter:description: Coalesce And Concat: The concatenation operator ``

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Coalesce And Concat

	:og:type: article

	:og:description: The concatenation operator ``

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Coalesce And Concat.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CoalesceAndConcat.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CoalesceAndConcat.html","name":"Coalesce And Concat","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The concatenation operator ``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Coalesce And Concat.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The concatenation operator ``.`` has precedence over the coalesce operator ``??``. 

It is recommended to add parenthesis to make this expression explicit.


.. code-block:: php
   
   <?php
   
   // Parenthesis are the right solution when in doubt
   echo a . ($b ?? 'd') . $e;
   
   // 'a' . $b is evaluated first, leading ot a useless ?? operator
   'a' . $b ?? $c;
   
   // 'd' . 'e' is evaluated first, leading to $b OR 'de'. 
   echo $b ?? 'd' . 'e';
   
   ?>
Connex PHP features
-------------------

  + `coalesce <https://php-dictionary.readthedocs.io/en/latest/dictionary/coalesce.ini.html>`_
  + `concat <https://php-dictionary.readthedocs.io/en/latest/dictionary/concat.ini.html>`_
  + `precedence <https://php-dictionary.readthedocs.io/en/latest/dictionary/precedence.ini.html>`_
  + `parenthesis <https://php-dictionary.readthedocs.io/en/latest/dictionary/parenthesis.ini.html>`_


Suggestions
___________

* Add parenthesis around ?? operator to avoid misbehavior
* Add parenthesis around the else condition to avoid misbehavior ( ?? ($a . $b))
* Do not use dot and ?? together in the same expression




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CoalesceAndConcat                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


