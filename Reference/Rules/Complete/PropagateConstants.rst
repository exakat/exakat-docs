.. _complete-propagateconstants:

.. _propagate-constants:

Propagate Constants
+++++++++++++++++++

.. meta\:\:
	:description:
		Propagate Constants: This command calculates constant expression values, and set them in the graph.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Propagate Constants
	:twitter:description: Propagate Constants: This command calculates constant expression values, and set them in the graph
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Propagate Constants
	:og:type: article
	:og:description: This command calculates constant expression values, and set them in the graph
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/PropagateConstants.html
	:og:locale: en
  This command calculates constant expression values, and set them in the graph.
After running this command, B has ``intval`` of 3. 

This command propagate ``const`` constants, class constants and `define() <https://www.php.net/define>`_ constants, when possible.

.. code-block:: php
   
   <?php
   
   const A = 1;
   const B = A + 2; 
   
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_
  + `static-constant-expression <https://php-dictionary.readthedocs.io/en/latest/dictionary/static-constant-expression.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/PropagateConstants                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


