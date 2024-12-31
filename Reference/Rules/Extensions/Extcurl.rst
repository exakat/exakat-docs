.. _extensions-extcurl:

.. _ext-curl:

ext/curl
++++++++

.. meta\:\:
	:description:
		ext/curl: Extension curl.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/curl
	:twitter:description: ext/curl: Extension curl
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/curl
	:og:type: article
	:og:description: Extension curl
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extcurl.html
	:og:locale: en
  Extension curl.

PHP supports libcurl, a library created by Daniel Stenberg. It allows the `connection <https://www.php.net/connection>`_ and communication to many different types of servers with many different types of protocols.

.. code-block:: php
   
   <?php
   
   $ch = curl_init("http://www.example.com/");
   $fp = fopen("example_homepage.txt", "w");
   
   curl_setopt($ch, CURLOPT_FILE, $fp);
   curl_setopt($ch, CURLOPT_HEADER, 0);
   
   curl_exec($ch);
   curl_close($ch);
   fclose($fp);
   ?>

See also `Curl for PHP <https://www.php.net/manual/en/book.curl.php>`_ and `curl <https://curl.haxx.se/libcurl/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extcurl                                                                                                                                                                      |
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


