.. _patterns-gettersetter:


.. _getter-and-setter:

Getter And Setter
+++++++++++++++++


.. meta::

	:description:

		Getter And Setter: A getter is a method whose purpose is to read the internal value of a class.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Getter And Setter

	:twitter:description: Getter And Setter: A getter is a method whose purpose is to read the internal value of a class

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Getter And Setter

	:og:type: article

	:og:description: A getter is a method whose purpose is to read the internal value of a class

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Getter And Setter.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Patterns\/GetterSetter.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Patterns\/GetterSetter.html","name":"Getter And Setter","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A getter is a method whose purpose is to read the internal value of a class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Getter And Setter.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A getter is a method whose purpose is to read the internal value of a class; a setter is a method whose purpose is to write a value inside a class. 

Exakat marks simple setters and getters : their content only writes (resp. reads) on property at a time. More refined getters/setters might appear in the future, when formatting and filter is detected and omitted.

.. code-block:: php
   
   <?php
   
   class x {
       private $p = 1;
       
       // getter
       function getP() {
           return $this->p;
       }
   
       // setter
       function setP($a) {
           $this->p = $a;
       }
   }
   
   ?>

See also `PHP: Getters and Setters <https://thisinterestsme.com/php-getters-and-setters/>`_.

Connex PHP features
-------------------

  + `getter <https://php-dictionary.readthedocs.io/en/latest/dictionary/getter.ini.html>`_
  + `setter <https://php-dictionary.readthedocs.io/en/latest/dictionary/setter.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Patterns/GetterSetter                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


