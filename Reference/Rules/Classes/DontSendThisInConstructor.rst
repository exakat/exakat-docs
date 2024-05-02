.. _classes-dontsendthisinconstructor:

.. _don't-send-$this-in-constructor:

Don't Send $this In Constructor
+++++++++++++++++++++++++++++++

  Don't use ``$this`` as an argument while in the `__construct() <https://www.php.net/manual/en/language.oop5.decon.php>`_. Until the constructor is finished, the object is not finished, and may be in an unstable state. Providing it to another code may lead to `error <https://www.php.net/error>`_. 

This is true when the receiving structure puts the incoming object immediately to work, and don't store it for later use.

.. code-block:: php
   
   <?php
   
   // $this is only provided when Foo is constructed
   class Foo {
       private $bar = null;
       private $data = array();
       
       static public function build($data) {
           $foo = new Foo($data);
           // Can't build in one call. Must make it separate.
           $foo->finalize();
       }
   
       private function __construct($data) {
           // $this is provided too early
           $this->data = $data;
       }
       
       function finalize() {
           $this->bar = new Bar($this);
       }
   }
   
   // $this is provided too early, leading to error in Bar
   class Foo2 extends Foo {
       private $bar = null;
       private $data = array();
       
       function __construct($data) {
           // $this is provided too early
           $this->bar = new Bar($this);
           $this->data = $data;
       }
   }
   
   class Bar {
       function __construct(Foo $foo) {
           // the cache is now initialized with a wrong 
           $this->cache = $foo->getIt();
       }
   }
   
   ?>

See also `Don't pass this out of a constructor <http://www.javapractices.com/topic/TopicAction.do?Id=252>`_.


Suggestions
___________

* Finish the constructor first, then call an external object.
* Sending $this should be made accessible in a separate method, so external objects may call it.
* Sending the current may be the responsibility of the method creating the object.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DontSendThisInConstructor                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | $this, constructor                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-classes-dontsendthisinconstructor`, :ref:`case-contao-classes-dontsendthisinconstructor`         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


