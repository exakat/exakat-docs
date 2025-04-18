.. _php-usestdclass:


.. _avoid-using-stdclass:

Avoid Using stdClass
++++++++++++++++++++

.. meta::
	:description:
		Avoid Using stdClass: ``stdClass`` is the default class for PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid Using stdClass
	:twitter:description: Avoid Using stdClass: ``stdClass`` is the default class for PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid Using stdClass
	:og:type: article
	:og:description: ``stdClass`` is the default class for PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid Using stdClass.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseStdclass.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseStdclass.html","name":"Avoid Using stdClass","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"``stdClass`` is the default class for PHP","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid Using stdClass.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``stdClass`` is the default class for PHP. It is instantiated when PHP needs to return a object, but no class is specifically available.

It is recommended to avoid instantiating this class. Some PHP or frameworks functions, such as `json_encode() <https://www.php.net/json_encode>`_, do return them : this is fine, although it is reported here.

If you need a ``stdClass`` object, it is faster to build it as an array, then cast it, than instantiate ``stdClass``. This is a micro-optimisation.

.. code-block:: php
   
   <?php
   
   $json = '{"a":1,"b":2,"c":3}';
   $object = json_decode($json);
   // $object is a stdClass, as returned by json_decode
   
   // Fast building of $o
   $a = [];
   $a['a'] = 1;
   $a['b'] = 2;
   $a['c'] = 3;
   json_encode( (object) $a);
   
   // Slow building of $o
   $o = new stdClass();
   $o->a = 1;
   $o->b = 2;
   $o->c = 3;
   json_encode($o);
   
   ?>
Connex PHP features
-------------------

  + `stdclass <https://php-dictionary.readthedocs.io/en/latest/dictionary/stdclass.ini.html>`_


Suggestions
___________

* Create a custom class to handle the properties




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseStdclass                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.1                                                                                                                   |
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


