.. _classes-avoidoptionarrays:

.. _avoid-option-arrays-in-constructors:

Avoid option arrays in constructors
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Avoid option arrays in constructors: Avoid option arrays in constructors.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid option arrays in constructors
	:twitter:description: Avoid option arrays in constructors: Avoid option arrays in constructors
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid option arrays in constructors
	:og:type: article
	:og:description: Avoid option arrays in constructors
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid option arrays in constructors.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AvoidOptionArrays.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/AvoidOptionArrays.html","name":"Avoid option arrays in constructors","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Mon, 03 Feb 2025 17:19:52 +0000","dateModified":"Mon, 03 Feb 2025 17:19:52 +0000","description":"Avoid option arrays in constructors","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Avoid option arrays in constructors.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Avoid option arrays in constructors. Use one parameter per injected element.

Arrays carry only the options at hand. They skip default values, or do not carry any checks and are prone to typos.

.. code-block:: php
   
   <?php
   
   class Foo {
       // Distinct arguments, all typehinted if possible
       function __construct(A $a, B $b, C $c, D $d) {
           $this->a = $a;
           $this->b = $b;
           $this->c = $c;
           $this->d = $d;
       }
   }
   
   class Bar {
       // One argument, spread over several properties
       function __construct(array $options) {
           $this->a = $options['a'];
           $this->b = $options['b'];
           $this->c = $options['c'];
           $this->d = $options['d'];
       }
   }
   
   ?>

See also `Avoid option arrays in constructors <http://bestpractices.thecodingmachine.com/php/design_beautiful_classes_and_methods.html#avoid-option-arrays-in-constructors>`_ and `PHP RFC: Named Arguments (Type-safe and documented options) <https://wiki.php.net/rfc/named_params#type-safe_and_documented_options>`_.

Connex PHP features
-------------------

  + `constructor <https://php-dictionary.readthedocs.io/en/latest/dictionary/constructor.ini.html>`_
  + `option <https://php-dictionary.readthedocs.io/en/latest/dictionary/option.ini.html>`_


Suggestions
___________

* Spread the options in the argument list, one argument each.
* Use a configuration class, that hold all the elements with clear names, instead of an array.
* Use named parameters to pass and document the arguments.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AvoidOptionArrays                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.9                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


