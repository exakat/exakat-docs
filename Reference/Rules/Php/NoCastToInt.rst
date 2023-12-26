.. _php-nocasttoint:

.. _do-not-cast-to-int:

Do Not Cast To Int
++++++++++++++++++

  Do not cast floats values to int. Uses conversion functions like `intval() <https://www.php.net/intval>`_, `round() <https://www.php.net/round>`_, `floor() <https://www.php.net/floor>`_ or `ceil() <https://www.php.net/ceil>`_ to convert the value to integer, with known behavior. 

Use functions like `floor() <https://www.php.net/floor>`_, `round() <https://www.php.net/round>`_ or `ceil() <https://www.php.net/ceil>`_ : they use an explicit method for rounding, that helps keeping the side effects under control.


.. code-block:: php
   
   <?php
   
       // echoes 7!
       echo (int) ( (0.1 + 0.7) * 10 ); 
   
   ?>

See also `Integers <https://www.php.net/manual/en/language.types.integer.php>`_.


Suggestions
___________

* Upgrade PHP version to 8.0, as those behavior are now the same
* Use one of the dedicated function : intval(), round(), floor() or ceil()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoCastToInt                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.6                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | cast, integer, float                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


