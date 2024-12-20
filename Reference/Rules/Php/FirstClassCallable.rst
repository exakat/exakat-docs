.. _php-firstclasscallable:

.. _first-class-callable:

First Class Callable
++++++++++++++++++++

  A syntax using ellipsis was introduced to make it easy to make a method into a callable.

.. code-block:: php
   
   <?php
   
   // Using ellipsis as the only argument
   $a = $object->method(...);
   
   // Old style equivalent
   $a = array($object, 'method');
   
   // calling the closure.
   $a();
   
   ?>

See also `PHP RFC: First-class callable syntax <https://wiki.php.net/rfc/first_class_callable_syntax>`_.

Connex PHP features
-------------------

  + `first-class-callable <https://php-dictionary.readthedocs.io/en/latest/dictionary/first-class-callable.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/FirstClassCallable                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


