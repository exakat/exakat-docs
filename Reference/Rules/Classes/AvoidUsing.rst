.. _classes-avoidusing:

.. _custom-class-usage:

Custom Class Usage
++++++++++++++++++

.. meta::
	:description:
		Custom Class Usage: List of usage of custom classes throughout the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Custom Class Usage
	:twitter:description: Custom Class Usage: List of usage of custom classes throughout the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Custom Class Usage
	:og:type: article
	:og:description: List of usage of custom classes throughout the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Custom Class Usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AvoidUsing.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AvoidUsing.html","name":"Custom Class Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"List of usage of custom classes throughout the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Custom Class Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>List of usage of custom classes throughout the code. This might be important when it is time to refactor or remove such usage, before removing the class itself.

.. code-block:: php
   
   <?php
   
   class x {}
   
   // This is a class usage
   $a = new X();
   
   ?>

+------------------+---------+----------+-------------------------------+
| Name             | Default | Type     | Description                   |
+------------------+---------+----------+-------------------------------+
| forbiddenClasses |         | ini_hash | List of classes to be avoided |
+------------------+---------+----------+-------------------------------+


Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AvoidUsing                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


