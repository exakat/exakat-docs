.. _structures-noneedgetclass:

.. _no-need-for-get\_class():

No Need For get_class()
+++++++++++++++++++++++

  There is no need to call `get_class() <https://www.php.net/get_class>`_ to build a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ call. The argument of `get_class() <https://www.php.net/get_class>`_ may be used directly.

.. code-block:: php
   
   <?php
   
   // 
   $a->b::$c
   
   // This is too much code
   get_class($a->b)::$c
   
   ?>

See also `Scope Resolution Operator (::) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Use get_called_class(), which may carry different class names
* Use self, static or parent keywords, if you are already in the current class
* Use the argument of get_class() directly




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoNeedGetClass                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.1                                                                                                                   |
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


