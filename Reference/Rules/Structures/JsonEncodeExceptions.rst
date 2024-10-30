.. _structures-jsonencodeexceptions:

.. _json\_encode()-without-catching-exceptions:

Json_encode() Without Catching Exceptions
+++++++++++++++++++++++++++++++++++++++++

  `json_encode() <https://www.php.net/json_encode>`_ and `json_decode() <https://www.php.net/json_decode>`_ should use the `exception <https://www.php.net/exception>`_ system, to detect invalid JSON syntax. 

The second argument is a bitmask, and shall include `JSON_THROW_ON_ERROR <https://www.php.net/JSON_THROW_ON_ERROR>`_, so that both function may emit an `exception <https://www.php.net/exception>`_ when a parsing `error <https://www.php.net/error>`_ happen. That `exception <https://www.php.net/exception>`_ can then be caught with a try/catch structure.
Alternatively, the `error <https://www.php.net/error>`_ may be check by calling `json_last_error() <https://www.php.net/json_last_error>`_ function. It will not be empty if an `error <https://www.php.net/error>`_ is called.

.. code-block:: php
   
   <?php
   
   try{
   	echo json_encode($response,  JSON_THROW_ON_ERROR | JSON_PRETY_PRINT);
   } catch (\JsonException $e) {
   	echo "Sorry, an error occured.";
   }
   ?>

See also `json_encode() <https://www.php.net/manual/en/function.json-encode.php>`_.

Connex PHP features
-------------------

  + `json <https://php-dictionary.readthedocs.io/en/latest/dictionary/json.ini.html>`_
  + `error-handling <https://php-dictionary.readthedocs.io/en/latest/dictionary/error-handling.ini.html>`_


Suggestions
___________

* Add the JSON_THROW_ON_ERROR in the second argument.
* Call json_validate() on the data, before parsing it.
* Check json_last_error() after the parsing, to detect any error




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/JsonEncodeExceptions                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
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


