.. _structures-couldusematch:


.. _could-use-match:

Could Use Match
+++++++++++++++


.. meta::

	:description:

		Could Use Match: The switch() syntax use may be replaced by a match() call.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Could Use Match

	:twitter:description: Could Use Match: The switch() syntax use may be replaced by a match() call

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Could Use Match

	:og:type: article

	:og:description: The switch() syntax use may be replaced by a match() call

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Match.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseMatch.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseMatch.html","name":"Could Use Match","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The switch() syntax use may be replaced by a match() call","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use Match.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ syntax use may be replaced by a `match() <https://www.php.net/manual/en/control-structures.match.php>`_ call. 

The simplest case for such refactoring is when each of the switch's case (including default), assign one value to the same variable. See this below : 
`Match() <https://www.php.net/manual/en/control-structures.match.php>`_ was introduced in PHP 8. It is not valid with older PHP versions.

.. code-block:: php
   
   <?php
       switch($a) {
           case 1: 
               $b = '1';
               break;
           case 2: 
               $b = '3';
               break;
           default:  
               $b = '0';
               break; 
       }
       
       /*
       $b = match($a) {
           1 => '1',
           2 => '3',
           default => '0'
       };
       */
   ?>

See also `Match() <https://www.php.net/manual/en/control-structures.match.php>`_.

Connex PHP features
-------------------

  + `match <https://php-dictionary.readthedocs.io/en/latest/dictionary/match.ini.html>`_
  + `switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_


Suggestions
___________

* Replace switch() with match()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseMatch                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


