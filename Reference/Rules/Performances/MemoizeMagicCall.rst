.. _performances-memoizemagiccall:


.. _memoize-magiccall:

Memoize MagicCall
+++++++++++++++++

.. meta::
	:description:
		Memoize MagicCall: Cache calls to magic methods in local variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Memoize MagicCall
	:twitter:description: Memoize MagicCall: Cache calls to magic methods in local variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Memoize MagicCall
	:og:type: article
	:og:description: Cache calls to magic methods in local variable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Memoize MagicCall.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/MemoizeMagicCall.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/MemoizeMagicCall.html","name":"Memoize MagicCall","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Cache calls to magic methods in local variable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Memoize MagicCall.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Cache calls to magic methods in local variable. Local cache is faster than calling again the magic method as soon as the second call, provided that the value hasn't changed.

``__get`` is slower, as it turns a simple member access into a full method call. 
The caching is not possible if the processing of the object changes the value of the property.

.. code-block:: php
   
   <?php
   
   class x {
       private $values = array();
       
       function __get($name) {
           return $this->values[$name];
       }
       // more code to set values to this class
   }
   
   function foo(x $b) {
       $a = $b->a; 
       $c = $b->c;
       
       $d = $c;     // using local cache, no new access to $b->__get($name)
       $e = $b->a;  // Second access to $b->a, through __get
   }
   
   function bar(x $b) {
       $a = $b->a; 
       $c = $b->c;
       
       $b->bar2(); // this changes $b->a and $b->c, but we don't see it
       
       $d = $b->c; 
       $e = $b->a;  // Second access to $b->a, through __get
   }
   
   ?>

+--------------------+---------+---------+-------------------------------------------------------------------------------+
| Name               | Default | Type    | Description                                                                   |
+--------------------+---------+---------+-------------------------------------------------------------------------------+
| minMagicCallsToGet | 2       | integer | Minimal number of calls of a magic property to make it worth locally caching. |
+--------------------+---------+---------+-------------------------------------------------------------------------------+



See also `__get performance questions with PHP <https://stackoverflow.com/questions/3330852/get-set-call-performance-questions-with-php>`_, :ref:`Make Magic Concrete <make-magic-concrete>` and `Benchmarking magic <https://www.garfieldtech.com/blog/benchmarking-magic>`_.

Connex PHP features
-------------------

  + `memoization <https://php-dictionary.readthedocs.io/en/latest/dictionary/memoization.ini.html>`_


Suggestions
___________

* Cache the value in a local variable, and reuse that variable
* Make the property concrete in the class, so as to avoid __get() altogether




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/MemoizeMagicCall                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.3                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


