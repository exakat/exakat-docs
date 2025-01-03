.. _structures-uselesscasting:

.. _useless-type-casting:

Useless Type Casting
++++++++++++++++++++

.. meta::
	:description:
		Useless Type Casting: There is no need to cast values that are already well typed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Type Casting
	:twitter:description: Useless Type Casting: There is no need to cast values that are already well typed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Type Casting
	:og:type: article
	:og:description: There is no need to cast values that are already well typed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Type Casting.html
	:og:locale: en
There is no need to cast values that are already well typed.

Typed values, such as properties, do not have to be cast again, as the `engine <https://www.php.net/engine>`_ always ensures their type.

Typed arguments are variables : after the initial check at method call time, they might change value and type. Those extra cast may then carry some value, although changing the type of an incoming value is not recommended.

.. code-block:: php
   
   <?php
   
   // trim always returns a string : cast is useless
   $a = (string) trim($b);
   
   // strpos doesn't always returns an integer : cast is useful
   $a = (boolean) strpos($b, $c);
   
   // comparison don't need casting, nor parenthesis
   $c = (bool) ($b > 2);
   
   function foo(array $a) {
       foreach((array) $a as $b) {
           // doSomething
       }
   }
   ?>

See also `Type juggling <https://www.php.net/manual/en/language.types.type-juggling.php>`_ and :ref:`Multiple Type Variable <multiple-type-variable>`.

Connex PHP features
-------------------

  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_
  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Remove the type cast




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessCasting                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.7                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-fuelcms-structures-uselesscasting`, :ref:`case-thinkphp-structures-uselesscasting`                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


