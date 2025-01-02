.. _classes-multipleclassesinfile:

.. _multiple-classes-in-one-file:

Multiple Classes In One File
++++++++++++++++++++++++++++

.. meta::
	:description:
		Multiple Classes In One File: It is regarded as a bad practice to store several classes in the same file.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Classes In One File
	:twitter:description: Multiple Classes In One File: It is regarded as a bad practice to store several classes in the same file
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Classes In One File
	:og:type: article
	:og:description: It is regarded as a bad practice to store several classes in the same file
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Classes In One File.html
	:og:locale: en
It is regarded as a bad practice to store several classes in the same file. This is usually done to make life of __autoload() easier. 

It is often unexpected to find class ``foo`` in the ``bar.php`` file. This is also the case for interfaces and traits.

One good reason to have multiple classes in one file is to reduce include time by providing everything into one nice include.

.. code-block:: php
   
   <?php
   
   // three classes in the same file
   class foo {}
   class bar {}
   class foobar{}
   
   ?>

See also `Is it a bad practice to have multiple classes in the same file? <https://stackoverflow.com/questions/360643/is-it-a-bad-practice-to-have-multiple-classes-in-the-same-file>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Split the file into smaller files, one for each class




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MultipleClassesInFile                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Coding conventions <ruleset-Coding-conventions>`                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


