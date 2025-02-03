.. _structures-noscream:


.. _@-operator:

@ Operator
++++++++++


.. meta::

	:description:

		@ Operator: @ is the 'no scream' operator : it suppresses error output.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: @ Operator

	:twitter:description: @ Operator: @ is the 'no scream' operator : it suppresses error output

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: @ Operator

	:og:type: article

	:og:description: @ is the 'no scream' operator : it suppresses error output

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/@ Operator.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Noscream.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Noscream.html","name":"@ Operator","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"@ is the 'no scream' operator : it suppresses error output","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/@ Operator.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`@ <https://www.php.net/manual/en/language.operators.errorcontrol.php>`_ is the 'no scream' operator : it suppresses `error <https://www.php.net/error>`_ output. 
This operator is very slow : it processes the `error <https://www.php.net/error>`_, and finally decides not to display it. It is often faster to check the conditions first, then run the method without ``@``.

You may also set display_error to 0 in the ``php.ini`` : this avoids user's `error <https://www.php.net/error>`_ display, and keeps the `error <https://www.php.net/error>`_ in the PHP logs, for later processing. 

The only situation where ``@`` is useful is when a native PHP function displays errors messages and there is no way to check it from the code beforehand. 

This was the case with `fopen() <https://www.php.net/fopen>`_, `stream_socket_server() <https://www.php.net/stream_socket_server>`_, `token_get_all() <https://www.php.net/token_get_all>`_. As of PHP 7.0, they are all hiding errors when ``@`` is active.

.. code-block:: php
   
   <?php
   
   // Set x with incoming value, or else null. 
   $x = @$_GET['x'];
   
   ?>

+---------------------+-------------------------+------+----------------------------------------------+
| Name                | Default                 | Type | Description                                  |
+---------------------+-------------------------+------+----------------------------------------------+
| authorizedFunctions | noscream_functions.json | data | Functions that are authorized to sports a @. |
+---------------------+-------------------------+------+----------------------------------------------+



See also `I scream, you scream, we all scream for @ <https://www.exakat.io/en/i-scream-you-scream-we-all-scream-for/>`_, `Error Control Operators <https://www.php.net/manual/en/language.operators.errorcontrol.php>`_ and `Five reasons why the shut-op operator should be avoided <https://derickrethans.nl/five-reasons-why-the-shutop-operator-should-be-avoided.html>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Remove the @ operator by default




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/Noscream                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-noscream <https://github.com/dseguy/clearPHP/tree/master/rules/no-noscream.md>`__                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phinx-structures-noscream`, :ref:`case-phpipam-structures-noscream`                                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


