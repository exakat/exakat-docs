.. _structures-useurlqueryfunctions:

.. _should-use-url-query-functions:

Should Use Url Query Functions
++++++++++++++++++++++++++++++

  PHP features several functions dedicated to processing URL's query string. 

+ `parse_str() <https://www.php.net/parse_str>`_
+ `parse_url() <https://www.php.net/parse_url>`_
+ `http_build_query() <https://www.php.net/http_build_query>`_

Those functions include extra checks : for example, `http_build_query() <https://www.php.net/http_build_query>`_ adds `urlencode() <https://www.php.net/urlencode>`_ call on the values, and allow for choosing the separator and the Query string format.

.. code-block:: php
   
   <?php
   $data = array(
       'foo' => 'bar',
       'baz' => 'boom',
       'cow' => 'milk',
       'php' => 'hypertext processor'
   );
   
   // safe and efficient way to build a query string
   echo http_build_query($data, '', '&') . PHP_EOL;
   
   // slow way to produce a query string
   foreach($data as $name => &$value) {
       $value = $name.'='.$value;
   }
   echo implode('&', $data) . PHP_EOL;
   
   ?>
Connex PHP features
-------------------

  + `url <https://php-dictionary.readthedocs.io/en/latest/dictionary/url.ini.html>`_


Suggestions
___________

* Use the URL query functions from PHP




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseUrlQueryFunctions                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.7                                                                                                                   |
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


