.. _classes-ambiguousstatic:

.. _ambiguous-static:

Ambiguous Static
++++++++++++++++

.. meta::
	:description:
		Ambiguous Static: Methods or properties with the same name, are defined static in one class, and not static in another.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Ambiguous Static
	:twitter:description: Ambiguous Static: Methods or properties with the same name, are defined static in one class, and not static in another
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Ambiguous Static
	:og:type: article
	:og:description: Methods or properties with the same name, are defined static in one class, and not static in another
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/AmbiguousStatic.html
	:og:locale: en
Methods or properties with the same name, are defined `static <https://www.php.net/manual/en/language.oop5.static.php>`_ in one class, and not `static <https://www.php.net/manual/en/language.oop5.static.php>`_ in another. This is `error <https://www.php.net/error>`_ prone, as it requires a good knowledge of the code to make it `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not. 

Try to keep the methods simple and unique. Consider renaming the methods and properties to distinguish them easily. A method and a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method have probably different responsibilities.

.. code-block:: php
   
   <?php
   
   class a {
       function mixedStaticMethod() {}
   }
   
   class b {
       static function mixedStaticMethod() {}
   }
   
   /... a lot more code later .../
   
   $c->mixedStaticMethod();
   // or 
   $c::mixedStaticMethod();
   
   ?>
Connex PHP features
-------------------

  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AmbiguousStatic                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.3                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


