.. _classes-throwindestruct:

.. _throw-in-destruct:

Throw In Destruct
+++++++++++++++++

.. meta::
	:description:
		Throw In Destruct: According to the manual, ``Attempting to throw an exception from a destructor (called in the time of script termination) causes a fatal error.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Throw In Destruct
	:twitter:description: Throw In Destruct: According to the manual, ``Attempting to throw an exception from a destructor (called in the time of script termination) causes a fatal error
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Throw In Destruct
	:og:type: article
	:og:description: According to the manual, ``Attempting to throw an exception from a destructor (called in the time of script termination) causes a fatal error
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Throw In Destruct.html
	:og:locale: en
According to the manual, ``Attempting to throw an `exception <https://www.php.net/exception>`_ from a destructor (called in the time of script termination) causes a fatal `error <https://www.php.net/error>`_.``

The destructor may be called during the lifespan of the script, but it is not certain. If the `exception <https://www.php.net/exception>`_ is thrown later, the script may end up with a fatal `error <https://www.php.net/error>`_. 

Thus, it is recommended to avoid throwing exceptions within the ``__destruct`` method of a class.

.. code-block:: php
   
   <?php
   
   // No exception thrown
   class Bar { 
       function __construct() {
           throw new Exception('__construct');
       }
   
       function __destruct() {
           $this->cleanObject();
       }
   }
   
   // Potential crash
   class Foo { 
       function __destruct() {
           throw new Exception('__destruct');
       }
   }
   
   ?>

See also `Constructors and Destructors <https://www.php.net/manual/en/language.oop5.decon.php>`_.

Connex PHP features
-------------------

  + `throw <https://php-dictionary.readthedocs.io/en/latest/dictionary/throw.ini.html>`_


Suggestions
___________

* Remove any exception thrown from a destructor




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ThrowInDestruct                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


