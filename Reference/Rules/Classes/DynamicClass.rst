.. _classes-dynamicclass:

.. _dynamic-classes:

Dynamic Classes
+++++++++++++++

.. meta::
	:description:
		Dynamic Classes: Dynamic calls of classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Classes
	:twitter:description: Dynamic Classes: Dynamic calls of classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Classes
	:og:type: article
	:og:description: Dynamic calls of classes
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/DynamicClass.html
	:og:locale: en
Dynamic calls of classes.

.. code-block:: php
   
   <?php
   
   class x {
       static function staticMethod() {}
   }
   
   $class = 'x';
   $class::staticMethod();
   
   ?>
Connex PHP features
-------------------

  + `dynamic-class <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-class.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DynamicClass                                                                                                                                                                    |
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
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


