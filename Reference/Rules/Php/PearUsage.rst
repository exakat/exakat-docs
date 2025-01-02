.. _php-pearusage:

.. _pear-usage:

Pear Usage
++++++++++

.. meta::
	:description:
		Pear Usage: Pear Usage : list of Pear packages in use.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Pear Usage
	:twitter:description: Pear Usage: Pear Usage : list of Pear packages in use
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Pear Usage
	:og:type: article
	:og:description: Pear Usage : list of Pear packages in use
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Pear Usage.html
	:og:locale: en
Pear Usage : list of Pear packages in use.

.. code-block:: php
   
   <?php
       require_once('MDB2.php');
       $dsn = 'mysql://user:pass@host';
       $mdb2 = &MDB2::factory($dsn);
       $mdb2->setFetchMode(MDB2_FETCHMODE_ASSOC);
   ?>

See also `PEAR <http://pear.php.net/>`_.

Connex PHP features
-------------------

  + `pear <https://php-dictionary.readthedocs.io/en/latest/dictionary/pear.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/PearUsage                                                                                                                                                                           |
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


