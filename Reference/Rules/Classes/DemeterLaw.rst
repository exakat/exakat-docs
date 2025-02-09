.. _classes-demeterlaw:


.. _law-of-demeter:

Law of Demeter
++++++++++++++

.. meta::
	:description:
		Law of Demeter: The law of Demeter specifies a number of constraints to apply to methodcalls from within an method, so as to keep dependencies to a minimum.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Law of Demeter
	:twitter:description: Law of Demeter: The law of Demeter specifies a number of constraints to apply to methodcalls from within an method, so as to keep dependencies to a minimum
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Law of Demeter
	:og:type: article
	:og:description: The law of Demeter specifies a number of constraints to apply to methodcalls from within an method, so as to keep dependencies to a minimum
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Law of Demeter.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DemeterLaw.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DemeterLaw.html","name":"Law of Demeter","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The law of Demeter specifies a number of constraints to apply to methodcalls from within an method, so as to keep dependencies to a minimum","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Law of Demeter.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The law of Demeter specifies a number of constraints to apply to methodcalls from within an method, so as to keep dependencies to a minimum.

.. code-block:: php
   
   <?php
   
   class x {
       function foo($arg) {
           $this->foo();    // calling oneself is OK
           $this->x->bar(); // calling one's property is OK
           $arg->bar2();    // calling arg's methods is OK
   
           $local = new y();
           $z = $y->bar3();      // calling a local variable is OK
   
           $z->bar4();      // calling a method on a previous result is wrong
       }
   }
   
   ?>

See also `Do your objects talk to strangers? <https://www.brandonsavage.net/do-your-objects-talk-to-strangers/>`_ and `Law of Demeter <https://en.wikipedia.org/wiki/Law_of_Demeter>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DemeterLaw                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


