.. _structures-noobjectasindex:


.. _no-object-as-index:

No Object As Index
++++++++++++++++++

.. meta::
	:description:
		No Object As Index: PHP accepts objects as index, though it reports various error messages when this happens.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Object As Index
	:twitter:description: No Object As Index: PHP accepts objects as index, though it reports various error messages when this happens
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Object As Index
	:og:type: article
	:og:description: PHP accepts objects as index, though it reports various error messages when this happens
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Object As Index.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoObjectAsIndex.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoObjectAsIndex.html","name":"No Object As Index","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"PHP accepts objects as index, though it reports various error messages when this happens","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Object As Index.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP accepts objects as index, though it reports various `error <https://www.php.net/error>`_ messages when this happens.

Thanks to `Gina Peter Banyard <https://twitter.com/Girgias>`_ for the inspiration.

.. code-block:: php
   
   <?php
   
   $s = 'Hello';
   $o = new stdClass();
   
   try {
       $s[$o] = 'A';
   } catch (\Throwable $e) {
       echo $e->getMessage(), "\n";
       //Cannot access offset of type stdClass on string
   }
   
   ?>

See also `Use an object as an offet <https://twitter.com/Girgias/status/1405519800575553540>`_.

Related PHP errors 
-------------------

  + `Cannot access offset of type %s on %s <https://php-errors.readthedocs.io/en/latest/messages/cannot-access-offset-of-type-%25s-on-%25s.html>`_
  + `Illegal offset type <https://php-errors.readthedocs.io/en/latest/messages/illegal-offset-type.html>`_
  + `Illegal offset type in isset or empty <https://php-errors.readthedocs.io/en/latest/messages/illegal-offset-type-in-isset-or-empty.html>`_
  + `Index invalid or out of range <https://php-errors.readthedocs.io/en/latest/messages/index-invalid-or-out-of-range.html>`_



Connex PHP features
-------------------

  + `index <https://php-dictionary.readthedocs.io/en/latest/dictionary/index.ini.html>`_


Suggestions
___________

* Filter values being used as index
* Filter values being used as array




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoObjectAsIndex                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


