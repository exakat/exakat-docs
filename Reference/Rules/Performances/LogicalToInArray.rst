.. _performances-logicaltoinarray:

.. _logical-to-in\_array:

Logical To in_array
+++++++++++++++++++

  Multiple exclusive comparisons with ``or``` may be replaced by faster alternative. 

+ `isset() <https://www.www.php.net/isset>`_ and an array which keys are the target comparisons
+ `array_key_exists() <https://www.php.net/array_key_exists>`_ and an array which keys are the target comparisons
+ `strpos() <https://www.php.net/strpos>`_ call, with all the target values merged into a string
+ `str_contains() <https://www.php.net/str_contains>`_ call, with all the target values merged into a string
+ `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ call, with each case being an assignation
+ `match() <https://www.php.net/manual/en/control-structures.match.php>`_ call
+ `in_array() <https://www.php.net/in_array>`_ call, with each values in an array

While each alternative has its performance gain, they make the code more readable by bringing the alternative values into one simple list. 

As little as three ``or`` comparisons are slower than using an alternative. The more calls, the slower is as string of ``or``. Also, the further the target value is in the ``or`` list, the slower it is to find it. Although, it is not easy to control that value. 

This analysis also reports `in_array() <https://www.php.net/in_array>`_ calls with arrays of a single element : those should be turned into a ``or`` call, or have more values in the array, or have the array published as a constant. 
This is a micro-optimisation : speed gain is low, and marginal. Code centralisation is a more significant advantage.

Thanks to `Frederic Bouchery <https://twitter.com/FredBouchery/>`_ for extending the alternatives of that analysis.

.. code-block:: php
   
   <?php
   
   $targetValues = array('a', 'b', 'c', 'd');
   $needle = 'd'; // for example
   
   // isset() & array_key_exists()
   $targets = array_flip($targetValues); // This might be a slow operation
   isset($targs[$a]);
   array_key_exists($a, $targs);
   
   // strpos() & str_contains
   $targets = implode('', $targeValues);
   strpos($targets, $needle) !== 0
   str_contains($targets, $needle) !== 0
   
   // switch()
   switch($needle) {
   	case 'a':  // Lots of typing to do
   	case 'b':
   	case 'c':
   	case 'd':
   		$result = true;
   		break;
   	
   	default:
   		$result = false;
   		break;
   }
   
   // match()
   // surprisingly, slitghly slower than switch()
   $result = match($needle) {
   	'a', 'b', 'c', 'd' => true,
   	default => false
   };
   
   // in_array()
   // Set the list of alternative in a variable, property or constant. 
   $result = in_array($a, $valid_values, true); // use third argument when you can
   
   // slowest and hard to read
   $result = $a == 'a' || $a == 'b' || $a == 'c' || $a == 'd');
   
   ?>

See also `in_array() <https://www.php.net/in_array>`_, `isset() <https://www.php.net/isset>`_, `match() <https://www.php.net/match>`_, `switch() <https://www.php.net/switch>`_ and `strpos() <https://www.php.net/strpos>`_.


Suggestions
___________

* Replace the list of comparisons with a in_array() call on an array filled with the various values
* Replace the list of comparisons with a strpos() call on an string joined with the various values
* Replace the list of comparisons with a match() call on an string joined with the various values
* Replace the list of comparisons with a switch() call on an string joined with the various values
* Replace the list of comparisons with a isset() call on a hash whose keys are the various values 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/LogicalToInArray                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-performances-logicaltoinarray`                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


