.. _classes-oldstylevar:

.. _var-keyword:

Var Keyword
+++++++++++

  Var was used in PHP 4 to mark properties as public. Nowadays, new keywords are available : public, protected, private. Var is equivalent to public. 

It is recommended to avoid using var, and explicitly use the new keywords.

.. code-block:: php
   
   <?php
   
   class foo {
       public $bar = 1;
       // Avoid var
       //var $bar = 1; 
   }
   
   ?>

See also `Visibility <https://www.php.net/manual/en/language.oop5.visibility.php>`_.

Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* It is recommended to avoid using var, and explicitly use the new keywords : private, protected, public




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/OldStyleVar                                                                                                     |
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
| ClearPHP     | `no-php4-class-syntax <https://github.com/dseguy/clearPHP/tree/master/rules/no-php4-class-syntax.md>`__                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xataface-classes-oldstylevar`                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


