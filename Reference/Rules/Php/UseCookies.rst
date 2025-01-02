.. _php-usecookies:

.. _use-cookies:

Use Cookies
+++++++++++

.. meta::
	:description:
		Use Cookies: This code source uses cookies.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Cookies
	:twitter:description: Use Cookies: This code source uses cookies
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Cookies
	:og:type: article
	:og:description: This code source uses cookies
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Cookies.html
	:og:locale: en
This code source uses cookies. 

Cookie usage is spotted with the usage of `setcookie() <https://www.php.net/setcookie>`_, `setrawcookie() <https://www.php.net/setrawcookie>`_ and `header() <https://www.php.net/header>`_ with the 'Set-Cookie' header.

.. code-block:: php
   
   <?php
   
        header('Set-Cookie: '.$name.'='.$value.'; EXPIRES'.$date.';');
   
       // From the PHP Manual : 
       setcookie('TestCookie3', $value, time()+3600, '/~rasmus/', 'example.com', 1);
   
   ?>

See also `Cookies <https://www.php.net/manual/en/features.cookies.php>`_.

Connex PHP features
-------------------

  + `cookie <https://php-dictionary.readthedocs.io/en/latest/dictionary/cookie.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseCookies                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.6                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


