.. _php-serializemagic:

.. _serialize-magic-method:

Serialize Magic Method
++++++++++++++++++++++

  Classes that defines __serialize() and __unserialize() are using Serialize Magic.

Serialize magic methods were introduced in PHP 7.4, and are not effective before.

.. code-block:: php
   
   <?php
   
   class x {
       function __serialize() {}
       function __unserialize() {}
   }
   
   ?>

See also `New custom object serialization mechanism <https://wiki.php.net/rfc/custom_object_serialization>`_.

Connex PHP features
-------------------

  + `serialize <https://php-dictionary.readthedocs.io/en/latest/dictionary/serialize.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/SerializeMagic                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.0                                                                                                                   |
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


