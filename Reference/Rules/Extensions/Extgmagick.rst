.. _extensions-extgmagick:


.. _ext-gmagick:

ext/gmagick
+++++++++++

.. meta::
	:description:
		ext/gmagick: Extension gmagick.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/gmagick
	:twitter:description: ext/gmagick: Extension gmagick
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/gmagick
	:og:type: article
	:og:description: Extension gmagick
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/gmagick.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extgmagick.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extgmagick.html","name":"ext\/gmagick","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension gmagick","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/gmagick.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension gmagick.

Gmagick is a php extension to create, modify and obtain meta information of images using the GraphicsMagick API.

.. code-block:: php
   
   <?php
   //Instantiate a new Gmagick object
   $image = new Gmagick('example.jpg');
   
   //Make thumbnail from image loaded. 0 for either axes preserves aspect ratio
   $image->thumbnailImage(100, 0);
   
   //Create a border around the image, then simulate how the image will look like as an oil painting
   //Note the chaining of mutator methods which is supported in gmagick
   $image->borderImage("yellow", 8, 8)->oilPaintImage(0.3);
   
   //Write the current image at the current state to a file
   $image->write('example_thumbnail.jpg');
   ?>

See also `PHP gmagick <http://www.php.net/manual/en/book.gmagick.php>`_ and `gmagick <http://www.graphicsmagick.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extgmagick                                                                                                                                                                   |
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


