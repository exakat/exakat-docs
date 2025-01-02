.. _structures-iffectation:

.. _iffectations:

Iffectations
++++++++++++

.. meta::
	:description:
		Iffectations: Affectations that appears in a condition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Iffectations
	:twitter:description: Iffectations: Affectations that appears in a condition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Iffectations
	:og:type: article
	:og:description: Affectations that appears in a condition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Iffectations.html
	:og:locale: en
Affectations that appears in a condition. 

Iffectations are a way to do both a test and an affectations. 
They may also be typos, such as if ($x = 3) { `... <https://www.php.net/manual/en/functions.arguments.php#functions.variable-arg-list>`_ }, leading to a constant condition.

.. code-block:: php
   
   <?php
   
   // an iffectation : assignation in a If condition
   if($connexion = mysql_connect($host, $user, $pass)) {
       $res = mysql_query($connexion, $query);
   }
   
   // Iffectation may happen in while too.
   while($row = mysql_fetch($res)) {
       $store[] = $row;
   }
   
   ?>
Connex PHP features
-------------------

  + `assignation <https://php-dictionary.readthedocs.io/en/latest/dictionary/assignation.ini.html>`_


Suggestions
___________

* Move the assignation inside the loop, and make an existence test in the condition.
* Move the assignation before the if/then, make an existence test in the condition.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/Iffectation                                                                                                  |
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
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


