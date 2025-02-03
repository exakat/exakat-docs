.. _php-usedatetimeimmutable:


.. _use-datetimeimmutable-class:

Use DateTimeImmutable Class
+++++++++++++++++++++++++++


.. meta::

	:description:

		Use DateTimeImmutable Class: The ``DateTimeImmutable`` class is the immutable version of the ``Datetime`` class.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Use DateTimeImmutable Class

	:twitter:description: Use DateTimeImmutable Class: The ``DateTimeImmutable`` class is the immutable version of the ``Datetime`` class

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Use DateTimeImmutable Class

	:og:type: article

	:og:description: The ``DateTimeImmutable`` class is the immutable version of the ``Datetime`` class

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use DateTimeImmutable Class.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseDateTimeImmutable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseDateTimeImmutable.html","name":"Use DateTimeImmutable Class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The ``DateTimeImmutable`` class is the immutable version of the ``Datetime`` class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use DateTimeImmutable Class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The ``DateTimeImmutable`` class is the immutable version of the ``Datetime`` class. 

While ``DateTime`` may be modified, ``DateTimeImmutable`` cannot be modified : it needs to be cloned instead. Any modification to such an object will return a new and distinct object. This prevents alterations that are hard to track.

.. code-block:: php
   
   <?php
   // Example extracted from Derick Rethans' article (link below)
   
   function formatNextMondayFromNow( DateTime $dt )
   {
           return $dt->modify( 'next monday' )->format( 'Y-m-d' );
   }
   
   $d = new DateTime();                          //2014-02-17
   echo formatNextMondayFromNow( $d ), "\n";
   echo $d->format( 'Y-m-d' ), "\n";             //2014-02-17
   ?>

See also `What's all this 'immutable date' stuff, anyway? <https://medium.com/@codebyjeff/whats-all-this-immutable-date-stuff-anyway-72d4130af8ce>`_, `DateTimeImmutable <https://derickrethans.nl/immutable-datetime.html>`_, `The DateTime class <https://www.php.net/manual/en/class.datetime.php>`_ and `The DateTimeImmutable class <https://www.php.net/manual/en/class.datetimeimmutable.php>`_.

Connex PHP features
-------------------

  + `immutable <https://php-dictionary.readthedocs.io/en/latest/dictionary/immutable.ini.html>`_
  + `date <https://php-dictionary.readthedocs.io/en/latest/dictionary/date.ini.html>`_


Suggestions
___________

* Always use DateTimeImmutable when manipulating dates.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseDateTimeImmutable                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


