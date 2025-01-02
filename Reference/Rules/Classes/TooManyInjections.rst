.. _classes-toomanyinjections:

.. _too-many-injections:

Too Many Injections
+++++++++++++++++++

.. meta::
	:description:
		Too Many Injections: When a class is constructed with more than four dependencies, it should be split into smaller classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Too Many Injections
	:twitter:description: Too Many Injections: When a class is constructed with more than four dependencies, it should be split into smaller classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Too Many Injections
	:og:type: article
	:og:description: When a class is constructed with more than four dependencies, it should be split into smaller classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Too Many Injections.html
	:og:locale: en
When a class is constructed with more than four dependencies, it should be split into smaller classes.

.. code-block:: php
   
   <?php
   
   // This class relies on 5 other instances. 
   // It is probably doing too much.
   class Foo {
       public function __construct(
               A $a, 
               B $b, 
               C $c,
               D $d
               E $e ) {
           $this->a = $a;
           $this->b = $b;
           $this->d = $d;
           $this->d = $d;
           $this->e = $e;
       }
   }
   
   ?>

+-----------------+---------+---------+-----------------------------------------------------------+
| Name            | Default | Type    | Description                                               |
+-----------------+---------+---------+-----------------------------------------------------------+
| injectionsCount | 5       | integer | Threshold for too many injected parameters for one class. |
+-----------------+---------+---------+-----------------------------------------------------------+



See also `Dependency Injection Smells <http://seregazhuk.github.io/2017/05/04/di-smells/>`_.

Connex PHP features
-------------------

  + `injection <https://php-dictionary.readthedocs.io/en/latest/dictionary/injection.ini.html>`_


Suggestions
___________

* Split the class into smaller classes. Try to do less in that class.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/TooManyInjections                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.6                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-nextcloud-classes-toomanyinjections`, :ref:`case-thelia-classes-toomanyinjections`                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


