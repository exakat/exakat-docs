.. _classes-couldbeprivatemethod:


.. _method-could-be-private-method:

Method Could Be Private Method
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Method Could Be Private Method: The following methods are never used outside their class of definition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Could Be Private Method
	:twitter:description: Method Could Be Private Method: The following methods are never used outside their class of definition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Could Be Private Method
	:og:type: article
	:og:description: The following methods are never used outside their class of definition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Method Could Be Private Method.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBePrivateMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBePrivateMethod.html","name":"Method Could Be Private Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The following methods are never used outside their class of definition","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Method Could Be Private Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The following methods are never used outside their class of definition. Given the analyzed code, they could be set as private. 
Note that dynamic properties (such as $x->$y) are not taken into account.

.. code-block:: php
   
   <?php
   
   class foo {
       public function couldBePrivate() {}
       public function cantdBePrivate() {}
       
       function bar() {
           // couldBePrivate is used internally. 
           $this->couldBePrivate();
       }
   }
   
   class foo2 extends foo {
       function bar2() {
           // cantdBePrivate is used in a child class. 
           $this->cantdBePrivate();
       }
   }
   
   //couldBePrivate() is not used outside 
   $foo = new foo();
   
   //cantdBePrivate is used outside the class
   $foo->cantdBePrivate();
   
   ?>
Connex PHP features
-------------------

  + `Private Visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/private.ini.html>`_
  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBePrivateMethod                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.11                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


