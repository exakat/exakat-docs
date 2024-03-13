.. _security-curloptions:

.. _safe-curl-options:

Safe Curl Options
+++++++++++++++++

  It is advised to always use ``CURLOPT_SSL_VERIFYPEER`` and ``CURLOPT_SSL_VERIFYHOST`` when requesting a SSL `connection <https://www.php.net/connection>`_. 

With those tests, the certificate is verified, and if it isn't valid, the `connection <https://www.php.net/connection>`_ fails : this is a safe behavior.

.. code-block:: php
   
   <?php
   $ch = curl_init();
   
   curl_setopt($ch, CURLOPT_URL, https://www.php.net/);
   
   // To be safe, always set this to true
   curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, true);
   
   curl_exec($ch);
   curl_close($ch);
   ?>

See also `Don’t turn off CURLOPT_SSL_VERIFYPEER, fix your PHP configuration <https://www.saotn.org/dont-turn-off-curlopt_ssl_verifypeer-fix-php-configuration/>`_, `Certainty: Automated CACert.pem Management for PHP Software <https://paragonie.com/blog/2017/10/certainty-automated-cacert-pem-management-for-php-software>`_ and `Server-Side HTTPS Requests <https://paragonie.com/blog/2017/12/2018-guide-building-secure-php-software#secure-server-side-https>`_.


Suggestions
___________

* Always use CURLOPT_SSL_VERIFYPEER and HTTPS for communication with other servers




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/CurlOptions                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | curl, ssl, https                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openconf-security-curloptions`                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


