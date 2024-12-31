.. _php-usesetcookie:

.. _should-use-setcookie():

Should Use SetCookie()
++++++++++++++++++++++

.. meta\:\:
	:description:
		Should Use SetCookie(): Use setcookie() or setrawcookie().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use SetCookie()
	:twitter:description: Should Use SetCookie(): Use setcookie() or setrawcookie()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use SetCookie()
	:og:type: article
	:og:description: Use setcookie() or setrawcookie()
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/UseSetCookie.html
	:og:locale: en
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

Connex PHP features
-------------------

  + `cookie <https://php-dictionary.readthedocs.io/en/latest/dictionary/cookie.ini.html>`_
  + `http-header <https://php-dictionary.readthedocs.io/en/latest/dictionary/http-header.ini.html>`_


Suggestions
___________

* Use setcookie() function, instead of header()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseSetCookie                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
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
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


