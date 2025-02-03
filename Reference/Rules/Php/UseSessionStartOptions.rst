.. _php-usesessionstartoptions:

.. _use-session\_start()-options:

Use session_start() Options
+++++++++++++++++++++++++++

.. meta::
	:description:
		Use session_start() Options: It is possible to set the session's option at session_start() call, skipping the usage of session_option().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use session_start() Options
	:twitter:description: Use session_start() Options: It is possible to set the session's option at session_start() call, skipping the usage of session_option()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use session_start() Options
	:og:type: article
	:og:description: It is possible to set the session's option at session_start() call, skipping the usage of session_option()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use session_start() Options.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseSessionStartOptions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseSessionStartOptions.html","name":"Use session_start() Options","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"It is possible to set the session's option at session_start() call, skipping the usage of session_option()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use session_start() Options.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>It is possible to set the session's option at `session_start() <https://www.php.net/session_start>`_ call, skipping the usage of session_option().

This way, session's options are set in one call, saving several hits.

This is available since PHP 7.0. It is recommended to set those values in the ``php.ini`` file, whenever possible.

.. code-block:: php
   
   <?php
   
   // PHP 7.0
   session_start(['session.name' => 'mySession',
                  'session.cookie_httponly' => 1,
                  'session.gc_maxlifetime' => 60 * 60);
   
   // PHP 5.6- old way 
   ini_set ('session.name', 'mySession');
   ini_set("session.cookie_httponly", 1); 
   ini_set('session.gc_maxlifetime', 60 * 60);
   session_start();
   
   ?>
Connex PHP features
-------------------

  + `session <https://php-dictionary.readthedocs.io/en/latest/dictionary/session.ini.html>`_


Suggestions
___________

* Use session_start() with array arguments




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseSessionStartOptions                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.8                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-php-usesessionstartoptions`                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


