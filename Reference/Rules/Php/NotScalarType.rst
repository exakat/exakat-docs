.. _php-notscalartype:


.. _not-a-scalar-type:

Not A Scalar Type
+++++++++++++++++

.. meta::
	:description:
		Not A Scalar Type: ``int`` is the actual PHP scalar type, not ``integer``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Not A Scalar Type
	:twitter:description: Not A Scalar Type: ``int`` is the actual PHP scalar type, not ``integer``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Not A Scalar Type
	:og:type: article
	:og:description: ``int`` is the actual PHP scalar type, not ``integer``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Not A Scalar Type.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NotScalarType.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NotScalarType.html","name":"Not A Scalar Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"``int`` is the actual PHP scalar type, not ``integer``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Not A Scalar Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``int`` is the actual PHP scalar type, not ``integer``. 

PHP 7 introduced several scalar types, in particular ``int``, ``bool``, ``string`` and ``float``. Those three types are easily mistaken with ``integer``, ``boolean``, ``real`` and ``double``. 

Unless those classes actually exists, PHP emits some strange `error <https://www.php.net/error>`_ messages.

Thanks to ``Benoit Viguier`` for the `original idea <https://twitter.`com <https://www.php.net/com>`_/b_viguier/status/940173951908700161>`__ for this analysis.

.. code-block:: php
   
   <?php
   
   // This expects a scalar of type 'integer'
   function foo(int $i) {}
   
   // This expects a object of class 'integer'
   function abr(integer $i) {}
   
   ?>

See also `Type declarations <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_ and `PHP RFC: Scalar Type Hints <https://wiki.php.net/rfc/scalar_type_hints>`_.

Related PHP errors 
-------------------

  + `"boolean" will be interpreted as a class name. Did you mean "bool"?  <https://php-errors.readthedocs.io/en/latest/messages/%25s%22-will-be-interpreted-as-a-class-name.-did-you-mean-%22%25s%22%3F-write-%22%25s%22%25s-to-suppress-this-warning.html>`_
  + `"resource" will be interpreted as a class name. Did you mean "\resource"?  <https://php-errors.readthedocs.io/en/latest/messages/%25s%22-will-be-interpreted-as-a-class-name.-did-you-mean-%22%25s%22%3F-write-%22%25s%22%25s-to-suppress-this-warning.html>`_
  + `"double" will be interpreted as a class name. Did you mean "\float"?  <https://php-errors.readthedocs.io/en/latest/messages/%25s%22-will-be-interpreted-as-a-class-name.-did-you-mean-%22%25s%22%3F-write-%22%25s%22%25s-to-suppress-this-warning.html>`_



Connex PHP features
-------------------

  + `Scalar Types <https://php-dictionary.readthedocs.io/en/latest/dictionary/scalar-typehint.ini.html>`_


Suggestions
___________

* Do not use ``int`` as a class name, an interface name or a trait name.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NotScalarType                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`Typechecks <ruleset-Typechecks>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.7                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


