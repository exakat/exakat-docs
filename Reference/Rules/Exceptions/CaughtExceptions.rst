.. _exceptions-caughtexceptions:

.. _caught-exceptions:

Caught Exceptions
+++++++++++++++++

.. meta::
	:description:
		Caught Exceptions: This rule collects the exceptions used in catch clause.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Caught Exceptions
	:twitter:description: Caught Exceptions: This rule collects the exceptions used in catch clause
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Caught Exceptions
	:og:type: article
	:og:description: This rule collects the exceptions used in catch clause
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Caught Exceptions.html
	:og:locale: en
This rule collects the exceptions used in catch clause. Those are the caught exceptions. 

Caught exceptions might be thrown from within the code, or from an outside library. 


.. code-block:: php
   
   <?php
   
   try {
       foo();
   } catch (MyException $e) {
       fixException();
   } catch (MyOtherException1|MyOtherException2) {
       fixException();
   } finally {
       clean();
   }
   
   ?>
Connex PHP features
-------------------

  + `catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/catch.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CaughtExceptions                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


