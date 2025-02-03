.. _structures-noneedforelse:


.. _no-need-for-else:

No Need For Else
++++++++++++++++

.. meta::
	:description:
		No Need For Else: Else is not needed when the Then ends with a break.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Need For Else
	:twitter:description: No Need For Else: Else is not needed when the Then ends with a break
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Need For Else
	:og:type: article
	:og:description: Else is not needed when the Then ends with a break
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Need For Else.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoNeedForElse.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoNeedForElse.html","name":"No Need For Else","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Else is not needed when the Then ends with a break","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Need For Else.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Else is not needed when the Then ends with a `break <https://www.php.net/manual/en/control-structures.break.php>`_. A `break <https://www.php.net/manual/en/control-structures.break.php>`_ may be the following keywords : `break <https://www.php.net/manual/en/control-structures.break.php>`_, `continue <https://www.php.net/manual/en/control-structures.continue.php>`_, return, goto. Any of these send the execution somewhere in the code. The else block is then executed as the main sequence, only if the condition fails.

.. code-block:: php
   
   <?php
   
   function foo() {
       // Else may be in the main sequence.
       if ($a1) {
           return $a1;
       } else {
           $a++;
       }
   
       // Same as above, but negate the condition : if (!$a2) { return $a2; }
       if ($a2) {
           $a++;
       } else {
           return $a2;
       }
   
       // This is OK
       if ($a3) {
           return;
       }
   
       // This has no break
       if ($a4) {
           $a++;
       } else {
           $b++;
       }
   
       // This has no else
       if ($a5) {
           $a++;
       }
   }
   ?>

See also `Object Calisthenics, rule # 2 <http://williamdurand.fr/2013/06/03/object-calisthenics/>`_.

Connex PHP features
-------------------

  + `if-then <https://php-dictionary.readthedocs.io/en/latest/dictionary/if-then.ini.html>`_


Suggestions
___________

* Remove else block, but keep the code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoNeedForElse                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.4                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thelia-structures-noneedforelse`, :ref:`case-thinkphp-structures-noneedforelse`                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


