.. _structures-switchtoswitch:

.. _switch-to-switch:

Switch To Switch
++++++++++++++++

.. meta::
	:description:
		Switch To Switch: The following structures are based on if / elseif / else.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Switch To Switch
	:twitter:description: Switch To Switch: The following structures are based on if / elseif / else
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Switch To Switch
	:og:type: article
	:og:description: The following structures are based on if / elseif / else
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Switch To Switch.html
	:og:locale: en
The following structures are based on if / elseif / else. Since they have more than three conditions (not withstanding the final else), it is recommended to use the switch structure, so as to make this more readable.

On the other hand, `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ structures with less than 3 elements should be expressed as a if / else structure.

Note that if condition that uses strict typing (=== or !==) can't be converted to `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ as the latter only performs == or != comparisons.
Note that simple switch statement, which compare a variable to a literal are optimised in PHP 7.2 and more recent. This gives a nice performance boost, and keep code readable.

.. code-block:: php
   
   <?php
   
   if ($a == 1) {
   
   } elseif ($a == 2) {
   
   } elseif ($a == 3) {
   
   } elseif ($a == 4) {
   
   } else {
   
   }
   
   // Better way to write long if/else lists
   switch ($a) {
       case 1 : 
           doSomething(1);
           break 1;
       
       case 2 : 
           doSomething(2);
           break 1;
   
       case 3 : 
           doSomething(3);
           break 1;
   
       case 4 : 
           doSomething(4);
           break 1;
       
       default :
           doSomething();
           break 1;
   }
   
   ?>

See also `PHP 7.2's switch optimisations <https://derickrethans.nl/php7.2-switch.html>`_ and `Is Your Code Readable By Humans? Cognitive Complexity Tells You <https://www.tomasvotruba.cz/blog/2018/05/21/is-your-code-readable-by-humans-cognitive-complexity-tells-you/>`_.

Connex PHP features
-------------------

  + `switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_
  + `match <https://php-dictionary.readthedocs.io/en/latest/dictionary/match.ini.html>`_


Suggestions
___________

* Use a switch statement, rather than a long string of if/else
* Use a match() statement, rather than a long string of if/else (PHP 8.0 +)




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SwitchToSwitch                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-thelia-structures-switchtoswitch`, :ref:`case-xoops-structures-switchtoswitch`                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


