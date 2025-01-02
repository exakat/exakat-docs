.. _php-reflectionexportisdeprecated:

.. _reflection-export()-is-deprecated:

Reflection Export() Is Deprecated
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Reflection Export() Is Deprecated: export() method in Reflection classes is now deprecated.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Reflection Export() Is Deprecated
	:twitter:description: Reflection Export() Is Deprecated: export() method in Reflection classes is now deprecated
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Reflection Export() Is Deprecated
	:og:type: article
	:og:description: export() method in Reflection classes is now deprecated
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Reflection Export() Is Deprecated.html
	:og:locale: en
export() method in `Reflection <https://www.php.net/reflection>`_ classes is now deprecated. It is obsolete since PHP 7.4 and will disappear in PHP 8.0.

The `Reflector <https://www.php.net/reflector>`_ interface, which is implemented by all `reflection <https://www.php.net/reflection>`_ classes, specifies two methods: `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and export().

.. code-block:: php
   
   <?php
   
   ReflectionFunction::export('foo');
   // same as
   echo new ReflectionFunction('foo'), "\n";
   
   $str = ReflectionFunction::export('foo', true);
   // same as
   $str = (string) new ReflectionFunction('foo');
   
   ?>

See also `Reflection export() methods <https://wiki.php.net/rfc/deprecations_php_7_4#reflection_export_methods>`_ and `Reflection <https://www.php.net/manual/en/book.reflection.php>`_.

Connex PHP features
-------------------

  + `reflection <https://php-dictionary.readthedocs.io/en/latest/dictionary/reflection.ini.html>`_


Suggestions
___________

* Cast the object to string
* Remove the call to export()




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ReflectionExportIsDeprecated                                                                                                                                                        |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.9.0                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                     |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.4                                                                                                                                                                                 |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


