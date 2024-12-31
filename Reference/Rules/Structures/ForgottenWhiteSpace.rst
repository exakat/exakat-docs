.. _structures-forgottenwhitespace:

.. _forgotten-whitespace:

Forgotten Whitespace
++++++++++++++++++++

.. meta\:\:
	:description:
		Forgotten Whitespace: Forgotten whitespaces brings unexpected error messages.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Forgotten Whitespace
	:twitter:description: Forgotten Whitespace: Forgotten whitespaces brings unexpected error messages
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Forgotten Whitespace
	:og:type: article
	:og:description: Forgotten whitespaces brings unexpected error messages
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ForgottenWhiteSpace.html
	:og:locale: en
  Forgotten whitespaces brings unexpected `error <https://www.php.net/error>`_ messages.

White spaces have been left at either end of a file : before the PHP opening tag, or after the closing tag. 

Usually, such whitespaces are forgotten, and may end up summoning the infamous 'headers already sent' `error <https://www.php.net/error>`_. It is better to remove them.

.. code-block:: php
   
   <?php
       // This script has no forgotten whitespace, not at the beginning
       function foo() {}
   
       // This script has no forgotten whitespace, not at the end
   ?>

See also `How to fix Headers already sent error in PHP <http://stackoverflow.com/questions/8028957/how-to-fix-headers-already-sent-error-in-php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Headers+already+sent.html>`_



Connex PHP features
-------------------

  + `whitespace <https://php-dictionary.readthedocs.io/en/latest/dictionary/whitespace.ini.html>`_


Suggestions
___________

* Remove all whitespaces before and after a script. This doesn't apply to template, which may need to use those spaces.
* Remove the final tag, to prevent any whitespace to be forgotten at the end of the file. This doesn't apply to the opening PHP tag, which is always necessary.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ForgottenWhiteSpace                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


