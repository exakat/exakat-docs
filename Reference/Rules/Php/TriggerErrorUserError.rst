.. _php-triggererrorusererror:


.. _trigger\_error()-with-user\_error:

trigger_error() With USER_ERROR
+++++++++++++++++++++++++++++++

.. meta::
	:description:
		trigger_error() With USER_ERROR: This rule report usage of trigger_error() with USER_ERROR constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: trigger_error() With USER_ERROR
	:twitter:description: trigger_error() With USER_ERROR: This rule report usage of trigger_error() with USER_ERROR constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: trigger_error() With USER_ERROR
	:og:type: article
	:og:description: This rule report usage of trigger_error() with USER_ERROR constant
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/trigger_error() With USER_ERROR.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/TriggerErrorUserError.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/TriggerErrorUserError.html","name":"trigger_error() With USER_ERROR","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:12:06 +0000","dateModified":"Wed, 05 Mar 2025 15:12:06 +0000","description":"This rule report usage of trigger_error() with USER_ERROR constant","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/trigger_error() With USER_ERROR.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule report usage of `trigger_error() <https://www.php.net/trigger_error>`_ with USER_ERROR constant. This feature is deprecated.

.. code-block:: php
   
   <?php
   
   trigger_error(USER_ERROR);
   
   ?>
Connex PHP features
-------------------

  + `trigger_error <https://php-dictionary.readthedocs.io/en/latest/dictionary/trigger_error.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/TriggerErrorUserError                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP84 <ruleset-CompatibilityPHP84>`, :ref:`CompatibilityPHP85 <ruleset-CompatibilityPHP85>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


