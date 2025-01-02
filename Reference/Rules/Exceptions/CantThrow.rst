.. _exceptions-cantthrow:

.. _can't-implement-throwable:

Can't Implement Throwable
+++++++++++++++++++++++++

.. meta::
	:description:
		Can't Implement Throwable: Classes extending ``Throwable`` can't be thrown, unless they also extend ``Exception``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Can't Implement Throwable
	:twitter:description: Can't Implement Throwable: Classes extending ``Throwable`` can't be thrown, unless they also extend ``Exception``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Can't Implement Throwable
	:og:type: article
	:og:description: Classes extending ``Throwable`` can't be thrown, unless they also extend ``Exception``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Can't Implement Throwable.html
	:og:locale: en
Classes extending ``Throwable`` can't be thrown, unless they also extend ``Exception``. The same applies to interfaces that extends ``Throwable``. 

Although such code lints, PHP throws a Fatal `error <https://www.php.net/error>`_ when executing or including it : ``Class fooThrowable cannot implement interface `Throwable <https://www.php.net/manual/en/class.`throwable <https://www.php.net/throwable>`_.php>`_, extend `Exception <https://www.php.net/exception>`_ or `Error <https://www.php.net/error>`_ instead``.

.. code-block:: php
   
   <?php
   
   // This is the way to go
   class fooException extends \Exception { }
   
   // This is not possible and a lot of work
   class fooThrowable implements \throwable { }
   
   ?>

See also `Throwable <https://www.php.net/manual/en/class.throwable.php>`_, `Exception <https://www.php.net/manual/en/class.exception.php>`_ and `Error <https://www.php.net/manual/en/class.error.php>`_.

Related PHP errors 
-------------------

  + `Class fooThrowable cannot implement interface Throwable, extend Exception or Error instead <https://php-errors.readthedocs.io/en/latest/messages/%25s-%25s-cannot-implement-interface-%25s%2C-extend-exception-or-error-instead.html>`_



Connex PHP features
-------------------

  + `throwable <https://php-dictionary.readthedocs.io/en/latest/dictionary/throwable.ini.html>`_
  + `error <https://php-dictionary.readthedocs.io/en/latest/dictionary/error.ini.html>`_
  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Extends the \Exception class
* Extends the \Error class




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CantThrow                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.3                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


