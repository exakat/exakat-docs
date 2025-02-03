.. _php-pregmatchallflag:


.. _preg\_match\_all()-flag:

preg_match_all() Flag
+++++++++++++++++++++


.. meta::

	:description:

		preg_match_all() Flag: preg_match_all() has an option to configure the structure of the results : it is either by capturing parenthesis (by default), or by result sets.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: preg_match_all() Flag

	:twitter:description: preg_match_all() Flag: preg_match_all() has an option to configure the structure of the results : it is either by capturing parenthesis (by default), or by result sets

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: preg_match_all() Flag

	:og:type: article

	:og:description: preg_match_all() has an option to configure the structure of the results : it is either by capturing parenthesis (by default), or by result sets

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/preg_match_all() Flag.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PregMatchAllFlag.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PregMatchAllFlag.html","name":"preg_match_all() Flag","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"preg_match_all() has an option to configure the structure of the results : it is either by capturing parenthesis (by default), or by result sets","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/preg_match_all() Flag.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`preg_match_all() <https://www.php.net/preg_match_all>`_ has an option to configure the structure of the results : it is either by capturing parenthesis (by default), or by `result <https://www.php.net/result>`_ sets. 

The second option is the most interesting when the following `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loop has to manipulate several captured strings at the same time. No need to use an index in the first array and use it in the other arrays.
The second syntax is easier to read and may be marginally faster to execute (`preg_match_all() <https://www.php.net/preg_match_all>`_ and `foreach()) <https://www.php.net/manual/en/control-structures.foreach.php>`_.

.. code-block:: php
   
   <?php
   $string = 'ababab';
   
   // default behavior
   preg_match_all('/(a)(b)/', $string, $r);
   $found = '';
   foreach($r[1] as $id => $s) {
       $found .= $s.$r[2][$id];
   }
   
   // better behavior
   preg_match_all('/(a)(b)/', $string, $r, PREG_SET_ORDER);
   $found = '';
   foreach($r as $s) {
       $found .= $s[1].$s[2];
   }
   
   ?>
Connex PHP features
-------------------

  + `regex <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_
  + `flag <https://php-dictionary.readthedocs.io/en/latest/dictionary/flag.ini.html>`_


Suggestions
___________

* Use flags to adapt the results of preg_match_all() to your code, not the contrary.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/PregMatchAllFlag                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-fuelcms-php-pregmatchallflag`                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


