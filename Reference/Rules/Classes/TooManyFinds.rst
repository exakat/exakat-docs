.. _classes-toomanyfinds:


.. _too-many-finds:

Too Many Finds
++++++++++++++

.. meta::
	:description:
		Too Many Finds: Too many methods called 'find*' in this class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Too Many Finds
	:twitter:description: Too Many Finds: Too many methods called 'find*' in this class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Too Many Finds
	:og:type: article
	:og:description: Too many methods called 'find*' in this class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Too Many Finds.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/TooManyFinds.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/TooManyFinds.html","name":"Too Many Finds","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Too many methods called 'find*' in this class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Too Many Finds.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Too many methods called 'find*' in this class. It is may be time to consider the `Specification pattern <https://en.wikipedia.org/wiki/Specification_pattern>`_.

.. code-block:: php
   
   <?php
   
   // quite a fishy interface
   interface UserInterface {
       public function findByEmail($email);
       public function findByUsername($username);
       public function findByFirstName($firstname);
       public function findByLastName($lastname);
       public function findByName($name);
       public function findById($id);
   
       public function insert($user);
       public function update($user);
   }
   
   ?>

+--------------+---------+---------+-------------------------------------------------------------------------------------------+
| Name         | Default | Type    | Description                                                                               |
+--------------+---------+---------+-------------------------------------------------------------------------------------------+
| minimumFinds | 5       | integer | Minimal number of prefixed methods to report.                                             |
+--------------+---------+---------+-------------------------------------------------------------------------------------------+
| findPrefix   | find    | string  | list of prefix to use when detecting the 'find'. Comma-separated list, case insensitive.  |
+--------------+---------+---------+-------------------------------------------------------------------------------------------+
| findSuffix   |         | string  | list of fix to use when detecting the 'find'. Comma-separated list, case insensitive.     |
+--------------+---------+---------+-------------------------------------------------------------------------------------------+



See also `On Taming Repository Classes in Doctrine <https://beberlei.de/2013/03/04/doctrine_repositories.html>`_ and `specifications <https://slides.pixelart.at/2017-02-04/fosdem/specifications/#/>`_.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Split the class into smaller classes
* Remove some of the find* methods




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/TooManyFinds                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


