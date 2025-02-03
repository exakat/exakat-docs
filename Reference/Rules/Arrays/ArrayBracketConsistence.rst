.. _arrays-arraybracketconsistence:


.. _array()---[--]-consistence:

Array() / [  ] Consistence
++++++++++++++++++++++++++

.. meta::
	:description:
		Array() / [  ] Consistence: array() or [ ] is the favorite.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Array() / [  ] Consistence
	:twitter:description: Array() / [  ] Consistence: array() or [ ] is the favorite
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Array() / [  ] Consistence
	:og:type: article
	:og:description: array() or [ ] is the favorite
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Array() / [  ] Consistence.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/ArrayBracketConsistence.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/ArrayBracketConsistence.html","name":"Array() \/ [  ] Consistence","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"array() or [ ] is the favorite","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Array() \/ [  ] Consistence.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`array() <https://www.php.net/array>`_ or [ ] is the favorite.

`array() <https://www.php.net/array>`_ and [ ] have the same functional use. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It happens that `array() <https://www.php.net/array>`_ or [] are used depending on coding style and files. One file may be consistently using `array() <https://www.php.net/array>`_, while the others are all using []. 

The only drawback to use [] over `array() <https://www.php.net/array>`_ is backward incompatibility.

.. code-block:: php
   
   <?php
   
   $a = array(1, 2);
   $b = array(array(3, 4), array(5, 6));
   $c = array(array(array(7, 8), array(9, 10)), array(11, 12), array(13, 14)));
   
   // be consistent
   $d = [1, 3];
   ?>

+-------------+---------+---------+-------------------------------------------------------------------------------------------+
| Name        | Default | Type    | Description                                                                               |
+-------------+---------+---------+-------------------------------------------------------------------------------------------+
| array_ratio | 10      | integer | Percentage of arrays in one of the syntaxes, to trigger the other syntax as a violation.  |
+-------------+---------+---------+-------------------------------------------------------------------------------------------+


Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use one syntax consistently.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/ArrayBracketConsistence                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


