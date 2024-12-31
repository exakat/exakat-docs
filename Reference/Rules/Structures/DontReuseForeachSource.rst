.. _structures-dontreuseforeachsource:

.. _don't-reuse-foreach-source:

Don't Reuse Foreach Source
++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Don't Reuse Foreach Source: It is dangerous to reuse the same variable inside a loop that use it as a source.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Don't Reuse Foreach Source
	:twitter:description: Don't Reuse Foreach Source: It is dangerous to reuse the same variable inside a loop that use it as a source
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Don't Reuse Foreach Source
	:og:type: article
	:og:description: It is dangerous to reuse the same variable inside a loop that use it as a source
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/DontReuseForeachSource.html
	:og:locale: en
  It is dangerous to reuse the same variable inside a loop that use it as a source.

PHP actually takes a copy of the source, so the `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loop is not affected by the modification. 

On the other hand, the source of the loop is modified after the loop (and actually, also during), which may come as a surprise to a later coder.

.. code-block:: php
   
   <?php
   
   $properties = [];
   foreach ($values as $i => $vars) {
   
       // $values is used again here, now as a blind variable
       foreach ($vars as $class => $values) {
           foreach ($values as $name => $v) {
               $properties[$class][$name][$i] = $v;
           }
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_


Suggestions
___________

* Do not reuse the source as another variable
* Use different names to disambiguate their purpose




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DontReuseForeachSource                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.5                                                                                                                   |
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


