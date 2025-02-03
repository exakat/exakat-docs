.. _extensions-extxmlreader:


.. _ext-xmlreader:

ext/xmlreader
+++++++++++++

.. meta::
	:description:
		ext/xmlreader: Extension XMLReader.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/xmlreader
	:twitter:description: ext/xmlreader: Extension XMLReader
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/xmlreader
	:og:type: article
	:og:description: Extension XMLReader
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/xmlreader.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extxmlreader.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extxmlreader.html","name":"ext\/xmlreader","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension XMLReader","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/xmlreader.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension `XMLReader <https://www.php.net/xmlreader>`_.

The `XMLReader <https://www.php.net/xmlreader>`_ extension is an XML Pull parser. The reader acts as a cursor going forward on the document stream and stopping at each node on the way.

.. code-block:: php
   
   <?php
   
       $xmlreader = new XMLReader();
       $xmlreader->xml("<xml><div>Content</div></xml>");
       $xmlreader->read();
       $xmlreader->read();
       $xmlreader->readString();
   
   ?>

See also `xmlreader <http://www.php.net/manual/en/book.xmlreader.php>`_.

Connex PHP features
-------------------

  + `xml <https://php-dictionary.readthedocs.io/en/latest/dictionary/xml.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extxmlreader                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


