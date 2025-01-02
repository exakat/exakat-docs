.. _extensions-extsvm:

.. _ext-svm:

ext/svm
+++++++

.. meta::
	:description:
		ext/svm: Extension ``SVM``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/svm
	:twitter:description: ext/svm: Extension ``SVM``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/svm
	:og:type: article
	:og:description: Extension ``SVM``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/svm.html
	:og:locale: en
Extension ``SVM``.

``SVM`` is in interface with the ``libsvm``, from . ``libsvm``is a library for Support Vector Machines, a classification tool for machine learning.

.. code-block:: php
   
   <?php
      $data = array(
          array(-1, 1 => 0.43, 3 => 0.12, 9284 => 0.2),
          array(1, 1 => 0.22, 5 => 0.01, 94 => 0.11),
      );
      
      $svm = new SVM();
      $model = $svm->train($data);
      
      $data = array(1 => 0.43, 3 => 0.12, 9284 => 0.2);
      $result = $model->predict($data);
      var_dump($result);
      $model->save('model.svm');
   ?>

See also `SVM <http://www.php.net/svm>`_, `LIBSVM -- A Library for Support Vector Machines <https://www.csie.ntu.edu.tw/~cjlin/libsvm/>`_, `ext/svm <https://pecl.php.net/package/svm>`_  and `ianbarber/php-svm <https://github.com/ianbarber/php-svm>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsvm                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.8                                                                                                                                                                                   |
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


