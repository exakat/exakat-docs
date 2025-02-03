.. _structures-emptyblocks:

.. _empty-blocks:

Empty Blocks
++++++++++++

.. meta::
	:description:
		Empty Blocks: Full empty block, part of a control structures.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Blocks
	:twitter:description: Empty Blocks: Full empty block, part of a control structures
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Blocks
	:og:type: article
	:og:description: Full empty block, part of a control structures
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Empty Blocks.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/EmptyBlocks.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/EmptyBlocks.html","name":"Empty Blocks","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Full empty block, part of a control structures","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Empty Blocks.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Full empty block, part of a control structures. 

It is recommended to remove those blocks, so as to reduce confusion in the code.

.. code-block:: php
   
   <?php
   
   foreach($foo as $bar) ; // This block seems erroneous
       $foobar++;
   
   if ($a === $b) {
       doSomething();
   } else {
       // Empty block. Remove this
   }
   
   // Blocks containing only empty expressions are also detected
   for($i = 0; $i < 10; $i++) {
       ;
   }
   
   // Although namespaces are not control structures, they are reported here
   namespace A;
   namespace B;
   
   ?>
Connex PHP features
-------------------

  + `block <https://php-dictionary.readthedocs.io/en/latest/dictionary/block.ini.html>`_


Suggestions
___________

* Fill the block with a command
* Fill the block with a comment that explain the situation
* Remove the block and its commanding operator




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EmptyBlocks                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-cleverstyle-structures-emptyblocks`, :ref:`case-phpipam-structures-emptyblocks`                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


