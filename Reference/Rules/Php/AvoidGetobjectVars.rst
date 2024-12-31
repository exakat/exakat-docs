.. _php-avoidgetobjectvars:

.. _avoid-get\_object\_vars():

Avoid get_object_vars()
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Avoid get_object_vars(): get_object_vars() changes behavior between PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid get_object_vars()
	:twitter:description: Avoid get_object_vars(): get_object_vars() changes behavior between PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid get_object_vars()
	:og:type: article
	:og:description: get_object_vars() changes behavior between PHP 7
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/AvoidGetobjectVars.html
	:og:locale: en
  `get_object_vars() <https://www.php.net/get_object_vars>`_ changes behavior between PHP 7.3 and 7.4. 

Calling `get_object_vars() <https://www.php.net/get_object_vars>`_ on an `ArrayObject <https://www.php.net/manual/en/class.`arrayobject <https://www.php.net/arrayobject>`_.php>`_ instance will now always return the properties of the `ArrayObject <https://www.php.net/manual/en/class.`arrayobject <https://www.php.net/arrayobject>`_.php>`_ itself (or a subclass). Previously it returned the values of the wrapped array/object unless the ArrayObject\:\:STD_PROP_LIST flag was specified.

It also behaves different within and outside a class.

.. code-block:: php
   
   <?php
   
   // Illustration courtesy of Doug Bierer
   $obj = new ArrayObject(['A' => 1,'B' => 2,'C' => 3]);
   var_dump($obj->getArrayCopy());
   var_dump(get_object_vars($obj));
   
   ?>

See also `get_object_vars script on 3V4L <https://3v4l.org/ELVGY>`_, `The Strange Case of ArrayObject <https://phptraining.net/articles/strange_case_of_array_object>`_ and `Standard PHP Library (SPL) <https://www.php.net/manual/en/migration74.incompatible.php#migration74.incompatible.spl>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `arrayobject <https://php-dictionary.readthedocs.io/en/latest/dictionary/arrayobject.ini.html>`_


Suggestions
___________

* Use ArrayObject and getArrayCopy() method




Specs
_____

+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/AvoidGetobjectVars                                                                                                                                                                       |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.2.1                                                                                                                                                                                        |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                        |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                              |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.4                                                                                                                                                                                      |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                                                                                         |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                      |
+------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


