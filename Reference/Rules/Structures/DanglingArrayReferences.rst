.. _structures-danglingarrayreferences:

.. _dangling-array-references:

Dangling Array References
+++++++++++++++++++++++++

.. meta::
	:description:
		Dangling Array References: Always unset a referenced-variable used in a loop.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dangling Array References
	:twitter:description: Dangling Array References: Always unset a referenced-variable used in a loop
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dangling Array References
	:og:type: article
	:og:description: Always unset a referenced-variable used in a loop
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dangling Array References.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DanglingArrayReferences.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DanglingArrayReferences.html","name":"Dangling Array References","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Mon, 03 Feb 2025 17:19:52 +0000","dateModified":"Mon, 03 Feb 2025 17:19:52 +0000","description":"Always unset a referenced-variable used in a loop","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dangling Array References.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Always unset a referenced-variable used in a loop.

It is highly recommended to unset blind variables when they are set up as references after a loop. 

When omitting this step, the next loop that will also require this variable will deal with garbage values, and produce unexpected results.

.. code-block:: php
   
   <?php
   
   $array = array(1,2,3,4);
   
   foreach($array as &$a) {
       $a += 1;
   }
   // This only unset the reference, not the value
   unset($a);
   
   // Dangling array problem
   foreach($array as &$a) {
       $a += 1;
   }
   //$array === array(3,4,5,6);
   
   // This does nothing (apparently)
   // $a is already a reference, even if it doesn't show here.
   foreach($array as $a) {}
   //$array === array(3,4,5,5);
   
   ?>

See also `No Dangling Reference <https://github.com/dseguy/clearPHP/blob/master/rules/no-dangling-reference.md>`_, `PHP foreach pass-by-reference: Do it right, or better not at all <https://coderwall.com/p/qx3fpa/php-foreach-pass-by-reference-do-it-right-or-better-not-at-all>`_, `How does PHP 'foreach' actually work? <https://stackoverflow.com/questions/10057671/how-does-php-foreach-actually-work/14854568#14854568>`_ and `References and foreach <https://schlueters.de/blog/archives/141-references-and-foreach.html>`_.

Connex PHP features
-------------------

  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Avoid using the reference altogether : sometimes, the reference is not needed.
* Add unset() right after the loop, to avoid reusing the reference.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DanglingArrayReferences                                                                                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-dangling-reference <https://github.com/dseguy/clearPHP/tree/master/rules/no-dangling-reference.md>`__                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-typo3-structures-danglingarrayreferences`, :ref:`case-sugarcrm-structures-danglingarrayreferences`                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`altering-foreach-without-reference`                                                                                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


