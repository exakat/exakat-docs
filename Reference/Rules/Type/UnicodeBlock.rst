.. _type-unicodeblock:

.. _unicode-blocks:

Unicode Blocks
++++++++++++++

.. meta::
	:description:
		Unicode Blocks: List of the Unicode blocks used in string literals.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unicode Blocks
	:twitter:description: Unicode Blocks: List of the Unicode blocks used in string literals
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unicode Blocks
	:og:type: article
	:og:description: List of the Unicode blocks used in string literals
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unicode Blocks.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/UnicodeBlock.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/UnicodeBlock.html","name":"Unicode Blocks","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"List of the Unicode blocks used in string literals","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unicode Blocks.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of the Unicode blocks used in string literals.

This is the kind of characters that can be found in the applications strings.
Note that Exakat only analyze PHP scripts : any translation available in a ``.po`` or external resource is not parsed and will not show.

.. code-block:: php
   
   <?php
   
   $a = "zoo"; 
   
   $b = "ఒ"; // Telugu character
   $b = "\u{0C12}"; Same as above
   
   $b = "人"; // Chinese Mandarin character
   $b = "\u{4EBA}"; Same as above
   
   ?>

See also `Unicode block <https://en.wikipedia.org/wiki/Unicode_block>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/UnicodeBlock                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


