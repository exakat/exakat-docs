.. _structures-multiplecatch:

.. _multiple-catch-with-try:

Multiple Catch With Try
+++++++++++++++++++++++

.. meta::
	:description:
		Multiple Catch With Try: This rule reports when a try structure have several catch statements.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Catch With Try
	:twitter:description: Multiple Catch With Try: This rule reports when a try structure have several catch statements
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Catch With Try
	:og:type: article
	:og:description: This rule reports when a try structure have several catch statements
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/MultipleCatch.html
	:og:locale: en
This rule reports when a try structure have several catch statements. Usually, try structures have only one catch, so more catch clauses are worth checking.

.. code-block:: php
   
   <?php
   
   // This try has several catch
   try {
       doSomething();
   } catch (RuntimeException $e) {
       processRuntimeException();
   } catch (OtherException $e) {
       processOtherException();
   }
   
   ?>
Connex PHP features
-------------------

  + `try <https://php-dictionary.readthedocs.io/en/latest/dictionary/try.ini.html>`_
  + `catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/catch.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MultipleCatch                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


