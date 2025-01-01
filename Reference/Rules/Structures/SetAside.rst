.. _structures-setaside:

.. _set-aside-code:

Set Aside Code
++++++++++++++

.. meta::
	:description:
		Set Aside Code: Setting aside code should be made into a method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Aside Code
	:twitter:description: Set Aside Code: Setting aside code should be made into a method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Aside Code
	:og:type: article
	:og:description: Setting aside code should be made into a method
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/SetAside.html
	:og:locale: en
Setting aside code should be made into a method. 

Setting aside code happens when one variable or member is stored locally, to be temporarily replaced by another value. Once the new value has been processed, the original value is reverted.

The temporary change of the value makes the code hard to read. 

It is a good example of a piece of code that could be moved to a separate method or function. Using the temporary value as a parameter makes the change visible, and avoid local pollution.

.. code-block:: php
   
   <?php
   
   // Setting aside database
   class cache extends Storage {
       private $database = null;
       
       function __construct($database) {
           $this->database = $database;
       }
       
       function foo($values) {
           // handling storage with sqlite3 
           $secondary = new cache(new Sqlite3(':memory:'));
           $secondary->store($values);
   
           $this->store($values);      // handling storage with injection 
       }
   }
   
   // Setting aside database to cache data in two distinct backend
   class cache extends Storage {
       private $database = null;
       
       function __construct(\Pdo $database) {
           $this->database = $database;
       }
       
       function foo($values) {
           // $this->database is set aside for secondary configuration
           $side = $this->database;
           $this->database = new Sqlite3(':memory:');
           $this->store($values);      // handling storage with sqlite3 
           $this->database = $side;
           // $this->database is restored
           $this->store($values);      // handling storage with injection 
       }
   }
   
   ?>

Suggestions
___________

* Extract the code that run with the temporary value to a separate method. 




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SetAside                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


