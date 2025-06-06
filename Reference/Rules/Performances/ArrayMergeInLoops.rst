.. _performances-arraymergeinloops:


.. _no-array\_merge()-in-loops:

No array_merge() In Loops
+++++++++++++++++++++++++

.. meta::
	:description:
		No array_merge() In Loops: array_merge() is memory intensive : every call will duplicate the arguments in memory, before merging them.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No array_merge() In Loops
	:twitter:description: No array_merge() In Loops: array_merge() is memory intensive : every call will duplicate the arguments in memory, before merging them
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No array_merge() In Loops
	:og:type: article
	:og:description: array_merge() is memory intensive : every call will duplicate the arguments in memory, before merging them
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No array_merge() In Loops.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/ArrayMergeInLoops.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/ArrayMergeInLoops.html","name":"No array_merge() In Loops","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"array_merge() is memory intensive : every call will duplicate the arguments in memory, before merging them","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No array_merge() In Loops.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`array_merge() <https://www.php.net/array_merge>`_ is memory intensive : every call will duplicate the arguments in memory, before merging them. 

To handle arrays that may be quite big, it is recommended to avoid using `array_merge() <https://www.php.net/array_merge>`_ in a loop. Instead, one should use `array_merge() <https://www.php.net/array_merge>`_ with as many arguments as possible, making the merge a on time call.
Note that `array_merge_recursive() <https://www.php.net/array_merge_recursive>`_ and `file_put_contents() <https://www.php.net/file_put_contents>`_ are affected and reported the same way.

.. code-block:: php
   
   <?php
   
   // A large multidimensional array
   $source = ['a' => ['a', 'b', /*...*/],
              'b' => ['b', 'c', 'd', /*...*/],
              /*...*/
              ];
   
   // Faster way
   $b = array();
   foreach($source as $key => $values) {
       //Collect in an array
       $b[] = $values;
   }
   
   // One call to array_merge
   $b = call_user_func_array('array_merge', $b);
   // or with variadic
   $b = call_user_func('array_merge', ..$b);
   
   // Fastest way (with above example, without checking nor data pulling)
   $b = call_user_func_array('array_merge', array_values($source))
   // or
   $b = call_user_func('array_merge', ...array_values($source))
   
   // Slow way to merge it all
   $b = array();
   foreach($source as $key => $values) {
       $b = array_merge($b, $values);
   }
   
   ?>

See also `Speed up array_merge() <https://www.exakat.io/en/speeding-up-array_merge/>`_.

Connex PHP features
-------------------

  + `Performance <https://php-dictionary.readthedocs.io/en/latest/dictionary/performance.ini.html>`_
  + `Loops <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Store all intermediate arrays in a temporary variable, and use array_merge() once, with ellipsis or call_user_func_array().




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/ArrayMergeInLoops                                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Top10 <ruleset-Top10>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-array_merge-in-loop <https://github.com/dseguy/clearPHP/tree/master/rules/no-array_merge-in-loop.md>`__                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-performances-arraymergeinloops`                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


