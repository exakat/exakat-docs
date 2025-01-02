.. _functions-semantictyping:

.. _semantic-typing:

Semantic Typing
+++++++++++++++

.. meta::
	:description:
		Semantic Typing: Arguments names are only useful inside the method's body.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Semantic Typing
	:twitter:description: Semantic Typing: Arguments names are only useful inside the method's body
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Semantic Typing
	:og:type: article
	:og:description: Arguments names are only useful inside the method's body
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Semantic Typing.html
	:og:locale: en
Arguments names are only useful inside the method's body. They are not actual type.

.. code-block:: php
   
   <?php
   
   // arguments should be a string and an array
   function foo($array, $str) {
       // more code
       return $boolean;
   }
   
   // typehint is actually checking the values
   function bar(iterable $closure) : bool {
       // more code
       return true;
   }
   
   ?>
Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_


Suggestions
___________

* Use a typehint to make sure the argument is of the expected type.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/SemanticTyping                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.5                                                                                                                   |
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


