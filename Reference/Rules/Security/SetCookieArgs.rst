.. _security-setcookieargs:

.. _set-cookie-safe-arguments:

Set Cookie Safe Arguments
+++++++++++++++++++++++++

  The last five arguments of `setcookie() <https://www.php.net/setcookie>`_ and `setrawcookie() <https://www.php.net/setrawcookie>`_ are for security. Use them anytime you can.

``setcookie ( string $name [, string $value = " [, int $expire = 0 [, string $path = " [, string $domain = " [, bool $`secure <https://www.php.net/secure>`_ = false [, bool $httponly = false ]]]]]] )``

The ``$expire`` argument sets the date of expiration of the cookie. It is recommended to make it as low as possible, to reduce its chances to be captured. Sometimes, low expiration date may be several days (for preferences), and other times, low expiration date means a few minutes. 

The ``$path`` argument limits the transmission of the cookie to URL whose path matches the one mentioned here. By default, it is ``'/'``, which means the whole server. If a cookie usage is limited to a part of the application, use it here.

The ``$domain`` argument limits the transmission of the cookie to URL whose domain matches the one mentioned here. By default, it is ``''``, which means any server on the internet. At worse, you may use ``mydomain.com`` to cover your whole domain, or better, refine it with the actual subdomain of usage.

The ``$`secure <https://www.php.net/secure>`_`` argument limits the transmission of the cookie over HTTP (by default) or HTTPS. The second is better, as the transmission of the cookie is crypted. In case HTTPS is still at the planned stage, use '$_SERVER["HTTPS"]'. This environment variable is false on HTTP, and true on HTTPS.

The ``$httponly`` argument limits the access of the cookie to JavaScript. It is only transmitted to the browser, and retransmitted. This helps reducing XSS and CSRF attacks, though it is disputed. 

The ``$samesite`` argument limits the sending of the cookie to the domain that initiated the request. It is by default ``Lax`` but should be upgraded to ``Strict`` whenever possible. This feature is available as PHP 7.3.

.. code-block:: php
   
   <?php
   
   //admin cookie, available only on https://admin.my-domain.com/system/, for the next minute, and not readable by javascript
   setcookie("admin", $login, time()+60, "/system/", "admin.my-domain.com", $_SERVER['HTTPS'], 1);
   
   //login cookie, available until the browser is closed, over http or https
   setcookie("login", $login);
   
   //removing the login cookie : Those situations are omitted by the analysis
   setcookie("login", '');
   
   ?>

See also `setcookie <http://www.php.net/setcookie>`_ and `'SameSite' cookie attribute <https://www.chromestatus.com/feature/4672634709082112>`_.


Suggestions
___________

* Use all the argument when setting cookies with PHP functions




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/SetCookieArgs                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.6                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | cookie                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


