.. _arrays-multipleidenticalkeys:

.. _multiple-index-definition:

Multiple Index Definition
+++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Index Definition: This rules lists the indexes that are defined multiple times in the same array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Index Definition
	:twitter:description: Multiple Index Definition: This rules lists the indexes that are defined multiple times in the same array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Index Definition
	:og:type: article
	:og:description: This rules lists the indexes that are defined multiple times in the same array
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Index Definition.html
	:og:locale: en
This rules lists the indexes that are defined multiple times in the same array. 

In reality, they are overwriting each other. This is most probably a typo or a failed copy/paste.


.. code-block:: php
   
   <?php
       // Multiple identical keys
       $x = array(1 => 2, 
                  2 => 3,  
                  1 => 3);
   
       // Multiple identical keys (sneaky version)
       $x = array(1 => 2, 
                  1.1 => 3,  
                  true => 4);
   
       // Multiple identical keys (automated version)
       $x = array(1 => 2, 
                  3,        // This is the index 2
                  2 => 4);  // this index is overwritten
   ?>

+--------------+---------+---------+--------------------------------------------------------------------------------------------------------------------+
| Name         | Default | Type    | Description                                                                                                        |
+--------------+---------+---------+--------------------------------------------------------------------------------------------------------------------+
| arrayMaxSize | 15000   | integer | Maximal size of arrays to be analyzed. This directive speeds up analysis, and leaves the largest arrays untouched. |
+--------------+---------+---------+--------------------------------------------------------------------------------------------------------------------+


Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_
  + `index <https://php-dictionary.readthedocs.io/en/latest/dictionary/index.ini.html>`_


Suggestions
___________

* Review the code and check that arrays only have keys defined once.
* Review carefully the code and check indirect values, like constants and static constants.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/MultipleIdenticalKeys                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Rector <ruleset-Rector>`                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-magento-arrays-multipleidenticalkeys`, :ref:`case-mediawiki-arrays-multipleidenticalkeys`                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


