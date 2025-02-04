.. _extensions-extldap:


.. _ext-ldap:

ext/ldap
++++++++

.. meta::
	:description:
		ext/ldap: Extension ext/ldap.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/ldap
	:twitter:description: ext/ldap: Extension ext/ldap
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/ldap
	:og:type: article
	:og:description: Extension ext/ldap
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/ldap.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extldap.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extldap.html","name":"ext\/ldap","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ext\/ldap","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/ldap.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension ext/ldap.

LDAP is the Lightweight `Directory <https://www.php.net/directory>`_ Access Protocol, and is a protocol used to access '`Directory <https://www.php.net/directory>`_ Servers'. The `Directory <https://www.php.net/directory>`_ is a special kind of database that holds information in a tree structure.

.. code-block:: php
   
   <?php
   // basic sequence with LDAP is connect, bind, search, interpret search
   // result, close connection
   
   echo '<h3>LDAP query test</h3>';
   echo 'Connecting ...';
   $ds=ldap_connect('localhost');  // must be a valid LDAP server!
   echo 'connect result is ' . $ds . '<br />';
   
   if ($ds) { 
       echo 'Binding ...'; 
       $r=ldap_bind($ds);     // this is an 'anonymous' bind, typically
                              // read-only access
       echo 'Bind result is ' . $r . '<br />';
   
       echo 'Searching for (sn=S*) ...';
       // Search surname entry
       $sr=ldap_search($ds, 'o=My Company, c=US', 'sn=S*');  
       echo 'Search result is ' . $sr . '<br />';
   
       echo 'Number of entries returned is ' . ldap_count_entries($ds, $sr) . '<br />';
   
       echo 'Getting entries ...<p>';
       $info = ldap_get_entries($ds, $sr);
       echo 'Data for ' . $info['count'] . ' items returned:<p>';
   
       for ($i=0; $i<$info['count']; $i++) {
           echo 'dn is: ' . $info[$i]['dn'] . '<br />';
           echo 'first cn entry is: ' . $info[$i]['cn'][0] . '<br />';
           echo 'first email entry is: ' . $info[$i]['mail'][0] . '<br /><hr />';
       }
   
       echo 'Closing connection';
       ldap_close($ds);
   
   } else {
       echo '<h4>Unable to connect to LDAP server</h4>';
   }
   ?>

See also `Lightweight Directory Access Protocol <https://www.php.net/manual/en/book.ldap.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extldap                                                                                                                                                                      |
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


