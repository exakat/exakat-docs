.. _structures-checkjson:

.. _check-json:

Check JSON
++++++++++

  Check errors whenever JSON is encoded or decoded. 

In particular, ``NULL`` is a valid decoded JSON response. If you want to avoid mistaking `NULL <https://www.php.net/manual/en/language.types.null.php>`_ for an `error <https://www.php.net/error>`_, it is recommended to call ``json_last_error``.

.. code-block:: php
   
   <?php
   
   $encoded = json_encode($incoming);
   // Unless JSON must contains some non-null data, this mistakes NULL and error
   if(json_last_error() != JSON_ERROR_NONE) {
       die('Error when encoding JSON');
   }
   
   $decoded = json_decode($incoming);
   // Unless JSON must contains some non-null data, this mistakes NULL and error
   if($decoded === null) {
       die('ERROR');
   }
   
   ?>

See also `Option to make json_encode and json_decode throw exceptions on errors <https://ayesh.me/Upgrade-PHP-7.3#json-exceptions>`_ and `json_last_error <https://www.php.net/json_last_error>`_.


Suggestions
___________

* Always check after JSON operation : encoding or decoding.
* Add a call to json_last_error()
* Configure operations to throw an exception upon error (``JSON_THROW_ON_ERROR``), and catch it.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CheckJson                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.0                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Features     | json                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-structures-checkjson`                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


