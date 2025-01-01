.. _php-assignand:

.. _assign-and-lettered-logical-operator-precedence:

Assign And Lettered Logical Operator Precedence
+++++++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Assign And Lettered Logical Operator Precedence: The lettered logical operators ``and``, ``or`` and ``xor`` have lower precedence than assignation.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Assign And Lettered Logical Operator Precedence
	:twitter:description: Assign And Lettered Logical Operator Precedence: The lettered logical operators ``and``, ``or`` and ``xor`` have lower precedence than assignation
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Assign And Lettered Logical Operator Precedence
	:og:type: article
	:og:description: The lettered logical operators ``and``, ``or`` and ``xor`` have lower precedence than assignation
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/AssignAnd.html
	:og:locale: en
The lettered logical operators ``and``, ``or`` and ``xor`` have lower precedence than assignation. It collects less information than expected.

When that precedence is taken into account, this is valid and useful code. Yet, as it is rare and surprising to many developers, it is recommended to avoid it.

It is recommended to use the &&, ^ and || operators, instead of and, or and xor, to prevent confusion.

.. code-block:: php
   
   <?php
   
   // The expected behavior is 
   // The following are equivalent
    $a =  $b  && $c;
    $a = ($b && $c);
   
   // The unexpected behavior is 
   // The following are equivalent
    $a = $b  and $c;
   ($a = $b) and $c;
   
   // Here, the result is collected. That result would not make use of the result of the throw expression
   $a = doSomething() or throw new Exception('Error happened');
   
   ?>

See also `Operator Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `precedence <https://php-dictionary.readthedocs.io/en/latest/dictionary/precedence.ini.html>`_
  + `operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/operator.ini.html>`_
  + `logical-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/logical-operator.ini.html>`_


Suggestions
___________

* Use symbolic operators rather than letter ones
* To be safe, add parenthesis to enforce priorities




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/AssignAnd                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-php-assignand`                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


