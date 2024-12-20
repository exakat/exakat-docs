.. _structures-curlversionnow:

.. _curl\_version()-has-no-argument:

curl_version() Has No Argument
++++++++++++++++++++++++++++++

  `curl_version() <https://www.php.net/curl_version>`_ used to accept ``CURLVERSION_NOW`` as argument. Since PHP 7.4, it is a function without arguments.

.. code-block:: php
   
   <?php
   
   // Compatible syntax
   $details = curl_version(CURLVERSION_NOW);
   
   // New PHP 7.4 syntax
   $details = curl_version();
   
   ?>

See also `curl_version <https://www.php.net/manual/en/function.curl-version.php>`_.


Suggestions
___________

* Drop all arguments from curl_version() calls.




Specs
_____

+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/CurlVersionNow                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                            |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.8.4                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                     |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                   |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                         |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.4 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                                                                              |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                               |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


