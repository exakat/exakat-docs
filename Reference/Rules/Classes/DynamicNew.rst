.. _classes-dynamicnew:

.. _dynamic-new:

Dynamic New
+++++++++++

.. meta\:\:
	:description:
		Dynamic New: Dynamic instantiation of classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic New
	:twitter:description: Dynamic New: Dynamic instantiation of classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic New
	:og:type: article
	:og:description: Dynamic instantiation of classes
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/DynamicNew.html
	:og:locale: en
  Dynamic instantiation of classes. It happens when the name of the class is an executable expression, and, as such, only known at execution time.

.. code-block:: php
   
   <?php
     
       $classname = foo();  
       $object = new $classname();
       
       $object = new (foo());
   ?>
Connex PHP features
-------------------

  + `new <https://php-dictionary.readthedocs.io/en/latest/dictionary/new.ini.html>`_
  + `parenthesis <https://php-dictionary.readthedocs.io/en/latest/dictionary/parenthesis.ini.html>`_
  + `dynamic-call <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-call.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DynamicNew                                                                                                                                                                      |
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


