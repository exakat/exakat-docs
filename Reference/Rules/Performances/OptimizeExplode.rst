.. _performances-optimizeexplode:


.. _optimize-explode():

Optimize Explode()
++++++++++++++++++


.. meta::

	:description:

		Optimize Explode(): Limit explode() results at call time.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Optimize Explode()

	:twitter:description: Optimize Explode(): Limit explode() results at call time

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Optimize Explode()

	:og:type: article

	:og:description: Limit explode() results at call time

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Optimize Explode().html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/OptimizeExplode.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/OptimizeExplode.html","name":"Optimize Explode()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Limit explode() results at call time","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Optimize Explode().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Limit `explode() <https://www.php.net/explode>`_ results at call time. `explode() <https://www.php.net/explode>`_ returns an array, after breaking the argument into smaller strings, with a delimiter. 

By default, `explode() <https://www.php.net/explode>`_ breaks the whole string into smaller strings, and returns the array. When not all the elements of the returned array are necessary, using the third argument of `explode() <https://www.php.net/explode>`_ speeds up the process, by removing unnecessary work.
Limiting `explode() <https://www.php.net/explode>`_ has no effect when the operation is already exact : it simply prevents `explode() <https://www.php.net/explode>`_ to cut more than needed if the argument is unexpectedly large. 

This optimisation applies to split(), `preg_split() <https://www.php.net/preg_split>`_ and `mb_split() <https://www.php.net/mb_split>`_, too.

This is a micro optimisation, unless the exploded string is large.

.. code-block:: php
   
   <?php
   
   $string = '1,2,3,4,5,';
   
   // explode() returns 2 elements, which are then assigned to the list() call.
   list($a, $b) = explode(',', $string, 2);
   
   // explode() returns 6 elements, only two of which are then assigned to the list() call. The rest are discarded.
   list($a, $b) = explode(',', $string, 2);
   
   // it is not possible to skip the first elements, but it is possible to skip the last ones. 
   echo explode(',', $string, 2)[1];
   
   // This protects PHP, in case $string ends up with a lot of commas
   $string = foo(); // usually '1,2' but not known
   list($a, $b) = explode(',', $string, 2);
   ?>

See also `Cryptography Extensions <https://www.php.net/manual/en/refs.crypto.php>`_.

Connex PHP features
-------------------

  + `crypto <https://php-dictionary.readthedocs.io/en/latest/dictionary/crypto.ini.html>`_


Suggestions
___________

* Add a limit to explode() call




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/OptimizeExplode                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


