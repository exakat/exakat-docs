.. _classes-disconnectedclasses:

.. _disconnected-classes:

Disconnected Classes
++++++++++++++++++++

.. meta::
	:description:
		Disconnected Classes: One class is extending the other, but they do not use any features from one another.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Disconnected Classes
	:twitter:description: Disconnected Classes: One class is extending the other, but they do not use any features from one another
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Disconnected Classes
	:og:type: article
	:og:description: One class is extending the other, but they do not use any features from one another
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Disconnected Classes.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DisconnectedClasses.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DisconnectedClasses.html","name":"Disconnected Classes","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"One class is extending the other, but they do not use any features from one another","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Disconnected Classes.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>One class is extending the other, but they do not use any features from one another. Basically, those two classes are using extends, but they are completely independent and may be separated. 

When using the 'extends' keyword, the newly created classes are now acting together and making one. This should be visible in calls from one class to the other, or simply by property usage : they can't live without each other.

On the other hand, two completely independent classes that are merged, although they should be kept separated.

.. code-block:: php
   
   <?php
   
   class A {
       private $pa = 1;
       
       function fooA() {
           $this->pa = 2;
       }
   }
   
   // class B and Class A are totally independent
   class B extends A {
       private $pb = 1;
       
       function fooB() {
           $this->pb = 2;
       }
   }
   
   
   // class C makes use of class A : it is dependent on the parent class
   class C extends A {
       private $pc = 1;
       
       function fooB() {
           $this->pc = 2 + $this->fooA();
       }
   }
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Remove the extension
* Make actual usage of the classes, at least from one of them




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DisconnectedClasses                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.9                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-classes-disconnectedclasses`                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


