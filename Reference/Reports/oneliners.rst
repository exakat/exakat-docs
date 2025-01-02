.. _report-oneliners:

OneLiners
+++++++++

OneLiners
_________

.. meta::
	:description:
		OneLiners: The One Liners report collects one liner usages, which makes using IDE hard..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: OneLiners
	:twitter:description: OneLiners: The One Liners report collects one liner usages, which makes using IDE hard.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: OneLiners
	:og:type: article
	:og:description: The One Liners report collects one liner usages, which makes using IDE hard.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The One Liners report collects one liner usages, which makes using IDE hard.

The One Liners report is based on Andreas Möllers's post `Avoiding one-liners in PHP <https://localheinz.com/articles/2023/03/18/avoiding-one-liners-in-php/#content-throw-expressions>`_. It reports all the one liners from that article.


::

    /app/Infra/functions.php:305	Php/Coalesce	Coalesce	$message ?: __('操作成功')
    /app/Infra/functions.php:305	Php/ShortTernary	Short Ternary	$message ?: __('操作成功')
    /app/Infra/Model.php:797	Php/Coalesce	Coalesce	$fields ?: $options['field']
    /app/Infra/Model.php:797	Php/Coalesce	Coalesce	$table ?: $this->getTableName( )
    /app/Infra/Model.php:797	Php/ShortTernary	Short Ternary	$fields ?: $options['field']
    /app/Infra/Model.php:797	Php/ShortTernary	Short Ternary	$table ?: $this->getTableName( )
    /app/Infra/Model.php:1581	Php/Coalesce	Coalesce	preg_replace('/[A-Z]/', '_\\0', $name) ?: ''
    /app/Infra/Model.php:1581	Php/ShortTernary	Short Ternary	preg_replace('/[A-Z]/', '_\\0', $name) ?: ''
    /app/Infra/Model.php:999	Php/Coalesce	Coalesce	$type ?: (!empty($data[$this->getPk( )]) ? self::MODEL_UPDATE : self::MODEL_INSERT)
    /app/Infra/Model.php:999	Php/ShortTernary	Short Ternary	$type ?: (!empty($data[$this->getPk( )]) ? self::MODEL_UPDATE : self::MODEL_INSERT)
    /app/Infra/Model.php:1326	Php/Coalesce	Coalesce	$fields ?: '*'
    /app/Infra/Model.php:1326	Php/ShortTernary	Short Ternary	$fields ?: '*'
    /app/Infra/Model.php:1578	Php/Coalesce	Coalesce	preg_replace_callback('/_([a-zA-Z])/', function ($match) { /**/ } , $name) ?: ''
    /app/Infra/Model.php:1578	Php/ShortTernary	Short Ternary	preg_replace_callback('/_([a-zA-Z])/', function ($match) { /**/ } , $name) ?: ''
    /app/Infra/Code.php:28	Php/Coalesce	Coalesce	Cache::get('captcha:' . $id) ?: ''
    /app/Infra/Code.php:28	Php/ShortTernary	Short Ternary	Cache::get('captcha:' . $id) ?: ''
    /app/Infra/PermissionCache.php:27	Php/Coalesce	Coalesce	(array) Cache::get('permission:' . $id) ?: ['static' => [ ], 'dynamic' => [ ]]
    /app/Infra/PermissionCache.php:27	Php/ShortTernary	Short Ternary	(array) Cache::get('permission:' . $id) ?: ['static' => [ ], 'dynamic' => [ ]]
    /app/Controller/Swagger/Index.php:39	Php/Coalesce	Coalesce	json_encode($openApi) ?: ''
    /app/Controller/Swagger/Index.php:39	Php/ShortTernary	Short Ternary	json_encode($openApi) ?: ''
    /app/Domain/Service/Search/Search.php:45	Php/Coalesce	Coalesce	$subService ?: $v
    /app/Domain/Service/Search/Search.php:45	Php/ShortTernary	Short Ternary	$subService ?: $v
    /app/Infra/Repository/User/User.php:28	Functions/UseArrowFunctions	Use Arrow Functions	fn (Select $select) => $select->where('name', $name)
    /app/Infra/Repository/User/User.php:41	Functions/UseArrowFunctions	Use Arrow Functions	fn (Select $select) => $select->where('id', $id)
    /app/Infra/ModelTest.php:3472	Functions/UseArrowFunctions	Use Arrow Functions	fn ( ) => $baseBrandModel->trans2(['first' => 'new1', 'second' => 'new2',  ])
    /app/Infra/ModelTest.php:3500	Functions/UseArrowFunctions	Use Arrow Functions	fn ( ) => $baseBrandModel->trans3(['first' => 'new1', 'second' => 'new2',  ])
    /app/Domain/Service/User/User/Users.php:23	Functions/UseArrowFunctions	Use Arrow Functions	fn (Select $select) => $select->eager(['role'])
    /app/Domain/Entity/Product/BaseBrandModel.php:237	Functions/UseArrowFunctions	Use Arrow Functions	fn ( ) => $this->trans3($in)
    /app/Domain/Entity/Product/BaseBrandModel.php:242	Functions/UseArrowFunctions	Use Arrow Functions	fn ( ) => $this->trans3($in)
    /app/Middleware/Filter.php:73	Functions/UseArrowFunctions	Use Arrow Functions	fn (mixed &$value, string $key) => $value = $this->transformValue($value, $key)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | OneLiners                                                        |
+--------------+------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | Text                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'oneliners'.                           |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


