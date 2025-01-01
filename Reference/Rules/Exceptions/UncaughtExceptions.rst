.. _exceptions-uncaughtexceptions:

.. _uncaught-exceptions:

Uncaught Exceptions
+++++++++++++++++++

.. meta::
	:description:
		Uncaught Exceptions: The following exceptions are thrown in the code, but are never caught.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Uncaught Exceptions
	:twitter:description: Uncaught Exceptions: The following exceptions are thrown in the code, but are never caught
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Uncaught Exceptions
	:og:type: article
	:og:description: The following exceptions are thrown in the code, but are never caught
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Exceptions/UncaughtExceptions.html
	:og:locale: en
The following exceptions are thrown in the code, but are never caught. 
Either they will lead to a Fatal `Error <https://www.php.net/error>`_, or they have to be caught by an including application. This is a valid behavior for libraries, but is not for a final application.

.. code-block:: php
   
   <?php
   
   // This exception is throw, but not caught. It will lead to a fatal error.
   if ($message = check_for_error()) {
       throw new My\Exception($message);
   }
   
   // This exception is throw, and caught. 
   try {
       if ($message = check_for_error()) {
           throw new My\Exception($message);
       }
   } catch (\Exception $e) {
       doSomething();
   }
   
   ?>

See also `Structuring PHP Exceptions <https://www.alainschlesser.com/structuring-php-exceptions/>`_.

Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_
  + `try-catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/try-catch.ini.html>`_


Suggestions
___________

* Catch all the exceptions you throw




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/UncaughtExceptions                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


