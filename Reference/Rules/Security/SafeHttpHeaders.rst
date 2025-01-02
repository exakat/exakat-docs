.. _security-safehttpheaders:

.. _safe-http-headers:

Safe HTTP Headers
+++++++++++++++++

.. meta::
	:description:
		Safe HTTP Headers: Avoid configuring HTTP headers with lax restriction from within PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Safe HTTP Headers
	:twitter:description: Safe HTTP Headers: Avoid configuring HTTP headers with lax restriction from within PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Safe HTTP Headers
	:og:type: article
	:og:description: Avoid configuring HTTP headers with lax restriction from within PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Safe HTTP Headers.html
	:og:locale: en
Avoid configuring HTTP headers with lax restriction from within PHP. 

There are a lot of HTTP headers those days, targeting various vulnerabilities. To ensure backward compatibility, those headers have a default mode that is lax and permissive. It is recommended to avoid using those from within the code.

.. code-block:: php
   
   <?php
   
   //Good configuration, limiting access to origin
   header('Access-Control-Allow-Origin: https://www.exakat.io');
   
   //Configuration is present, but doesn't restrict anything : any external site is a potential source
   header('Access-Control-Allow-Origin: *');
   
   ?>

See also `Hardening Your HTTP Security Headers <https://www.keycdn.com/blog/http-security-headers>`_, `How To Secure Your Web App With HTTP Headers <https://www.smashingmagazine.com/2017/04/secure-web-app-http-headers/>`_ and `SecurityHeaders <https://securityheaders.com/>`_.

Connex PHP features
-------------------

  + `http-header <https://php-dictionary.readthedocs.io/en/latest/dictionary/http-header.ini.html>`_


Suggestions
___________

* Remove usage of those headers




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/SafeHttpHeaders                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


