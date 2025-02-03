.. _structures-continueisforloop:

.. _continue-is-for-loop:

Continue Is For Loop
++++++++++++++++++++

.. meta::
	:description:
		Continue Is For Loop: break and continue are very similar in PHP : they both break out of loop or switch.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Continue Is For Loop
	:twitter:description: Continue Is For Loop: break and continue are very similar in PHP : they both break out of loop or switch
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Continue Is For Loop
	:og:type: article
	:og:description: break and continue are very similar in PHP : they both break out of loop or switch
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Continue Is For Loop.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ContinueIsForLoop.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ContinueIsForLoop.html","name":"Continue Is For Loop","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"break and continue are very similar in PHP : they both break out of loop or switch","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Continue Is For Loop.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`break <https://www.php.net/manual/en/control-structures.break.php>`_ and `continue <https://www.php.net/manual/en/control-structures.continue.php>`_ are very similar in PHP : they both `break <https://www.php.net/manual/en/control-structures.break.php>`_ out of loop or switch. Yet, `continue <https://www.php.net/manual/en/control-structures.continue.php>`_ should be reserved for loops.

Since PHP 7.3, the execution emits a warning when finding a ``continue`` inside a ``switch`` : '"`continue <https://www.php.net/manual/en/control-structures.continue.php>`_" targeting switch is equivalent to "`break <https://www.php.net/manual/en/control-structures.break.php>`_". Did you mean to use "`continue <https://www.php.net/manual/en/control-structures.continue.php>`_ 2"?'

.. code-block:: php
   
   <?php
   
   while ($foo) {
       switch ($bar) {
           case 'baz':
               continue; // In PHP: Behaves like 'break;'
                         // In C:   Behaves like 'continue 2;'
       }
   }
   
   ?>

See also `Deprecate and remove continue targeting switch <https://wiki.php.net/rfc/continue_on_switch_deprecation>`_.

Related PHP errors 
-------------------

  + `"continue" targeting switch is equivalent to "break". Did you mean to use "continue 2"? <https://php-errors.readthedocs.io/en/latest/messages/continue%22-targeting-switch-is-equivalent-to-%22break.html>`_



Connex PHP features
-------------------

  + `continue <https://php-dictionary.readthedocs.io/en/latest/dictionary/continue.ini.html>`_
  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Replace continue by break




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ContinueIsForLoop                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>`, :ref:`CompatibilityPHP73 <ruleset-CompatibilityPHP73>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.9                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.3 and more recent                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-xoops-structures-continueisforloop`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


