.. _extensions-extteds:


.. _ext-teds:

ext/teds
++++++++


.. meta::

	:description:

		ext/teds: teds (Tentative Extra Data Structures) is a collection of data structures and iterable functionality.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/teds

	:twitter:description: ext/teds: teds (Tentative Extra Data Structures) is a collection of data structures and iterable functionality

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/teds

	:og:type: article

	:og:description: teds (Tentative Extra Data Structures) is a collection of data structures and iterable functionality

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/teds.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extteds.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extteds.html","name":"ext\/teds","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"teds (Tentative Extra Data Structures) is a collection of data structures and iterable functionality","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/teds.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

teds (Tentative Extra Data Structures) is a collection of data structures and iterable functionality.

.. code-block:: php
   
   <?php
   // discards keys
   $it = new Teds\BitVector(['first' => true, 'second' => false]);
   foreach ($it as $key => $value) {
       printf("Key: %s\nValue: %s\n", var_export($key, true), var_export($value, true));
   }
   var_dump($it);
   var_dump((array)$it);
   
   $it = new Teds\BitVector([]);
   var_dump($it);
   var_dump((array)$it);
   foreach ($it as $key => $value) {
       echo "Unreachable\n";
   }
   
   // Teds\BitVector will always reindex keys in the order of iteration, like array_values() does.
   $it = new Teds\BitVector([2 => true, 0 => false]);
   var_dump($it);
   
   var_dump(new Teds\BitVector([-1 => false]));
   ?>

See also `PECL TEDS <https://github.com/TysonAndre/pecl-teds/blob/main/tests/BitVector/BitVector.phpt>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extteds                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.8                                                                                                                   |
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


