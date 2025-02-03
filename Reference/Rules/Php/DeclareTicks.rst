.. _php-declareticks:

.. _ticks-usage:

Ticks Usage
+++++++++++

.. meta::
	:description:
		Ticks Usage: Usage of ``declare()`` with ``ticks``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Ticks Usage
	:twitter:description: Ticks Usage: Usage of ``declare()`` with ``ticks``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Ticks Usage
	:og:type: article
	:og:description: Usage of ``declare()`` with ``ticks``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Ticks Usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DeclareTicks.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/DeclareTicks.html","name":"Ticks Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Usage of ``declare()`` with ``ticks``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Ticks Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Usage of ``declare()`` with ``ticks``. When ticks are declared, a related handler must be registered with `register_tick_function() <https://www.php.net/register_tick_function>`_.

.. code-block:: php
   
   <?php
   
   // Setting ticks value
   declare(ticks = 2);
   
   ?>

See also `declare <https://www.php.net/manual/en/control-structures.declare.php>`_.

Connex PHP features
-------------------

  + `tick <https://php-dictionary.readthedocs.io/en/latest/dictionary/tick.ini.html>`_
  + `declare <https://php-dictionary.readthedocs.io/en/latest/dictionary/declare.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/DeclareTicks                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Preferences <ruleset-Preferences>`                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.1                                                                                                                                                                                  |
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


