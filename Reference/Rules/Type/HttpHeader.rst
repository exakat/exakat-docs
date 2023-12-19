.. _type-httpheader:

.. _http-headers:

Http Headers
++++++++++++

  List of HTTP headers use in the code. 


.. code-block:: php
   
   <?php
   
   header('Location: http://www.example.com/');
   
   // Parseable headers are also reported
   header('Location: http://www.example.com/');
   
   // UnParseable headers are not reported
   header('GarbagexxxxXXXXxxxGarbagexxxxXXXXxxx');
   header($header);
   
   ?>


Those headers are mostly used with `header() <https://www.php.net/header>`_ function to send to browser.

See also `List of HTTP header fields <https://en.wikipedia.org/wiki/List_of_HTTP_header_fields>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/HttpHeader                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Inventory <ruleset-Inventory>`                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | http, http-header                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


