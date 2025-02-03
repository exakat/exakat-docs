.. _type-hexadecimal:


.. _hexadecimal-glossary:

Hexadecimal Glossary
++++++++++++++++++++


.. meta::

	:description:

		Hexadecimal Glossary: This rule lists of all the integer values, written in the hexadecimal format.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Hexadecimal Glossary

	:twitter:description: Hexadecimal Glossary: This rule lists of all the integer values, written in the hexadecimal format

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Hexadecimal Glossary

	:og:type: article

	:og:description: This rule lists of all the integer values, written in the hexadecimal format

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Hexadecimal Glossary.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Hexadecimal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Hexadecimal.html","name":"Hexadecimal Glossary","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"This rule lists of all the integer values, written in the hexadecimal format","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Hexadecimal Glossary.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule lists of all the integer values, written in the hexadecimal format.

The hexadecimal syntax is a zero, followed by ``x`` and then, up to 16 hexadecimal digits: ``0x[0-9a-z]+``. The format is case insensitive.

Up to 16 characters after the x gives an integer. From 17 to 243, it gives a float. Beyond, it returns infinite ``INF``.


.. code-block:: php
   
   <?php
   
   $hexadecimal = 0x10;
   
   $anotherHexadecimal = 0XAF;
   
   ?>

See also https://www.php.net/manual/en/language.types.integer.php#language.types.integer.syntax.

Connex PHP features
-------------------

  + `hexadecimal-integer <https://php-dictionary.readthedocs.io/en/latest/dictionary/hexadecimal-integer.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Hexadecimal                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`binary-glossary`, :ref:`octal-glossary`                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


