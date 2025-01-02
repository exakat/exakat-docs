.. _classes-abstractclass:

.. _abstract-class-usage:

Abstract Class Usage
++++++++++++++++++++

.. meta::
	:description:
		Abstract Class Usage: This rule lists of all abstract classes defined.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Abstract Class Usage
	:twitter:description: Abstract Class Usage: This rule lists of all abstract classes defined
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Abstract Class Usage
	:og:type: article
	:og:description: This rule lists of all abstract classes defined
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Abstract Class Usage.html
	:og:locale: en
This rule lists of all abstract classes defined. Abstract classes cannot be instanciated, and must be extended to be used.

.. code-block:: php
   
   <?php
   
   abstract class foo {
       function foobar(); 
   }
   
   class bar extends foo {
       // extended method
       function foobar() {
           // doSomething()
       }
   
       // extra method
       function barbar() {
           // doSomething()
       }
   }
   ?>

See also `Classes abstraction <https://www.php.net/abstract>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `abstract <https://php-dictionary.readthedocs.io/en/latest/dictionary/abstract.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/Abstractclass                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


