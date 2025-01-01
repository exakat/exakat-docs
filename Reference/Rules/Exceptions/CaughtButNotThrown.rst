.. _exceptions-caughtbutnotthrown:

.. _undefined-caught-exceptions:

Undefined Caught Exceptions
+++++++++++++++++++++++++++

.. meta::
	:description:
		Undefined Caught Exceptions: Those are exceptions that are caught in the code, but are not defined in the application.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Caught Exceptions
	:twitter:description: Undefined Caught Exceptions: Those are exceptions that are caught in the code, but are not defined in the application
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Caught Exceptions
	:og:type: article
	:og:description: Those are exceptions that are caught in the code, but are not defined in the application
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Exceptions/CaughtButNotThrown.html
	:og:locale: en
Those are exceptions that are caught in the code, but are not defined in the application. 

They may be externally defined, such as in core PHP, extensions or libraries. Make sure those exceptions are useful to your application : otherwise, they are dead code.

.. code-block:: php
   
   <?php
   
   try {
       library_function($some, $args);
       
   } catch (LibraryException $e) {
       // This exception is not defined, and probably belongs to Library
       print "Library failed\n";
   
   } catch (OtherLibraryException $e) {
       // This exception is not defined, and probably do not belongs to this code
       print "Library failed\n";
   
   } catch (\Exception $e) {
       // This exception is a PHP standard exception
       print "Something went wrong, but not at Libary level\n";
   }
   
   ?>
Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_
  + `predefined-exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/predefined-exception.ini.html>`_


Suggestions
___________

* Remove the catch clause, as it is dead code
* Make sure the exception is thrown by the underlying code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CaughtButNotThrown                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


