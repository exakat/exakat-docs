.. _extensions-extexif:

.. _ext-exif:

ext/exif
++++++++

.. meta::
	:description:
		ext/exif: Extension EXIF : Exchangeable image file format.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/exif
	:twitter:description: ext/exif: Extension EXIF : Exchangeable image file format
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/exif
	:og:type: article
	:og:description: Extension EXIF : Exchangeable image file format
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extexif.html
	:og:locale: en
Extension EXIF : Exchangeable image file format.

The EXIF extension manipulates image meta data.

.. code-block:: php
   
   <?php
   echo 'test1.jpg:<br />';
   $exif = exif_read_data('tests/test1.jpg', 'IFD0');
   echo $exif===false ? 'No header data found.<br />' : 'Image contains headers<br />';
   
   $exif = exif_read_data('tests/test2.jpg', 0, true);
   echo 'test2.jpg:<br />';
   foreach ($exif as $key => $section) {
       foreach ($section as $name => $val) {
           echo $key.$name.': '.$val.'<br />';
       }
   }
   ?>

See also `Exchangeable image information <https://www.php.net/manual/en/book.exif.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extexif                                                                                                                                                                      |
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


