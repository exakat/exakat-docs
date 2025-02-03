.. _structures-dontmixplusplus:

.. _don't-mix-++:

Don't Mix ++
++++++++++++

.. meta::
	:description:
		Don't Mix ++: ++ operators, pre and post, have two distinct behaviors, and should be used separately.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Don't Mix ++
	:twitter:description: Don't Mix ++: ++ operators, pre and post, have two distinct behaviors, and should be used separately
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Don't Mix ++
	:og:type: article
	:og:description: ++ operators, pre and post, have two distinct behaviors, and should be used separately
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Don't Mix ++.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DontMixPlusPlus.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DontMixPlusPlus.html","name":"Don't Mix ++","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"++ operators, pre and post, have two distinct behaviors, and should be used separately","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Don't Mix ++.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>++ operators, pre and post, have two distinct behaviors, and should be used separately.

When mixed in a larger expression, they are difficult to read, and may lead to unwanted behaviors.

.. code-block:: php
   
   <?php
   
       // Clear and defined behavior
       $i++;
       $a[$i] = $i;
   
       // The index is also incremented, as it is used AFTP the incrementation
       // With $i = 2; $a is array(3 => 3)
       $a[$i] = ++$i;
   
       // $i is actually modified twice 
       $i = --$i + 1; 
   ?>

See also `EXP30-C. Do not depend on the order of evaluation for side effects <https://wiki.sei.cmu.edu/confluence/display/c/EXP30-C.+Do+not+depend+on+the+order+of+evaluation+for+side+effects>`_.

Connex PHP features
-------------------

  + `readability <https://php-dictionary.readthedocs.io/en/latest/dictionary/readability.ini.html>`_


Suggestions
___________

* Extract the increment from the expression, and put it on a separate line.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontMixPlusPlus                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-structures-dontmixplusplus`, :ref:`case-typo3-structures-dontmixplusplus`                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


