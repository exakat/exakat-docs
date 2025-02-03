.. _security-registerglobals:


.. _register-globals:

Register Globals
++++++++++++++++

.. meta::
	:description:
		Register Globals: ``register_globals`` was a PHP directive that dumped all incoming variables from GET, POST, COOKIE and FILES as global variables in the called scripts.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Register Globals
	:twitter:description: Register Globals: ``register_globals`` was a PHP directive that dumped all incoming variables from GET, POST, COOKIE and FILES as global variables in the called scripts
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Register Globals
	:og:type: article
	:og:description: ``register_globals`` was a PHP directive that dumped all incoming variables from GET, POST, COOKIE and FILES as global variables in the called scripts
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Register Globals.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/RegisterGlobals.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/RegisterGlobals.html","name":"Register Globals","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"``register_globals`` was a PHP directive that dumped all incoming variables from GET, POST, COOKIE and FILES as global variables in the called scripts","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Register Globals.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``register_globals`` was a PHP directive that dumped all incoming variables from GET, POST, COOKIE and FILES as global variables in the called scripts.
This lead to security failures, as the variables were often used but not filtered. 

Though it is less often found in more recent code, ``register_globals`` is sometimes needed in legacy code, that haven't made the move to eradicate this style of coding.
Backward compatible pieces of code that mimic the ``register_globals`` features usually create even greater security risks by being run after scripts startup. At that point, some important variables are already set, and may be overwritten by the incoming call, creating confusion in the script.

Mimicking ``register_globals`` is achieved with variables variables, `extract() <https://www.php.net/extract>`_, `parse_str() <https://www.php.net/parse_str>`_ and import_request_variables() (Up to PHP 5.4).

.. code-block:: php
   
   <?php
   
   // Security warning ! This overwrites existing variables. 
   extract($_POST);
   
   // Security warning ! This overwrites existing variables. 
   foreach($_REQUEST as $var => $value) {
       $$var = $value;
   }
   
   ?>
Connex PHP features
-------------------

  + `register-globals <https://php-dictionary.readthedocs.io/en/latest/dictionary/register-globals.ini.html>`_


Suggestions
___________

* Avoid implementing again ``register_globals``
* Use a container to store and access commonly used values




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/RegisterGlobals                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-teampass-security-registerglobals`, :ref:`case-xoops-security-registerglobals`                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


