.. _structures-couldusecompact:

.. _could-use-compact:

Could Use Compact
+++++++++++++++++

.. meta::
	:description:
		Could Use Compact: Compact() turns a group of variables into an array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Compact
	:twitter:description: Could Use Compact: Compact() turns a group of variables into an array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Compact
	:og:type: article
	:og:description: Compact() turns a group of variables into an array
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Compact.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseCompact.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseCompact.html","name":"Could Use Compact","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Compact() turns a group of variables into an array","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use Compact.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`Compact() <https://www.php.net/compact>`_ turns a group of variables into an array. It may be used to simplify expressions. 
Note that compact accepts any string, and any undefined variable is not set, without a warning.

.. code-block:: php
   
   <?php
   
   $a = 1;
   $b = 2;
   
   // Compact call
   $array = compact('a', 'b');
   
   $array === [1, 2];
   
   // Detailing all the keys and their value
   $array = ['a' => $a, 'b' => $b];
   
   ?>

See also `compact <http://www.php.net/compact>`_.

Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Replace the array() call with a compact() call.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseCompact                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-structures-couldusecompact`                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


