.. _structures-inconsistentconcatenation:


.. _inconsistent-concatenation:

Inconsistent Concatenation
++++++++++++++++++++++++++


.. meta::

	:description:

		Inconsistent Concatenation: Concatenations happens within a string or using the dot operator.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Inconsistent Concatenation

	:twitter:description: Inconsistent Concatenation: Concatenations happens within a string or using the dot operator

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Inconsistent Concatenation

	:og:type: article

	:og:description: Concatenations happens within a string or using the dot operator

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Inconsistent Concatenation.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InconsistentConcatenation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InconsistentConcatenation.html","name":"Inconsistent Concatenation","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"Concatenations happens within a string or using the dot operator","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Inconsistent Concatenation.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Concatenations happens within a string or using the dot operator. Using both is an inconsistent way of writing concatenations.

Switching methods of concatenation, sometimes in the same expression, is `error <https://www.php.net/error>`_ prone. The reader gets confused, and may miss important information. 

There are some situations where using concatenation are compulsory : when calling a constant, or a function, or make use of the escape sequence. Those are ignored in this analysis.

.. code-block:: php
   
   <?php
   
     //Concatenation
     $consistent = $a . 'b'. $c;
   
     //Interpolation
     $consistentToo = "{$a}b$c";
   
     // Concatenation and interpolation
     $inconsistent = $a . "b$c";
   
     // Concatenation and interpolation too
     $consistentThree = <<<CONSISTENT
   {$a}b$c
   CONSISTENT;
   
     // Concatenation and interpolation collisions
     $collision = theClass::CONSTANTE . "b{$c}".number_format($t, 2).' $CAD'."\n";
   
   ?>
Connex PHP features
-------------------

  + `concat <https://php-dictionary.readthedocs.io/en/latest/dictionary/concat.ini.html>`_


Suggestions
___________

* Make concatenation consistent, to make the code easier to read.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InconsistentConcatenation                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-fuelcms-structures-inconsistentconcatenation`                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


