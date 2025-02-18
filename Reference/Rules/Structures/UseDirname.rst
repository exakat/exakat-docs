.. _structures-usedirname:


.. _use-dirname():

Use dirname()
+++++++++++++

.. meta::
	:description:
		Use dirname(): Using the ``/.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use dirname()
	:twitter:description: Use dirname(): Using the ``/
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use dirname()
	:og:type: article
	:og:description: Using the ``/
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use dirname().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseDirname.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseDirname.html","name":"Use dirname()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 14 Feb 2025 23:59:55 +0000","dateModified":"Fri, 14 Feb 2025 23:59:55 +0000","description":"Using the ``\/","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use dirname().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Using the ``/../`` special folder on top of ``__DIR__`` is the same as applying ``dirname()`` on that constant.

.. code-block:: php
   
   <?php
   
   $path = __DIR__.'/../../path/to/file';
   
   // 2nd argument is the number of ../ used
   $path = dirname(__DIR__, 2).'/path/to/file';
   
   ?>
Connex PHP features
-------------------

  + `dirname <https://php-dictionary.readthedocs.io/en/latest/dictionary/dirname.ini.html>`_


Suggestions
___________

* Replace the ``../`` with a call to dirname(), unless it is in a static expression.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseDirname                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.7.0                                                                                                                   |
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


