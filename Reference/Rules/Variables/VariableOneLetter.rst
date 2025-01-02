.. _variables-variableoneletter:

.. _variables-with-one-letter-names:

Variables With One Letter Names
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		Variables With One Letter Names: Variables with one letter name are the shortest name for variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Variables With One Letter Names
	:twitter:description: Variables With One Letter Names: Variables with one letter name are the shortest name for variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Variables With One Letter Names
	:og:type: article
	:og:description: Variables with one letter name are the shortest name for variables
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Variables With One Letter Names.html
	:og:locale: en
Variables with one letter name are the shortest name for variables. They also bear very little meaning : what does contain the variable ``$w`` ? 

Some one-letter variables have meaning : ``$x`` and ``$y`` for coordinates, ``$i``, ``$j``, ``$k`` for blind variables. Others tend to be an easy way to give a name to a variable, without thinking too hard a good name.

.. code-block:: php
   
   <?php
   
   // $a is reported as a one-letter variable
   $a = 0;
   
   // $i is considered a false positive. 
   for($i = 0; $i < 10; ++$i) {
       $a += doSomething($i);
   }
   
   ?>

See also `Using single characters for variable names in loops/exceptions <https://softwareengineering.stackexchange.com/questions/71710/using-single-characters-for-variable-names-in-loops-exceptions?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa/>`_ and `Single Letter Variable Names Still Considered Harmful <https://odetocode.com/blogs/scott/archive/2008/11/17/single-letter-variable-names-still-considered-harmful.aspx>`_.


Suggestions
___________

* Make the variable more meaningful, with full words




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/VariableOneLetter                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


