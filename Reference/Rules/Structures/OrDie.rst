.. _structures-ordie:

.. _or-die:

Or Die
++++++

.. meta::
	:description:
		Or Die: Classic old style failed error management.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Or Die
	:twitter:description: Or Die: Classic old style failed error management
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Or Die
	:og:type: article
	:og:description: Classic old style failed error management
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/OrDie.html
	:og:locale: en
Classic old style failed `error <https://www.php.net/error>`_ management. 



Interrupting a script will leave the application with a blank page, will make your life miserable for testing. Just don't do that.

.. code-block:: php
   
   <?php
   
   // In case the connexion fails, this kills the current script
   mysql_connect('localhost', $user, $pass) or die();
   
   ?>

See also `pg_last_error <https://www.php.net/manual/en/function.pg-last-error.php>`_ and `PDO::exec <https://www.php.net/manual/en/pdo.exec.php>`_.


Suggestions
___________

* Throw an exception
* Trigger an error with trigger_error()
* Use your own error mechanism




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OrDie                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-implied-if <https://github.com/dseguy/clearPHP/tree/master/rules/no-implied-if.md>`__                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tine20-structures-ordie`, :ref:`case-openconf-structures-ordie`                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


