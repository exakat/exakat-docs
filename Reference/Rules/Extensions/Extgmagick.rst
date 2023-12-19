.. _extensions-extgmagick:

.. _ext-gmagick:

ext/gmagick
+++++++++++

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


