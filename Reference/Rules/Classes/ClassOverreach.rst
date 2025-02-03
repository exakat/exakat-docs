.. _classes-classoverreach:


.. _class-overreach:

Class Overreach
+++++++++++++++

.. meta::
	:description:
		Class Overreach: An object of class A may reach any private or protected properties, constants or methods in another object of the same class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class Overreach
	:twitter:description: Class Overreach: An object of class A may reach any private or protected properties, constants or methods in another object of the same class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class Overreach
	:og:type: article
	:og:description: An object of class A may reach any private or protected properties, constants or methods in another object of the same class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Class Overreach.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ClassOverreach.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ClassOverreach.html","name":"Class Overreach","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"An object of class A may reach any private or protected properties, constants or methods in another object of the same class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Class Overreach.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

An object of class A may reach any private or protected properties, constants or methods in another object of the same class. This is a PHP feature, though seldom known.

This feature is also called class invasion.

.. code-block:: php
   
   <?php
   
   class A {
       private $p = 1;
       
       public function foo(A $a) {
           return $a->p + 1;
       }
   }
   
   echo (new A)->foo(new A);
   
   ?>

See also `Visibility from other objects <https://www.php.net/manual/en/language.oop5.visibility.php#language.oop5.visibility-other-objects>`_ and `spatie/invade <https://github.com/spatie/invade>`_.

Connex PHP features
-------------------

  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_
  + `class-invasion <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-invasion.ini.html>`_


Suggestions
___________

* Use a getter to reach inside the other object private properties




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ClassOverreach                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


