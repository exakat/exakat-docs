.. _classes-cantoverwritefinalconstant:

.. _can't-overwrite-final-constant:

Can't Overwrite Final Constant
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Can't Overwrite Final Constant: A class constant may be ``final``, and can't be overwritten in a child class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Can't Overwrite Final Constant
	:twitter:description: Can't Overwrite Final Constant: A class constant may be ``final``, and can't be overwritten in a child class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Can't Overwrite Final Constant
	:og:type: article
	:og:description: A class constant may be ``final``, and can't be overwritten in a child class
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/CantOverwriteFinalConstant.html
	:og:locale: en
A class constant may be ``final``, and can't be overwritten in a child class. ``final`` is a way to make sure a constant cannot be changed in children classes.

``private`` constants can't be made final, as they are not accessible to any other class. 


.. code-block:: php
   
   <?php
   
   class y extends x { 
       const F = 1;
       const P = 2;
   }
   
   class x { 
       final const F = 3;
       private const PRI = 5; // Private can't be final
       const P = 4;
   }
   
   ?>
Related PHP errors 
-------------------

  + `%s::%s cannot override final constant %s::%s <https://php-errors.readthedocs.io/en/latest/messages/%25s%3A%3A%25s-cannot-override-final-constant-%25s%3A%3A%25s.html>`_



Connex PHP features
-------------------

  + `final <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_
  + `overwrite <https://php-dictionary.readthedocs.io/en/latest/dictionary/overwrite.ini.html>`_


Suggestions
___________

* Remove the final keyword in the parent class
* Remove the class constant in the child class
* Rename the class constant in the child class




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantOverwriteFinalConstant                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.9                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


