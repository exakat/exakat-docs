.. _structures-unusedlabel:

.. _unused-label:

Unused Label
++++++++++++

.. meta\:\:
	:description:
		Unused Label: Some labels have been defined in the code, but they are not used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unused Label
	:twitter:description: Unused Label: Some labels have been defined in the code, but they are not used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unused Label
	:og:type: article
	:og:description: Some labels have been defined in the code, but they are not used
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/UnusedLabel.html
	:og:locale: en
  Some labels have been defined in the code, but they are not used. They may be removed as they are dead code.



There is no analysis for undefined goto call, as PHP checks that goto has a destination label at compile time :

.. code-block:: php
   
   <?php
   
   $a = 0;
   A: 
   
       ++$a;
       
       // A loop. A: is used
       if ($a < 10) { goto A; }
   
   // B is never called explicitly. This is useless.
   B: 
   
   ?>

See also `Goto <https://www.php.net/manual/en/control-structures.goto.php>`_.

Connex PHP features
-------------------

  + `label <https://php-dictionary.readthedocs.io/en/latest/dictionary/label.ini.html>`_
  + `goto <https://php-dictionary.readthedocs.io/en/latest/dictionary/goto.ini.html>`_


Suggestions
___________

* Remove the unused label
* Add a goto call to this label
* Check for spelling mistakes
* Check that it is not a coding typo, like a raw ``http://www.php.net``, left in the code (It is actually valid PHP code)




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnusedLabel                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


