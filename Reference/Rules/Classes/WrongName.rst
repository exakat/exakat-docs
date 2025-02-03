.. _classes-wrongname:

.. _illegal-name-for-method:

Illegal Name For Method
+++++++++++++++++++++++

.. meta::
	:description:
		Illegal Name For Method: PHP has reserved usage of methods starting with ``__`` for magic methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Illegal Name For Method
	:twitter:description: Illegal Name For Method: PHP has reserved usage of methods starting with ``__`` for magic methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Illegal Name For Method
	:og:type: article
	:og:description: PHP has reserved usage of methods starting with ``__`` for magic methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Illegal Name For Method.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/WrongName.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/WrongName.html","name":"Illegal Name For Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"PHP has reserved usage of methods starting with ``__`` for magic methods","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Illegal Name For Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>PHP has reserved usage of methods starting with ``__`` for magic methods. It is recommended to avoid using this prefix, to prevent confusions.

.. code-block:: php
   
   <?php
   
   class foo{
       // Constructor
       function __construct() {}
   
       // Constructor's typo
       function __constructor() {}
   
       // Illegal function name, even as private
       private function __bar() {}
   }
   
   ?>

See also `Magic Methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.

Connex PHP features
-------------------

  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Avoid method names starting with a double underscore : ``__``
* Use method visibilities to ensure that methods are only available to the current class or its children




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/WrongName                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-prestashop-classes-wrongname`, :ref:`case-magento-classes-wrongname`                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


