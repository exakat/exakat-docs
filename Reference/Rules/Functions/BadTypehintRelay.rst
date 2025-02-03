.. _functions-badtypehintrelay:


.. _bad-type-relay:

Bad Type Relay
++++++++++++++


.. meta::

	:description:

		Bad Type Relay: A bad type relay happens where a types argument is relayed to a parameter with another type.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Bad Type Relay

	:twitter:description: Bad Type Relay: A bad type relay happens where a types argument is relayed to a parameter with another type

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Bad Type Relay

	:og:type: article

	:og:description: A bad type relay happens where a types argument is relayed to a parameter with another type

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Bad Type Relay.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/BadTypehintRelay.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/BadTypehintRelay.html","name":"Bad Type Relay","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A bad type relay happens where a types argument is relayed to a parameter with another type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Bad Type Relay.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A bad type relay happens where a types argument is relayed to a parameter with another type. This leads to a Fatal `error <https://www.php.net/error>`_, and stops execution. This is possibly a piece of dead code.

It is recommended to harmonize the types, so the two methods are compatible.

.. code-block:: php
   
   <?php
   
   // the $i argument is relayed to bar, which is expecting a string. 
   function foo(int $i) : string {
       return bar($i);
   }
   
   // the return value for the bar function is not compatible with the one from foo;
   function bar(string $s) : int {
       return (int) $string + 1;
   }
   
   ?>
Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Suggestions
___________

* Harmonize the type so they match one with the other.
* Remove dead code
* Apply type casting before calling the next function, or return value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/BadTypehintRelay                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Typechecks <ruleset-Typechecks>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


