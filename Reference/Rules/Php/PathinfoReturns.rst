.. _php-pathinforeturns:

.. _pathinfo()-returns-may-vary:

Pathinfo() Returns May Vary
+++++++++++++++++++++++++++

  `pathinfo() <https://www.php.net/pathinfo>`_ function returns an array whose content may vary. It is recommended to collect the values after check, rather than directly.
The same applies to `parse_url() <https://www.php.net/parse_url>`_, which returns an array with various index.

.. code-block:: php
   
   <?php
   
   $file = '/a/b/.c';
   //$extension may be missing, leading to empty $filename and filename in $extension
   list( $dirname, $basename, $extension, $filename ) = array_values( pathinfo($file) );
   
   //Use PHP 7.1 list() syntax to assign correctly the values, and skip array_values()
   //This emits a warning in case of missing index
   ['dirname'   => $dirname, 
    'basename'  => $basename, 
    'extension' => $extension, 
    'filename'  => $filename ] = pathinfo($file);
    
   //This works without warning
   $details = pathinfo($file);
   $dirname   = $details['dirname'] ?? getpwd();
   $basename  = $details['basename'] ?? '';
   $extension = $details['extension'] ?? '';
   $filename  = $details['filename'] ?? '';
   
   ?>
Connex PHP features
-------------------

  + `path <https://php-dictionary.readthedocs.io/en/latest/dictionary/path.ini.html>`_


Suggestions
___________

* Add a check on the return value of pathinfo() before using it.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/PathinfoReturns                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.11                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-nextcloud-php-pathinforeturns`                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


