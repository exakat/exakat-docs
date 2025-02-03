.. _php-missingmagicisset:


.. _missing-\_\_isset()-method:

Missing __isset() Method
++++++++++++++++++++++++


.. meta::

	:description:

		Missing __isset() Method: When using empty() on magic properties, the magic method __isset() must be implemented.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Missing __isset() Method

	:twitter:description: Missing __isset() Method: When using empty() on magic properties, the magic method __isset() must be implemented

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Missing __isset() Method

	:og:type: article

	:og:description: When using empty() on magic properties, the magic method __isset() must be implemented

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Missing __isset() Method.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/MissingMagicIsset.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/MissingMagicIsset.html","name":"Missing __isset() Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"When using empty() on magic properties, the magic method __isset() must be implemented","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Missing __isset() Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When using empty() on magic properties, the magic method `__isset() <https://www.php.net/manual/en/language.oop5.magic.php>`_ must be implemented.

.. code-block:: php
   
   <?php
   
   class foo {
       function __get($name) { return 'foo'; }
       // No __isset method
   }
   
   // Return TRUE, until __isset() exists
   var_dump(
      empty((new foo)->bar);
   );
   
   ?>

See also `When empty is not empty <https://freek.dev/1057-when-empty-is-not-empty>`_.

Connex PHP features
-------------------

  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_
  + `isset <https://php-dictionary.readthedocs.io/en/latest/dictionary/isset.ini.html>`_


Suggestions
___________

* Implement __isset() method when using empty on magic properties




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/MissingMagicIsset                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                                                      |
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


