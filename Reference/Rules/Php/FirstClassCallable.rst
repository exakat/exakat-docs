.. _php-firstclasscallable:


.. _first-class-callable:

First Class Callable
++++++++++++++++++++

.. meta::
	:description:
		First Class Callable: A syntax using ellipsis was introduced to make it easy to make a method into a callable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: First Class Callable
	:twitter:description: First Class Callable: A syntax using ellipsis was introduced to make it easy to make a method into a callable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: First Class Callable
	:og:type: article
	:og:description: A syntax using ellipsis was introduced to make it easy to make a method into a callable
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/First Class Callable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/FirstClassCallable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/FirstClassCallable.html","name":"First Class Callable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A syntax using ellipsis was introduced to make it easy to make a method into a callable","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/First Class Callable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A syntax using ellipsis was introduced to make it easy to make a method into a callable.

.. code-block:: php
   
   <?php
   
   // Using ellipsis as the only argument
   $a = $object->method(...);
   
   // Old style equivalent
   $a = array($object, 'method');
   
   // calling the closure.
   $a();
   
   ?>

See also `PHP RFC: First-class callable syntax <https://wiki.php.net/rfc/first_class_callable_syntax>`_.

Connex PHP features
-------------------

  + `first-class-callable <https://php-dictionary.readthedocs.io/en/latest/dictionary/first-class-callable.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/FirstClassCallable                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


