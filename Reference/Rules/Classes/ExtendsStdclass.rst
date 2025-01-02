.. _classes-extendsstdclass:

.. _extends-stdclass:

Extends stdClass
++++++++++++++++

.. meta::
	:description:
		Extends stdClass: Those classes extends ``stdClass``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Extends stdClass
	:twitter:description: Extends stdClass: Those classes extends ``stdClass``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Extends stdClass
	:og:type: article
	:og:description: Those classes extends ``stdClass``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Extends stdClass.html
	:og:locale: en
Those classes extends ``stdClass``.

Traditionally, classes are defined independently, without any native class extension. 

In PHP 8.2, dynamic properties are deprecated, and yield a warning in the logs. Adding 'extends \`stdClass <https://www.php.net/stdclass>`_' to classes signature removes this warning, as `stdclass <https://www.php.net/stdclass>`_ is the empty class, without any method, property nor constants.

.. code-block:: php
   
   <?php
   
   class myClass extends \stdClass {
       function __set($a, $b) {
           $this->$a = $b;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `stdclass <https://php-dictionary.readthedocs.io/en/latest/dictionary/stdclass.ini.html>`_
  + `dynamic-property <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-property.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ExtendsStdclass                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>`, :ref:`Inventory <ruleset-Inventory>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.2                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


