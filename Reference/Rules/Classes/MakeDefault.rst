.. _classes-makedefault:

.. _assign-default-to-properties:

Assign Default To Properties
++++++++++++++++++++++++++++

  Properties may be assigned default values at declaration time. Such values may be later modified, if needed. 
Default values will save some instructions in the constructor, and makes the value obvious in the code.

.. code-block:: php
   
   <?php
   
   class foo {
       private $propertyWithDefault = 1;
       private $propertyWithoutDefault;
       private $propertyThatCantHaveDefault;
       
       public function __construct() {
           // Skip this extra line, and give the default value above
           $this->propertyWithoutDefault = 1;
   
           // Static expressions are available to set up simple computation at definition time.
           $this->propertyWithoutDefault = OtherClass::CONSTANT + 1;
   
           // Arrays, just like scalars, may be set at definition time
           $this->propertyWithoutDefault = [1,2,3];
   
           // Objects or resources can't be made default. That is OK.
           $this->propertyThatCantHaveDefault = fopen('/path/to/file.txt');
           $this->propertyThatCantHaveDefault = new Fileinfo();
       }
   }
   
   ?>

See also `PHP Default parameters <https://www.phptutorial.net/php-tutorial/php-default-parameters/>`_.

Connex PHP features
-------------------

  + `default-value <https://php-dictionary.readthedocs.io/en/latest/dictionary/default-value.ini.html>`_


Suggestions
___________

* Add a default value whenever possible. This is easy for scalars, and array()




Specs
_____

+--------------+---------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MakeDefault                                                                                                       |
+--------------+---------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+---------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                     |
+--------------+---------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                       |
+--------------+---------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                     |
+--------------+---------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                          |
+--------------+---------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                 |
+--------------+---------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `use-properties-default-values <https://github.com/dseguy/clearPHP/tree/master/rules/use-properties-default-values.md>`__ |
+--------------+---------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-livezilla-classes-makedefault`, :ref:`case-phpmyadmin-classes-makedefault`                                     |
+--------------+---------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_   |
+--------------+---------------------------------------------------------------------------------------------------------------------------+


