.. _classes-dynamicpropertycall:

.. _dynamic-property:

Dynamic Property
++++++++++++++++

.. meta::
	:description:
		Dynamic Property: Dynamic access to class property.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Property
	:twitter:description: Dynamic Property: Dynamic access to class property
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Property
	:og:type: article
	:og:description: Dynamic access to class property
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dynamic Property.html
	:og:locale: en
Dynamic access to class property. This is when the the name of the property is stored in a variable (or other container), rather than statically provided.

.. code-block:: php
   
   <?php
   
   class x {
       static public $foo = 1;
              public $bar = 2;
   }
   
   $staticproperty = 'foo';
   // dynamic static property call to x::$foo
   echo x::${$staticproperty};
   
   $property = 'bar';
   // dynamic property call to bar()
   $object = new x();
   $object->$property = 4;
   
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DynamicPropertyCall                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


