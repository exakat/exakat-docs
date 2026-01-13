.. _performances-precalculateuse:

.. _pre-calculate-use:

Pre-Calculate Use
+++++++++++++++++

  In a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, it is faster to pass a final value, rather than calculate it at call time. 

In the ``use`` clause of the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_, make sure that the passed variables do not require any more processing, such as a call to another function or an extra expression.



This is a micro-optimisation. It has more potential with the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ used in a loop, or an array function.

.. code-block:: php
   
   <?php
   
   // $b->get is calculated inside the closure
   $d = $b->get();
   $f = function ($a) use ($d) {
   	return $d + $a;
   }
   
   // $b->get is calculated inside the closure
   $f = function ($a) use ($b) {
   	return $b->get() + $a;
   }
   ?>
Connex PHP features
-------------------

  + `closure <https://php-dictionary.readthedocs.io/en/latest/dictionary/closure.ini.html>`_
  + `micro-optimisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/micro-optimisation.ini.html>`_


Suggestions
___________

* Inject the final value in the closure and avoid method calls inside the closure




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/PreCalculateUse                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


