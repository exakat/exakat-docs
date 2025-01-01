.. _structures-nodirectusage:

.. _no-direct-usage-of-returned-value:

No Direct Usage Of Returned Value
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Direct Usage Of Returned Value: The results of the following functions shouldn't be used directly, but checked first.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Direct Usage Of Returned Value
	:twitter:description: No Direct Usage Of Returned Value: The results of the following functions shouldn't be used directly, but checked first
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Direct Usage Of Returned Value
	:og:type: article
	:og:description: The results of the following functions shouldn't be used directly, but checked first
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/NoDirectUsage.html
	:og:locale: en
The results of the following functions shouldn't be used directly, but checked first. 

For example, `glob() <https://www.php.net/glob>`_ returns an array, unless an `error <https://www.php.net/error>`_ happens, in which case it returns ``false``. In such case, however rare it is, plugging `glob() <https://www.php.net/glob>`_ directly in a `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops yields errors.

.. code-block:: php
   
   <?php
       // Used without check : 
       foreach(glob('.') as $file) { /* do Something */ }.
       
       // Used without check : 
       $files = glob('.');
       if (!is_array($files)) {
           foreach($files as $file) { /* do Something */ }.
       }
   ?>
Related PHP errors 
-------------------

  + `foreach() argument must be of type array|object, false given  <https://php-errors.readthedocs.io/en/latest/messages/foreach%5C%28%5C%29-argument-must-be-of-type-array%5C%7Cobject.html>`_




Suggestions
___________

* Check the return of the function before using it, in particular for false, or array().




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoDirectUsage                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-edusoho-structures-nodirectusage`, :ref:`case-xoops-structures-nodirectusage`                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


