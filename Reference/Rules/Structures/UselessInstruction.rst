.. _structures-uselessinstruction:

.. _useless-instructions:

Useless Instructions
++++++++++++++++++++

.. meta::
	:description:
		Useless Instructions: Those instructions are useless, or contains useless parts.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Instructions
	:twitter:description: Useless Instructions: Those instructions are useless, or contains useless parts
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Instructions
	:og:type: article
	:og:description: Those instructions are useless, or contains useless parts
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Instructions.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessInstruction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessInstruction.html","name":"Useless Instructions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Those instructions are useless, or contains useless parts","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Instructions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Those instructions are useless, or contains useless parts. 

For example, an addition whose `result <https://www.php.net/result>`_ is not stored in a variable, or immediately used, does nothing : it is actually performed, and the `result <https://www.php.net/result>`_ is lost. Just plain lost. In fact, PHP might detect it, and optimize it away. 

Here the useless instructions that are spotted :

.. code-block:: php
   
   <?php
   
   // Concatenating with an empty string is useless.
   $string = 'This part '.$is.' useful but '.$not.'';
   
   // This is a typo, that PHP turns into a constant, then a string, then nothing.
   continue;
   
   // Empty string in a concatenation
   $a = 'abc' . '';
   
   // Returning expression, whose result is not used (additions, comparisons, properties, closures, new without =, ...)
   1 + 2;
   
   // Returning post-incrementation
   function foo($a) {
       return $a++;
   }
   
   // array_replace() with only one argument
   $replaced = array_replace($array);
   // array_replace() is OK with ... 
   $replaced = array_replace(...$array);
   
   // @ operator on source array, in foreach, or when assigning literals
   $array = @array(1,2,3);
   
   // Multiple comparisons in a for loop : only the last is actually used.
   for($i = 0; $j = 0; $j < 10, $i < 20; ++$j, ++$i) {
       print $i.' '.$j.PHP_EOL;
   }
   
   // Counting the keys and counting the array is the same.
   $c = count(array_keys($array))
   
   //array_keys already provides an array with only unique values, as they were keys in a previous array
   $d = array_unique(array_keys($file['messages']))
   
   // No need for assignation inside the ternary operator
   $closeQuote = $openQuote[3] === "'" ? substr($openQuote, 4, -2) : $closeQuote = substr($openQuote, 3);
   
   ?>

Suggestions
___________

* Remove the extra semi-colon
* Remove the useless instruction
* Assign this expression to a variable and make use of it




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessInstruction                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-useless-instruction <https://github.com/dseguy/clearPHP/tree/master/rules/no-useless-instruction.md>`__                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


