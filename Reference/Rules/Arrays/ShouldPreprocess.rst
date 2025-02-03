.. _arrays-shouldpreprocess:


.. _preprocess-arrays:

Preprocess Arrays
+++++++++++++++++


.. meta::

	:description:

		Preprocess Arrays: Using long list of assignations for initializing arrays is significantly slower than the declaring them as an array.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Preprocess Arrays

	:twitter:description: Preprocess Arrays: Using long list of assignations for initializing arrays is significantly slower than the declaring them as an array

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Preprocess Arrays

	:og:type: article

	:og:description: Using long list of assignations for initializing arrays is significantly slower than the declaring them as an array

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Preprocess Arrays.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/ShouldPreprocess.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/ShouldPreprocess.html","name":"Preprocess Arrays","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Using long list of assignations for initializing arrays is significantly slower than the declaring them as an array","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Preprocess Arrays.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Using long list of assignations for initializing arrays is significantly slower than the declaring them as an array. 

If the array has to be completed rather than created, it is also faster to use += when there are more than ten elements to add.

.. code-block:: php
   
   <?php
   
   // Slow way
   $a = []; // also with $a = array();
   $a[1] = 2;
   $a[2] = 3;
   $a[3] = 5;
   $a[4] = 7;
   $a[5] = 11;
   
   // Faster way
   $a = [1 => 2, 
         2 => 3,
         3 => 5,
         4 => 7,
         5 => 11];
   
   // Even faster way if indexing is implicit
   $a = [2, 3, 5, 7, 11];
   
   ?>
Connex PHP features
-------------------

  + `preprocess <https://php-dictionary.readthedocs.io/en/latest/dictionary/preprocess.ini.html>`_


Suggestions
___________

* Preprocess the code so PHP doesn't do it at execution time. Keep the detailed version into comments.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/ShouldPreprocess                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


