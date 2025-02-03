.. _classes-cantoverwritefinalmethod:

.. _can't-overwrite-final-method:

Can't Overwrite Final Method
++++++++++++++++++++++++++++

.. meta::
	:description:
		Can't Overwrite Final Method: A final method is a method that cannot be overwritten in a child class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Can't Overwrite Final Method
	:twitter:description: Can't Overwrite Final Method: A final method is a method that cannot be overwritten in a child class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Can't Overwrite Final Method
	:og:type: article
	:og:description: A final method is a method that cannot be overwritten in a child class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Can't Overwrite Final Method.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CantOverwriteFinalMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CantOverwriteFinalMethod.html","name":"Can't Overwrite Final Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"A final method is a method that cannot be overwritten in a child class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Can't Overwrite Final Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>A final method is a method that cannot be overwritten in a child class. This means that no class below the current class may define a method with the same name.

.. code-block:: php
   
   <?php
   
   class y extends x { 
       function method() {}
   }
   
   class x { 
       final function method() {}
   }
   
   ?>
Related PHP errors 
-------------------

  + `Cannot override final method %s::%s() <https://php-errors.readthedocs.io/en/latest/messages/cannot-override-final-%25s%3A%3A%25s%28%29-with-%25s%3A%3A%25s%28%29.html>`_



Connex PHP features
-------------------

  + `final <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_
  + `overwrite <https://php-dictionary.readthedocs.io/en/latest/dictionary/overwrite.ini.html>`_


Suggestions
___________

* Remove the final keyword in the parent class
* Remove the method in the child class
* Rename the method in the child class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CantOverwriteFinalMethod                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


