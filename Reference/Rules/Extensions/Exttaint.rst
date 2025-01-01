.. _extensions-exttaint:

Extensions/Exttaint
+++++++++++++++++++

.. meta::
	:description:
		Extensions/Exttaint: Taint is a extension used to detect and track tainted string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Extensions/Exttaint
	:twitter:description: Extensions/Exttaint: Taint is a extension used to detect and track tainted string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Extensions/Exttaint
	:og:type: article
	:og:description: Taint is a extension used to detect and track tainted string
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Exttaint.html
	:og:locale: en
Taint is a extension used to detect and track tainted string. It follows each assignation of the code and keeps track of its taint. And also can be used to spot sql injection vulnerabilities, shell inject, etc.

.. code-block:: php
   
   <?php
   $a = trim($_GET['a']);
   
   $file_name = '/tmp' .  $a;
   $output    = "Welcome, {$a} !!!";
   
   //Warning: main() [function.echo]: Attempt to echo a string that might be tainted
   
   ?>

See also `taint <https://www.php.net/manual/en/book.taint.php>`_ and `taint on github <https://github.com/laruence/taint>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Attempt+to+echo+a+string+that+might+be+tainted.html>`_



Connex PHP features
-------------------

  + `taint <https://php-dictionary.readthedocs.io/en/latest/dictionary/taint.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exttaint                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


