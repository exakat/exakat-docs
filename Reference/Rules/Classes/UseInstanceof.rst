.. _classes-useinstanceof:

.. _use-instanceof:

Use Instanceof
++++++++++++++

.. meta::
	:description:
		Use Instanceof: The ``instanceof`` operator is a more precise alternative to ``is_object()``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Instanceof
	:twitter:description: Use Instanceof: The ``instanceof`` operator is a more precise alternative to ``is_object()``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Instanceof
	:og:type: article
	:og:description: The ``instanceof`` operator is a more precise alternative to ``is_object()``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Instanceof.html
	:og:locale: en
The ``instanceof`` operator is a more precise alternative to ``is_object()``. It is also faster.

`instanceof <https://www.php.net/manual/en/language.operators.type.php>`_ checks for an variable to be of a class or its parents or the interfaces it implements. 
Once ``instanceof`` has been used, the actual attributes available (properties, constants, methods) are known, unlike with ``is_object()``.

Last, ``instanceof`` may be upgraded to Typehint, by moving it to the method signature. 
``instanceof`` and ``is_object()`` may not be always interchangeable. Consider using `isset() <https://www.www.php.net/isset>`_ on a known property for a simple check on objects. You may also consider `is_string() <https://www.php.net/is_string>`_, `is_integer() <https://www.php.net/is_integer>`_ or `is_scalar() <https://www.php.net/is_scalar>`_, in particular instead of ``!`is_object() <https://www.php.net/is_object>`_``.

The ``instanceof`` operator is also faster than the ``is_object()`` functioncall.

.. code-block:: php
   
   <?php
   
   class Foo {
   
       // Don't use is_object
       public function bar($o) {
           if (!is_object($o)) { return false; } // Classic argument check
           return $o->method();
       }
   
       // use instanceof
       public function bar($o) {
           if ($o instanceof myClass) {  // Now, we know which methods are available
               return $o->method();
           }
           
           return false; } // Default behavior
       }
   
       // use of typehinting
       // in case $o is not of the right type, exception is raised automatically
       public function bar(myClass $o) {
           return $o->method();
       }
   }
   
   ?>

See also `Type Operators <https://www.php.net/manual/en/language.operators.type.php#language.operators.type>`_ and `is_object <https://www.php.net/manual/en/function.is-object.php>`_.

Connex PHP features
-------------------

  + `instanceof <https://php-dictionary.readthedocs.io/en/latest/dictionary/instanceof.ini.html>`_


Suggestions
___________

* Use instanceof and remove is_object()
* Create a high level interface to check a whole family of classes, instead of testing them individually
* Use typehint when possible
* Avoid mixing scalar types and objects in the same variable




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UseInstanceof                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-teampass-classes-useinstanceof`, :ref:`case-zencart-classes-useinstanceof`                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


