.. _php-foreachobject:


.. _foreach-on-object:

Foreach On Object
+++++++++++++++++

.. meta::
	:description:
		Foreach On Object: Foreach on object looks like a typo.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Foreach On Object
	:twitter:description: Foreach On Object: Foreach on object looks like a typo
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Foreach On Object
	:og:type: article
	:og:description: Foreach on object looks like a typo
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Foreach On Object.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ForeachObject.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ForeachObject.html","name":"Foreach On Object","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Foreach on object looks like a typo","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Foreach On Object.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Foreach on object looks like a typo. This is particularly `true <https://www.php.net/true>`_ when both object and member are variables.

Foreach on an object member is a legit PHP syntax, though it is very rare : blind variables rarely have to be securing in an object to be processed.

.. code-block:: php
   
   <?php
   
   // This is the real thing
   foreach($array as $o => $b) { 
       doSomething();
   }
   
   // Looks suspicious
   foreach($array as $o -> $b) { 
       doSomething();
   }
   
   ?>
Connex PHP features
-------------------

  + `Foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `Loops <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ForeachObject                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


