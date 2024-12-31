.. _structures-multiplybyone:

.. _multiply-by-one:

Multiply By One
+++++++++++++++

.. meta\:\:
	:description:
		Multiply By One: Multiplying by 1 is a fancy type cast.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiply By One
	:twitter:description: Multiply By One: Multiplying by 1 is a fancy type cast
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiply By One
	:og:type: article
	:og:description: Multiplying by 1 is a fancy type cast
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/MultiplyByOne.html
	:og:locale: en
  Multiplying by 1 is a fancy type cast. 

If it is used to type cast a value to number, then casting (int) or (float) is clearer. This behavior may change with PHP 7.1, which has unified the behavior of all hidden casts.

.. code-block:: php
   
   <?php
   
   // Still the same value than $m, but now cast to integer or float
   $m = $m * 1; 
   
   // Still the same value than $m, but now cast to integer or float
   $n *= 1; 
   
   // make typecasting clear, and merge it with the producing call.
   $n = (int) $n;
   
   ?>

See also `Type Juggling <https://www.php.net/manual/en/language.types.type-juggling.php>`_.

Connex PHP features
-------------------

  + `neutral-element <https://php-dictionary.readthedocs.io/en/latest/dictionary/neutral-element.ini.html>`_


Suggestions
___________

* Typecast to (int) or (float) for better readability
* Skip useless math operation altogether




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MultiplyByOne                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Rector <ruleset-Rector>`                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-useless-math <https://github.com/dseguy/clearPHP/tree/master/rules/no-useless-math.md>`__                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-sugarcrm-structures-multiplybyone`, :ref:`case-edusoho-structures-multiplybyone`                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


