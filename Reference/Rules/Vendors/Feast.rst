.. _vendors-feast:

.. _feast-usage:

Feast usage
+++++++++++

  This analysis reports usage of the Feast framework.

FEAST is a radically different PHP Framework that was built from the ground up to be an alternative to the dependency-heavy frameworks that exist already. Its goal is a light-weight footprint that just lets you get stuff done.


.. code-block:: php
   
   <?php
   
   $this->httpRequest->postJson(self::URL . '/subscribers');
   $this->httpRequest->addArguments($data);
   $this->httpRequest->authenticate($this->apiKey, '');
   $this->httpRequest->makeRequest();
   $response = $this-httpRequest->getResponseAsJson();
   
   ?>

See also `Feast <https://docs.feast-framework.com/>`_ and `Feast on github<https://github.com/feastframework/framework>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Feast                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | framework                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


