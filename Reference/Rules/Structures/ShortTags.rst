.. _structures-shorttags:

.. _using-short-tags:

Using Short Tags
++++++++++++++++

.. meta::
	:description:
		Using Short Tags: The code makes use of short tags.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Using Short Tags
	:twitter:description: Using Short Tags: The code makes use of short tags
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Using Short Tags
	:og:type: article
	:og:description: The code makes use of short tags
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ShortTags.html
	:og:locale: en
The code makes use of short tags. Short tags are the following : ``<?`` . A full scripts looks like that : ``<? /* php code */ ?>`` .

It is recommended to avoid using short tags, and use standard PHP tags. This makes PHP code compatible with XML standards. Short tags used to be popular, but have lost it.

See also `PHP Tags <https://www.php.net/manual/en/language.basic-syntax.phptags.php>`_.

Connex PHP features
-------------------

  + `short-tag <https://php-dictionary.readthedocs.io/en/latest/dictionary/short-tag.ini.html>`_
  + `php-tag <https://php-dictionary.readthedocs.io/en/latest/dictionary/php-tag.ini.html>`_
  + `echo-tag <https://php-dictionary.readthedocs.io/en/latest/dictionary/echo-tag.ini.html>`_


Suggestions
___________

* Use full tags




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShortTags                                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-short-tags <https://github.com/dseguy/clearPHP/tree/master/rules/no-short-tags.md>`__                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


