.. _structures-staticloop:


.. _static-loop:

Static Loop
+++++++++++

.. meta::
	:description:
		Static Loop: Static loop may be preprocessed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Static Loop
	:twitter:description: Static Loop: Static loop may be preprocessed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Static Loop
	:og:type: article
	:og:description: Static loop may be preprocessed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Static Loop.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/StaticLoop.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/StaticLoop.html","name":"Static Loop","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Static loop may be preprocessed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Static Loop.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`Static <https://www.php.net/manual/en/language.oop5.static.php>`_ loop may be preprocessed.

It looks like the following loops are `static <https://www.php.net/manual/en/language.oop5.static.php>`_ : the same code is executed each time, without taking into account loop variables.
It is possible to create loops that don't use any blind variables, though this is fairly rare. In particular, calling a method may update an internal pointer, like `next() <https://www.php.net/next>`_ or ``SimpleXMLIterator\:\:`next() <https://www.php.net/next>`_``. 

It is recommended to turn a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ loop into an expression that avoid the loop. For example, replacing the sum of all integers by the ``function $n * ($n + 1) / 2``, or using `array_sum() <https://www.php.net/array_sum>`_.

This analysis doesn't detect usage of variables with ``compact``.

.. code-block:: php
   
   <?php
   
   // Static loop
   $total = 0;
   for($i = 0; $i < 10; $i++) {
       $total += $i;
   }
   
   // The above loop may be replaced by (with some math help)
   $total = 10 * (10  + 1) / 2;
   
   // Non-Static loop (the loop depends on the size of the array)
   $n = count($array);
   for($i = 0; $i < $n; $i++) {
       $total += $i;
   }
   
   ?>
Connex PHP features
-------------------

  + `Loops <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Precalculate the result of that loop and removes it altogether
* Check that the loop is not missing a blind variable usage
* Replace the usage of a loop with a native PHP call : for example, with str_repeat(). Although the loop is still here, it usually reflects better the intend.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/StaticLoop                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


