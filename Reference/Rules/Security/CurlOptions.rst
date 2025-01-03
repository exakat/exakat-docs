.. _security-curloptions:

.. _safe-curl-options:

Safe Curl Options
+++++++++++++++++

.. meta::
	:description:
		Safe Curl Options: It is advised to always use ``CURLOPT_SSL_VERIFYPEER`` and ``CURLOPT_SSL_VERIFYHOST`` when requesting a SSL connection.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Safe Curl Options
	:twitter:description: Safe Curl Options: It is advised to always use ``CURLOPT_SSL_VERIFYPEER`` and ``CURLOPT_SSL_VERIFYHOST`` when requesting a SSL connection
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Safe Curl Options
	:og:type: article
	:og:description: It is advised to always use ``CURLOPT_SSL_VERIFYPEER`` and ``CURLOPT_SSL_VERIFYHOST`` when requesting a SSL connection
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Safe Curl Options.html
	:og:locale: en
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

Connex PHP features
-------------------

  + `curl <https://php-dictionary.readthedocs.io/en/latest/dictionary/curl.ini.html>`_
  + `ssl <https://php-dictionary.readthedocs.io/en/latest/dictionary/ssl.ini.html>`_
  + `https <https://php-dictionary.readthedocs.io/en/latest/dictionary/https.ini.html>`_


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
| Examples     | :ref:`case-openconf-security-curloptions`                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


