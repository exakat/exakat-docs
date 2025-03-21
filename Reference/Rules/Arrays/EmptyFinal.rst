.. _arrays-emptyfinal:


.. _empty-final-element-in-array:

Empty Final Element In Array
++++++++++++++++++++++++++++

.. meta::
	:description:
		Empty Final Element In Array: The array() construct allows for the empty last element.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Final Element In Array
	:twitter:description: Empty Final Element In Array: The array() construct allows for the empty last element
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Final Element In Array
	:og:type: article
	:og:description: The array() construct allows for the empty last element
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Empty Final Element In Array.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/EmptyFinal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Arrays\/EmptyFinal.html","name":"Empty Final Element In Array","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"The array() construct allows for the empty last element","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Empty Final Element In Array.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The `array() <https://www.php.net/array>`_ construct allows for the empty last element. 

By putting an element on each line, and adding the final comma, it is possible to reduce the size of the diff when comparing code with the previous version.

.. code-block:: php
   
   <?php
   
   // Array definition with final empty element
   $array = [1,
             2,
             3,
             ];
   
   // New version of the code above
   // This array definition has only one line of diff with the previous array : the line with '4,'
   $array = [1,
             2,
             3,
             4,
             ];
   
   // New version of the first code above
   // This array definition is totally different from the first array : VCS will identify 3 removed lines, and one modified.
   $array = [1, 2, 3, 4];
   
   ?>

See also `Array <https://www.php.net/manual/en/language.types.array.php>`_, `Zend Framework Coding Standard <https://framework.zend.com/manual/2.4/en/ref/coding.standard.html#arrays>`_ and `How clean is your code? How clean are your diffs? <https://blog.madewithlove.be/post/code-style-options-for-cleaner-diffs/>`_.

Connex PHP features
-------------------

  + `Trailing Comma <https://php-dictionary.readthedocs.io/en/latest/dictionary/trailing-comma.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/EmptyFinal                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.0                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


