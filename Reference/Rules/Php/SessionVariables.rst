.. _php-sessionvariables:

.. _session-variables:

Session Variables
+++++++++++++++++

.. meta::
	:description:
		Session Variables: Sessions names, used across the application.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Session Variables
	:twitter:description: Session Variables: Sessions names, used across the application
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Session Variables
	:og:type: article
	:og:description: Sessions names, used across the application
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Session Variables.html
	:og:locale: en
Sessions names, used across the application.

.. code-block:: php
   
   <?php
   
   if (isset($_SESSION['mySessionVariable'])) {
       $_SESSION['mySessionVariable']['counter']++;
   } else {
       $_SESSION['mySessionVariable'] = array('counter'  => 1, 
                                              'creation' => time());
   }
   
   ?>

See also `Sessions <https://www.php.net/manual/en/book.session.php>`_.

Connex PHP features
-------------------

  + `session <https://php-dictionary.readthedocs.io/en/latest/dictionary/session.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/SessionVariables                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.16                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


