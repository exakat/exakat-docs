.. _namespaces-couldusemagicconstant:

.. _could-use-namespace-magic-constant:

Could Use Namespace Magic Constant
++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Could Use Namespace Magic Constant: Use the __NAMESPACE__ magic constant, instead of hardcoding the current namespace.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Namespace Magic Constant
	:twitter:description: Could Use Namespace Magic Constant: Use the __NAMESPACE__ magic constant, instead of hardcoding the current namespace
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Namespace Magic Constant
	:og:type: article
	:og:description: Use the __NAMESPACE__ magic constant, instead of hardcoding the current namespace
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Namespaces/CouldUseMagicConstant.html
	:og:locale: en
  Use the `__NAMESPACE__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ magic constant, instead of hardcoding the current namespace. That way, the namespace is easier to read, and it will change with the namespace expression.

.. code-block:: php
   
   <?php
   
   namespace A\B\C {
   	class D {}
   	$className = 'D';
   
   	// hardcoded namespace, needed to instantiate dynamically the class
   	// Don't forget the extra \ 
   print	$fullclassName = '\'.__NAMESPACE__.'\'.$className;
   	$object = new $fullclassName;
   	
   	
   	// hardcoded namespace, needed to instantiate dynamically the class
   	$path = "\A\B\C"; 
   	$fullclassName = $path.$className;
   	$object = new $fullclassName;
   
   }
   ?>
Connex PHP features
-------------------

  + `magic-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-constant.ini.html>`_


Suggestions
___________

* Replace the hardcoded namespace with the __NAMESPACE__ constant, and extra separators.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/CouldUseMagicConstant                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


