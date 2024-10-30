.. _php-closetags:

.. _closing-tags:

Closing Tags
++++++++++++

  PHP manual recommends that script should be left open, without the final closing ``?>``. This way, one will avoid the infamous bug ``'Header already sent'``, associated with left-over spaces, that are lying after this closing tag.
<?php

// some code

// no closing tag

See also `PHP Closing Tag <https://codeigniter.com/userguide3/general/styleguide.html#php-closing-tag>`_.

Connex PHP features
-------------------

  + `close-tag <https://php-dictionary.readthedocs.io/en/latest/dictionary/close-tag.ini.html>`_


Suggestions
___________

* Always leave the last closing tag out




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CloseTags                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `leave-last-closing-out <https://github.com/dseguy/clearPHP/tree/master/rules/leave-last-closing-out.md>`__             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


