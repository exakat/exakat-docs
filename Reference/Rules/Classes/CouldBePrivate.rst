.. _classes-couldbeprivate:


.. _property-could-be-private:

Property Could Be Private
+++++++++++++++++++++++++

.. meta::
	:description:
		Property Could Be Private: The following properties are never used outside their class of definition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Property Could Be Private
	:twitter:description: Property Could Be Private: The following properties are never used outside their class of definition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Property Could Be Private
	:og:type: article
	:og:description: The following properties are never used outside their class of definition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Property Could Be Private.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBePrivate.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBePrivate.html","name":"Property Could Be Private","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The following properties are never used outside their class of definition","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Property Could Be Private.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following properties are never used outside their class of definition. Given the analyzed code, they could be set as private. 
Note that dynamic properties (such as $x->$y) are not taken into account.

.. code-block:: php
   
   <?php
   
   class foo {
       public $couldBePrivate = 1;
       public $cantdBePrivate = 1;
       
       function bar() {
           // couldBePrivate is used internally. 
           $this->couldBePrivate = 3;
       }
   }
   
   class foo2 extends foo {
       function bar2() {
           // cantdBePrivate is used in a child class. 
           $this->cantdBePrivate = 3;
       }
   }
   
   //$couldBePrivate is not used outside 
   $foo = new foo();
   
   //$cantdBePrivate is used outside the class
   $foo->cantdBePrivate = 2;
   
   ?>
Connex PHP features
-------------------

  + `Visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Remove the unused property
* Use the private property
* Change the visibility to allow access the property from other part of the code




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBePrivate                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


