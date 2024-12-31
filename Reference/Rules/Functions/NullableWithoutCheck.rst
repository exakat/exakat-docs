.. _functions-nullablewithoutcheck:

.. _nullable-without-check:

Nullable Without Check
++++++++++++++++++++++

.. meta\:\:
	:description:
		Nullable Without Check: Nullable typed argument or properties should be checked before usage.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Nullable Without Check
	:twitter:description: Nullable Without Check: Nullable typed argument or properties should be checked before usage
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Nullable Without Check
	:og:type: article
	:og:description: Nullable typed argument or properties should be checked before usage
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/NullableWithoutCheck.html
	:og:locale: en
  Nullable typed argument or properties should be checked before usage. When they are null, they probably won't behave like the other type, and lead to an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // This will emit a fatal error when $a = null
   function foo(?A $a) {
       return $a->m();
   }
   
   // This is stable
   function foo(?A $a) {
       if ($a === null) {
           return 42;
       } else {
           return $a->m();
       }
   }
   
   ?>

See also `Null Return Types <https://afilina.com/learn/nulls/return-types>`_.

Connex PHP features
-------------------

  + `null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_
  + `return-typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/return-typehint.ini.html>`_


Suggestions
___________

* Add a check on return value




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/NullableWithoutCheck                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


