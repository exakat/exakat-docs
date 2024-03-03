.. _attributes-friend:

.. _friend-attribute:

Friend Attribute
++++++++++++++++

  A method or class can supply via a #[Friend] `attribute <https://www.php.net/attribute>`_ a list of classes. Only these classes can call the method. This is loosely based on the C++ friend feature.

+ Multiple classes can be specified. E.g. #[Friend(Foo\:\:class, Bar\:\:class)]
+ A class can have a #[Friend] `attribute <https://www.php.net/attribute>`_, classes listed here are applied to every method.
+ The #[Friend] `attribute <https://www.php.net/attribute>`_ is additive. If a class and a method have the #[Friend] the method can be called from any of the classes listed. E.g.
+ This is is currently limited to method calls (including `__construct) <https://www.php.net/manual/en/language.oop5.decon.php>`_.

+ The `Attribute <https://www.php.net/attribute>`_ is limited to the exact classes, the family hierarchy is not searched.
+ Multiple attributes can be specified to add more classes. E.g. #[Friend(Foo\:\:class)] #[Friend(Bar\:\:class)]

Based on the specificiations from Dave Liddament.

.. code-block:: php
   
   <?php
   
   class Person
   {
       #[Friend(PersonBuilder::class)]
       public function __construct()
       {
           // Some implementation
       }
   }
   
   
   class PersonBuilder
   {
       public function build(): Person
       {
           $person = new Person(): // OK as PersonBuilder is allowed to call Person's construct method.
           // set up Person
           return $person;
       }
   }
   
   
   // ERROR Call to Person::__construct is not from PersonBuilder
   $person = new Person();
   
   ?>

See also `Friend <https://github.com/DaveLiddament/php-language-extensions#friend>`_ and `php-language-extension <https://github.com/DaveLiddament/php-language-extensions>`_.


Suggestions
___________

* Add the reported classes as friend to the original class
* Remove the call to the class from the reported classes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/Friend                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | attribute                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


