.. _structures-novariableisacondition:

.. _variable-is-not-a-condition:

Variable Is Not A Condition
+++++++++++++++++++++++++++

  Avoid using a lone variable as a condition. It is recommended to use a comparative value, or one of the filtering function, such as `isset() <https://www.www.php.net/isset>`_, empty(). 

Using the raw variable as a condition blurs the difference between an undefined variable and an empty value. By using an explicit comparison or validation function, it is easier to understand what the variable stands for.
Thanks to the `PMB <https://www.sigb.net/>`_ team for the inspiration.

.. code-block:: php
   
   <?php
   
   if (isset($error)) {
       echo 'Found one error : '.$error!;
   }
   
   //
   if ($errors) {
       print count($errors).' errors found : '.join('', $errors).PHP_EOL;
       echo 'Not found';
   }
   
   ?>

Suggestions
___________

* Make the validation explicit, by using a comparison operator, or one of the validation function.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoVariableIsACondition                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | comparison, iffectation                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


