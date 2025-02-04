.. _typehints-couldbearray:


.. _could-be-array-type:

Could Be Array Type
+++++++++++++++++++

.. meta::
	:description:
		Could Be Array Type: This rule spots arguments, class constants, properties or return values that may be labeled with the ``array`` scalar type.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Array Type
	:twitter:description: Could Be Array Type: This rule spots arguments, class constants, properties or return values that may be labeled with the ``array`` scalar type
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Array Type
	:og:type: article
	:og:description: This rule spots arguments, class constants, properties or return values that may be labeled with the ``array`` scalar type
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Array Type.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/CouldBeArray.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/CouldBeArray.html","name":"Could Be Array Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"This rule spots arguments, class constants, properties or return values that may be labeled with the ``array`` scalar type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Array Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule spots arguments, class constants, properties or return values that may be labeled with the ``array`` scalar type.

.. code-block:: php
   
   <?php
   
   // $arg is used as an array in this function, so it may be typed : array
   functions foo($arg) {
   
       // the returned value is always an array, so this function might be typed as : array
       return array($arg[3]);
   }
   
   ?>

See also `Type declarations  <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `Array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Add ``array`` type to the code.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeArray                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


