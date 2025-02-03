.. _extensions-extyar:


.. _extensions-yar:

Extensions yar
++++++++++++++

.. meta::
	:description:
		Extensions yar: yar : Yet Another RPC framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Extensions yar
	:twitter:description: Extensions yar: yar : Yet Another RPC framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Extensions yar
	:og:type: article
	:og:description: yar : Yet Another RPC framework
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Extensions yar.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extyar.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extyar.html","name":"Extensions yar","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"yar : Yet Another RPC framework","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Extensions yar.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

yar : Yet Another RPC framework.

.. code-block:: php
   
   <?php
   
   /* assume this page can be accessed by http://example.com/operator.php */
   
   class Operator {
   
       /**
        * Add two operands
        * @param interge 
        * @return interge
        */
       public function add($a, $b) {
           return $this->_add($a, $b);
       }
   
       /**
        * Sub 
        */
       public function sub($a, $b) {
           return $a - $b;
       }
   
       /**
        * Mul
        */
       public function mul($a, $b) {
           return $a * $b;
       }
   
       /**
        * Protected methods will not be exposed
        * @param interge 
        * @return interge
        */
       protected function _add($a, $b) {
           return $a + $b;
       }
   }
   
   $server = new Yar_Server(new Operator());
   $server->handle();
   ?>

See also `yar <https://github.com/laruence/yar>`_.

Connex PHP features
-------------------

  + `rpc <https://php-dictionary.readthedocs.io/en/latest/dictionary/rpc.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extyar                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


