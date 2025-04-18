.. _structures-couldusestrrepeat:


.. _could-use-str\_repeat():

Could Use str_repeat()
++++++++++++++++++++++

.. meta::
	:description:
		Could Use str_repeat(): Use str_repeat() or str_pad() instead of making a loop.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use str_repeat()
	:twitter:description: Could Use str_repeat(): Use str_repeat() or str_pad() instead of making a loop
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use str_repeat()
	:og:type: article
	:og:description: Use str_repeat() or str_pad() instead of making a loop
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use str_repeat().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseStrrepeat.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseStrrepeat.html","name":"Could Use str_repeat()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use str_repeat() or str_pad() instead of making a loop","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use str_repeat().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use `str_repeat() <https://www.php.net/str_repeat>`_ or `str_pad() <https://www.php.net/str_pad>`_ instead of making a loop.

Making a loop to repeat the same concatenation is actually much longer than using `str_repeat() <https://www.php.net/str_repeat>`_. As soon as the loop repeats more than twice, `str_repeat() <https://www.php.net/str_repeat>`_ is much faster. With arrays of 30, the difference is significant, though the whole operation is short by itself.

.. code-block:: php
   
   <?php
   
   // This adds 7 'e' to $x
   $x .= str_repeat('e', 7);
   
   // This is the same as above, 
   for($a = 3; $a < 10; ++$a) {
       $x .= 'e';
   }
   
   // here, $default must contains 7 elements to be equivalent to the previous code
   foreach($default as $c) {
       $x .= 'e';
   }
   
   ?>
Connex PHP features
-------------------

  + `String <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_


Suggestions
___________

* Use strrepeat() whenever possible




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseStrrepeat                                                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.0                                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-structures-couldusestrrepeat`                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


