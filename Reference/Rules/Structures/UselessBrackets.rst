.. _structures-uselessbrackets:

.. _useless-brackets:

Useless Brackets
++++++++++++++++

  Standalone brackets have no use. Brackets are used to delimit a block of code, and are used by control statements. They may also be used to protect variables in strings. 

Standalone brackets may be a left over of an old instruction, or a misunderstanding of the alternative syntax.

.. code-block:: php
   
   <?php
   
   // The following brackets are useless : they are a leftover from an older instruction
   // if (DEBUG) 
   {
       $a = 1;
   }
   
   // Here, the extra brackets are useless
   for($a = 2; $a < 5; $a++) : {
       $b++;
   } endfor;
   
   ?>
Connex PHP features
-------------------

  + `block <https://php-dictionary.readthedocs.io/en/latest/dictionary/block.ini.html>`_
  + `curly-bracket <https://php-dictionary.readthedocs.io/en/latest/dictionary/curly-bracket.ini.html>`_


Suggestions
___________

* Remove the brackets
* Restore the flow-control operation that was there and removed
* Move the block into a method or function, and call it




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessBrackets                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-structures-uselessbrackets`, :ref:`case-piwigo-structures-uselessbrackets`                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


