.. _php-returnwithparenthesis:


.. _return-with-parenthesis:

Return With Parenthesis
+++++++++++++++++++++++

.. meta::
	:description:
		Return With Parenthesis: return statement doesn't require parenthesis.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Return With Parenthesis
	:twitter:description: Return With Parenthesis: return statement doesn't require parenthesis
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Return With Parenthesis
	:og:type: article
	:og:description: return statement doesn't require parenthesis
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Return With Parenthesis.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ReturnWithParenthesis.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ReturnWithParenthesis.html","name":"Return With Parenthesis","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"return statement doesn't require parenthesis","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Return With Parenthesis.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

return statement doesn't require parenthesis. PHP tolerates them with return statement, but it is recommended not to use them. 

From the PHP Manual : 'Note: Note that since return is a language construct and not a function, the parentheses surrounding its argument are not required and their use is discouraged.'.

.. code-block:: php
   
   <?php
   
   function foo() {
       $a = rand(0, 10);
   
       // No need for parenthesis
       return $a;
   
       // Parenthesis are useless here
       return ($a);
   
       // Parenthesis are useful here: they are needed by the multplication.
       return ($a + 1) * 3;
   }
   
   ?>

See also `PHP return(value); vs return value; <https://stackoverflow.com/questions/2921843/php-returnvalue-vs-return-value>`_ and `return <https://www.php.net/manual/en/function.return.php>`_.

Connex PHP features
-------------------

  + `Return Value <https://php-dictionary.readthedocs.io/en/latest/dictionary/return-value.ini.html>`_


Suggestions
___________

* Remove the parenthesis




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ReturnWithParenthesis                                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


