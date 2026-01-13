.. _structures-substrtotrim:

.. _substr-to-trim:

Substr To Trim
++++++++++++++

  When removing the first or the last character of a string, `trim() <https://www.php.net/trim>`_ does a more readable job. 

`trim() <https://www.php.net/trim>`_, `ltrim() <https://www.php.net/ltrim>`_ and `rtrim() <https://www.php.net/rtrim>`_ accept a string as second argument. Those will all be removed from the endings of the string.
`trim() <https://www.php.net/trim>`_ will remove all occurrences of the requested char(). This may remove a loop with `substr() <https://www.php.net/substr>`_, or remove more than is needed. 

`trim() <https://www.php.net/trim>`_ doesn't work with multi-bytes strings, but so does `substr() <https://www.php.net/substr>`_. For that, use `mb_substr() <https://www.php.net/mb_substr>`_, as there isn't any mb_trim() function (so far in PHP 8.2).

.. code-block:: php
   
   <?php
   
   $a = '$drop the dollar'; 
   $b = substr($a, 1); // drop the first char 
   $b = ltrim($a, '$'); // remove the initial '$'s
   
   
   $b = substr($a, 1);     // replace with ltrim()
   
   $b = substr($a, 0, -1); // replace with rtrim()
   
   $b = substr($a, 1, -1); // replace with trim()
   
   ?>

See also `trim <https://www.php.net/manual/en/function.trim.php>`_, `ltrim <https://www.php.net/manual/en/function.ltrim.php>`_ and `rtrim <https://www.php.net/manual/en/function.rtrim.php>`_.


Suggestions
___________

* Replace substr() with trim(), ltrim() or rtrim().




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SubstrToTrim                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


