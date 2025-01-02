.. _classes-accessprivate:

.. _accessing-private:

Accessing Private
+++++++++++++++++

.. meta::
	:description:
		Accessing Private: List of calls to private properties/methods that will compile but yield some fatal error upon execution.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Accessing Private
	:twitter:description: Accessing Private: List of calls to private properties/methods that will compile but yield some fatal error upon execution
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Accessing Private
	:og:type: article
	:og:description: List of calls to private properties/methods that will compile but yield some fatal error upon execution
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Accessing Private.html
	:og:locale: en
List of calls to private properties/methods that will compile but yield some fatal `error <https://www.php.net/error>`_ upon execution.

.. code-block:: php
   
   <?php
   
   class a {
       private $a;
   }
   
   class b extends a {
       function c() {
           $this->a;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `private <https://php-dictionary.readthedocs.io/en/latest/dictionary/private.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AccessPrivate                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


