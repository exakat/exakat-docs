.. _functions-toomanyparameters:


.. _too-many-parameters:

Too Many Parameters
+++++++++++++++++++

.. meta::
	:description:
		Too Many Parameters: Method has too many parameters.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Too Many Parameters
	:twitter:description: Too Many Parameters: Method has too many parameters
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Too Many Parameters
	:og:type: article
	:og:description: Method has too many parameters
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Too Many Parameters.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/TooManyParameters.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/TooManyParameters.html","name":"Too Many Parameters","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Method has too many parameters","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Too Many Parameters.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Method has too many parameters. Exakat has a default parameter count which may be configured.

A method that needs more than 8 parameters is trying to do too much : it should be reviewed and split into smaller methods.

.. code-block:: php
   
   <?php
   
   // This methods has too many parameters.
   function alertSomeone($name, $email, $title, $message, $attachements, $signature, $bcc, $cc, $extra_headers) { 
       /* too much code here */ 
   }
   
   ?>

+-----------------+---------+---------+-----------------------------------------+
| Name            | Default | Type    | Description                             |
+-----------------+---------+---------+-----------------------------------------+
| parametersCount | 8       | integer | Minimal number of parameters to report. |
+-----------------+---------+---------+-----------------------------------------+



See also `How many parameters is too many ? <https://www.exakat.io/how-many-parameters-is-too-many/>`_ and `Too Many Parameters <http://wiki.c2.com/?TooManyParameters>`_.

Connex PHP features
-------------------

  + `Parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_


Suggestions
___________

* Reduce the number of parameters to a lower level
* Break the function into smaller functions
* Turn the function into a class




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/TooManyParameters                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-functions-toomanyparameters`, :ref:`case-churchcrm-functions-toomanyparameters`                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


