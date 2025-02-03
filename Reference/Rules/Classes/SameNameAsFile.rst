.. _classes-samenameasfile:

.. _not-same-name-as-file:

Not Same Name As File
+++++++++++++++++++++

.. meta::
	:description:
		Not Same Name As File: The class, interface or trait in this file as a different name, case included, than the file name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Not Same Name As File
	:twitter:description: Not Same Name As File: The class, interface or trait in this file as a different name, case included, than the file name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Not Same Name As File
	:og:type: article
	:og:description: The class, interface or trait in this file as a different name, case included, than the file name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Not Same Name As File.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/SameNameAsFile.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/SameNameAsFile.html","name":"Not Same Name As File","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The class, interface or trait in this file as a different name, case included, than the file name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Not Same Name As File.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The class, interface or trait in this file as a different name, case included, than the file name. 

In the following example,  the file name is ``Foo.php``.

.. code-block:: php
   
   <?php
   
   // normal host of this file
   class Foo {
       // some code
   }
   
   // case-typo this file
   class foo {
       // some code
   }
   
   // strangely stored class 
   class foo {
       // some code
   }
   
   // This is valid name, but there is also a Foo class, and other classe in this file. 
   interface Foo {}
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/SameNameAsFile                                                                                                  |
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


