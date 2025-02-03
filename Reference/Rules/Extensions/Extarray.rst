.. _extensions-extarray:

.. _ext-array:

ext/array
+++++++++

.. meta::
	:description:
		ext/array: Core functions processing arrays.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/array
	:twitter:description: ext/array: Core functions processing arrays
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/array
	:og:type: article
	:og:description: Core functions processing arrays
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/array.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extarray.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extarray.html","name":"ext\/array","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Core functions processing arrays","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/array.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Core functions processing arrays.

These functions manipulate arrays in various ways. Arrays are essential for storing, managing, and operating on sets of variables.

This is not a real extension : it is a documentation section, that helps classifying the functions.

.. code-block:: php
   
   <?php
   function odd($var)
   {
       // returns whether the input integer is odd
       return($var & 1);
   }
   
   function even($var)
   {
       // returns whether the input integer is even
       return(!($var & 1));
   }
   
   $array1 = array('a'=>1, 'b'=>2, 'c'=>3, 'd'=>4, 'e'=>5);
   $array2 = array(6, 7, 8, 9, 10, 11, 12);
   
   echo 'Odd :'.PHP_EOL;
   print_r(array_filter($array1, 'odd'));
   echo 'Even:'.PHP_EOL;
   print_r(array_filter($array2, 'even'));
   ?>

See also `Arrays <https://www.php.net/manual/en/book.array.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extarray                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


