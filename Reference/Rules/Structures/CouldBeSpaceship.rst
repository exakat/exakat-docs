.. _structures-couldbespaceship:


.. _could-be-spaceship:

Could Be Spaceship
++++++++++++++++++

.. meta::
	:description:
		Could Be Spaceship: The spaceship operator compares values and returns 0 for equality, 1 for superior and -1 for inferior.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Spaceship
	:twitter:description: Could Be Spaceship: The spaceship operator compares values and returns 0 for equality, 1 for superior and -1 for inferior
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Spaceship
	:og:type: article
	:og:description: The spaceship operator compares values and returns 0 for equality, 1 for superior and -1 for inferior
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Spaceship.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldBeSpaceship.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldBeSpaceship.html","name":"Could Be Spaceship","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The spaceship operator compares values and returns 0 for equality, 1 for superior and -1 for inferior","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Spaceship.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The spaceship operator compares values and returns 0 for equality, 1 for superior and -1 for inferior. 

It is the same as below, and prevents lots of code.

.. code-block:: php
   
   <?php
   
   if ($a) {
       return 1;
   } elseif ($b) {
       return 0;
   } else {
       return -1;
   }
   ?>

See also `spaceship operator <https://www.php.net/manual/en/migration70.new-features.php#migration70.new-features.spaceship-op>`_ and `Remembering what spaceship operator do on comparison in PHP <https://www.amitmerchant.com/remembering-what-spaceship-operator-do-comparison-php/>`_.

Connex PHP features
-------------------

  + `Spaceship Operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/spaceship.ini.html>`_


Suggestions
___________

* Adopt the spaceship operator




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldBeSpaceship                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                             |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


