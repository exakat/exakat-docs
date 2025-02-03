.. _classes-finalbyocramius:

.. _class-should-be-final-by-ocramius:

Class Should Be Final By Ocramius
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Class Should Be Final By Ocramius: 'Make your classes always final, if they implement an interface, and no other public methods are defined'.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class Should Be Final By Ocramius
	:twitter:description: Class Should Be Final By Ocramius: 'Make your classes always final, if they implement an interface, and no other public methods are defined'
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class Should Be Final By Ocramius
	:og:type: article
	:og:description: 'Make your classes always final, if they implement an interface, and no other public methods are defined'
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Class Should Be Final By Ocramius.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/FinalByOcramius.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/FinalByOcramius.html","name":"Class Should Be Final By Ocramius","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"'Make your classes always final, if they implement an interface, and no other public methods are defined'","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Class Should Be Final By Ocramius.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>'Make your classes always final, if they implement an interface, and no other public methods are defined'.

When a class should be final, as explained by ``Ocramius`` (``Marco Pivetta``).

.. code-block:: php
   
   <?php
   
   interface i1 {
       function i1() ;
   }
   
   // Class should final, as its public methods are in an interface
   class finalClass implements i1 {
       // public interface 
       function i1 () {}
       
       // private method
       private function a1 () {}
   }
   
   ?>

See also `Final classes by default, why? <https://matthiasnoback.nl/2018/09/final-classes-by-default-why/>`_ and `When to declare classes final <http://ocramius.github.io/blog/when-to-declare-classes-final/>`_.

Connex PHP features
-------------------

  + `final <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/FinalByOcramius                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


