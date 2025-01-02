.. _structures-concatempty:

.. _concat-empty-string:

Concat Empty String
+++++++++++++++++++

.. meta::
	:description:
		Concat Empty String: Using a concatenation to make a value a string should be replaced with a type cast.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Concat Empty String
	:twitter:description: Concat Empty String: Using a concatenation to make a value a string should be replaced with a type cast
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Concat Empty String
	:og:type: article
	:og:description: Using a concatenation to make a value a string should be replaced with a type cast
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Concat Empty String.html
	:og:locale: en
Using a concatenation to make a value a string should be replaced with a type cast.

Type cast to a string is done with ``(string)`` operator. There is also the function `strval() <https://www.php.net/strval>`_, although it is less recommended.

.. code-block:: php
   
   <?php
   
   $a = 3;
   
   // explicite way to cast a value
   $b = (string) $a; // $b is a string with the content 3
   
   // Wrong way to cast a value
   $c = $a . ''; // $c is a string with the content 3
   $c = '' . $a; // $c is a string with the content 3
   $a .= '';     // $a is a string with the content 3
   
   // Wrong way to cast a value
   $c = $a . '' . $b; // This is not reported. The empty string is useless, but not meant to type cast
   
   ?>

See also `Type Casting <https://php.net/manual/en/language.types.type-juggling.php#language.types.typecasting>`_ and `PHP Type Casting <https://developer.hyvor.com/tutorials/php/type-casting>`_.

Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_


Suggestions
___________

* Avoid concatenating with empty strings
* Use (string) operator to cast to string
* Remove any concatenated empty string




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ConcatEmpty                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.0                                                                                                                   |
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


