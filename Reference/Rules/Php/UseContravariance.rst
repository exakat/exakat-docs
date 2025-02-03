.. _php-usecontravariance:


.. _use-contravariance:

Use Contravariance
++++++++++++++++++


.. meta::

	:description:

		Use Contravariance: Contravariance is compatible argument typehint.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Use Contravariance

	:twitter:description: Use Contravariance: Contravariance is compatible argument typehint

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Use Contravariance

	:og:type: article

	:og:description: Contravariance is compatible argument typehint

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Contravariance.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseContravariance.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseContravariance.html","name":"Use Contravariance","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Contravariance is compatible argument typehint","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use Contravariance.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Contravariance is compatible argument typehint. A child class may accept an object of a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class of the argument type of its `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_'s method.

Since a children class may accept a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class of the argument type, the evolution is in opposite order. 

Contravariance is a PHP 7.4 feature. Contravariance is distinct from return type covariance.

.. code-block:: php
   
   <?php
   class X {
     function m(Y $z): X {}
   }
   
   // m is overwriting the parent's method. 
   // The return type is different.
   // The return type is compatible, as Y is also a sub-class of X.
   class Y extends X {
     function m(X $z): Y {}
   }
   
   ?>

See also `Covariant Returns and Contravariant Parameters <https://wiki.php.net/rfc/covariant-returns-and-contravariant-parameters>`_ and :ref:`No title for `Php/UseCovariance` <No anchor for `Php/UseCovariance`>`.

Connex PHP features
-------------------

  + `type-covariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-covariance.ini.html>`_
  + `type-contravariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-contravariance.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseContravariance                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


