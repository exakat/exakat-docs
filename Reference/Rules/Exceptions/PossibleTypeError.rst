.. _exceptions-possibletypeerror:


.. _possible-typeerror:

Possible TypeError
++++++++++++++++++


.. meta::

	:description:

		Possible TypeError: Report possible errors when a string is given to a int or float typed container.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Possible TypeError

	:twitter:description: Possible TypeError: Report possible errors when a string is given to a int or float typed container

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Possible TypeError

	:og:type: article

	:og:description: Report possible errors when a string is given to a int or float typed container

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Possible TypeError.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/PossibleTypeError.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/PossibleTypeError.html","name":"Possible TypeError","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Report possible errors when a string is given to a int or float typed container","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Possible TypeError.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Report possible errors when a string is given to a int or float typed container. 

That `error <https://www.php.net/error>`_ will be emitted when strict_types is active, or if the string cannot be formatted into a float or an int. Otherwise, the code works as intended.



It is recommended to set a try/catch around those expressions, to catch them.

.. code-block:: php
   
   <?php
   
   // This is OK, as the string will be successfully turned into a float
   foo("12.34");
   
   // This is KO, as the string will not bet turned into a float
   foo("12.34a");
   
   function foo(float $price) {
   	intdiv($price, 3);
   }
   
   ?>

See also `TypeError <https://www.php.net/manual/en/class.typeerror.php>`.

Connex PHP features
-------------------

  + `typeerror <https://php-dictionary.readthedocs.io/en/latest/dictionary/typeerror.ini.html>`_


Suggestions
___________

* Add the try expression around the assignation, to catch the error
* Validate the incoming value to ensure it can be converted to the target type
* Cast the value to int or float




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/PossibleTypeError                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
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


