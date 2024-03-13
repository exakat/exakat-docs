.. _functions-closure2string:

.. _closure-could-be-a-callback:

Closure Could Be A Callback
+++++++++++++++++++++++++++

  `Closure <https://www.php.net/manual/en/class.`closure <https://www.php.net/closure>`_.php>`_ and arrow function may be simplified to a callback. Callbacks are strings or arrays.

A simple `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ that only returns arguments relayed to another function or method, could be reduced to a simpler expression.  

`Closure <https://www.php.net/manual/en/class.`closure <https://www.php.net/closure>`_.php>`_ may be simplified with a string, for functioncall, with an array for methodcalls and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ methodcalls. 

Performances : simplifying a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ tends to reduce the call time by 50%.

.. code-block:: php
   
   <?php
   
   // Simple and faster call to strtoupper
   $filtered = array_map('strtoupper', $array);
   
   // Here the closure doesn't add any feature over strtoupper
   $filtered = array_map(function ($x) { return strtoupper($x);}, $array);
   
   // Methodcall example : no fix
   $filtered = array_map(function ($x) { return $x->strtoupper() ;}, $array);
   
   // Methodcall example  : replace with array($y, 'strtoupper')
   $filtered = array_map(function ($x) use ($y) { return $y->strtoupper($x) ;}, $array);
   
   // Static methodcall example 
   $filtered = array_map(function ($x) { return $x::strtoupper() ;}, $array);
   
   // Static methodcall example   : replace with array('A', 'strtoupper')
   $filtered = array_map(function ($x) { return A::strtoupper($x) ;}, $array);
   
   ?>

See also `Closure class <https://www.php.net/closure>`_ and `Callbacks / Callables <https://www.php.net/manual/en/language.types.callable.php>`_.


Suggestions
___________

* Replace the closure by a string, with the name of the called function
* Replace the closure by an array, with the name of the called method and the object as first element




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/Closure2String                                                                                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Rector <ruleset-Rector>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.3                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | closure, callback                                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-functions-closure2string`, :ref:`case-nextcloud-functions-closure2string`                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


