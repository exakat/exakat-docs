.. _performances-useblindvar:


.. _use-the-blind-var:

Use The Blind Var
+++++++++++++++++

.. meta::
	:description:
		Use The Blind Var: When in a loop, it is faster to rely on the blind var, rather than the original source.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use The Blind Var
	:twitter:description: Use The Blind Var: When in a loop, it is faster to rely on the blind var, rather than the original source
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use The Blind Var
	:og:type: article
	:og:description: When in a loop, it is faster to rely on the blind var, rather than the original source
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use The Blind Var.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/UseBlindVar.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/UseBlindVar.html","name":"Use The Blind Var","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When in a loop, it is faster to rely on the blind var, rather than the original source","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use The Blind Var.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When in a loop, it is faster to rely on the blind var, rather than the original source.

When the key is referenced in the foreach loop, it is faster to use the available container to access a value for reading.

Note that it is also faster to use the value with a reference to handle the writings.

.. code-block:: php
   
   <?php
   
   // Reaching $source[$key] via $value is faster
   foreach($source as $key => $value) {
       $coordinates = array('x' => $value[0],
                            'y' => $value[1]);
   }
   
   // Reaching $source[$key] via $source is slow
   foreach($source as $key => $value) {
       $coordinates = array('x' => $source[$key][0],
                            'y' => $source[$key][1]);
   }
   
   ?>
Connex PHP features
-------------------

  + `Blind Variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/blind-variable.ini.html>`_


Suggestions
___________

* Use the blind var




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/UseBlindVar                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.9                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


