.. _structures-blindvariableusedbeyondloop:


.. _blind-variable-used-beyond-loop:

Blind Variable Used Beyond Loop
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Blind Variable Used Beyond Loop: Foreach() loops defines variables, which are traditionally used only inside the loop block.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Blind Variable Used Beyond Loop
	:twitter:description: Blind Variable Used Beyond Loop: Foreach() loops defines variables, which are traditionally used only inside the loop block
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Blind Variable Used Beyond Loop
	:og:type: article
	:og:description: Foreach() loops defines variables, which are traditionally used only inside the loop block
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Blind Variable Used Beyond Loop.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/BlindVariableUsedBeyondLoop.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/BlindVariableUsedBeyondLoop.html","name":"Blind Variable Used Beyond Loop","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Foreach() loops defines variables, which are traditionally used only inside the loop block","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Blind Variable Used Beyond Loop.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops defines variables, which are traditionally used only inside the loop block. Using them beyond that limit often leads to surprises.

.. code-block:: php
   
   <?php
   
   foreach($a as $b => $c) {
   	echo "$b : $c\n";
   }
   // $b is set inside the loop, but used beyond
   $max = $b;
   
   ?>
Connex PHP features
-------------------

  + `Blind Variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/blind-variable.ini.html>`_
  + `Loops <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/BlindVariableUsedBeyondLoop                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


