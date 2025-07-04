.. _classes-privatewritingpropertyisfinal:


.. _private-set-visibility-makes-property-final:

Private Set Visibility Makes Property Final
+++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Private Set Visibility Makes Property Final: A property with a ``private(set)`` property is automatically ``final``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Private Set Visibility Makes Property Final
	:twitter:description: Private Set Visibility Makes Property Final: A property with a ``private(set)`` property is automatically ``final``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Private Set Visibility Makes Property Final
	:og:type: article
	:og:description: A property with a ``private(set)`` property is automatically ``final``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Private Set Visibility Makes Property Final.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PrivateWritingPropertyIsFinal.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/PrivateWritingPropertyIsFinal.html","name":"Private Set Visibility Makes Property Final","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"A property with a ``private(set)`` property is automatically ``final``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Private Set Visibility Makes Property Final.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A property with a ``private(set)`` property is automatically ``final``. A child class cannot declare again that property.
Related PHP errors 
-------------------

  + `Cannot override final property %s::$%s <https://php-errors.readthedocs.io/en/latest/messages/cannot-override-final-property-%25s%3A%3A%24%25s.html>`_



Connex PHP features
-------------------

  + `Asymetric Visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/asymmetric-visibility.ini.html>`_
  + `Final Keyword <https://php-dictionary.readthedocs.io/en/latest/dictionary/final.ini.html>`_


Suggestions
___________

* Remove the ``private(set)`` asymmetric visibility.
* Move the ``private(set)`` asymmetric visibility to ``protected(set)``.
* Remove the child class property definition.
* Add the ``final`` keyword to the property declaration in the parent (and adapt the children).




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/PrivateWritingPropertyIsFinal                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.7.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.4 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


