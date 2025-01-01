.. _namespaces-multiplealiasdefinitionperfile:

.. _multiple-alias-definitions-per-file:

Multiple Alias Definitions Per File
+++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Alias Definitions Per File: Avoid aliasing the same name with different aliases.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Alias Definitions Per File
	:twitter:description: Multiple Alias Definitions Per File: Avoid aliasing the same name with different aliases
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Alias Definitions Per File
	:og:type: article
	:og:description: Avoid aliasing the same name with different aliases
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Namespaces/MultipleAliasDefinitionPerFile.html
	:og:locale: en
Avoid aliasing the same name with different aliases. This leads to confusion.

.. code-block:: php
   
   <?php
   
   // first occurrence
   use name\space\ClasseName;
   
   // when this happens, several other uses are mentioned
   
   // name\space\ClasseName has now two names
   use name\space\ClasseName as anotherName;
   
   ?>

See also :ref:`No title for `Namespaces/MultipleAliasDefinition`_ <No anchor for `Namespaces/MultipleAliasDefinition`_>`.

Connex PHP features
-------------------

  + `alias <https://php-dictionary.readthedocs.io/en/latest/dictionary/alias.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Namespaces/MultipleAliasDefinitionPerFile                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.3                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


