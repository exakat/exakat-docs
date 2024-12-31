.. _security-dontechoerror:

.. _don't-echo-error:

Don't Echo Error
++++++++++++++++

.. meta\:\:
	:description:
		Don't Echo Error: It is recommended to avoid displaying error messages directly to the browser.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Don't Echo Error
	:twitter:description: Don't Echo Error: It is recommended to avoid displaying error messages directly to the browser
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Don't Echo Error
	:og:type: article
	:og:description: It is recommended to avoid displaying error messages directly to the browser
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Security/DontEchoError.html
	:og:locale: en
  It is recommended to avoid displaying `error <https://www.php.net/error>`_ messages directly to the browser.

PHP's uses the ``display_errors`` directive to control display of errors to the browser. This must be kept to ``off`` when in production.
`Error <https://www.php.net/error>`_ messages should be logged, but not displayed.

.. code-block:: php
   
   <?php
   
   // Inside a 'or' test
   mysql_connect('localhost', $user, $pass) or die(mysql_error());
   
   // Inside a if test
   $result = pg_query( $db, $query );
   if( !$result )
   {
   	echo Erreur SQL: . pg_error();
   	exit;
   }
   
   // Changing PHP configuration
   ini_set('display_errors', 1);
   // This is also a security error : 'false' means actually true.
   ini_set('display_errors', 'false');
   
   ?>

See also `Error reporting <https://php.earth/docs/security/intro#error-reporting>`_ and `List of php.ini directives <https://www.php.net/manual/en/ini.list.php>`_.


Suggestions
___________

* Remove any echo, print, printf() call built with error messages from an exception, or external source.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/DontEchoError                                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.7                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-security-dontechoerror`, :ref:`case-phpdocumentor-security-dontechoerror`                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


