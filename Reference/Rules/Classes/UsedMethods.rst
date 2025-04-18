.. _classes-usedmethods:


.. _used-methods:

Used Methods
++++++++++++

.. meta::
	:description:
		Used Methods: Those methods are used in the code: this means they have a definition and at least one call.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Methods
	:twitter:description: Used Methods: Those methods are used in the code: this means they have a definition and at least one call
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Methods
	:og:type: article
	:og:description: Those methods are used in the code: this means they have a definition and at least one call
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Used Methods.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsedMethods.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsedMethods.html","name":"Used Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Those methods are used in the code: this means they have a definition and at least one call","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Used Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those methods are used in the code: this means they have a definition and at least one call. They may have more than one call too. This analysis is mostly useful for detecting unused methods.

.. code-block:: php
   
   <?php
   
   class foo {
       public function used() {
           $this->used();
       }
   
       // No usage of 'unused', as method call, in or out of the definition class.
       public function unused() {
           $this->used();
       }
   }
   
   class bar extends foo {
       public function some() {
           $this->used();
       }
   }
   
   $a = new foo();
   $a->used();
   
   ?>
Connex PHP features
-------------------

  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UsedMethods                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


