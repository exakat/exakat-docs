.. _php-strtrarguments:

.. _strtr-arguments:

Strtr Arguments
+++++++++++++++

.. meta::
	:description:
		Strtr Arguments: Strtr() replaces characters by others in a string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Strtr Arguments
	:twitter:description: Strtr Arguments: Strtr() replaces characters by others in a string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Strtr Arguments
	:og:type: article
	:og:description: Strtr() replaces characters by others in a string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Strtr Arguments.html
	:og:locale: en
`Strtr() <https://www.php.net/strtr>`_ replaces characters by others in a string. When using strings, `strtr() <https://www.php.net/strtr>`_ replaces characters as long as they have a replacement. All others are ignored.

In particular, `strtr() <https://www.php.net/strtr>`_ works on strings of the same size, and cannot be used to remove chars.

.. code-block:: php
   
   <?php
   
   $string = 'abcde';
   echo strtr($string, 'abc', 'AB');
   echo strtr($string, 'ab', 'ABC');
   // displays ABcde 
   // c is ignored each time
   
   // strtr can't remove a char
   echo strtr($string, 'a', '');
   // displays a
   
   ?>

See also `strtr <http://www.php.net/strtr>`_.


Suggestions
___________

* Check the call to strtr() and make sure the arguments are of the same size
* Replace strtr() with str_replace(), which works with strings and array, not chars
* Replace strtr() with preg_match(), which works with patterns and not chars




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/StrtrArguments                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.3                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-php-strtrarguments`                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


