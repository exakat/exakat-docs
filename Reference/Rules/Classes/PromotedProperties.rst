.. _classes-promotedproperties:

.. _promoted-properties:

Promoted Properties
+++++++++++++++++++

  Promoted properties is a way to declare the properties within the constructor, and have them assigned to the constructing value at instantiation.

.. code-block:: php
   
   <?php
   
       class CustomerDTO
       {
           public function __construct(
               public string $name, 
               public string $email, 
               public DateTimeImmutable $birth_date,
           ) {}
       }
       
   ?>

See also `Constructor Promotion <https://www.php.net/manual/en/language.oop5.decon.php#language.oop5.decon.constructor.promotion>`_ and `PHP 8: Constructor property promotion <https://stitcher.io/blog/constructor-promotion-in-php-8>`_.


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PromotedProperties                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.1                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | promoted-property                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


