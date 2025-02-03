.. _php-unknownpcre2option:


.. _unknown-pcre2-option:

Unknown Pcre2 Option
++++++++++++++++++++


.. meta::

	:description:

		Unknown Pcre2 Option: ``PCRE2`` supports different options, compared to ``PCRE1``.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Unknown Pcre2 Option

	:twitter:description: Unknown Pcre2 Option: ``PCRE2`` supports different options, compared to ``PCRE1``

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Unknown Pcre2 Option

	:og:type: article

	:og:description: ``PCRE2`` supports different options, compared to ``PCRE1``

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unknown Pcre2 Option.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UnknownPcre2Option.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UnknownPcre2Option.html","name":"Unknown Pcre2 Option","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"``PCRE2`` supports different options, compared to ``PCRE1``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unknown Pcre2 Option.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``PCRE2`` supports different options, compared to ``PCRE1``. ``PCRE2`` was adopted with PHP 7.3. 

The ``S`` modifier : it used to tell PCRE to spend more time studying the regex, so as to be faster at execution. This is now the default behavior, and may be dropped from the regex.

The ``X`` modifier : ``X`` is still existing with ``PCRE2``, though it is now the default for ``PCRE2``, and not for PHP as time of writing. In particular, ``Any backslash in a pattern that is followed by a letter that has no special meaning causes an `error <https://www.php.net/error>`_, thus reserving these combinations for future expansion. ``. It is recommended to avoid using useless sequence \s in regex to get ready for that change. All the following letters ``gijkmoqyFIJMOTY`` . Note that ``clLpPuU`` are valid ``PRCE`` sequences, and are probably failing for other reasons.

.. code-block:: php
   
   <?php
   
   // \y has no meaning. With X option, this leads to a regex compilation error, and a failed test.
   preg_match('/ye\y/', $string);
   preg_match('/ye\y/X', $string);
   
   ?>

See also `Pattern Modifiers <https://www.php.net/manual/en/reference.pcre.pattern.modifiers.php>`_ and `PHP RFC: PCRE2 migration <https://wiki.php.net/rfc/pcre2-migration>`_.

Connex PHP features
-------------------

  + `regex <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UnknownPcre2Option                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


