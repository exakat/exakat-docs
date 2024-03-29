.. _php-usepathinfoargs:

.. _use-pathinfo()-arguments:

Use pathinfo() Arguments
++++++++++++++++++++++++

  `pathinfo() <https://www.php.net/pathinfo>`_ has a second argument to select only useful data. 

It is twice faster to get only one element from `pathinfo() <https://www.php.net/pathinfo>`_ than get the four of them, and use only one.

This analysis reports `pathinfo() <https://www.php.net/pathinfo>`_ usage, without second argument, where only one or two indices are used, after the call.
Depending on the situation, the functions `dirname() <https://www.php.net/dirname>`_ and `basename() <https://www.php.net/basename>`_ may also be used. They are even faster, when only fetching those data.

.. code-block:: php
   
   <?php
   
   // This could use only PATHINFO_BASENAME
   function foo_db() {
       $a = pathinfo($file2);
       return $a['basename'];
   }
   
   // This could be 2 calls, with PATHINFO_BASENAME and PATHINFO_DIRNAME.
   function foo_de() {
       $a = pathinfo($file3);
       return $a['dirname'].'/'.$a['basename'];
   }
   
   // This is OK : 3 calls to pathinfo() is slower than array access.
   function foo_deb() {
       $a = pathinfo($file4);
       return  $a['dirname'].'/'.$a['filename'].'.'.$a['extension'];
   }
   
   ?>

See also `list <https://www.php.net/manual/en/function.list.php>`_.


Suggestions
___________

* Use PHP native function pathinfo() and its arguments




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UsePathinfoArgs                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Performances <ruleset-Performances>`                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.12                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | path                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zend-config-php-usepathinfoargs`, :ref:`case-thinkphp-php-usepathinfoargs`                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


