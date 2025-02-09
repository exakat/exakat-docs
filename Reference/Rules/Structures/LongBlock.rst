.. _structures-longblock:


.. _too-long-a-block:

Too Long A Block
++++++++++++++++

.. meta::
	:description:
		Too Long A Block: The loop is operating on a block that is too long.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Too Long A Block
	:twitter:description: Too Long A Block: The loop is operating on a block that is too long
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Too Long A Block
	:og:type: article
	:og:description: The loop is operating on a block that is too long
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Too Long A Block.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/LongBlock.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/LongBlock.html","name":"Too Long A Block","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The loop is operating on a block that is too long","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Too Long A Block.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The loop is operating on a block that is too long. 

This analysis is applied to loops (for, foreach, while, do..while) and if/then/else/elseif structures.

Then length of a block is managed with the ``longBlock`` parameter. By default, it is 200 lines, from beginning to the end. Comments are taken into account.

.. code-block:: php
   
   <?php
   
   $i = 0;
   do {
       // 200 lines of PHP code
       
       ++$i;
   } while($i < 100);
   
   ?>

+-----------+---------+---------+---------------------------------------------------------------------------------------------------------------------------+
| Name      | Default | Type    | Description                                                                                                               |
+-----------+---------+---------+---------------------------------------------------------------------------------------------------------------------------+
| longBlock | 200     | integer | Size of a block for it to be too long. A block is commanded by a for, foreach, while, do...while, if/then else structure. |
+-----------+---------+---------+---------------------------------------------------------------------------------------------------------------------------+


Connex PHP features
-------------------

  + `Block <https://php-dictionary.readthedocs.io/en/latest/dictionary/block.ini.html>`_


Suggestions
___________

* Move the code of the block to an method or a function
* Move part of the code of the block to methods or functions
* Extract repeated patterns and use them




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/LongBlock                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
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


