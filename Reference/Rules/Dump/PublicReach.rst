.. _dump-publicreach:


.. _public-reach-to-private-methods:

Public Reach To Private Methods
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Public Reach To Private Methods: This rule reports the ways to reach private and protected methods, by using only public methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Public Reach To Private Methods
	:twitter:description: Public Reach To Private Methods: This rule reports the ways to reach private and protected methods, by using only public methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Public Reach To Private Methods
	:og:type: article
	:og:description: This rule reports the ways to reach private and protected methods, by using only public methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Public Reach To Private Methods.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/PublicReach.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/PublicReach.html","name":"Public Reach To Private Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rule reports the ways to reach private and protected methods, by using only public methods","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Public Reach To Private Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports the ways to reach private and protected methods, by using only public methods. 

Each internal is reported here, with the origin and destination. When connecting the calls from methods to method, it is possible to draw the path from public methods to private methods.

This class map is useful to prepare tests and improve coverage by targeting public methods that may use restricted methods.

Note that conditions will apply (pun intended) : a link between two methods only means that one may call the other, given the right conditions.

.. code-block:: php
   
   <?php
   
   class A {
   	// This method be reached publicly, and it triggers a call to bar()
   	public function foo() {
   		$this->bar();
   	}
   	
   	// This method cannot be reached publicly
   	private function bar() {
   		// doSomething()
   	}
   }
   
   ?>
Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/PublicReach                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


