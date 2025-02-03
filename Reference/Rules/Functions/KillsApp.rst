.. _functions-killsapp:


.. _exit-like-methods:

Exit-like Methods
+++++++++++++++++


.. meta::

	:description:

		Exit-like Methods: Those methods terminate the execution.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Exit-like Methods

	:twitter:description: Exit-like Methods: Those methods terminate the execution

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Exit-like Methods

	:og:type: article

	:og:description: Those methods terminate the execution

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Exit-like Methods.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/KillsApp.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/KillsApp.html","name":"Exit-like Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Those methods terminate the execution","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Exit-like Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those methods terminate the execution. 

They are detected when they do call `exit() <https://www.www.php.net/exit>`_ or `die() <https://www.php.net/die>`_. They may also be identified with the PHP 8.0 ``#[NoReturn]`` `attribute <https://www.php.net/attribute>`_, or the PHPdoc ``@noreturn`` (case insensitive).

If they are called, they will stop the application. They are a user-land equivalent of `exit() <https://www.www.php.net/exit>`_ or `die() <https://www.php.net/die>`_.

.. code-block:: php
   
   <?php
   
   // This function anytime the code has finished its processing.
   function finish() {
       global $html;
       
       echo $html;
       die();
   }
   
   ?>

See also `PhpStorm 2020.3 EAP #4: Custom PHP 8 Attributes  <https://blog.jetbrains.com/phpstorm/2020/10/phpstorm-2020-3-eap-4/>`_.

Connex PHP features
-------------------

  + `exit <https://php-dictionary.readthedocs.io/en/latest/dictionary/exit.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/KillsApp                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


