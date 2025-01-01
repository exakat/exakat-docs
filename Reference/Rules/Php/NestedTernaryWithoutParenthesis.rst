.. _php-nestedternarywithoutparenthesis:

.. _nested-ternary-without-parenthesis:

Nested Ternary Without Parenthesis
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Nested Ternary Without Parenthesis: It is not allowed to nest ternary operator within itself, without parenthesis.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nested Ternary Without Parenthesis
	:twitter:description: Nested Ternary Without Parenthesis: It is not allowed to nest ternary operator within itself, without parenthesis
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nested Ternary Without Parenthesis
	:og:type: article
	:og:description: It is not allowed to nest ternary operator within itself, without parenthesis
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/NestedTernaryWithoutParenthesis.html
	:og:locale: en
It is not allowed to nest ternary operator within itself, without parenthesis. This has been implemented in PHP 7.4.

The reason behind this feature is to keep the code expressive. See the Warning message for more explanations

.. code-block:: php
   
   <?php
   
   $a ? 1 : ($b ? 2 : 3);
   
   // Still valid, as not ambiguous 
   $a ? $b ? 1 : 2 : 3;
   
   // Produces a warning
   //Unparenthesized `a ? b : c ? d : e` is deprecated. Use either `(a ? b : c) ? d : e` or `a ? b : (c ? d : e)`
   $a ? 1 : $b ? 2 : 3;
   
   ?>

See also `PHP RFC: Deprecate left-associative ternary operator <https://wiki.php.net/rfc/ternary_associativity>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Unparenthesized+%60a+%3F+b+%3A+c+%3F+d+%3A+e%60+is+deprecated.+Use+either+%60%28a+%3F+b+%3A+c%29+%3F+d+%3A+e%60+or+%60a+%3F+b+%3A+%28c+%3F+d+%3A+e%29%60.html>`_



Connex PHP features
-------------------

  + `ternary <https://php-dictionary.readthedocs.io/en/latest/dictionary/ternary.ini.html>`_
  + `parenthesis <https://php-dictionary.readthedocs.io/en/latest/dictionary/parenthesis.ini.html>`_


Suggestions
___________

* Add parenthesis to nested ternary calls




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NestedTernaryWithoutParenthesis                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`, :ref:`Deprecated <ruleset-Deprecated>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


