.. _structures-dontchangeblindkey:


.. _don't-change-the-blind-var:

Don't Change The Blind Var
++++++++++++++++++++++++++

.. meta::
	:description:
		Don't Change The Blind Var: When using a foreach(), the blind variables hold a copy of the original value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Don't Change The Blind Var
	:twitter:description: Don't Change The Blind Var: When using a foreach(), the blind variables hold a copy of the original value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Don't Change The Blind Var
	:og:type: article
	:og:description: When using a foreach(), the blind variables hold a copy of the original value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Don't Change The Blind Var.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DontChangeBlindKey.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DontChangeBlindKey.html","name":"Don't Change The Blind Var","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When using a foreach(), the blind variables hold a copy of the original value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Don't Change The Blind Var.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When using a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_, the blind variables hold a copy of the original value. It is confusing to modify them, as it seems that the original value may be changed.

When actually changing the original value, use the reference in the foreach definition to make it obvious, and save the final reassignation.

When the value has to be prepared before usage, then save the filtered value in a separate variable. This makes the clean value obvious, and preserve the original value for a future usage.

.. code-block:: php
   
   <?php
   
   // $bar is duplicated and kept 
   $foo = [1, 2, 3];
   foreach($foo as $bar) {
       // $bar is updated but its original value is kept
       $nextBar = $bar + 1;
       print $bar . ' => ' . ($nextBar) . PHP_EOL;
       foobar($nextBar);
   }
   
   // $bar is updated and lost
   $foo = [1, 2, 3];
   foreach($foo as $bar) {
       // $bar is updated but its final value is lost
       print $bar . ' => ' . (++$bar) . PHP_EOL;
       // Now that $bar is reused, it is easy to confuse its value
       foobar($bar);
   }
   
   // $bar is updated and kept
   $foo = [1, 2, 3];
   foreach($foo as &$bar) {
       // $bar is updated and keept
       print $bar . ' => ' . (++$bar) . PHP_EOL;
       foobar($bar);
   }
   
   ?>
Connex PHP features
-------------------

  + `Loops <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_
  + `Blind Variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/blind-key.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontChangeBlindKey                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
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


