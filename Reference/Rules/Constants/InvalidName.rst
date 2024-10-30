.. _constants-invalidname:

.. _invalid-constant-name:

Invalid Constant Name
+++++++++++++++++++++

  There is a naming convention for PHP constants names. 

According to PHP's manual, constant names, ' A valid constant name starts with a letter or underscore, followed by any number of letters, numbers, or underscores.'.

Constant, must follow this regex : ``/[a-zA-Z_\x7f-\xff][a-zA-Z0-9_\x7f-\xff]*/``.

In particular when defined using `define() <https://www.php.net/define>`_ function, no `error <https://www.php.net/error>`_ is produced. When using ``const``, on the other hand, the name must be valid at linting time.

.. code-block:: php
   
   <?php
   
   define('+3', 1); // wrong constant name! 
   
   echo constant('+3'); // invalid constant access
   
   // This won't compile, with a syntax error.
   // const 3A = 3;
   
   ?>

See also `Constants <https://www.php.net/manual/en/language.constants.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/syntax+error%2C+unexpected+%27-%27%2C+expecting+%27%3D%27.html>`_



Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Suggestions
___________

* Change constant name




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/InvalidName                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-constants-invalidname`                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


