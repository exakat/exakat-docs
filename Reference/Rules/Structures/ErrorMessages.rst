.. _structures-errormessages:

.. _error-messages:

Error Messages
++++++++++++++

.. meta::
	:description:
		Error Messages: Error message when an error is reported in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Error Messages
	:twitter:description: Error Messages: Error message when an error is reported in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Error Messages
	:og:type: article
	:og:description: Error message when an error is reported in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Error Messages.html
	:og:locale: en
`Error <https://www.php.net/error>`_ message when an `error <https://www.php.net/error>`_ is reported in the code. Those messages will be read by whoever is triggering the `error <https://www.php.net/error>`_, and it has to be helpful. 

It is a good exercise to read the messages out of context, and try to understand what is about.
`Error <https://www.php.net/error>`_ messages are spotted via `die <https://www.php.net/die>`_, `exit <https://www.www.php.net/exit>`_, `trigger_error() <https://www.php.net/trigger_error>`_ or throw.

.. code-block:: php
   
   <?php
   
   // Not so helpful messages
   die('Here be monsters');
   exit('An error happened');
   throw new Exception('Exception thrown at runtime');
   
   ?>
Connex PHP features
-------------------

  + `error <https://php-dictionary.readthedocs.io/en/latest/dictionary/error.ini.html>`_
  + `die <https://php-dictionary.readthedocs.io/en/latest/dictionary/die.ini.html>`_
  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ErrorMessages                                                                                                                                                                |
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


