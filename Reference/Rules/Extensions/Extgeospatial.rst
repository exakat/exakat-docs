.. _extensions-extgeospatial:

.. _geospatial:

Geospatial
++++++++++

  PHP Extension to handle common geospatial functions. The extension currently has implementations of the Haversine and Vincenty's formulas for calculating distances, an initial bearing calculation function, a Helmert transformation function to transfer between different supported datums, conversions between polar and Cartesian coordinates, conversions between Degree/Minute/Seconds and decimal degrees, a method to simplify linear geometries, as well as a method to calculate intermediate points on a LineString.
NB : description and exemples are extracted from the extension source code.

.. code-block:: php
   
   <?php
   $from = array(
       'type' => 'Point',
       'coordinates' => array( -104.88544, 39.06546 )
   );
   $to = array(
       'type' => 'Point',
       'coordinates' => array( -104.80, 39.06546 )
   );
   var_dump(haversine($to, $from));
   ?>

See also `geospatial - PHP Geospatial Extension <https://github.com/php-geospatial/geospatial>`.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extgeospatial                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


