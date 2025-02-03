.. _classes-finalprivate:


.. _final-private-methods:

Final Private Methods
+++++++++++++++++++++

.. meta::
	:description:
		Final Private Methods: PHP's private methods cannot be overwritten, as they are dedicated to the current class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Final Private Methods
	:twitter:description: Final Private Methods: PHP's private methods cannot be overwritten, as they are dedicated to the current class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Final Private Methods
	:og:type: article
	:og:description: PHP's private methods cannot be overwritten, as they are dedicated to the current class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Final Private Methods.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/FinalPrivate.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/FinalPrivate.html","name":"Final Private Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"PHP's private methods cannot be overwritten, as they are dedicated to the current class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Final Private Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP's private methods cannot be overwritten, as they are dedicated to the current class. That way, the ``final`` keyword is useless. 

PHP 8.0 warns when it finds such a method.

.. code-block:: php
   
   <?php
   
   class foo {
       // Final and private both prevent child classes to overwrite the method
       final private function bar() {}
   
       // Final and protected (or public) keep this method available, but not overwritable
       final protected function bar() {}
   }
   
   ?>

See also `Final Keyword <https://www.php.net/manual/en/language.oop5.final.php>`_.

Related PHP errors 
-------------------

  + `Private methods cannot be final as they are never overridden by other classes <https://php-errors.readthedocs.io/en/latest/messages/private-methods-cannot-be-final-as-they-are-never-overridden-by-other-classes.html>`_



Connex PHP features
-------------------

  + `final <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_
  + `private <https://php-dictionary.readthedocs.io/en/latest/dictionary/private.ini.html>`_


Suggestions
___________

* Remove the final keyword
* Relax visibility




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/FinalPrivate                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                                                                                   |
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


