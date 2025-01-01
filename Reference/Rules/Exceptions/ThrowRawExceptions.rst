.. _exceptions-throwrawexceptions:

.. _throw-raw-exceptions:

Throw Raw Exceptions
++++++++++++++++++++

.. meta::
	:description:
		Throw Raw Exceptions: Avoid throwing native PHP exceptions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Throw Raw Exceptions
	:twitter:description: Throw Raw Exceptions: Avoid throwing native PHP exceptions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Throw Raw Exceptions
	:og:type: article
	:og:description: Avoid throwing native PHP exceptions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Exceptions/ThrowRawExceptions.html
	:og:locale: en
Avoid throwing native PHP exceptions. Consider defining specific and meaningful `exception <https://www.php.net/exception>`_, by extending the native one.
Thanks to `Atif Shahab Qureshi <https://twitter.com/Atif__Shahab>`_ for the inspiration.

.. code-block:: php
   
   <?php
   
   // Throwing a raw exception
   throw new exception('This is an error!');
   
   class myException extends Exception {}
   
   throw new myException('This is a distinguished error!');
   
   ?>

See also `Stop using regular exceptions in PHP! <https://abdlrahmansaber.medium.com/stop-using-regular-exceptions-in-php-e6aed2629dce>`_.

Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Define an adapted exception and throw it instead




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/ThrowRawExceptions                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


