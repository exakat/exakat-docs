.. _structures-testthencast:

.. _test-then-cast:

Test Then Cast
++++++++++++++

.. meta::
	:description:
		Test Then Cast: A test is run on a value without a cast, and later the cast value is later used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Test Then Cast
	:twitter:description: Test Then Cast: A test is run on a value without a cast, and later the cast value is later used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Test Then Cast
	:og:type: article
	:og:description: A test is run on a value without a cast, and later the cast value is later used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Test Then Cast.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/TestThenCast.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/TestThenCast.html","name":"Test Then Cast","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A test is run on a value without a cast, and later the cast value is later used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Test Then Cast.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>A test is run on a value without a cast, and later the cast value is later used. 

The cast may introduce a distortion to the value, and still lead to the unwanted situation. For example, comparing to 0, then later casting to an int. The comparison to 0 is done without casting, and as such, 0.1 is different from 0. Yet, (int) 0.1 is actually 0, leading to a Division by 0 `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // Here. $x may be different from 0, but (int) $x may be 0
   $x = 0.1;
   
   if ($x != 0) {
       $y = 4 / (int) $x;
   }
   
   // Safe solution : check the cast value.
   if ( (int) $x != 0) {
       $y = 4 / (int) $x;
   }
   
   ?>
Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Test with the cast value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/TestThenCast                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-dolphin-structures-testthencast`, :ref:`case-suitecrm-structures-testthencast`                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


