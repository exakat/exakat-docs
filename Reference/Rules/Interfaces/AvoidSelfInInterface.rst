.. _interfaces-avoidselfininterface:

.. _avoid-self-in-interface:

Avoid Self In Interface
+++++++++++++++++++++++

.. meta::
	:description:
		Avoid Self In Interface: Self and Parent are tricky when used in an interface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid Self In Interface
	:twitter:description: Avoid Self In Interface: Self and Parent are tricky when used in an interface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid Self In Interface
	:og:type: article
	:og:description: Self and Parent are tricky when used in an interface
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Avoid Self In Interface.html
	:og:locale: en
`Self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ and `Parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ are tricky when used in an interface. 

``self`` refers to the current interface or its extended parents : as long as the constant is defined in the interface family, this is valid.  On the other hand, when ``self`` refers to the current class, the resolution of names would happen at execution time, leading to undefined errors.

``self`` may be used for typing : then, argument types in the host class must use the interface name, and can't use ``self`` nor the class name, for compatibility reason. ``self`` can be used for returntype, as expected.

``parent`` has the same behavior than ``self``, except that it cannot be used inside an interface. This is one of those `error <https://www.php.net/error>`_ that lint but won't execute in certain conditions : namely, when a class implements the interface with `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, but has no `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ by itself. This is now a dependency to the host class.

``static`` can't be used in an interface, as it needs to be resolved at call time.

.. code-block:: php
   
   <?php
   
   interface i extends ii {
       // This 'self' is valid : it refers to the interface i
       public const I = self::I2 + 2;
   
       // This 'self' is also valid, as it refers to interface ii, which is a part of interface i
       public const I2 = self::IP + 4; 
   
       // This makes interface i dependant on the host class
       public const I3 = parent::A;
   
       // This makes interface i dependant on the host class, where X must be defined. 
       // It actually yields an error :  Undefined class constant 'self::I'
       public const I4 = self::X;
   }
   
   class x implements k {
       const X = 1;
   }
   ?>

See also `Scope Resolution Operator (::) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

Related PHP errors 
-------------------

  + `Cannot access parent:: when current class scope has no parent <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-parent%3A%3A-when-current-class-scope-has-no-parent.html>`_
  + `Undefined class constant <https://php-errors.readthedocs.io/en/latest/messages/undefined-class-constant-%22%25s%5C%3A%5C%3A%25s%22.html>`_
  + `"static::" is not allowed in compile-time constants <https://php-errors.readthedocs.io/en/latest/messages/%22static%3A%3A%22+is+not+allowed+in+compile-time+constants.html>`_



Connex PHP features
-------------------

  + `self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_
  + `interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_


Suggestions
___________

* Use a fully qualified namespace instead of self
* Use a locally defined constant, so self is a valid reference




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/AvoidSelfInInterface                                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.4                                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                       |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


