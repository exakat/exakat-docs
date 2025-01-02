.. _variables-overwriting:

.. _overwriting-variable:

Overwriting Variable
++++++++++++++++++++

.. meta::
	:description:
		Overwriting Variable: Replacing the content of a variable by something different is prone to errors.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwriting Variable
	:twitter:description: Overwriting Variable: Replacing the content of a variable by something different is prone to errors
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwriting Variable
	:og:type: article
	:og:description: Replacing the content of a variable by something different is prone to errors
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Overwriting Variable.html
	:og:locale: en
Replacing the content of a variable by something different is prone to errors. For example, it is not obvious if the $text variable is plain text or HTML text. 
Besides, it is possible that the source is needed later, for extra processing. 

Note that accumulators, like += .=  or [] etc., that are meant to collect lots of values with consistent type are OK.

.. code-block:: php
   
   <?php
   
   // Confusing
   $text = htmlentities($text);
   
   // Better
   $textHTML = htmlentities($text);
   
   ?>
Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/Overwriting                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


