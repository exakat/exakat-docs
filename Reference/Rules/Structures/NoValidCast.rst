.. _structures-novalidcast:


.. _no-a-valid-cast:

No A Valid Cast
+++++++++++++++


.. meta::

	:description:

		No A Valid Cast: This cast generates an error, as there is no way to directly convert an object to an int.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: No A Valid Cast

	:twitter:description: No A Valid Cast: This cast generates an error, as there is no way to directly convert an object to an int

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: No A Valid Cast

	:og:type: article

	:og:description: This cast generates an error, as there is no way to directly convert an object to an int

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No A Valid Cast.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoValidCast.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoValidCast.html","name":"No A Valid Cast","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"This cast generates an error, as there is no way to directly convert an object to an int","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No A Valid Cast.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This cast generates an `error <https://www.php.net/error>`_, as there is no way to directly convert an object to an int. 

The `result <https://www.php.net/result>`_ is 1, with a warning. 

This rule applies to float and int. This doesn't apply to string cast, as the magic method `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ allows for such conversions.

.. code-block:: php
   
   <?php
   
   $a = (int) foo();
   
   function foo() : A {} 
   
   ?>
Related PHP errors 
-------------------

  + `Object of class stdClass could not be converted to int <https://php-errors.readthedocs.io/en/latest/messages/object-of-class-%25s-could-not-be-converted-to-int.html>`_
  + `Object of class stdClass could not be converted to float <https://php-errors.readthedocs.io/en/latest/messages/object-of-class-%25s-could-not-be-converted-to-float.html>`_
  + `Object of class stdClass could not be converted to string <https://php-errors.readthedocs.io/en/latest/messages/object-of-class-%25s-could-not-be-converted-to-string.html>`_



Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Create a method that convert the original object to the target type




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoValidCast                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


