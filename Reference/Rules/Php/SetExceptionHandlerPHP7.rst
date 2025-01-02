.. _php-setexceptionhandlerphp7:

.. _set\_exception\_handler()-warning:

set_exception_handler() Warning
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		set_exception_handler() Warning: The set_exception_handler() callable function has to be adapted to PHP 7 : ``Exception`` is not the right type, it is now ``Throwable``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: set_exception_handler() Warning
	:twitter:description: set_exception_handler() Warning: The set_exception_handler() callable function has to be adapted to PHP 7 : ``Exception`` is not the right type, it is now ``Throwable``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: set_exception_handler() Warning
	:og:type: article
	:og:description: The set_exception_handler() callable function has to be adapted to PHP 7 : ``Exception`` is not the right type, it is now ``Throwable``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/set_exception_handler() Warning.html
	:og:locale: en
The `set_exception_handler() <https://www.php.net/set_exception_handler>`_ callable function has to be adapted to PHP 7 : ``Exception`` is not the right type, it is now ``Throwable``. 

When in doubt about backward compatibility, just drop the type. Otherwise, use ``Throwable``.

.. code-block:: php
   
   <?php
   
   // PHP 5.6- type with Exception
   class foo { static function bar(\Exception $e) {} }
   
   // PHP 7+ type with Throwable
   class foo { static function bar(\Throwable $e) {} }
   
   // PHP 5 and PHP 7 compatible type (note : there is none)
   class foo { static function bar($e) {} }
   
   set_exception_handler([Foo::class, 'bar']);
   
   ?>

See also Drop the type and Use Throwable type.

Connex PHP features
-------------------

  + `error-handler <https://php-dictionary.readthedocs.io/en/latest/dictionary/error-handler.ini.html>`_


Suggestions
___________

* Change the typehint from Exception to Throwable.




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/SetExceptionHandlerPHP7                                                                                                          |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Slow (1 hour)                                                                                                                        |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/setExceptionHandlerType.html>`__                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


