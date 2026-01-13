.. _structures-coalesceandconcat:

.. _coalesce-and-concat:

Coalesce And Concat
+++++++++++++++++++

  The concatenation operator ``.`` has precedence over the coalesce operator ``??``. 

It is recommended to add parenthesis to make this expression explicit.


.. code-block:: php
   
   <?php
   
   // Parenthesis are the right solution when in doubt
   echo a . ($b ?? 'd') . $e;
   
   // 'a' . $b is evaluated first, leading ot a useless ?? operator
   'a' . $b ?? $c;
   
   // 'd' . 'e' is evaluated first, leading to $b OR 'de'. 
   echo $b ?? 'd' . 'e';
   
   ?>
Connex PHP features
-------------------

  + `coalesce <https://php-dictionary.readthedocs.io/en/latest/dictionary/coalesce.ini.html>`_
  + `concat <https://php-dictionary.readthedocs.io/en/latest/dictionary/concat.ini.html>`_
  + `precedence <https://php-dictionary.readthedocs.io/en/latest/dictionary/precedence.ini.html>`_
  + `parenthesis <https://php-dictionary.readthedocs.io/en/latest/dictionary/parenthesis.ini.html>`_


Suggestions
___________

* Add parenthesis around ?? operator to avoid misbehavior
* Add parenthesis around the else condition to avoid misbehavior ( ?? ($a . $b))
* Do not use dot and ?? together in the same expression




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CoalesceAndConcat                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


