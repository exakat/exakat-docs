.. _php-hasvirtualproperty:

.. _has-virtual-property:

Has Virtual Property
++++++++++++++++++++

.. meta::
	:description:
		Has Virtual Property: Virtual properties are properties with hooks, which do not rely on storage, but process values stored somewhere else.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Has Virtual Property
	:twitter:description: Has Virtual Property: Virtual properties are properties with hooks, which do not rely on storage, but process values stored somewhere else
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Has Virtual Property
	:og:type: article
	:og:description: Virtual properties are properties with hooks, which do not rely on storage, but process values stored somewhere else
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Has Virtual Property.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HasVirtualProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/HasVirtualProperty.html","name":"Has Virtual Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Virtual properties are properties with hooks, which do not rely on storage, but process values stored somewhere else","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Has Virtual Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Virtual properties are properties with hooks, which do not rely on storage, but process values stored somewhere else.

Virtual proeprties are akin to view, in SQL, where columns are calculated on the fly. 


.. code-block:: php
   
   <?php
   
   class x {
   	// This property doesn't store any data
   	private $random {
   		get { return rand(0, 10); }
   		set { }
   	}
   
   	// This property rely on another property
   	// here for history reasons
   	private $legacy {
   		get { return $this->random; }
   		set { }
   	}
   
   }
   
   ?>
Connex PHP features
-------------------

  + `hook <https://php-dictionary.readthedocs.io/en/latest/dictionary/hook.ini.html>`_
  + `virtual-property <https://php-dictionary.readthedocs.io/en/latest/dictionary/virtual-property.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/HasVirtualProperty                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.4 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


