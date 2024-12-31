.. _security-shouldusesessionregenerateid:

.. _should-use-session\_regenerateid():

Should Use session_regenerateid()
+++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Should Use session_regenerateid(): session_regenerateid() should be used when sessions are used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use session_regenerateid()
	:twitter:description: Should Use session_regenerateid(): session_regenerateid() should be used when sessions are used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use session_regenerateid()
	:og:type: article
	:og:description: session_regenerateid() should be used when sessions are used
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Security/ShouldUseSessionRegenerateId.html
	:og:locale: en
  session_regenerateid() should be used when sessions are used.

When using sessions, a session ID is assigned to the user. It is a random number, used to connect the user and its data on the server. Actually, anyone with the session ID may have access to the data. This is why those session ID are so long and complex.

A good approach to protect the session ID is to reduce its lifespan : the shorter the time of use, the better. While changing the session ID at every hit on the page may no be possible, a more reasonable approach is to change the session id when an important action is about to take place. What important means is left to the application to decide.

Based on this philosophy, a code source that uses Zend\Session but never uses Zend\Session\:\:regenerateId() has to be updated.

.. code-block:: php
   
   <?php
   
       session_start();
       
       $id = (int) $_SESSION['id'];
       // no usage of session_regenerateid() anywhere triggers the analysis
       
       // basic regeneration every 20 hits on the page. 
       if (++$_SESSION['count'] > 20) {
           session_regenerateid();
       }
   
   ?>

See also `session_regenerateid() <https://www.php.net/session_regenerate_id>`_ and `PHP Security Guide: Sessions <http://phpsec.org/projects/guide/4.html>`_.

Connex PHP features
-------------------

  + `session <https://php-dictionary.readthedocs.io/en/latest/dictionary/session.ini.html>`_


Suggestions
___________

* Add session_regenerateid() call before any important operation on the application




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/ShouldUseSessionRegenerateId                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.4                                                                                                                  |
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


