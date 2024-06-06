.. _classes-nonnullablesetters:

.. _non-nullable-getters:

Non Nullable Getters
++++++++++++++++++++

  A getter needs to be nullable when a property is injected. 

In particular, if the injection happens with a separate method, there is a time where the object is not consistent, and the property holds a default non-object value.

.. code-block:: php
   
   <?php
   
   class Consistent {
       private $db = null;
       
       function __construct(Db $db) { 
           $this->db = $db;
           // Object is immediately consistent 
       }
       
       // Db might be null
       function getDb() {
           return $this->db;
       }
   }
   
   class Inconsistent {
       private $db = null;
       
       function __construct() { 
           // No initialisation
       }
   
       // This might be called on time, or not
       // This typehint cannot be nullable, nor use null as default 
       function setDb(DB $db) {
           return $this->db;
       }
   
       // Db might be null
       function getDb() {
           return $this->db;
       }
   }
   ?>

Suggestions
___________

* Remove the nullable option and the tests on ``null``.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NonNullableSetters                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | injection                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


