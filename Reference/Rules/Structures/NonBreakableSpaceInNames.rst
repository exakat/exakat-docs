.. _structures-nonbreakablespaceinnames:


.. _non-breakable-space-in-names:

Non Breakable Space In Names
++++++++++++++++++++++++++++


.. meta::

	:description:

		Non Breakable Space In Names: PHP allows non-breakable spaces in structures names, such as class, interfaces, traits, and variables.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Non Breakable Space In Names

	:twitter:description: Non Breakable Space In Names: PHP allows non-breakable spaces in structures names, such as class, interfaces, traits, and variables

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Non Breakable Space In Names

	:og:type: article

	:og:description: PHP allows non-breakable spaces in structures names, such as class, interfaces, traits, and variables

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Non Breakable Space In Names.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NonBreakableSpaceInNames.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NonBreakableSpaceInNames.html","name":"Non Breakable Space In Names","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP allows non-breakable spaces in structures names, such as class, interfaces, traits, and variables","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Non Breakable Space In Names.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP allows non-breakable spaces in structures names, such as class, interfaces, traits, and variables.

This may be a nice trick to make names more readable outside code context, like long-named methods for tests. 
Original post by ``Matthieu Napoli``.
.

.. code-block:: php
   
   <?php
   
   class class with non breakable spaces {}
   
   class ClassWithoutNonBreakableSpaces {}
   
   ?>

See also `Using non-breakable spaces in test method names <http://mnapoli.fr/using-non-breakable-spaces-in-test-method-names/>`_ and `PHP Variable Names <http://schappo.blogspot.nl/2015/06/php-variable-names.html>`_.

Connex PHP features
-------------------

  + `non-breakable-space <https://php-dictionary.readthedocs.io/en/latest/dictionary/non-breakable-space.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NonBreakableSpaceInNames                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.0                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


