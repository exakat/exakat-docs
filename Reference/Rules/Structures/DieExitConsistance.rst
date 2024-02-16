.. _structures-dieexitconsistance:

.. _die-exit-consistence:

Die Exit Consistence
++++++++++++++++++++

  `Die <https://www.php.net/die>`_ and `Exit <https://www.www.php.net/exit>`_ have the same functional use. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It happens that `die <https://www.php.net/die>`_ or `exit <https://www.www.php.net/exit>`_ are used depending on coding style and files. One file may be consistently using `exit <https://www.www.php.net/exit>`_, while the others are all using `exit <https://www.www.php.net/exit>`_. 

Using `die <https://www.php.net/die>`_ or `exit <https://www.www.php.net/exit>`_ is also the target of other analysis.

.. code-block:: php
   
   <?php
   
   // be consistent
   switch ($a) {
       case 1 : 
           exit;
       case 2 : 
           exit;
       case 3 : 
           exit;
       case 4 : 
           exit;
       case 5 : 
           exit;
       case 6 : 
           exit;
       case 7 : 
           exit;
       case 8 : 
           exit;
       case 9 : 
           exit;
       case 10 : 
           exit;
       default : 
           die();   // Be consistent, always use the same. 
   }
   
   ?>

Suggestions
___________

* Adopt one of the two syntaxes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DieExitConsistance                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | die                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


