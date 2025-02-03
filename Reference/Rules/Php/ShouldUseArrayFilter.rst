.. _php-shouldusearrayfilter:


.. _should-use-array\_filter():

Should Use array_filter()
+++++++++++++++++++++++++


.. meta::

	:description:

		Should Use array_filter(): Should use array_filter().

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Should Use array_filter()

	:twitter:description: Should Use array_filter(): Should use array_filter()

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Should Use array_filter()

	:og:type: article

	:og:description: Should use array_filter()

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Use array_filter().html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ShouldUseArrayFilter.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ShouldUseArrayFilter.html","name":"Should Use array_filter()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Should use array_filter()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Use array_filter().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Should use `array_filter() <https://www.php.net/array_filter>`_.

`array_filter() <https://www.php.net/array_filter>`_ is a native PHP function, that extract elements from an array, based on a custom call. Using `array_filter() <https://www.php.net/array_filter>`_ shortens your code, and allows for reusing the filtering logic across the application, instead of hard coding it every time.
`array_filter() <https://www.php.net/array_filter>`_ is faster than `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ (with or without the `isset() <https://www.www.php.net/isset>`_ test) with 3 elements or more, and it is significantly faster beyond 5 elements. Memory consumption is the same.

.. code-block:: php
   
   <?php
   
   $a = range(0, 10); // integers from 0 to 10
   
   // Extracts odd numbers
   $odds = array_filter($a, function($x) { return $x % 2; });
   $odds = array_filter($a, 'odd');
   
   // Slow and cumbersome code for extracting odd numbers
   $odds = array();
   foreach($a as $v) {
       if ($a % 2) { // same filter than the closure above, or the odd function below
           $bColumn[] = $v;
       }
   }
   
   function foo($x) {
       return $x % 2; 
   }
   
   ?>

See also `array_filter <https://php.net/array_filter>`_.


Suggestions
___________

* Use array_filter()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ShouldUseArrayFilter                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-php-shouldusearrayfilter`, :ref:`case-shopware-php-shouldusearrayfilter`                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


