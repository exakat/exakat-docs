.. _type-onevariablestrings:

.. _one-variable-string:

One Variable String
+++++++++++++++++++

.. meta::
	:description:
		One Variable String: These strings only contains one variable or property or array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: One Variable String
	:twitter:description: One Variable String: These strings only contains one variable or property or array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: One Variable String
	:og:type: article
	:og:description: These strings only contains one variable or property or array
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Type/OneVariableStrings.html
	:og:locale: en
These strings only contains one variable or property or array. 
When the goal is to convert a variable to a string, it is recommended to use the type casting (string) operator : it is then clearer to understand the conversion. It is also marginally faster, though very little.

.. code-block:: php
   
   <?php
   
   $a = 0;
   $b = "$a"; // This is a one-variable string
   
   // Better way to write the above
   $b = (string) $a;
   
   // Alternatives : 
   $b2 = "$a[1]"; // This is a one-variable string
   $b3 = "$a->b"; // This is a one-variable string
   $c = "d";
   $d = "D";
   $b4 = "{$$c}";
   $b5 = "{$a->foo()}";
   
   ?>

See also `Strings <https://www.php.net/manual/en/language.types.string.php>`_ and `Type Juggling <https://www.php.net/manual/en/language.types.type-juggling.php>`_.

Connex PHP features
-------------------

  + `string <https://php-dictionary.readthedocs.io/en/latest/dictionary/string.ini.html>`_
  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_
  + `interpolation <https://php-dictionary.readthedocs.io/en/latest/dictionary/interpolation.ini.html>`_


Suggestions
___________

* Drop the surrounding string, keep the variable (or property...)
* Include in the string any concatenation that comes unconditionally after or before
* Convert the variable to a string with the (type) operator




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/OneVariableStrings                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tikiwiki-type-onevariablestrings`, :ref:`case-nextcloud-type-onevariablestrings`                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


