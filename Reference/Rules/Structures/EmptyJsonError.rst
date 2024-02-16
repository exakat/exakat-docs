.. _structures-emptyjsonerror:

.. _empty-json-error:

Empty Json Error
++++++++++++++++

  `json_last_error() <https://www.php.net/json_last_error>`_ keeps the last `error <https://www.php.net/error>`_ that was generated while decoding a JSON string. To reset this cache to empty, one must run a call to `json_decode() <https://www.php.net/json_decode>`_ that succeed. This leads some code to make an apparently pointless call, just to empty the `error <https://www.php.net/error>`_ cache, and avoid confusing the message with the one of a previous call. 

.. code-block:: php
   
   <?php
   
   // This generates an error
   $json = json_decode([);
   
   $json = json_decode($valid_json);
   
   echo json_last_error(); // This error is confused for the last call, not the first one.
   
   // pointless call, except to empty the cache.
   $json = json_decode([]);
   
   $json = json_decode($valid_json);
   
   echo json_last_error(); // This error is dedicated to the last call
   
   ?>

Specs
_____

+--------------+------------------------------------------------------------+
| Short name   | Structures/EmptyJsonError                                  |
+--------------+------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>` |
+--------------+------------------------------------------------------------+
| Exakat since | 2.6.6                                                      |
+--------------+------------------------------------------------------------+
| PHP Version  | All                                                        |
+--------------+------------------------------------------------------------+
| Severity     | Minor                                                      |
+--------------+------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                            |
+--------------+------------------------------------------------------------+
| Precision    | High                                                       |
+--------------+------------------------------------------------------------+
| Available in |                                                            |
+--------------+------------------------------------------------------------+


