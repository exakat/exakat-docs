.. _dump-collectblocksize:

.. _collect-block-size:

Collect Block Size
++++++++++++++++++

  Collect block size for instructions such as for, foreach, while, do...while, ifthen.

This is a starting point for reviewing large blocks of code and extract methods.

.. code-block:: php
   
   <?php
   
   foreach($array as $key => $value) {
   	// This is a one line block for the foreach
   	doSomething();
   }
   
   if($a === $b) {
   	$a++;
   	// This is a two lines block for the ifthen
   	doSomething($a, $b);
   }
   
   ?>
Connex PHP features
-------------------

  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_
  + `ifthen <https://php-dictionary.readthedocs.io/en/latest/dictionary/ifthen.ini.html>`_
  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `while <https://php-dictionary.readthedocs.io/en/latest/dictionary/while.ini.html>`_
  + `dowhile <https://php-dictionary.readthedocs.io/en/latest/dictionary/dowhile.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectBlockSize                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


