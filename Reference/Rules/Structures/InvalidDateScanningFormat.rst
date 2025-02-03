.. _structures-invaliddatescanningformat:


.. _invalid-date-scanning-format:

Invalid Date Scanning Format
++++++++++++++++++++++++++++


.. meta::

	:description:

		Invalid Date Scanning Format: The format string used with Datetime::createFromFormat() method (or similar) contains unknown characters.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Invalid Date Scanning Format

	:twitter:description: Invalid Date Scanning Format: The format string used with Datetime::createFromFormat() method (or similar) contains unknown characters

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Invalid Date Scanning Format

	:og:type: article

	:og:description: The format string used with Datetime::createFromFormat() method (or similar) contains unknown characters

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Invalid Date Scanning Format.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InvalidDateScanningFormat.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InvalidDateScanningFormat.html","name":"Invalid Date Scanning Format","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The format string used with Datetime::createFromFormat() method (or similar) contains unknown characters","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Invalid Date Scanning Format.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The format string used with `Datetime\:\:createFromFormat() <https://www.php.net/manual/en/datetime.createfromformat.php>`_ method (or similar) contains unknown characters. 

This won't raise an `error <https://www.php.net/error>`_, though the resulting values should be checked.

.. code-block:: php
   
   <?php
   
   // format is valid
   $date = datetimeimmutable::createFromFormat('d/m/Y', $a);
   // When wrong, $date is false
   // The errors are in datetimeimmutable::getLastErrors();
   
   // X is not a valid character for 
   $date = datetimeimmutable::createFromFormat('d/X/Y', $a);
   
   ?>
Connex PHP features
-------------------

  + `date <https://php-dictionary.readthedocs.io/en/latest/dictionary/date.ini.html>`_
  + `external-format <https://php-dictionary.readthedocs.io/en/latest/dictionary/external-format.ini.html>`_


Suggestions
___________

* Remove the unknown characters
* Replace the unknown character with the expected one




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InvalidDateScanningFormat                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


