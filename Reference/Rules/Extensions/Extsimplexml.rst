.. _extensions-extsimplexml:

.. _ext-simplexml:

ext/simplexml
+++++++++++++

  Extension ``SimpleXML``.

The ``SimpleXML`` extension provides a very simple and easily usable toolset to convert XML to an object that can be processed with normal property selectors and array iterators.


.. code-block:: php
   
   <?php
   
   $xml = <<<'XML'
   <?xml version='1.0' standalone='yes' ? >
   <movies>
    <movie>
     <title>PHP: Behind the Parser</title>
     <characters>
      <character>
       <name>Ms. Coder</name>
       <actor>Onlivia Actora</actor>
      </character>
      <character>
       <name>Mr. Coder</name>
       <actor>El Act&#211;r</actor>
      </character>
     </characters>
     <plot>
      So, this language. It's like, a programming language. Or is it a
      scripting language? All is revealed in this thrilling horror spoof
      of a documentary.
     </plot>
     <great-lines>
      <line>PHP solves all my web problems</line>
     </great-lines>
     <rating type="thumbs">7</rating>
     <rating type="stars">5</rating>
    </movie>
   </movies>
   XML;
   
   $movies = new SimpleXMLElement($xml);
   
   echo $movies->movie[0]->plot;
   ?>

See also `SimpleXML <https://www.php.net/manual/en/book.simplexml.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsimplexml                                                                                                                                                                 |
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


