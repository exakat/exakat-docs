.. _php-nocasttoint:


.. _do-not-cast-to-int:

Do Not Cast To Int
++++++++++++++++++


.. meta::

	:description:

		Do Not Cast To Int: Do not cast floats values to int.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Do Not Cast To Int

	:twitter:description: Do Not Cast To Int: Do not cast floats values to int

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Do Not Cast To Int

	:og:type: article

	:og:description: Do not cast floats values to int

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Do Not Cast To Int.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoCastToInt.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/NoCastToInt.html","name":"Do Not Cast To Int","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Do not cast floats values to int","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Do Not Cast To Int.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Do not cast floats values to int. Uses conversion functions like `intval() <https://www.php.net/intval>`_, `round() <https://www.php.net/round>`_, `floor() <https://www.php.net/floor>`_ or `ceil() <https://www.php.net/ceil>`_ to convert the value to integer, with known behavior. 

Use functions like `floor() <https://www.php.net/floor>`_, `round() <https://www.php.net/round>`_ or `ceil() <https://www.php.net/ceil>`_ : they use an explicit method for rounding, that helps keeping the side effects under control.

.. code-block:: php
   
   <?php
   
       // echoes 7!
       echo (int) ( (0.1 + 0.7) * 10 ); 
   
   ?>

See also `Integers <https://www.php.net/manual/en/language.types.integer.php>`_.

Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_
  + `integer <https://php-dictionary.readthedocs.io/en/latest/dictionary/integer.ini.html>`_
  + `float <https://php-dictionary.readthedocs.io/en/latest/dictionary/float.ini.html>`_


Suggestions
___________

* Upgrade PHP version to 8.0, as those behavior are now the same
* Use one of the dedicated function : intval(), round(), floor() or ceil()




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NoCastToInt                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.6                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


