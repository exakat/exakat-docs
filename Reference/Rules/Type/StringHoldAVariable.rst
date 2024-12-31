.. _type-stringholdavariable:

.. _string-may-hold-a-variable:

String May Hold A Variable
++++++++++++++++++++++++++

.. meta\:\:
	:description:
		String May Hold A Variable: Strings that contains a variable, yet are not interpolated.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: String May Hold A Variable
	:twitter:description: String May Hold A Variable: Strings that contains a variable, yet are not interpolated
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: String May Hold A Variable
	:og:type: article
	:og:description: Strings that contains a variable, yet are not interpolated
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Type/StringHoldAVariable.html
	:og:locale: en
  Strings that contains a variable, yet are not interpolated. 

Single quotes and Nowdoc syntax may include $ signs. They are treated as literals, and not replaced with a variable value. 

However, there are some potential variables in those strings, making it possible for an `error <https://www.php.net/error>`_ : the variable was forgotten and will be published as such. It is worth checking the content and make sure those strings are not variables.

.. code-block:: php
   
   <?php
   
   $a = 2;
   
   // Explicit variable, but literal effect is needed
   echo '$a is '.$a;
   
   // One of the variable has been forgotten
   echo '$a is $a';
   
   // $CAD is not a variable, rather a currency unit
   $total = 12;
   echo $total.' $CAD';
   
   // $CAD is not a variable, rather a currency unit
   $total = 12;
   
   // Here, $total has been forgotten
   echo <<<'TEXT'
   $total $CAD
   TEXT;
   
   ?>
Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_
  + `interpolation <https://php-dictionary.readthedocs.io/en/latest/dictionary/interpolation.ini.html>`_


Suggestions
___________

* Check if the variable is really a variable
* Turn the string into an interpolated string (double quote, heredoc, concatenation)




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/StringHoldAVariable                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


