.. _structures-newlinestyle:


.. _new-line-style:

New Line Style
++++++++++++++

.. meta::
	:description:
		New Line Style: New lines may be written with the sequence \n or with the constant PHP_EOL.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Line Style
	:twitter:description: New Line Style: New lines may be written with the sequence \n or with the constant PHP_EOL
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Line Style
	:og:type: article
	:og:description: New lines may be written with the sequence \n or with the constant PHP_EOL
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/New Line Style.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NewLineStyle.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NewLineStyle.html","name":"New Line Style","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"New lines may be written with the sequence \\n or with the constant PHP_EOL","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/New Line Style.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

New lines may be written with the sequence \n or with the constant `PHP_EOL <https://www.php.net/PHP_EOL>`_.

When one of those alternatives is used over 90% of the time, it is considered as standard : the remaining are reported.

\n are only located when used alone, in "\n" \(including the double quotes\). When \n is used inside a double-quoted string, its replacement with `PHP_EOL <https://www.php.net/PHP_EOL>`_ would be cumbersome : as such, they are ignored by this analyzer.

.. code-block:: php
   
   <?php
   
   // This may be repeated over 10 times
   $a = "PHP is a great language\n"; 
   $a .= "\n"; 
   
   // This only appears once in the code : this line is reported.
   $b = $a.PHP_EOL.$c; 
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NewLineStyle                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.8                                                                                                                   |
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


