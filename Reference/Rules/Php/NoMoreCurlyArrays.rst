.. _php-nomorecurlyarrays:

.. _no-more-curly-arrays:

No More Curly Arrays
++++++++++++++++++++

  Only use square brackets to access array elements. The usage of curly brackets for array access is deprecated since PHP 7.4.

.. code-block:: php
   
   <?php
   
   $array = [1,2,3];
   
   // always valid
   echo $array[1];
   
   // deprecated in PHP 7.4
   echo $array{1};
   
   ?>

See also `Deprecate curly brace syntax <https://derickrethans.nl/phpinternalsnews-19.html>`_ and `Deprecate curly brace syntax for accessing array elements and string offsets <https://wiki.php.net/rfc/deprecate_curly_braces_array_access>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Array+and+string+offset+access+syntax+with+curly+braces+is+deprecated.html>`_



Connex PHP features
-------------------

  + `array-curly-braces <https://php-dictionary.readthedocs.io/en/latest/dictionary/array-curly-braces.ini.html>`_


Suggestions
___________

* Always use square brackets to access particular index in an array




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoMoreCurlyArrays                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


