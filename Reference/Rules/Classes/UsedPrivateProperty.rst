.. _classes-usedprivateproperty:

.. _used-static-properties:

Used Static Properties
++++++++++++++++++++++

.. meta::
	:description:
		Used Static Properties: List of all static properties that are used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Static Properties
	:twitter:description: Used Static Properties: List of all static properties that are used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Static Properties
	:og:type: article
	:og:description: List of all static properties that are used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Used Static Properties.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsedPrivateProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsedPrivateProperty.html","name":"Used Static Properties","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"List of all static properties that are used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Used Static Properties.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of all `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties that are used.

A private property is used when it is defined and read. A private property that is only written is not used. A property that is only read is used, as it may have a default value, or act as `NULL <https://www.php.net/manual/en/language.types.null.php>`_.

.. code-block:: php
   
   <?php
   
   class foo {
       // This is a used property (see bar method)
       private $used = 1;
   
       function bar($a) {
           $this->used += $a;
           
           return $this->used;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UsedPrivateProperty                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


