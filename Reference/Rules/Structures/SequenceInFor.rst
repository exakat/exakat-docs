.. _structures-sequenceinfor:


.. _sequences-in-for:

Sequences In For
++++++++++++++++


.. meta::

	:description:

		Sequences In For: For() instructions allow several instructions in each of its parameters.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Sequences In For

	:twitter:description: Sequences In For: For() instructions allow several instructions in each of its parameters

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Sequences In For

	:og:type: article

	:og:description: For() instructions allow several instructions in each of its parameters

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Sequences In For.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SequenceInFor.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SequenceInFor.html","name":"Sequences In For","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"For() instructions allow several instructions in each of its parameters","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Sequences In For.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`For() <https://www.php.net/manual/en/control-structures.for.php>`_ instructions allow several instructions in each of its parameters. Then, the instruction separator is comma ',', not semi-colon, which is used for separating the 3 arguments.
This loop will simultaneously increment `$a` and `$b`. It will stop only when the last of the central sequence reach a value of false : here, when `$b` reach 20 and `$a` will be 6. 

This structure is rarely used, and makes the `for()` instruction quite difficult to read. It is also easy to oversee the multiples instructions, and omit one of them.

It is recommended not to use it.

.. code-block:: php
   
   <?php
      for ($a = 0, $b = 0; $a < 10, $b < 20; $a++, $b += 3) {
       // For loop
      }
   ?>
Connex PHP features
-------------------

  + `for <https://php-dictionary.readthedocs.io/en/latest/dictionary/for.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SequenceInFor                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Surprising <ruleset-Surprising>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


