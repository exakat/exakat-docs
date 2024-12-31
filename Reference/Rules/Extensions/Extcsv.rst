.. _extensions-extcsv:

.. _ext-csv:

ext/CSV
+++++++

.. meta\:\:
	:description:
		ext/CSV: A small PHP extension to add/improve the handling of CSV strings.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/CSV
	:twitter:description: ext/CSV: A small PHP extension to add/improve the handling of CSV strings
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/CSV
	:og:type: article
	:og:description: A small PHP extension to add/improve the handling of CSV strings
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extcsv.html
	:og:locale: en
  A small PHP extension to add/improve the handling of CSV strings.

.. code-block:: php
   
   <?php
   $fields = [
       'Hello',
       'World',
   ];
   
   $output = "Hello,World";
   
   var_dump($output === CSV::arrayToRow($fields));
   var_dump(CSV::rowToArray($output));
   ?>

See also `PHP csv extension <https://gitlab.com/Girgias/csv-php-extension>`_.

Connex PHP features
-------------------

  + `csv <https://php-dictionary.readthedocs.io/en/latest/dictionary/csv.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extcsv                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
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


