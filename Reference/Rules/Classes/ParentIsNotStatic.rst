.. _classes-parentisnotstatic:


.. _parent-is-not-static:

Parent Is Not Static
++++++++++++++++++++

.. meta::
	:description:
		Parent Is Not Static: The `parent` keyword behaves like `self`, not like `static`.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Parent Is Not Static
	:twitter:description: Parent Is Not Static: The `parent` keyword behaves like `self`, not like `static`
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Parent Is Not Static
	:og:type: article
	:og:description: The `parent` keyword behaves like `self`, not like `static`
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Parent Is Not Static.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ParentIsNotStatic.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ParentIsNotStatic.html","name":"Parent Is Not Static","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The `parent` keyword behaves like `self`, not like `static`","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Parent Is Not Static.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The `parent` keyword behaves like `self`, not like `static`. It links to the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ of the defining expression, not to the one being called.

This may skip the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ of the calling class, and create a `Undefined method` call, or yield the wrong `\:\:class` value. It may also skip a local version of the method.

.. code-block:: php
   
   <?php
   
   class w {
   }
   
   class x extends w {
       function foo() {
           parent::method();
       }
   
       // method() is in the parent of Y, but not in the one of X.
       function method() {
           print __METHOD__;
       }
   }
   
   class y extends x {}
   
   (new y)->foo(); 
   // print W::method
   (new y)->method(); 
   // print x::method
   
   ?>
Connex PHP features
-------------------

  + `Self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_
  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_


Suggestions
___________

* Use self keyword
* Use static keyword
* Use hard-coded class name keyword




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ParentIsNotStatic                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.3                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


