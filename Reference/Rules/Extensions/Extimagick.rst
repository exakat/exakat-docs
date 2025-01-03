.. _extensions-extimagick:

.. _ext-imagick:

ext/imagick
+++++++++++

.. meta::
	:description:
		ext/imagick: Extension Imagick for PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/imagick
	:twitter:description: ext/imagick: Extension Imagick for PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/imagick
	:og:type: article
	:og:description: Extension Imagick for PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/imagick.html
	:og:locale: en
Extension Imagick for PHP.

Imagick is a native php extension to create and modify images using the ImageMagick API.

.. code-block:: php
   
   <?php
   
   header('Content-type: image/jpeg');
   
   $image = new Imagick('image.jpg');
   
   // If 0 is provided as a width or height parameter,
   // aspect ratio is maintained
   $image->thumbnailImage(100, 0);
   
   echo $image;
   
   ?>

See also `Imagick for PHP <https://www.php.net/manual/en/book.imagick.php>`_ and `Imagick <https://www.imagemagick.org/script/index.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extimagick                                                                                                                                                                   |
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


