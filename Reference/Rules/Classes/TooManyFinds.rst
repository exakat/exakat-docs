.. _classes-toomanyfinds:

.. _too-many-finds:

Too Many Finds
++++++++++++++

  Too many methods called 'find*' in this class. It is may be time to consider the `Specification pattern <https://en.wikipedia.org/wiki/Specification_pattern>`_.

.. code-block:: php
   
   <?php
   
   // quite a fishy interface
   interface UserInterface {
       public function findByEmail($email);
       public function findByUsername($username);
       public function findByFirstName($firstname);
       public function findByLastName($lastname);
       public function findByName($name);
       public function findById($id);
   
       public function insert($user);
       public function update($user);
   }
   
   ?>

+--------------+---------+---------+-------------------------------------------------------------------------------------------+
| Name         | Default | Type    | Description                                                                               |
+--------------+---------+---------+-------------------------------------------------------------------------------------------+
| minimumFinds | 5       | integer | Minimal number of prefixed methods to report.                                             |
+--------------+---------+---------+-------------------------------------------------------------------------------------------+
| findPrefix   | find    | string  | list of prefix to use when detecting the 'find'. Comma-separated list, case insensitive.  |
+--------------+---------+---------+-------------------------------------------------------------------------------------------+
| findSuffix   |         | string  | list of fix to use when detecting the 'find'. Comma-separated list, case insensitive.     |
+--------------+---------+---------+-------------------------------------------------------------------------------------------+



See also `On Taming Repository Classes in Doctrine <https://beberlei.de/2013/03/04/doctrine_repositories.html>`_ and `specifications <https://slides.pixelart.at/2017-02-04/fosdem/specifications/#/>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Split the class into smaller classes
* Remove some of the find* methods




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/TooManyFinds                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


