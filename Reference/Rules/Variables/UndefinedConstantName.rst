.. _variables-undefinedconstantname:

.. _undefined-constant-name:

Undefined Constant Name
+++++++++++++++++++++++

.. meta::
	:description:
		Undefined Constant Name: When using the ```` syntax for variable variable, the name used must be a defined constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Constant Name
	:twitter:description: Undefined Constant Name: When using the ```` syntax for variable variable, the name used must be a defined constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Constant Name
	:og:type: article
	:og:description: When using the ```` syntax for variable variable, the name used must be a defined constant
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined Constant Name.html
	:og:locale: en
When using the ```` syntax for variable variable, the name used must be a defined constant. It is not a simple string, like ``'x'``, it is an actual constant name.

Interestingly, it is possible to use a qualified name within the brackets, relative ````, full ```` or partial ````. PHP lints such code, and collects the value of the constant immediately. Since there is no fallback mechanism for fully qualified names, this ends with a Fatal `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   const x = "a";
   $a = "Hello";
   
   // Display 'Hello'  -> $a -> Hello
   echo ${x};
   
   // Yield a PHP Warning 
   // Use of undefined constant y - assumed 'y' (this will throw an Error in a future version of PHP)
   echo ${y};
   
   // Yield a PHP Fatal error as PHP first checks that the constant exists 
   //Undefined constant 'y'
   echo ${a\y};
   
   ?>
Related PHP errors 
-------------------

  + `Undefined constant '%s' <https://php-errors.readthedocs.io/en/latest/messages/undefined-constant-%22%25s.html>`_




Suggestions
___________

* Define the constant
* Turn the dynamic syntax into a normal variable syntax
* Use a fully qualified name (at least one \ ) to turn this syntax into a Fatal error when the constant is not found. This doesn't fix the problem, but may make it more obvious during the diagnostic.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/UndefinedConstantName                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


