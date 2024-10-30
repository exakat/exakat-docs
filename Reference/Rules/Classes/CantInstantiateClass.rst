.. _classes-cantinstantiateclass:

.. _can't-instantiate-class:

Can't Instantiate Class
+++++++++++++++++++++++

  When constructor is not public, it is not possible to instantiate such a class. Either this is a conception choice, or there are factories to handle that. Either way, it is not possible to call new on such class.

.. code-block:: php
   
   <?php
   
   //This is the way to go
   $x = X::factory();
   
   //This is not possible
   $x = new X();
   
   class X {
       //This is also the case with proctected __construct
       private function __construct() {}
   
       static public function factory() {
           return new X();
       }
   }
   
   ?>

See also `In a PHP5 class, when does a private constructor get called? <https://stackoverflow.com/questions/26079/in-a-php5-class-when-does-a-private-constructor-get-called>`_, `Named Constructors in PHP <http://verraes.net/2014/06/named-constructors-in-php/>`_ and `PHP Constructor Best Practices And The Prototype Pattern <http://ralphschindler.com/2012/03/09/php-constructor-best-practices-and-the-prototype-pattern>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Call+to+private+Y%3A%3A__construct%28%29+from+invalid+context.html>`_



Connex PHP features
-------------------

  + `constructor <https://php-dictionary.readthedocs.io/en/latest/dictionary/constructor.ini.html>`_
  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Make the constructor public
* Create a factory, as a static method, in that class, to create objects
* Remove the new call




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantInstantiateClass                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-classes-cantinstantiateclass`                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


