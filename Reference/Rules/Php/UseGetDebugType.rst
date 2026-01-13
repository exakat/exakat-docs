.. _php-usegetdebugtype:

.. _use-get\_debug\_type():

Use get_debug_type()
++++++++++++++++++++

  `get_debug_type() <https://www.php.net/get_debug_type>`_ returns the given type of a variable. It was introduced in PHP 8.0: this makes it incompatible with previous versions.

.. code-block:: php
   
   <?php
     // From the RFC 
     throw new TypeError('Expected ' . Foo::class . ' got ' . (is_object($bar) ? get_class($bar) : gettype($bar)));
   
     // Becomes
     throw new TypeError('Expected ' . Foo::class . ' got ' . get_debug_type($bar));
   
   ?>

See also `PHP RFC: get_debug_type <https://wiki.php.net/rfc/get_debug_type>`_.

Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_
  + `debug <https://php-dictionary.readthedocs.io/en/latest/dictionary/debug.ini.html>`_
  + `backward incompatible <https://php-dictionary.readthedocs.io/en/latest/dictionary/backward+incompatible.ini.html>`_


Suggestions
___________

* Replace the ternary with a call to get_debug_type()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseGetDebugType                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


