.. _extensions-extposix:

.. _ext-posix:

ext/posix
+++++++++

.. meta\:\:
	:description:
		ext/posix: Extension POSIX.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/posix
	:twitter:description: ext/posix: Extension POSIX
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/posix
	:og:type: article
	:og:description: Extension POSIX
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extposix.html
	:og:locale: en
  Extension POSIX.

Ext/posix contains an interface to those functions defined in the IEEE 1003.1 (POSIX.1) standards document which are not accessible through other means.

.. code-block:: php
   
   <?php
   posix_kill(999459,SIGKILL);
   echo 'Your error returned was '.posix_get_last_error(); //Your error was ___
   ?>

See also `1003.1-2008 - IEEE Standard for Information Technology - Portable Operating System Interface (POSIX(R)) <https://standards.ieee.org/findstds/standard/1003.1-2008.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extposix                                                                                                                                                                     |
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


