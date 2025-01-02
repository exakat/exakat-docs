.. _dump-collectmbstringencodings:

.. _collect-mbstring-encodings:

Collect Mbstring Encodings
++++++++++++++++++++++++++

.. meta::
	:description:
		Collect Mbstring Encodings: This analysis collects the encoding names, used by ext/mb functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Mbstring Encodings
	:twitter:description: Collect Mbstring Encodings: This analysis collects the encoding names, used by ext/mb functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Mbstring Encodings
	:og:type: article
	:og:description: This analysis collects the encoding names, used by ext/mb functions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Mbstring Encodings.html
	:og:locale: en
This analysis collects the encoding names, used by ext/mb functions.

.. code-block:: php
   
   <?php
   
   mb_stotolower('PHP', 'iso-8859-1');
   
   mb_stotolower('PHP', 'iso-8859-1');
   
   ?>
Connex PHP features
-------------------

  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectMbstringEncodings                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


