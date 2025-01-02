.. _classes-pppdeclarationstyle:

.. _properties-declaration-consistence:

Properties Declaration Consistence
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Properties Declaration Consistence: Properties may be declared all at once, or one by one.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Properties Declaration Consistence
	:twitter:description: Properties Declaration Consistence: Properties may be declared all at once, or one by one
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Properties Declaration Consistence
	:og:type: article
	:og:description: Properties may be declared all at once, or one by one
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Properties Declaration Consistence.html
	:og:locale: en
Properties may be declared all at once, or one by one. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It happens that choosing unique declarations or multiple depends on coding style and files.

.. code-block:: php
   
   <?php
   
   class x {
       // Some declarations are made by batch
       private $a1 = 1,
               $a2 = 2;
       public $c = 1, $c2 = 2, $c4 = 3;
   
       // Most declarations are made one by one
       protected $b = 1;
       protected $b1 = 1;
       protected $b2 = 1;
       protected $b3 = 1;
       protected $b4 = 1;
       protected $b5 = 1;
       protected $b6 = 1;
       protected $b7 = 1;
       protected $b8 = 1;
       protected $b9 = 1;
       protected $b10 = 1;
       protected $b11 = 1;
       protected $b12 = 1;
       protected $b13 = 1;
       protected $b14 = 1;
       protected $b15 = 1;
       protected $b16 = 1;
       protected $b17 = 1;
       protected $b18 = 1;
       protected $b19 = 1;
   
   }
   ?>

See also `PSR-12: Properties and constants <https://www.php-fig.org/psr/psr-12/#43-properties-and-constants>`_.

Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Suggestions
___________

* Make the declaration consistent : one or multiple.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PPPDeclarationStyle                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


