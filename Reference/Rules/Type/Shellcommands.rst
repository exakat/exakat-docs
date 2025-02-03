.. _type-shellcommands:


.. _shell-commands:

Shell commands
++++++++++++++

.. meta::
	:description:
		Shell commands: Shell commands, called from PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Shell commands
	:twitter:description: Shell commands: Shell commands, called from PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Shell commands
	:og:type: article
	:og:description: Shell commands, called from PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Shell commands.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Shellcommands.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Shellcommands.html","name":"Shell commands","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Shell commands, called from PHP","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Shell commands.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Shell commands, called from PHP. 

Shell commands are detected with the italic quotes, and using `shell_exec() <https://www.php.net/shell_exec>`_, `system() <https://www.php.net/system>`_, `exec() <https://www.php.net/exec>`_ and `proc_open() <https://www.php.net/proc_open>`_.

.. code-block:: php
   
   <?php
   
   // Shell command in a shell_exec() call
   shell_exec('ls -1');
   
   // Shell command with backtick operator
   `ls -1 $path`;
   
   ?>

See also `Execution operator <https://www.php.net/manual/en/language.operators.execution.php>`_, `shell_exec <https://www.php.net/manual/en/function.shell-exec.php>`_ and `exec <https://www.php.net/manual/en/function.exec.php>`_.

Connex PHP features
-------------------

  + `system-call <https://php-dictionary.readthedocs.io/en/latest/dictionary/system-call.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Shellcommands                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
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


