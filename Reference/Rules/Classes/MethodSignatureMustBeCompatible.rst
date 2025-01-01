.. _classes-methodsignaturemustbecompatible:

.. _method-signature-must-be-compatible:

Method Signature Must Be Compatible
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Method Signature Must Be Compatible: Make sure methods signature are compatible.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Method Signature Must Be Compatible
	:twitter:description: Method Signature Must Be Compatible: Make sure methods signature are compatible
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Method Signature Must Be Compatible
	:og:type: article
	:og:description: Make sure methods signature are compatible
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/MethodSignatureMustBeCompatible.html
	:og:locale: en
Make sure methods signature are compatible.

PHP generates the infamous Fatal `error <https://www.php.net/error>`_ at execution : ``Declaration of FooParent\:\:Bar() must be compatible with FooChildren\:\:Bar()``

.. code-block:: php
   
   <?php
   
   class x {
       function xa() {}
   }
   
   class xxx extends xx {
       function xa($a) {}
   }
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Declaration+of+FooParent%3A%3ABar%28%29+must+be+compatible+with+FooChildren%3A%3ABar%28%29.html>`_



Connex PHP features
-------------------

  + `typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/typehint.ini.html>`_
  + `type-covariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-covariance.ini.html>`_
  + `type-contravariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-contravariance.ini.html>`_


Suggestions
___________

* Fix the child class method() signature.
* Fix the parent class method() signature, after checking that it won't affect the other children.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MethodSignatureMustBeCompatible                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.2.9                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


