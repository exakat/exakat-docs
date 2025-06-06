.. _structures-nochangeincomingvariables:


.. _don't-change-incomings:

Don't Change Incomings
++++++++++++++++++++++

.. meta::
	:description:
		Don't Change Incomings: PHP hands over a lot of information using special variables like $_GET, $_POST, etc.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Don't Change Incomings
	:twitter:description: Don't Change Incomings: PHP hands over a lot of information using special variables like $_GET, $_POST, etc
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Don't Change Incomings
	:og:type: article
	:og:description: PHP hands over a lot of information using special variables like $_GET, $_POST, etc
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Don't Change Incomings.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoChangeIncomingVariables.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoChangeIncomingVariables.html","name":"Don't Change Incomings","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"PHP hands over a lot of information using special variables like $_GET, $_POST, etc","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Don't Change Incomings.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP hands over a lot of information using special variables like `$_GET <https://www.php.net/manual/en/reserved.variables.get.php>`_, `$_POST <https://www.php.net/manual/en/reserved.variables.post.php>`_, etc... Modifying those variables and those values inside variables means that the original content is lost, while it will still look like raw data, and, as such, will be untrustworthy.
It is recommended to put the modified values in another variable, and keep the original one intact.

.. code-block:: php
   
   <?php
   
   // filtering and keeping the incoming value. 
   $_DATA'id'] = (int) $_GET['id'];
   
   // filtering and changing the incoming value. 
   $_GET['id'] = strtolower($_GET['id']);
   
   ?>
Related PHP errors 
-------------------

  + `Cannot re-assign $this <https://php-errors.readthedocs.io/en/latest/messages/cannot-re-assign-%24this.html>`_
  + `Cannot re-assign auto-global variable $_GET <https://php-errors.readthedocs.io/en/latest/messages/cannot-re-assign-auto-global-variable-%25s.html>`_



Connex PHP features
-------------------

  + `Incoming Data <https://php-dictionary.readthedocs.io/en/latest/dictionary/incoming-data.ini.html>`_
  + `Outgoing Data <https://php-dictionary.readthedocs.io/en/latest/dictionary/outgoing-data.ini.html>`_


Suggestions
___________

* Set the value to another variable and apply modifications to that variable




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoChangeIncomingVariables                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


