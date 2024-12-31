.. _performances-toomanyextractions:

.. _too-many-extractions:

Too Many Extractions
++++++++++++++++++++

.. meta\:\:
	:description:
		Too Many Extractions: Using a loop to extract all the values from an array or an object, but failing to use them all later.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Too Many Extractions
	:twitter:description: Too Many Extractions: Using a loop to extract all the values from an array or an object, but failing to use them all later
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Too Many Extractions
	:og:type: article
	:og:description: Using a loop to extract all the values from an array or an object, but failing to use them all later
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Performances/TooManyExtractions.html
	:og:locale: en
  Using a loop to extract all the values from an array or an object, but failing to use them all later.

This means too much work was applied to the extraction, and it could be shorten by choosing the actual values.

.. code-block:: php
   
   <?php
   
   function bar($array) {
   	foreach(source() as $k => $v) {
   		$data[$k] = $v;
   	}
   	
   	// returning the whole array, so all can be useful
   	return $data;
   }
   
   function foo($array) {
   	foreach(source() as $k => $v) {
   		$data[$k] = $v;
   	}
   	
   	// only using one value, the rest is wasted
   	echo $data['foo'];
   }
   
   ?>

Suggestions
___________

* Filter data before extracting them
* Do not use a loop to extract all, but cherry pick the one that are needed




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/TooManyExtractions                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                    |
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


