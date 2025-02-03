.. _exceptions-alreadycaught:


.. _exception-order:

Exception Order
+++++++++++++++

.. meta::
	:description:
		Exception Order: When catching exception, the most specialized exceptions must be in the early catch, and the most general exceptions must be in the later catch.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Exception Order
	:twitter:description: Exception Order: When catching exception, the most specialized exceptions must be in the early catch, and the most general exceptions must be in the later catch
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Exception Order
	:og:type: article
	:og:description: When catching exception, the most specialized exceptions must be in the early catch, and the most general exceptions must be in the later catch
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Exception Order.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/AlreadyCaught.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/AlreadyCaught.html","name":"Exception Order","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"When catching exception, the most specialized exceptions must be in the early catch, and the most general exceptions must be in the later catch","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Exception Order.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When catching `exception <https://www.php.net/exception>`_, the most specialized exceptions must be in the early catch, and the most general exceptions must be in the later catch. Otherwise, the general catches intercept the `exception <https://www.php.net/exception>`_, and the more specialized will not be read.

.. code-block:: php
   
   <?php
   
   class A extends \Exception {}
   class B extends A {}
   
   try {
       throw new A();
   } 
   catch(A $a1) { }
   catch(B $b2 ) { 
       // Never reached, as previous Catch is catching the early worm
   }
   
   ?>
Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Remove one of the catch clause




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/AlreadyCaught                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-exceptions-alreadycaught`                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


