.. _dump-environnementvariables:

.. _environment-variable-usage:

Environment Variable Usage
++++++++++++++++++++++++++

.. meta::
	:description:
		Environment Variable Usage: This rule collects all environment variables used in the application, for inventory purposes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Environment Variable Usage
	:twitter:description: Environment Variable Usage: This rule collects all environment variables used in the application, for inventory purposes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Environment Variable Usage
	:og:type: article
	:og:description: This rule collects all environment variables used in the application, for inventory purposes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Environment Variable Usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/EnvironnementVariables.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/EnvironnementVariables.html","name":"Environment Variable Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rule collects all environment variables used in the application, for inventory purposes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Environment Variable Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This rule collects all environment variables used in the application, for inventory purposes. Environment variables are detected with the usage of the ``$_SERVER`` superglobal variable, or calls to the `getenv() <https://www.php.net/getenv>`_ and setenv() native functions. 

This helps catalog the interactions between the application and its host environment.

.. code-block:: php
   
   <?php
   
   echo $_SERVER['MY_GLOBAL'];
   
   print getenv('DB_HOST');
   
   setenv('SPECIAL_KEY', $calculatedKey);
   
   ?>

See also `Variable scope <https://www.php.net/manual/en/language.variables.scope.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/EnvironnementVariables                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


