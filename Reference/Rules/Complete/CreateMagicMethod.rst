.. _complete-createmagicmethod:


.. _create-magic-method:

Create Magic Method
+++++++++++++++++++


.. meta::

	:description:

		Create Magic Method: This command creates a link DEFINITION between a ``__call()`` and ``__callStatic()`` calls, and its equivalent magic method.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Create Magic Method

	:twitter:description: Create Magic Method: This command creates a link DEFINITION between a ``__call()`` and ``__callStatic()`` calls, and its equivalent magic method

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Create Magic Method

	:og:type: article

	:og:description: This command creates a link DEFINITION between a ``__call()`` and ``__callStatic()`` calls, and its equivalent magic method

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Create Magic Method.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateMagicMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/CreateMagicMethod.html","name":"Create Magic Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This command creates a link DEFINITION between a ``__call()`` and ``__callStatic()`` calls, and its equivalent magic method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Create Magic Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This command creates a link DEFINITION between a ``__call()`` and ``__callStatic()`` calls, and its equivalent magic method.
This command may not detect all possible link for the ``__get()`` and ``__set()`` call. It may be missing information about the nature of the object. ``Self``, ``static``, ``parent`` and simple variables are detected.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           // This is linked to __call
           $this->c();
           
           // This is linked to __callStatic
           return $this::C();
       }
       
       function __call($name, $args) {
           // Normal method call
       }
   
       function __callStatic($name, $args) {
           // Static method call
       }
   }
   
   ?>

See also `Magic Methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.

Connex PHP features
-------------------

  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/CreateMagicMethod                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.6                                                                                                                   |
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


