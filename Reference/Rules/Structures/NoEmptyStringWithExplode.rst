.. _structures-noemptystringwithexplode:

.. _no-empty-string-with-explode():

No Empty String With explode()
++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Empty String With explode(): explode() doesn't allow empty strings as separator.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Empty String With explode()
	:twitter:description: No Empty String With explode(): explode() doesn't allow empty strings as separator
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Empty String With explode()
	:og:type: article
	:og:description: explode() doesn't allow empty strings as separator
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Empty String With explode().html
	:og:locale: en
`explode() <https://www.php.net/explode>`_ doesn't allow empty strings as separator. Until PHP 8.0, it would make a warning, and return false. After that version, it raises a `ValueError <https://www.php.net/valueerror>`_.

To `break <https://www.php.net/manual/en/control-structures.break.php>`_ a string into individual characters, it is possible to use the array notation on strings, or to use the `str_split() <https://www.php.net/str_split>`_ function.

.. code-block:: php
   
   <?php
   
   explode('', "a");
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Empty+delimiter.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/explode%28%29%3A+Argument+%231+%28%24separator%29+cannot+be+empty.html>`_




Suggestions
___________

* Check for empty strings (or equivalent) before using explode()
* Use the array notation to access individual chars
* Use str_split() to break the string into an array




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/NoEmptyStringWithExplode                                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.5.2                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0                                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                    |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


