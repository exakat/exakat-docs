.. _exceptions-throwfunctioncall:

.. _throw-functioncall:

Throw Functioncall
++++++++++++++++++

.. meta::
	:description:
		Throw Functioncall: The ``throw`` keyword expects to use an exception.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Throw Functioncall
	:twitter:description: Throw Functioncall: The ``throw`` keyword expects to use an exception
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Throw Functioncall
	:og:type: article
	:og:description: The ``throw`` keyword expects to use an exception
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Exceptions/ThrowFunctioncall.html
	:og:locale: en
The ``throw`` keyword expects to use an `exception <https://www.php.net/exception>`_. Calling a function to prepare that `exception <https://www.php.net/exception>`_ before throwing it is possible, but forgetting the new keyword is also possible. 
When the ``new`` keyword is forgotten, then the class constructor is used as a function name, and now `exception <https://www.php.net/exception>`_ is emitted, but an ``Undefined function`` fatal `error <https://www.php.net/error>`_ is emitted.

.. code-block:: php
   
   <?php
   
   // Forgotten new
   throw \RuntimeException('error!');
   
   // Code is OK, function returns an exception
   throw getException(ERROR_TYPE, 'error!');
   
   function getException(ERROR_TYPE, $message) {
       return new \RuntimeException($messsage);
   }
   
   ?>
Related PHP errors 
-------------------

  + `Call to undefined function <https://php-errors.readthedocs.io/en/latest/messages/call-to-undefined-function.html>`_
  + `Call to undefined function %s() <https://php-errors.readthedocs.io/en/latest/messages/call-to-undefined-function-%25s%28%29.html>`_



Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Add the new operator to the call
* Make sure the function is really a functioncall, not a class name
* Use return type for functions, so that Exception may be detected




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/ThrowFunctioncall                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-sugarcrm-exceptions-throwfunctioncall`, :ref:`case-zurmo-exceptions-throwfunctioncall`                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


