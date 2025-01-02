.. _structures-noappendonsource:

.. _no-append-on-source:

No Append On Source
+++++++++++++++++++

.. meta::
	:description:
		No Append On Source: Do not append new elements to an array in a foreach loop.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Append On Source
	:twitter:description: No Append On Source: Do not append new elements to an array in a foreach loop
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Append On Source
	:og:type: article
	:og:description: Do not append new elements to an array in a foreach loop
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Append On Source.html
	:og:locale: en
Do not append new elements to an array in a foreach loop. Since PHP 7.0, the array is still used as a source, and will be augmented, and used again. 
Thanks to `Frederic Bouchery <https://twitter.com/FredBouchery/>`_ for the reminder.

.. code-block:: php
   
   <?php
   
   // Relying on the initial copy
   $a = [1];
   $initial = $a;
   foreach($initial as $v) {
       $a[] = $v + 1;
   }
   
   // Keep new results aside
   $a = [1];
   $tmp = [];
   foreach($a as $v) {
       $tmp[] = $v + 1;
   }
   $a = array_merge($a, $tmp);
   unset($tmp);
   
   // Example, courtesy of Frederic Bouchery
   // This is an infinite loop
   $a = [1];
   foreach($a as $v) {
       $a[] = $v + 1;
   }
   
   ?>

See also `foreach <https://www.php.net/manual/en/control-structures.foreach.php>`_ and `What will this code return? #PHP <https://twitter.com/FredBouchery/status/1135480412703211520>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Use a copy of the source, to avoid modifying it during the loop
* Store the new values in a separate storage




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoAppendOnSource                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.2                                                                                                                   |
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


