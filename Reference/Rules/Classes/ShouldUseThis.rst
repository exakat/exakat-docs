.. _classes-shouldusethis:


.. _should-use-local-class:

Should Use Local Class
++++++++++++++++++++++


.. meta::

	:description:

		Should Use Local Class: Methods should use the defining class, or be functions.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Should Use Local Class

	:twitter:description: Should Use Local Class: Methods should use the defining class, or be functions

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Should Use Local Class

	:og:type: article

	:og:description: Methods should use the defining class, or be functions

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Use Local Class.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ShouldUseThis.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ShouldUseThis.html","name":"Should Use Local Class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Methods should use the defining class, or be functions","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Use Local Class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Methods should use the defining class, or be functions.

Methods should use ``$this`` with another method or a property, or call ``parent\:\:``. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods should call another `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, or a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property. 
Methods which are overwritten by a child class are omitted : the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class act as a default value for the children class, and this is correct.
Note that a method using a class constant is not considered as using the local class, for this analyzer.

.. code-block:: php
   
   <?php
   
   class foo {
       public function __construct() {
           // This method should do something locally, or be removed.
       }
   }
   
   class bar extends foo {
       private $a = 1;
       
       public function __construct() {
           // Calling parent:: is sufficient
           parent::__construct();
       }
   
       public function barbar() {
           // This is acting on the local object
           $this->a++;
       }
   
       public function barfoo($b) {
           // This has no action on the local object. It could be a function or a closure where needed
           return 3 + $b;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `$this <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24this.ini.html>`_
  + `self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_


Suggestions
___________

* Make this method a function
* Actually use $this, or any related attributes of the class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ShouldUseThis                                                                                                   |
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
| ClearPHP     | `not-a-method <https://github.com/dseguy/clearPHP/tree/master/rules/not-a-method.md>`__                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


