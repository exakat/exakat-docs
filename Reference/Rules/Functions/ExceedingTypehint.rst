.. _functions-exceedingtypehint:


.. _exceeding-type:

Exceeding Type
++++++++++++++


.. meta::

	:description:

		Exceeding Type: The type is not fully used in the method.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Exceeding Type

	:twitter:description: Exceeding Type: The type is not fully used in the method

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Exceeding Type

	:og:type: article

	:og:description: The type is not fully used in the method

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Exceeding Type.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/ExceedingTypehint.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/ExceedingTypehint.html","name":"Exceeding Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"The type is not fully used in the method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Exceeding Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The type is not fully used in the method. Some of the defined methods in the type are unused. A tighter type could be used, to avoid method pollution.

Tight type prevents the argument from doing too much. They also require more maintenance : creation of dedicated interfaces, method management to keep all types tight.

.. code-block:: php
   
   <?php
   
   interface i {
       function i1();
       function i2();
   }
   
   interface j {
       function j1();
       function j2();
   }
   
   function foo(i $a, j $b) {
       // the i type is totally used
       $a->i1();
       $a->i2();
       
       // the i type is not totally used : j2() is not used.
       $b->j1();
   }
   
   ?>

See also :ref:`Insufficient Type <insufficient-type>`.

Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Suggestions
___________

* Keep the type tight, do not inject more than needed.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/ExceedingTypehint                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


