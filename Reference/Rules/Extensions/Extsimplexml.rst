.. _extensions-extsimplexml:


.. _ext-simplexml:

ext/simplexml
+++++++++++++

.. meta::
	:description:
		ext/simplexml: Extension ``SimpleXML``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/simplexml
	:twitter:description: ext/simplexml: Extension ``SimpleXML``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/simplexml
	:og:type: article
	:og:description: Extension ``SimpleXML``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/simplexml.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extsimplexml.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extsimplexml.html","name":"ext\/simplexml","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ``SimpleXML``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/simplexml.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension ``SimpleXML``.

The ``SimpleXML`` extension provides a very simple and easily usable toolset to convert XML to an object that can be processed with normal property selectors and array iterators.

.. code-block:: php
   
   <?php
   
   $xml = <<<'XML'
   <?xml version='1.0' standalone='yes' ? >
   <movies>
    <movie>
     <title>PHP: Behind the Parser</title>
     <characters>
      <character>
       <name>Ms. Coder</name>
       <actor>Onlivia Actora</actor>
      </character>
      <character>
       <name>Mr. Coder</name>
       <actor>El Act&#211;r</actor>
      </character>
     </characters>
     <plot>
      So, this language. It's like, a programming language. Or is it a
      scripting language? All is revealed in this thrilling horror spoof
      of a documentary.
     </plot>
     <great-lines>
      <line>PHP solves all my web problems</line>
     </great-lines>
     <rating type="thumbs">7</rating>
     <rating type="stars">5</rating>
    </movie>
   </movies>
   XML;
   
   $movies = new SimpleXMLElement($xml);
   
   echo $movies->movie[0]->plot;
   ?>

See also `SimpleXML <https://www.php.net/manual/en/book.simplexml.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsimplexml                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


