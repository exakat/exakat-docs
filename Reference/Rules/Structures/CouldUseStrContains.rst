.. _structures-couldusestrcontains:

.. _could-use-strcontains():

Could Use strcontains()
+++++++++++++++++++++++

  PHP 8 introduced the strcontains() function, which is a replacement for `strpos() <https://www.php.net/strpos>`_. strcontains() checks if a string is found inside a string, and returns a boolean. 

When `strpos() <https://www.php.net/strpos>`_ is used as a boolean, or compared to a boolean, strcontains() is a good replacement. When `strpos() <https://www.php.net/strpos>`_ is actually used to calculate a position inside a string, it should not be replaced.

strcontains() is not backward compatible, so it should be be used before PHP 8.0. Polyfills are available.

.. code-block:: php
   
   <?php
   
   // Could use strcontains()
   if (strpos($haystack, $needle) !== false) { }
   
   // Not a possible replacement 
   $position = strpos($haystack, $needle); 
   $haystack[$position + 1] = 'A'; 
   
   ?>

Suggestions
___________

* Replace strpos() by strcontains()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseStrContains                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Rector <ruleset-Rector>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


