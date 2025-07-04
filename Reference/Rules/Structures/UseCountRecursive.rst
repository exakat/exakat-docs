.. _structures-usecountrecursive:


.. _use-recursive-count():

Use Recursive count()
+++++++++++++++++++++

.. meta::
	:description:
		Use Recursive count(): The native count() function is recursive: it can count all the elements inside multi-dimensional arrays.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Recursive count()
	:twitter:description: Use Recursive count(): The native count() function is recursive: it can count all the elements inside multi-dimensional arrays
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Recursive count()
	:og:type: article
	:og:description: The native count() function is recursive: it can count all the elements inside multi-dimensional arrays
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Recursive count().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseCountRecursive.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseCountRecursive.html","name":"Use Recursive count()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The native count() function is recursive: it can count all the elements inside multi-dimensional arrays","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use Recursive count().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The native `count() <https://www.php.net/count>`_ function is recursive: it can count all the elements inside multi-dimensional arrays. 

The second argument of count, when set to ``COUNT_RECURSIVE``, count recursively the elements. 

Recursive `count() <https://www.php.net/count>`_ counts all the elements, includeing the recusrive elements themselves. For a 2 dimensional array, this means removing the normal count of elements from the list. For higher dimensions, removing the recursive elememnts requires better filtering.

.. code-block:: php
   
   <?php
   
   $array = array( array(1,2,3), array(4,5,6));
   
   print (count($array, COUNT_RECURSIVE) - count($array, COUNT_NORMAL));
   
   $count = 0;
   foreach($array as $a) {
       $count += count($a);
   }
   print $count;
   
   ?>

See also `count <https://www.php.net/count>`_.


Suggestions
___________

* Drop the loop and use the 2nd argument of count()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseCountRecursive                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-structures-usecountrecursive`, :ref:`case-prestashop-structures-usecountrecursive`                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


