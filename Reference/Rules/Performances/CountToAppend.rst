.. _performances-counttoappend:

.. _count()-to-array-append:

Count() To Array Append
+++++++++++++++++++++++

  The array append operator is able to generate a sane index, without relying on the `count() <https://www.php.net/count>`_ function. This is faster, and safer.

.. code-block:: php
   
   <?php
   
   $newArray  = [];
   foreach($array as $value) {
   	// count is overkill here
   	$newArray[count($newArray)] = $value;
   }
   
   ?>
Connex PHP features
-------------------

  + `append <https://php-dictionary.readthedocs.io/en/latest/dictionary/append.ini.html>`_


Suggestions
___________

* Remove the call to count()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/CountToAppend                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


