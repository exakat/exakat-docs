.. _functions-couldtypewithiterable:

.. _could-type-with-iterable:

Could Type With Iterable
++++++++++++++++++++++++

.. meta\:\:
	:description:
		Could Type With Iterable: Suggest using ``iterable`` typehint for arguments.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Type With Iterable
	:twitter:description: Could Type With Iterable: Suggest using ``iterable`` typehint for arguments
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Type With Iterable
	:og:type: article
	:og:description: Suggest using ``iterable`` typehint for arguments
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/CouldTypeWithIterable.html
	:og:locale: en
  Suggest using ``iterable`` typehint for arguments.

``iterable`` represents both ``array`` and objects that implements ``Iterator`` interface. Both types are coerced, and usable here.

.. code-block:: php
   
   <?php
   
   // $s may be both an array or an iterator
   function foo($s) : int {
       $t = 0;
       foreach($s as $v) {
           $t += (int) $v;
       }
       
       return $t;
   }
   
   ?>

See also `Iterables <https://www.php.net/manual/en/language.types.iterable.php>`_.

Connex PHP features
-------------------

  + `iterable <https://php-dictionary.readthedocs.io/en/latest/dictionary/iterable.ini.html>`_


Suggestions
___________

* Add the iterable type




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CouldTypeWithIterable                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


