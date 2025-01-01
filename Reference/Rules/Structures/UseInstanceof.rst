.. _structures-useinstanceof:

.. _avoid-get\_class():

Avoid get_class()
+++++++++++++++++

.. meta::
	:description:
		Avoid get_class(): ``get_class()`` should be replaced with the ``instanceof`` operator to check the class of an object.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid get_class()
	:twitter:description: Avoid get_class(): ``get_class()`` should be replaced with the ``instanceof`` operator to check the class of an object
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid get_class()
	:og:type: article
	:og:description: ``get_class()`` should be replaced with the ``instanceof`` operator to check the class of an object
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/UseInstanceof.html
	:og:locale: en
``get_class()`` should be replaced with the ``instanceof`` operator to check the class of an object. 

``get_class()`` only compares the full namespace name of the object's class, while ``instanceof`` actually resolves the name, using the local namespace and aliases.

.. code-block:: php
   
   <?php
   
       use Stdclass as baseClass;
       
       function foo($arg) {
           // Slow and prone to namespace errors
           if (get_class($arg) === 'Stdclass') {
               // doSomething()
           }
       }
   
       function bar($arg) {
           // Faster, and uses aliases.
           if ($arg instanceof baseClass) {
               // doSomething()
           }
       }
   ?>

See also `get_class <https://www.php.net/get_class>`_ and `Instanceof <https://www.php.net/manual/en/language.operators.type.php>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Suggestions
___________

* Replace get_class() with the instanceof operator




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseInstanceof                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


