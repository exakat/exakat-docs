.. _report-compatibilityphp56:

CompatibilityPHP56
++++++++++++++++++

CompatibilityPHP56
__________________

The CompatibilityPHP56 report list all detected issues with PHP 5.6 compatibility.

The CompatibilityPHP56 report displays one result per line, grouped by rule, and ordered by file and line number. Here is an example : 

::
    
   /path/from/project/root/to/file:line[space]name of analysis
   
   
This format is fast, and fitted for human review. It is the same format as PerRule. 



::

    ----------------------------------------------------------------------------------------------------
     Coalesce Equal (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#php-coalesceequal)
    ----------------------------------------------------------------------------------------------------
     /src/Bridges/Tracy/BlueScreenPanel.php:25                    $blueScreen ??= Tracy\Debugger::getBlueScreen( )
     /src/Bridges/Tracy/LattePanel.php:32                         $bar ??= Tracy\Debugger::getBar( )      
     /src/Latte/Compiler/Lexer.php:371                            $type ??= $this->defaultSyntax          
     /src/Latte/Compiler/Nodes/FragmentNode.php:38                $this->line ??= $node->line             
     /src/Latte/Compiler/Parser.php:723                           $layer ??= $this->layer                 
     /src/Latte/Compiler/PhpWriter.php:137                        $uniq ??= '$' . bin2hex(random_bytes(5))
     /src/Latte/Compiler/PhpWriter.php:194                        $tokens ??= $this->tokens               
     /src/Latte/Extensions/Blueprint.php:83                       $native ??= (PHP_VERSION_ID >= 70400)   
     /src/Latte/Extensions/Filters.php:52                         $info->contentType ??= 'html'           
     /src/Latte/Runtime/Template.php:340                          $block ??= new Block                    
     /src/Latte/Runtime/Template.php:399                          $destId ??= $staticId                   
    ----------------------------------------------------------------------------------------------------
    
    
    ----------------------------------------------------------------------------------------------------
     Const Visibility Usage (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#classes-constvisibilityusage)
    ----------------------------------------------------------------------------------------------------
     /src/Latte/Compiler/Lexer.php:26                             public const RE_STRING = '\'(?:\\\\.|[^\'\\\\])*+\'|"(?:\\\\.|[^"\\\\])*+"'
     /src/Latte/Compiler/Lexer.php:29                             public const RE_TAG_NAME = '[a-zA-Z][a-zA-Z0-9:_.-]*'
     /src/Latte/Compiler/Lexer.php:30                             public const RE_VALUE_NAME = '[^\p{C} "\'<>=`/{}]+'
     /src/Latte/Compiler/Lexer.php:31                             public const RE_INDENT = '((?<=\n|^)[ \t]+)?'
     /src/Latte/Compiler/Lexer.php:34                             public const N_PREFIX = 'n:'            
     /src/Latte/Compiler/Lexer.php:37                             public const STATE_PLAIN_TEXT = 'statePlain', STATE_HTML_TEXT = 'stateHtmlText'
     /src/Latte/Compiler/MacroTokens.php:18                       public const T_WHITESPACE = 1, T_COMMENT = 2, T_SYMBOL = 3, T_NUMBER = 4, T_VARIABLE = 5, T_STRING = 6, T_CAST = 7, T_KEYWORD = 8, T_CHAR = 9
     /src/Latte/Compiler/MacroTokens.php:29                       public const SIGNIFICANT = [self::T_SYMBOL, self::T_NUMBER, self::T_VARIABLE, self::T_STRING, self::T_CAST, self::T_KEYWORD, self::T_CHAR], NON_SIGNIFICANT = [self::T_COMMENT, self::T_WHITESPACE]
     /src/Latte/Compiler/NodeTraverser.php:15                     public const DONT_TRAVERSE_CHILDREN = 1 
     /src/Latte/Compiler/NodeTraverser.php:16                     public const STOP_TRAVERSAL = 2         
     /src/Latte/Compiler/Parser.php:30                            public const LOCATION_HEAD = 1, LOCATION_TEXT = 2, LOCATION_TAG = 3
     /src/Latte/Compiler/Tag.php:25                               public const PREFIX_INNER = 'inner', PREFIX_TAG = 'tag', PREFIX_NONE = ''
     /src/Latte/Compiler/Token.php:20                             public const TEXT = 'text'              
     /src/Latte/Compiler/Token.php:21                             public const WHITESPACE = 'whitespace'  
     /src/Latte/Compiler/Token.php:22                             public const SLASH = 'slash'            
     /src/Latte/Compiler/Token.php:23                             public const EQUALS = 'equals'          
     /src/Latte/Compiler/Token.php:24                             public const QUOTE = 'quote'            
     /src/Latte/Compiler/Token.php:26                             public const LATTE_TAG_OPEN = 'latteTagOpen'
     /src/Latte/Compiler/Token.php:27                             public const LATTE_TAG_END = 'latteTagEnd'
     /src/Latte/Compiler/Token.php:28                             public const LATTE_NAME = 'latteName'   
     /src/Latte/Compiler/Token.php:29                             public const LATTE_ARGS = 'latteArgs'   
     /src/Latte/Compiler/Token.php:30                             public const LATTE_COMMENT_OPEN = 'latteCommentOpen'
     /src/Latte/Compiler/Token.php:31                             public const LATTE_COMMENT_CLOSE = 'latteCommentClose'
     /src/Latte/Compiler/Token.php:33                             public const HTML_TAG_OPEN = 'htmlTagOpen'
     /src/Latte/Compiler/Token.php:34                             public const HTML_TAG_CLOSE = 'htmlTagClose'
     /src/Latte/Compiler/Token.php:35                             public const HTML_COMMENT_OPEN = 'htmlCommentOpen'
     /src/Latte/Compiler/Token.php:36                             public const HTML_COMMENT_CLOSE = 'htmlCommentClose'
     /src/Latte/Compiler/Token.php:37                             public const HTML_BOGUS_TAG_OPEN = 'htmlBogusTagOpen'
     /src/Latte/Compiler/Token.php:38                             public const HTML_NAME = 'htmlName'     
     /src/Latte/Compiler/Tokenizer.php:25                         public const VALUE = 0, OFFSET = 1, TYPE = 2
     /src/Latte/Context.php:19                                    public const TEXT = 'text', HTML = 'html', XML = 'xml', JS = 'js', CSS = 'css', ICAL = 'ical'
     /src/Latte/Context.php:27                                    public const HTML_TEXT = null, HTML_COMMENT = 'Comment', HTML_BOGUSTAG = 'Bogus', HTML_CSS = 'Css', HTML_JS = 'Js', HTML_TAG = 'Tag', HTML_ATTRIBUTE = 'Attr', HTML_ATTRIBUTE_JS = 'AttrJs', HTML_ATTRIBUTE_CSS = 'AttrCss', HTML_ATTRIBUTE_URL = 'AttrUrl', HTML_ATTRIBUTE_UNQUOTED = 'Unquoted'
     /src/Latte/Context.php:40                                    public const XML_TEXT = null, XML_COMMENT = 'Comment', XML_BOGUSTAG = 'Bogus', XML_TAG = 'Tag', XML_ATTRIBUTE = 'Attr'
     /src/Latte/Engine.php:20                                     public const VERSION = '3.0.0-dev'      
     /src/Latte/Engine.php:21                                     public const VERSION_ID = 30000         
     /src/Latte/Engine.php:24                                     public const CONTENT_HTML = Context::HTML, CONTENT_XML = Context::XML, CONTENT_JS = Context::JS, CONTENT_CSS = Context::CSS, CONTENT_ICAL = Context::ICAL, CONTENT_TEXT = Context::TEXT
     /src/Latte/Runtime/SnippetDriver.php:23                      public const TYPE_STATIC = 'static', TYPE_DYNAMIC = 'dynamic', TYPE_AREA = 'area'
     /src/Latte/Runtime/Template.php:24                           public const LAYER_TOP = 0, LAYER_SNIPPET = 'snippet', LAYER_LOCAL = 'local'
     /src/Latte/Runtime/Template.php:29                           protected const CONTENT_TYPE = Latte\Context::HTML
     /src/Latte/Runtime/Template.php:31                           protected const BLOCKS = [ ]            
     /src/Latte/Sandbox/SecurityPolicy.php:22                     public const ALL = ['*']                
     /src/Latte/exceptions.php:45                                 public const MESSAGES = [PREG_INTERNAL_ERROR => 'Internal error', PREG_BACKTRACK_LIMIT_ERROR => 'Backtrack limit was exhausted', PREG_RECURSION_LIMIT_ERROR => 'Recursion limit was exhausted', PREG_BAD_UTF8_ERROR => 'Malformed UTF-8 data', PREG_BAD_UTF8_OFFSET_ERROR => 'Offset didn\'t correspond to the begin of a valid UTF-8 code point', 6 => 'Failed due to limited JIT stack space',  ]
    ----------------------------------------------------------------------------------------------------
    
    ----------------------------------------------------------------------------------------------------
     Generator Cannot Return (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#functions-generatorcannotreturn)
    ----------------------------------------------------------------------------------------------------
     /src/Latte/Compiler/Lexer.php:321                            private function match(string $re) : \Generator { /**/ } 
     /src/Latte/Compiler/Node.php:21                              public function &getIterator( ) : \Generator { /**/ } 
     /src/Latte/Extensions/CoreExtension.php:229                  public function parseSyntax(Tag $tag, Parser $parser) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/BlockNode.php:37                 public static function parse(Tag $tag, Parser $parser) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/CaptureNode.php:33               public static function parse(Tag $tag) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/DefineNode.php:36                public static function parse(Tag $tag, Parser $parser) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/EmbedNode.php:38                 public static function parse(Tag $tag, Parser $parser) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/FirstLastSepNode.php:36          public static function parse(Tag $tag) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/ForNode.php:31                   public static function parse(Tag $tag) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/ForeachNode.php:37               public static function parse(Tag $tag) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/IfChangedNode.php:32             public static function parse(Tag $tag) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/IfContentNode.php:33             public static function parse(Tag $tag, Parser $parser) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/IfNode.php:40                    public static function parse(Tag $tag, Parser $parser) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/IterateWhileNode.php:34          public static function parse(Tag $tag) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/SnippetAreaNode.php:36           public static function parse(Tag $tag, Parser $parser) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/SnippetNode.php:41               public static function parse(Tag $tag, Parser $parser) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/SpacelessNode.php:30             public static function parse(Tag $tag) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/SwitchNode.php:32                public static function parse(Tag $tag) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/TranslateNode.php:34             public static function parse(Tag $tag, Parser $parser) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/TryNode.php:30                   public static function parse(Tag $tag) : \Generator { /**/ } 
     /src/Latte/Extensions/Nodes/WhileNode.php:32                 public static function parse(Tag $tag) : \Generator { /**/ } 
    ----------------------------------------------------------------------------------------------------
    
    
    ----------------------------------------------------------------------------------------------------
     List Short Syntax (https://exakat.readthedocs.io/en/latest/Reference/Rules.html#php-listshortsyntax)
    ----------------------------------------------------------------------------------------------------
     /src/Latte/Compiler/Parser.php:311                           [$prevDepth, $this->htmlDepth]          
     /src/Latte/Compiler/Parser.php:644                           [$gen, $line]                           
     /src/Latte/Compiler/PhpHelpers.php:35                        [$name, $token]                         
     /src/Latte/Compiler/PhpWriter.php:85                         [ , $l, $source, $format, $cond, $r]    
     /src/Latte/Compiler/PhpWriter.php:865                        [$contentType, $context, $flag]         
     /src/Latte/Compiler/PhpWriter.php:866                        [$lq, $rq]                              
     /src/Latte/Compiler/Tokenizer.php:76                         [$line, $col]                           
     /src/Latte/Extensions/CoreExtension.php:233                  [$inner]                                
     /src/Latte/Extensions/CoreExtension.php:247                  [$name, $mod]                           
     /src/Latte/Extensions/Nodes/BlockNode.php:40                 [$name, $local]                         
     /src/Latte/Extensions/Nodes/BlockNode.php:53                 [$node->content]                        
     /src/Latte/Extensions/Nodes/CaptureNode.php:42               [$node->content]                        
     /src/Latte/Extensions/Nodes/DefineNode.php:39                [$name, $local]                         
     /src/Latte/Extensions/Nodes/DefineNode.php:49                [$node->content]                        
     /src/Latte/Extensions/Nodes/EmbedNode.php:43                 [$node->name, $mode]                    
     /src/Latte/Extensions/Nodes/EmbedNode.php:50                 [$node->blocks]                         
     /src/Latte/Extensions/Nodes/FirstLastSepNode.php:51          [$node->then, $nextTag]                 
     /src/Latte/Extensions/Nodes/FirstLastSepNode.php:54          [$node->else]                           
     /src/Latte/Extensions/Nodes/ForNode.php:36                   [$node->content]                        
     /src/Latte/Extensions/Nodes/ForeachNode.php:57               [$node->content, $nextTag]              
     /src/Latte/Extensions/Nodes/ForeachNode.php:60               [$node->else]                           
     /src/Latte/Extensions/Nodes/IfChangedNode.php:43             [$node->then, $nextTag]                 
     /src/Latte/Extensions/Nodes/IfChangedNode.php:46             [$node->else]                           
     /src/Latte/Extensions/Nodes/IfContentNode.php:38             [$node->content]                        
     /src/Latte/Extensions/Nodes/IfNode.php:158                   [$name, $block]                         
     /src/Latte/Extensions/Nodes/IfNode.php:54                    [$node->then, $nextTag]                 
     /src/Latte/Extensions/Nodes/IfNode.php:61                    [$node->else, $nextTag]                 
     /src/Latte/Extensions/Nodes/IncludeBlockNode.php:40          [$name]                                 
     /src/Latte/Extensions/Nodes/IncludeFileNode.php:37           [$node->file]                           
     /src/Latte/Extensions/Nodes/IterateWhileNode.php:49          [$node->content, $nextTag]              
     /src/Latte/Extensions/Nodes/SnippetAreaNode.php:44           [$node->content]                        
     /src/Latte/Extensions/Nodes/SnippetNode.php:85               [$node->content]                        
     /src/Latte/Extensions/Nodes/SpacelessNode.php:34             [$node->content]                        
     /src/Latte/Extensions/Nodes/SwitchNode.php:109               [&$case, &$stmt]                        
     /src/Latte/Extensions/Nodes/SwitchNode.php:43                [$content, $nextTag]                    
     /src/Latte/Extensions/Nodes/SwitchNode.php:55                [$content, $nextTag]                    
     /src/Latte/Extensions/Nodes/SwitchNode.php:63                [$content, $nextTag]                    
     /src/Latte/Extensions/Nodes/SwitchNode.php:82                [$condition, $stmt]                     
     /src/Latte/Extensions/Nodes/TranslateNode.php:48             [$node->content]                        
     /src/Latte/Extensions/Nodes/TryNode.php:40                   [$node->try, $nextTag]                  
     /src/Latte/Extensions/Nodes/TryNode.php:43                   [$node->else]                           
     /src/Latte/Extensions/Nodes/WhileNode.php:41                 [$node->content, $nextTag]              
     /src/Latte/Runtime/FilterExecutor.php:119                    [$callback, $aware]                     
     /src/Latte/Runtime/FilterExecutor.php:67                     [$callback, $aware]                     
     /src/Latte/Runtime/SnippetDriver.php:76                      [$name, $obStarted]                     
     /src/Latte/Runtime/Template.php:402                          [$method, $contentType]                 
    ----------------------------------------------------------------------------------------------------
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | CompatibilityPHP56                                               |
+--------------+------------------------------------------------------------------+
| Rulesets     | CompatibilityPHP56.                                              |
+--------------+------------------------------------------------------------------+
| Type         | Text                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'stdout'.                              |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


