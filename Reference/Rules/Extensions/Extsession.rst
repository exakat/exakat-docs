.. _extensions-extsession:

.. _ext-session:

ext/session
+++++++++++

.. meta\:\:
	:description:
		ext/session: Extension ext/session.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/session
	:twitter:description: ext/session: Extension ext/session
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/session
	:og:type: article
	:og:description: Extension ext/session
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extsession.html
	:og:locale: en
  Extension ext/session.

Session support in PHP consists of a way to preserve certain data across subsequent accesses.

.. code-block:: php
   
   <?php
   session_start();
   if (!isset($_SESSION['count'])) {
     $_SESSION['count'] = 0;
   } else {
     $_SESSION['count']++;
   }
   ?>

See also `Session <https://www.php.net/manual/en/book.session.php>`_.

Connex PHP features
-------------------

  + `session <https://php-dictionary.readthedocs.io/en/latest/dictionary/session.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsession                                                                                                                                                                   |
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


