.. _classes-cantextendfinal:

.. _can't-extend-final:

Can't Extend Final
++++++++++++++++++

.. meta::
	:description:
		Can't Extend Final: It is not possible to extend final classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Can't Extend Final
	:twitter:description: Can't Extend Final: It is not possible to extend final classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Can't Extend Final
	:og:type: article
	:og:description: It is not possible to extend final classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Can't Extend Final.html
	:og:locale: en
It is not possible to extend final classes. 

Since PHP fails with a fatal `error <https://www.php.net/error>`_, this means that the extending class is probably not used in the rest of the code. Check for dead code.
In a separate file :

.. code-block:: php
   
   <?php
       // File Foo
       final class foo {
           public final function bar() {
               // doSomething
           }
       }
   ?>

See also `Final Keyword <https://www.php.net/manual/en/language.oop5.final.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Class+y+cannot+extend+final+class+x.html>`_



Connex PHP features
-------------------

  + `final <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_


Suggestions
___________

* Remove the final keyword
* Remove the extending class




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantExtendFinal                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


