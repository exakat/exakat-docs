.. _typehints-couldbecallable:

.. _could-be-callable:

Could Be Callable
+++++++++++++++++

.. meta::
	:description:
		Could Be Callable: Mark arguments and return types that can be set to ``callable``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Callable
	:twitter:description: Could Be Callable: Mark arguments and return types that can be set to ``callable``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Callable
	:og:type: article
	:og:description: Mark arguments and return types that can be set to ``callable``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Callable.html
	:og:locale: en
Mark arguments and return types that can be set to ``callable``.

The analysis also reports properties that could be 'callable', although PHP doesn't allow that configuration.
Note that properties cannot be callable. It reports a compilation `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // Accept a callable as input 
   function foo($b) {
       // Returns value as return
       return $b();
   }
   
   ?>

See also `Callbacks / callables <https://www.php.net/manual/en/language.types.callable.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Property+x%3A%3A%24x+cannot+have+type+callable.html>`_



Connex PHP features
-------------------

  + `callback <https://php-dictionary.readthedocs.io/en/latest/dictionary/callback.ini.html>`_
  + `callable <https://php-dictionary.readthedocs.io/en/latest/dictionary/callable.ini.html>`_


Suggestions
___________

* Add `callable` typehint to arguments or returntypes.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeCallable                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


