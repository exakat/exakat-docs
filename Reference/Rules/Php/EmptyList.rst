.. _php-emptylist:

.. _empty-list:

Empty List
++++++++++

.. meta\:\:
	:description:
		Empty List: Empty list() are not allowed anymore in PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty List
	:twitter:description: Empty List: Empty list() are not allowed anymore in PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty List
	:og:type: article
	:og:description: Empty list() are not allowed anymore in PHP 7
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/EmptyList.html
	:og:locale: en
  Empty `list() <https://www.php.net/list>`_ are not allowed anymore in PHP 7. There must be at least one variable in the list call.

.. code-block:: php
   
   <?php
   
   //Not accepted since PHP 7.0
   list() = array(1,2,3);
   
   //Still valid PHP code
   list(,$x) = array(1,2,3);
   
   ?>
Connex PHP features
-------------------

  + `list <https://php-dictionary.readthedocs.io/en/latest/dictionary/list.ini.html>`_


Suggestions
___________

* Remove empty list() calls




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/EmptyList                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


