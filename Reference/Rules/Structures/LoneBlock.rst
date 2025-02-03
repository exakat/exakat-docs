.. _structures-loneblock:


.. _lone-blocks:

Lone Blocks
+++++++++++


.. meta::

	:description:

		Lone Blocks: Grouped code without a commanding structure is useless and may be removed.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Lone Blocks

	:twitter:description: Lone Blocks: Grouped code without a commanding structure is useless and may be removed

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Lone Blocks

	:og:type: article

	:og:description: Grouped code without a commanding structure is useless and may be removed

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Lone Blocks.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/LoneBlock.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/LoneBlock.html","name":"Lone Blocks","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Grouped code without a commanding structure is useless and may be removed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Lone Blocks.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Grouped code without a commanding structure is useless and may be removed. 

Blocks are compulsory when defining a structure, such as a class, a function or a switch. They are most often used with flow control instructions, like if then or foreach. 

Blocks are also valid syntax that group several instructions together, though they have no effect at all. They are unusual enough to confuse the reader. 

Most often, it is a ruin from a previous flow control instruction, whose condition was removed or commented. They should be removed.

.. code-block:: php
   
   <?php
   
       // Lone block without artefact
       {
       	$a = 3;
       	$c = 4;
       }
   
       // Lone block with commented out loop
       //foreach($a as $b) 
       {
           $b = 1;
       }
   ?>
Connex PHP features
-------------------

  + `block <https://php-dictionary.readthedocs.io/en/latest/dictionary/block.ini.html>`_


Suggestions
___________

* Remove the useless curly brackets




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/LoneBlock                                                                                                                                                                    |
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
| Examples     | :ref:`case-thinkphp-structures-loneblock`, :ref:`case-tine20-structures-loneblock`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


