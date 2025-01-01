.. _structures-invalidregex:

.. _invalid-regex:

Invalid Regex
+++++++++++++

.. meta::
	:description:
		Invalid Regex: The PCRE regex doesn't compile.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Invalid Regex
	:twitter:description: Invalid Regex: The PCRE regex doesn't compile
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Invalid Regex
	:og:type: article
	:og:description: The PCRE regex doesn't compile
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/InvalidRegex.html
	:og:locale: en
The PCRE regex doesn't compile. It isn't a valid regex.

Several reasons may lead to this situation : syntax `error <https://www.php.net/error>`_, Unknown modifier, missing parenthesis or reference.



Regex are check with the Exakat version of PHP. 

Dynamic regex are only checked for simple values. Dynamic values may eventually generate a compilation `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // valid regex
   preg_match('/[abc]/', $string);
   
   // invalid regex (missing terminating ] for character class 
   preg_match('/[abc/', $string);
   
   ?>

Suggestions
___________

* Fix the regex before running it




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InvalidRegex                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-sugarcrm-structures-invalidregex`                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


