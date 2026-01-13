.. _structures-arraymappassesbyvalue:

.. _array\_map()-passes-by-value:

Array_Map() Passes By Value
+++++++++++++++++++++++++++

  `array_map() <https://www.php.net/array_map>`_ requires the callback to receive elements by value. Unlike `array_walk() <https://www.php.net/array_walk>`_, which accepts by value or by reference, depending on the action taken.

PHP 8.0 and more recent emits a Warning

.. code-block:: php
   
   <?php
   // Example, courtery of Juliette Reinders Folmer
   function trimNewlines(&$line, $key) {
       $line = str_replace(array("\n", "\r" ), '', $line);
   }
   
   $original = [
       "text\n\n",
       "text\n\r" 
   ];
   
   $array = $original;
   array_walk($array, 'trimNewlines');
   
   var_dump($array);
   
   array_map('trimNewlines', $original, [0, 1]);
   
   ?>

See also `array_map <https://www.php.net/array_map>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Argument+%231+%28%24line%29+must+be+passed+by+reference.html>`_



Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `map <https://php-dictionary.readthedocs.io/en/latest/dictionary/map.ini.html>`_
  + `by-value <https://php-dictionary.readthedocs.io/en/latest/dictionary/by-value.ini.html>`_
  + `by-reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/by-reference.ini.html>`_


Suggestions
___________

* Make the callback first argument a reference




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ArrayMapPassesByValue                                                                                                                                                               |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


