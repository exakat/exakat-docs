.. _php-usesetcookie:

.. _should-use-setcookie():

Should Use SetCookie()
++++++++++++++++++++++

  Use `setcookie() <https://www.php.net/setcookie>`_ or `setrawcookie() <https://www.php.net/setrawcookie>`_. Avoid using `header() <https://www.php.net/header>`_ to do so, as the PHP native functions are more convenient and easier to spot during a refactoring.

`setcookie() <https://www.php.net/setcookie>`_ applies some encoding internally, for the value of the cookie and the date of expiration. Rarely, this encoding has to be skipped : then, use setrawencoding().

Both functions help by giving a checklist of important attributes to be used with the cookie.

.. code-block:: php
   
   <?php
   
   // same as below
   setcookie("myCookie", 'chocolate', time()+3600, "/", "", true, true);
   
   // same as above. Slots for path and domain are omitted, but should be used whenever possible
   header('Set-Cookie: myCookie=chocolate; Expires='.date('r', (time()+3600)).'; Secure; HttpOnly');
   
   ?>

See also `Set-Cookie <https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie>`_ and `setcookie <http://www.php.net/setcookie>`_.


Suggestions
___________

* Use setcookie() function, instead of header()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseSetCookie                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
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
| Features     | cookie, http-header                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


