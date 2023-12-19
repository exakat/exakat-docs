.. _structures-namedregex:

.. _named-regex:

Named Regex
+++++++++++

  Captured subpatterns may be named, for easier reference. 

From the manual : It is possible to name a subpattern using the syntax ``(?P<name>pattern)``. This subpattern will then be indexed in the matches array by its normal numeric position and also by name. PHP 5.2.2 introduced two alternative syntaxes ``(?<name>pattern)`` and ``(?'name'pattern)``.

Naming subpatterns makes it easier to know what is read from the results of the subpattern : for example, ``$r['name']`` has more meaning than ``$r[1]``. 

Named subpatterns may also be shifted in the regex without impact on the resulting array. 


.. code-block:: php
   
   <?php
   
   $x = 'abc';
   preg_match_all('/(?<name>a)/', $x, $r);
   print_r($r[1]);
   print_r($r['name']);
   
   preg_match("/(?<name>a)(?'sub'b)/", $x, $s);
   print $s[2];
   print $s['sub'];
   
   ?>

See also `Subpatterns <https://www.php.net/manual/en/regexp.reference.subpatterns.php>`_.


Suggestions
___________

* Use named regex, and stop using integer-named subpatterns




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NamedRegex                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | regex                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phinx-structures-namedregex`, :ref:`case-shopware-structures-namedregex`                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


