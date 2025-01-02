.. _structures-emptyloop:

.. _empty-loop:

Empty Loop
++++++++++

.. meta::
	:description:
		Empty Loop: This rule reports empty loop.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Empty Loop
	:twitter:description: Empty Loop: This rule reports empty loop
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Empty Loop
	:og:type: article
	:og:description: This rule reports empty loop
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Empty Loop.html
	:og:locale: en
This rule reports empty loop. An empty loop has no operation in its main block. 

Some empty loop may have features: they are calling methods in the condition, which may change the status of a resource. 

Empty loop may come from a typo, where a semi colon detach the block from its loop.

.. code-block:: php
   
   <?php
   
   $i = 0;
   // sneaky semi-colon behind the while
   while($i < 10) ; {
   	$i++;
   }
   
   // another sneaky semicolon
   foreach($a as $b) ; 
   {
   	$i++;
   }
   
   // This skips the first empty lines
   $fp = fopen('/path/to/file', 'r');
   while(!($row = fgets($fp))) {
   	
   }
   
   ?>
Connex PHP features
-------------------

  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Remove the extra semicolon
* Fill the loop with a payload




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/EmptyLoop                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


