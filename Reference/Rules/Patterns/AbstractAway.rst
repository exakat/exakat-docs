.. _patterns-abstractaway:

.. _abstract-away:

Abstract Away
+++++++++++++

.. meta::
	:description:
		Abstract Away: Avoid using PHP native functions that produce data directly in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Abstract Away
	:twitter:description: Abstract Away: Avoid using PHP native functions that produce data directly in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Abstract Away
	:og:type: article
	:og:description: Avoid using PHP native functions that produce data directly in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Abstract Away.html
	:og:locale: en
Avoid using PHP native functions that produce data directly in the code. For example, `date() <https://www.php.net/date>`_ or `random_int() <https://www.php.net/random_int>`_. They should be abstracted away in a method, that will be replaced later for testing purposes, or even debugging.

To abstract such calls, place them in a method, and add an interface to this method. Then, create and use those objects.
This analysis targets two API for abstraction : time and random values. Time and date related functions may be replaced by `Carbon <https://carbon.nesbot.com/docs/>`_, `Clock <https://github.com/lcobucci/clock>`_, `Chronos <https://github.com/cakephp/chronos>`_. Random values may be replaced with `RandomLib <https://github.com/ircmaxell/RandomLib/>`_ or a custom interface.

.. code-block:: php
   
   <?php
   
   // abstracted away date 
   $today = new MyDate();
   echo 'Date : '.$today->date('r');
   
   // hard coded date of today : it changes all the time.
   echo 'Date : '.date('r');
   
   interface MyCalendar{
       function date($format) : string ;
   }
   
   class MyDate implements MyCalendar {
       function date($format) : string { return date('r'); }
   }
   
   // Valid implementation, reserved for testing purpose
   // This prevents from waiting 4 years for a test.
   class MyDateForTest implements MyCalendar {
       function date($format) : string { return date('r', strtotime('2016-02-29 12:00:00')); }
   }
   
   ?>

+---------------------+---------+----------+----------------------------------------------------------------------+
| Name                | Default | Type     | Description                                                          |
+---------------------+---------+----------+----------------------------------------------------------------------+
| abstractableCalls   |         | ini_hash | Functions that shouldn't be called directly, unless in a method.     |
+---------------------+---------+----------+----------------------------------------------------------------------+
| abstractableClasses |         | ini_hash | Classes that shouldn't be instantiated directly, unless in a method. |
+---------------------+---------+----------+----------------------------------------------------------------------+



See also `Being in control of time in PHP <https://blog.frankdejonge.nl/being-in-control-of-time-in-php/>`_ and `How to test non-deterministic code <https://www.orbitale.io/2019/12/24/how-to-test-non-deterministic-code.html>`_.


Suggestions
___________

* Abstract away the calls to native PHP functions, and upgrade the unit tests




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Patterns/AbstractAway                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


