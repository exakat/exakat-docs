.. _structures-returntruefalse:

.. _return-true-false:

Return True False
+++++++++++++++++

.. meta\:\:
	:description:
		Return True False: These conditional expressions return true/false, depending on the condition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Return True False
	:twitter:description: Return True False: These conditional expressions return true/false, depending on the condition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Return True False
	:og:type: article
	:og:description: These conditional expressions return true/false, depending on the condition
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ReturnTrueFalse.html
	:og:locale: en
  These conditional expressions return true/false, depending on the condition. This may be simplified by dropping the control structure altogether.
This may be simplified with : 
This may be applied to assignations and ternary operators too.

.. code-block:: php
   
   <?php
   
   if (version_compare($a, $b) >= 0) {
       return true;
   } else {
       return false;
   }
   
   ?>
Connex PHP features
-------------------

  + `boolean <https://php-dictionary.readthedocs.io/en/latest/dictionary/boolean.ini.html>`_


Suggestions
___________

* Return directly the comparison, without using the if/then structure
* Cast the value to (boolean) and use it instead of the ternary




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ReturnTrueFalse                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mautic-structures-returntruefalse`, :ref:`case-fuelcms-structures-returntruefalse`                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


