.. _typehints-couldbenull:

.. _could-be-null:

Could Be Null
+++++++++++++

.. meta::
	:description:
		Could Be Null: Mark arguments, properties, class constants and return types that can be ``null``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Null
	:twitter:description: Could Be Null: Mark arguments, properties, class constants and return types that can be ``null``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Null
	:og:type: article
	:og:description: Mark arguments, properties, class constants and return types that can be ``null``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Null.html
	:og:locale: en
Mark arguments, properties, class constants and return types that can be ``null``. Null was introduced as a standlone type in PHP 8.2. Before that, null had to be paired with another type.

.. code-block:: php
   
   <?php
   
   // Accept null as input, when used as third argument of file_get_contents
   function foo($b) {
       $s = file_get_contents(URL, false, $b);
   
       // Returns a string
       return shell_exec($s);
   }
   
   ?>
Connex PHP features
-------------------

  + `null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_
  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_
  + `nullable <https://php-dictionary.readthedocs.io/en/latest/dictionary/nullable.ini.html>`_


Suggestions
___________

* Add `null` typehint to the code (PHP 8.0+).
* Add `?` typehint to the code.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeNull                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Typechecks <ruleset-Typechecks>`                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


