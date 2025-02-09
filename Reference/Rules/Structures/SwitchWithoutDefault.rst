.. _structures-switchwithoutdefault:


.. _switch-without-default:

Switch Without Default
++++++++++++++++++++++

.. meta::
	:description:
		Switch Without Default: Always use a default statement in switch() and match().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Switch Without Default
	:twitter:description: Switch Without Default: Always use a default statement in switch() and match()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Switch Without Default
	:og:type: article
	:og:description: Always use a default statement in switch() and match()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Switch Without Default.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SwitchWithoutDefault.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/SwitchWithoutDefault.html","name":"Switch Without Default","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Always use a default statement in switch() and match()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Switch Without Default.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Always use a default statement in `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ and `match() <https://www.php.net/manual/en/control-structures.match.php>`_. 

Switch statements hold a number of 'case' that cover all known situations, and a 'default' one which is executed when all other options are exhausted. 

For Match statements, a missing default will lead to the ``UnhandledMatchError``` `exception <https://www.php.net/exception>`_ being raised. On the other hand, the switch statement will simply `exit <https://www.www.php.net/exit>`_ without action nor alert. 
Most of the time, `switch() <https://www.php.net/manual/en/control-structures.switch.php>`_ do need a default case, so as to catch the odd situation where the 'value is not what it was expected'. This is a good place to catch unexpected values, to set a default behavior.

.. code-block:: php
   
   <?php
   
   // Missing default
   switch($format) {
       case 'gif' : 
           processGif();
           break 1;
       
       case 'jpeg' : 
           processJpeg();
           break 1;
           
       case 'bmp' :
           throw new UnsupportedFormat($format);
   }
   // In case $format is not known, then switch is ignored and no processing happens, leading to preparation errors
   
   
   // switch with default
   switch($format) {
       case 'text' : 
           processText();
           break 1;
       
       case 'jpeg' : 
           processJpeg();
           break 1;
           
       case 'rtf' :
           throw new UnsupportedFormat($format);
           
       default :
           throw new UnknownFileFormat($format);
   }
   // In case $format is not known, an exception is thrown for processing 
   
   ?>

See also `UnhandledMatchError <https://www.php.net/manual/en/class.unhandledmatcherror.php>`_.

Connex PHP features
-------------------

  + `Match <https://php-dictionary.readthedocs.io/en/latest/dictionary/match.ini.html>`_
  + `Switch <https://php-dictionary.readthedocs.io/en/latest/dictionary/switch.ini.html>`_
  + `Case <https://php-dictionary.readthedocs.io/en/latest/dictionary/case.ini.html>`_
  + `Default <https://php-dictionary.readthedocs.io/en/latest/dictionary/default.ini.html>`_


Suggestions
___________

* Add a default case
* Catch the UnhandledMatchError exception




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/SwitchWithoutDefault                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-switch-without-default <https://github.com/dseguy/clearPHP/tree/master/rules/no-switch-without-default.md>`__                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zencart-structures-switchwithoutdefault`, :ref:`case-traq-structures-switchwithoutdefault`                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


