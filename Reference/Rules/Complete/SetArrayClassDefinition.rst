.. _complete-setarrayclassdefinition:

.. _set-array-class-definition:

Set Array Class Definition
++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Set Array Class Definition: Link arrays with their related method definition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Array Class Definition
	:twitter:description: Set Array Class Definition: Link arrays with their related method definition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Array Class Definition
	:og:type: article
	:og:description: Link arrays with their related method definition
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Complete/SetArrayClassDefinition.html
	:og:locale: en
  Link arrays with their related method definition.

PHP accepts an array structure such as ``[class, method]``, or ``[$object, method]`` as a valid method callback. This analysis builds such relations, whenever they are `static <https://www.php.net/manual/en/language.oop5.static.php>`_.

.. code-block:: php
   
   <?php
   
   class x {
       public function foo() {}
   }
   
   // designate the foo method in the x class
   $f = [\x, 'foo'];
   
   array_
   
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetArrayClassDefinition                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                                                                                   |
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


