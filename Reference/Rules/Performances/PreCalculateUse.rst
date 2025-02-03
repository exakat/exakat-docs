.. _performances-precalculateuse:

.. _pre-calculate-use:

Pre-Calculate Use
+++++++++++++++++

.. meta::
	:description:
		Pre-Calculate Use: In a closure, it is faster to pass a final value, rather than calculate it at call time.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Pre-Calculate Use
	:twitter:description: Pre-Calculate Use: In a closure, it is faster to pass a final value, rather than calculate it at call time
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Pre-Calculate Use
	:og:type: article
	:og:description: In a closure, it is faster to pass a final value, rather than calculate it at call time
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Pre-Calculate Use.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/PreCalculateUse.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/PreCalculateUse.html","name":"Pre-Calculate Use","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"In a closure, it is faster to pass a final value, rather than calculate it at call time","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Pre-Calculate Use.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>In a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, it is faster to pass a final value, rather than calculate it at call time. 

In the ``use`` clause of the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, make sure that the passed variables do not require any more processing, such as a call to another function or an extra expression.

This is a micro-optimisation. It has more potential with the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ used in a loop, or an array function.

.. code-block:: php
   
   <?php
   
   // $b->get is calculated inside the closure
   $d = $b->get();
   $f = function ($a) use ($d) {
   	return $d + $a;
   }
   
   // $b->get is calculated inside the closure
   $f = function ($a) use ($b) {
   	return $b->get() + $a;
   }
   ?>
Connex PHP features
-------------------

  + `closure <https://php-dictionary.readthedocs.io/en/latest/dictionary/closure.ini.html>`_
  + `micro-optimisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/micro-optimisation.ini.html>`_


Suggestions
___________

* Inject the final value in the closure and avoid method calls inside the closure




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/PreCalculateUse                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


