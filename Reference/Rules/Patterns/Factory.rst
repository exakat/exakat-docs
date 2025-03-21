.. _patterns-factory:


.. _an-oop-factory:

An OOP Factory
++++++++++++++

.. meta::
	:description:
		An OOP Factory: A method or function that implements a factory.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: An OOP Factory
	:twitter:description: An OOP Factory: A method or function that implements a factory
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: An OOP Factory
	:og:type: article
	:og:description: A method or function that implements a factory
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/An OOP Factory.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Patterns\/Factory.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Patterns\/Factory.html","name":"An OOP Factory","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A method or function that implements a factory","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/An OOP Factory.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A method or function that implements a factory. A factory is a class that handles the creation of an object, based on parameters. The factory hides the logic that leads to the creation of the object.

.. code-block:: php
   
   <?php
       class AutomobileFactory {
           public static function create($make, $model) {
               $className = "\Automaker\Brand$make";
               return new $className($model);
           }
       }
       
       // The factory is able to build any car, based on their 
       $fuego = AutomobileFactory::create('Renault', 'Fuego');
       
       print_r($fuego->getMakeAndModel()); // outputs "Renault Fuego" 
   ?>

See also `Factory (object-oriented programming) <https://en.wikipedia.org/wiki/Factory_(object-oriented_programming)>`_ and `Factory <https://phptherightway.com/pages/Design-Patterns.html#factory>`_.

Connex PHP features
-------------------

  + `Design Pattern <https://php-dictionary.readthedocs.io/en/latest/dictionary/pattern.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Patterns/Factory                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


