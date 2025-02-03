.. _variables-uncommonenvvar:


.. _environment-variables:

Environment Variables
+++++++++++++++++++++

.. meta::
	:description:
		Environment Variables: Environment variables are used to interact with the hosting system.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Environment Variables
	:twitter:description: Environment Variables: Environment variables are used to interact with the hosting system
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Environment Variables
	:og:type: article
	:og:description: Environment variables are used to interact with the hosting system
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Environment Variables.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/UncommonEnvVar.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/UncommonEnvVar.html","name":"Environment Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Environment variables are used to interact with the hosting system","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Environment Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Environment variables are used to interact with the hosting system. 

They often provides configuration parameter that are set by the host of the application to be used. 
That way, information is not hardcoded in the application, and may be changed at production.

.. code-block:: php
   
   <?php
   
   //ENVIRONMENT set the production context
   if (getenv('ENVIRONMENT') === 'Production') {
       $sshKey = getenv('HOST_KEY');
   } elseif (getenv('ENVIRONMENT') === 'Developper') {
       $sshKey = 'NO KEY';
   } else {
       header('No website here.');
       die();
   }
   
   ?>

See also `$_ENV <https://www.php.net/reserved.variables.environment.php>`_.

Connex PHP features
-------------------

  + `environment-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/environment-variable.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/UncommonEnvVar                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


