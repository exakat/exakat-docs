.. _security-parseurlwithoutparameters:

.. _parse\_str()-warning:

parse_str() Warning
+++++++++++++++++++

.. meta\:\:
	:description:
		parse_str() Warning: The parse_str() function parses a query string and assigns the resulting variables to the local scope.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: parse_str() Warning
	:twitter:description: parse_str() Warning: The parse_str() function parses a query string and assigns the resulting variables to the local scope
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: parse_str() Warning
	:og:type: article
	:og:description: The parse_str() function parses a query string and assigns the resulting variables to the local scope
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Security/parseUrlWithoutParameters.html
	:og:locale: en
  The `parse_str() <https://www.php.net/parse_str>`_ function parses a query string and assigns the resulting variables to the local scope. This may create a unexpected number of variables, and even overwrite the existing one.
Always use an empty variable a second parameter to `parse_str() <https://www.php.net/parse_str>`_, so as to collect the incoming values, and then, filter them in that array.

.. code-block:: php
   
   <?php
     function foo( ) {
       global $a;
       
       echo $a;
     }
   
     parse_str('a=1'); // No second parameter
     foo( );
     // displays 1
   ?>

See also `parse_url() <https://www.php.net/manual/en/function.parse-url.php>`_ and `PHP SSRF Techniques <https://medium.com/secjuice/php-ssrf-techniques-9d422cb28d51>`_.

Connex PHP features
-------------------

  + `query-string <https://php-dictionary.readthedocs.io/en/latest/dictionary/query-string.ini.html>`_


Suggestions
___________

* Use the second parameter when calling parse_url();
* Change to PHP 8.0 version, which made the second argument compulsory




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/parseUrlWithoutParameters                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `know-your-variables <https://github.com/dseguy/clearPHP/tree/master/rules/know-your-variables.md>`__                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


