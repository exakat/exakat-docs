.. _classes-usedprotectedmethod:

.. _used-protected-method:

Used Protected Method
+++++++++++++++++++++

.. meta::
	:description:
		Used Protected Method: This rule marks protected methods being used in the current class or its children classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Protected Method
	:twitter:description: Used Protected Method: This rule marks protected methods being used in the current class or its children classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Protected Method
	:og:type: article
	:og:description: This rule marks protected methods being used in the current class or its children classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Used Protected Method.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsedProtectedMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsedProtectedMethod.html","name":"Used Protected Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rule marks protected methods being used in the current class or its children classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Used Protected Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This rule marks protected methods being used in the current class or its children classes. This show how the methods are used inside a class hierarchy.

.. code-block:: php
   
   <?php
   
   class foo {
       // This is reported
       protected usedByChildren() {}
   
       // This is not reported
       protected notUsedByChildren() {}
   }
   
   class bar extends foo {
       // The parent method is not overloaded, though it may be 
       protected someMethod() {
           // The parent method is called 
           $this->usedByChildren();
       }
   
   }
   
   ?>

See also `Visibility <https://www.php.net/manual/en/language.oop5.visibility.php>`_.

Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UsedProtectedMethod                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


