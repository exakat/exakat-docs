.. _classes-classoperatoronobject:


.. _class-operator-on-object:

\:\:class Operator On Object
++++++++++++++++++++++++++++

.. meta::
	:description:
		::class Operator On Object: ``::class`` operator used to work only on class identifier.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ::class Operator On Object
	:twitter:description: ::class Operator On Object: ``::class`` operator used to work only on class identifier
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ::class Operator On Object
	:og:type: article
	:og:description: ``::class`` operator used to work only on class identifier
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/::class Operator On Object.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ClassOperatorOnObject.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ClassOperatorOnObject.html","name":"::class Operator On Object","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 07 Mar 2025 15:43:32 +0000","dateModified":"Fri, 07 Mar 2025 15:43:32 +0000","description":"``::class`` operator used to work only on class identifier","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/::class Operator On Object.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``\:\:class`` operator used to work only on class identifier. Since PHP 8.0, it also works on objects: this saves a call to ``get_class()`` or equivalent.

It is convenient when the class is available through an object parameter.

.. code-block:: php
   
   <?php
   
   function foo(Bar $x) {
       return $x::class; // returns the class of the object
   
       return get_class($x); // same as above
   }
   
   ?>
Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `Scope Resolution Operator :: <https://php-dictionary.readthedocs.io/en/latest/dictionary/scope-resolution-operator.ini.html>`_


Suggestions
___________

* Use the ``::class`` operator, instead of ``get_class()``.




Specs
_____

+--------------+------------------------------------------------------------------------------+
| Short name   | Classes/ClassOperatorOnObject                                                |
+--------------+------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>` |
+--------------+------------------------------------------------------------------------------+
| Exakat since | 2.7.0                                                                        |
+--------------+------------------------------------------------------------------------------+
| PHP Version  | All                                                                          |
+--------------+------------------------------------------------------------------------------+
| Severity     | Minor                                                                        |
+--------------+------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                              |
+--------------+------------------------------------------------------------------------------+
| Precision    | High                                                                         |
+--------------+------------------------------------------------------------------------------+
| Available in |                                                                              |
+--------------+------------------------------------------------------------------------------+


