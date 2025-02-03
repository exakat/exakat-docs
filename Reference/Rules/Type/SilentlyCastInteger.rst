.. _type-silentlycastinteger:


.. _silently-cast-integer:

Silently Cast Integer
+++++++++++++++++++++

.. meta::
	:description:
		Silently Cast Integer: Those are integer literals that are cast to a float when running PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Silently Cast Integer
	:twitter:description: Silently Cast Integer: Those are integer literals that are cast to a float when running PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Silently Cast Integer
	:og:type: article
	:og:description: Those are integer literals that are cast to a float when running PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Silently Cast Integer.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/SilentlyCastInteger.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/SilentlyCastInteger.html","name":"Silently Cast Integer","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Those are integer literals that are cast to a float when running PHP","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Silently Cast Integer.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those are integer literals that are cast to a float when running PHP. They are too big for the current PHP version, and PHP resorts to cast them into a float, which has a much larger capacity but a lower precision.

Compare your literals to ``PHP_MAX_INT`` (typically ``9223372036854775807``) and ``PHP_MIN_INT`` (typically ``-9223372036854775808``).
This applies to binary (``0b10101``...), octal (``0123123``...) and hexadecimal (``0xfffff``...) too.

.. code-block:: php
   
   <?php
   
   echo 0b1010101101010110101011010101011010101011010101011010101011010111;
   //6173123008118052203
   echo 0b10101011010101101010110101010110101010110101010110101010110101111;
   //1.2346246016236E+19
   
   echo 0123123123123123123123;
   //1498121094048818771
   echo 01231231231231231231231;
   //1.1984968752391E+19
   
   echo 0x12309812311230;
   //5119979279159856
   echo 0x12309812311230fed;
   //2.0971435127439E+19
   
   echo 9223372036854775807; //PHP_MAX_INT
   //9223372036854775807
   echo 9223372036854775808;
   9.2233720368548E+18
   
   ?>

See also `Integer overflow <https://www.php.net/manual/en/language.types.integer.php#language.types.integer.overflow>`_.

Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_
  + `silent-cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/silent-cast.ini.html>`_


Suggestions
___________

* Make sure hexadecimal numbers have the right number of digits : generally, it is 15, but it may depends on your PHP version.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/SilentlyCastInteger                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mediawiki-type-silentlycastinteger`                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


