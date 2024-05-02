.. _structures-nohardcodedip:

.. _no-hardcoded-ip:

No Hardcoded Ip
+++++++++++++++

  Do not leave hard coded IP in your code.

It is recommended to move such configuration in external files or databases, for each update. 
This may also come handy when testing. 
``127.0.0.1``, ``\:\:1`` and ``\:\:0`` are omitted, and not considered as a violation.

.. code-block:: php
   
   <?php
   
   // This IPv4 is hardcoded. 
   $ip = '183.207.224.50';
   // This IPv6 is hardcoded. 
   $ip = '2001:0db8:85a3:0000:0000:8a2e:0370:7334';
   
   // This looks like an IP
   $thisIsNotAnIP = '213.187.99.50';
   $thisIsNotAnIP = '2133:1387:9393:5330';
   
   ?>

See also `Use of Hardcoded IPv4 Addresses <https://docs.microsoft.com/en-us/windows/desktop/winsock/use-of-hardcoded-ipv4-addresses-2>`_ and `Never hard code sensitive information <https://wiki.sei.cmu.edu/confluence/display/java/MSC03-J.+Never+hard+code+sensitive+information>`_.


Suggestions
___________

* Move the hardcoded IP to an external source : environment variable, configuration file, database.
* Remove the hardcoded IP and ask for it at execution.
* Use a literal value for default messages in form.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoHardcodedIp                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Security <ruleset-Security>`                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | ip                                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-structures-nohardcodedip`, :ref:`case-nextcloud-structures-nohardcodedip`                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


