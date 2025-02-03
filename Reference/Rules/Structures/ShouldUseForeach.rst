.. _structures-shoulduseforeach:

.. _should-use-foreach:

Should Use Foreach
++++++++++++++++++

.. meta::
	:description:
		Should Use Foreach: Use the ``foreach`` loop instead of ``for`` when traversing an array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use Foreach
	:twitter:description: Should Use Foreach: Use the ``foreach`` loop instead of ``for`` when traversing an array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use Foreach
	:og:type: article
	:og:description: Use the ``foreach`` loop instead of ``for`` when traversing an array
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Use Foreach.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShouldUseForeach.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ShouldUseForeach.html","name":"Should Use Foreach","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use the ``foreach`` loop instead of ``for`` when traversing an array","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Use Foreach.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Use the ``foreach`` loop instead of ``for`` when traversing an array.

`Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ is the modern loop : it maps automatically every element of the array to a blind variable, and iterate. This is faster and safer.

.. code-block:: php
   
   <?php
   
   // Foreach version
   foreach($array as $element) {
       doSomething($element);
   }
   
   // The above case may even be upgraded with array_map and a callback, 
   // for the simplest one of them
   $array = array_map('doSomething', $array);
   
   // For version (one of various alternatives)
   for($i = 0; $i < count($array); $i++) {
       $element = $array[$i];
       doSomething($element);
   }
   
   // Based on array_pop or array_shift()
   while($value = array_pop($array)) {
       doSomething($array);
   }
   
   ?>

See also `foreach <https://www.php.net/manual/en/control-structures.foreach.php>`_ and `5 Ways To Loop Through An Array In PHP <https://www.codewall.co.uk/5-ways-to-loop-through-array-php/>`_.

Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `for <https://php-dictionary.readthedocs.io/en/latest/dictionary/for.ini.html>`_


Suggestions
___________

* Move for() loops to foreach(), whenever they apply to a finite list of elements




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShouldUseForeach                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.7                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-expressionengine-structures-shoulduseforeach`, :ref:`case-woocommerce-structures-shoulduseforeach`           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


