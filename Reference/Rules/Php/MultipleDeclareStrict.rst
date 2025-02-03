.. _php-multipledeclarestrict:


.. _multiple-declaration-of-strict\_types:

Multiple Declaration Of Strict_types
++++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		Multiple Declaration Of Strict_types: At least two declare() commands are declaring `strict_types` in one file.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Multiple Declaration Of Strict_types

	:twitter:description: Multiple Declaration Of Strict_types: At least two declare() commands are declaring `strict_types` in one file

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Multiple Declaration Of Strict_types

	:og:type: article

	:og:description: At least two declare() commands are declaring `strict_types` in one file

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Declaration Of Strict_types.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/MultipleDeclareStrict.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/MultipleDeclareStrict.html","name":"Multiple Declaration Of Strict_types","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"At least two declare() commands are declaring `strict_types` in one file","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Multiple Declaration Of Strict_types.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

At least two declare() commands are declaring `strict_types` in one file. Only one is sufficient, and should be the first expression in the file.

Indeed, any `strict_types` set to 1 will have the final word. Setting `strict_types` to 0 will not revert the configuration, wherever is this call made.

.. code-block:: php
   
   <?php 
   declare(strict_types=1);
   declare(strict_types=1);
   
   // rest of the code 
   
   ?>

See also `Declare <https://www.php.net/manual/en/control-structures.declare.php>`_.

Connex PHP features
-------------------

  + `declare <https://php-dictionary.readthedocs.io/en/latest/dictionary/declare.ini.html>`_
  + `strict_types <https://php-dictionary.readthedocs.io/en/latest/dictionary/strict_types.ini.html>`_


Suggestions
___________

* Remove all but one of them. Keep the first one. 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/MultipleDeclareStrict                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


