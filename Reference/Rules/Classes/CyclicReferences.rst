.. _classes-cyclicreferences:


.. _cyclic-references:

Cyclic References
+++++++++++++++++

.. meta::
	:description:
		Cyclic References: Avoid cyclic references.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cyclic References
	:twitter:description: Cyclic References: Avoid cyclic references
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cyclic References
	:og:type: article
	:og:description: Avoid cyclic references
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cyclic References.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CyclicReferences.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CyclicReferences.html","name":"Cyclic References","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Avoid cyclic references","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Cyclic References.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid cyclic references. 

Cyclic references happen when an object points to another object, which reciprocate. This is particularly possible with classes, when the child class has to keep a reference to the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class. 
Cyclic references, or circular references, are memory intensive : only the garbage collector can understand when they may be flushed from memory, which is a costly operation. On the other hand, in an acyclic reference code, the reference counter will know immediately know that an object is free or not.

.. code-block:: php
   
   <?php
   
   class a {
       private $p = null;
       
       function foo() {
           $this->p = new b();
           // the current class is stored in the child class
           $this->p->m($this);
       }
   }
   
   class b {
       private $pb = null;
       
       function n($a) {
           // the current class keeps a link to its parent
           $this->pb = $a;
       }
   }
   ?>

See also `About circular references in PHP <https://johann.pardanaud.com/blog/about-circular-references-in-php>`_ and `A Journey to find a memory leak <https://jolicode.com/blog/a-journey-to-find-a-memory-leak/>`_.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `extends <https://php-dictionary.readthedocs.io/en/latest/dictionary/extends.ini.html>`_


Suggestions
___________

* Use a different object when calling the child objects. 
* Refactor your code to avoid the cyclic reference.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CyclicReferences                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.3                                                                                                                                                      |
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


