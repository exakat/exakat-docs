.. _structures-dropelseafterreturn:

.. _drop-else-after-return:

Drop Else After Return
++++++++++++++++++++++

.. meta::
	:description:
		Drop Else After Return: Avoid else clause when the then clause returns, but not the else.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Drop Else After Return
	:twitter:description: Drop Else After Return: Avoid else clause when the then clause returns, but not the else
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Drop Else After Return
	:og:type: article
	:og:description: Avoid else clause when the then clause returns, but not the else
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/DropElseAfterReturn.html
	:og:locale: en
Avoid else clause when the then clause returns, but not the else. And vice-versa.

This way, the else block disappears, and is now the main sequence of the function. 

This is also true if else has a return, and then not. When doing so, don't forget to reverse the condition.

.. code-block:: php
   
   <?php
   
   // drop the else
   if ($a) {
       return $a;
   } else {
       doSomething();
   }
   
   // drop the then
   if ($b) {
       doSomething();
   } else {
       return $a;
   }
   
   // return in else and then
   if ($a3) {
       return $a;
   } else {
       $b = doSomething();
       return $b;
   }
   
   ?>
Connex PHP features
-------------------

  + `return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_


Suggestions
___________

* Remove the else clause and move its code to the main part of the method




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DropElseAfterReturn                                                                                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.6                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


