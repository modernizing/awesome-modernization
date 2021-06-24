# awesome-modernization

Awesome legacy system modernization tools.

Flow:

 - target architecture
 - analysis
   - language parser
 - visualize
   - relationship
   - status
 - plan
   - tech debt
   - tasks
   - steps
 - migration
   - decoupling
   - refactor
 - guard
   - arch guard

## Code

**[Polyglot Code Explorer](https://github.com/kornysietsma/polyglot-code-explorer)** -  Multi-language source code metrics visualization 

Output samples:

![Polyglot Code](https://blog.korny.info/2020-09-01-polyglot-explorer/main_ui_sample.png)

**[Tags 2 UML](https://github.com/ruben2020/tags2uml)** -  Generates UML class diagrams, from source code. Command line tool to convert from a Exuberant-ctags tags file to a UML class diagram, through Graphviz DOT, for all object oriented languages supported by ctags 

Output:

![Tags2uml](https://raw.githubusercontent.com/ruben2020/tags2uml/master/doc/guava-eventbus.png)

**[Coca](https://github.com/inherd/coca)** -  Coca is a toolbox which is design for legacy system refactoring and analysis, includes call graph, concept analysis, api tree, design patterns suggest. Coca 是一个用于系统重构、系统迁移和系统分析的瑞士军刀。它可以分析代码中的测试坏味道、模块化分析、行数统计、分析调用与依赖、Git 分析以及自动化重构等。 

Usage:

```
coca analysis
coca arch
```

Output samples(bs):

```json
{
   "dataClass": [
      {
         "File": "examples/api/BookController.java",
         "BS": "dataClass"
      }
   ],
   "lazyElement": [
      {
         "File": "examples/api/model/BookRepresentaion.java",
         "BS": "lazyElement"
      }
   ]
}
```

## DevOps

**[Coco](https://github.com/inherd/coco)** -  An effective DevOps analysis and auto-suggest tool。Coco 是一个研发效能分析工具，如团队发展现状（根据架构复杂度及行数变更）、团队演进、历史分析等。生成可视化报告及对应的改进建议。 

Usage:

```
coco --file-history=true --git-years=3
```

Output Samples: [Coco Nginx Reports](https://inherd.org/cases/nginx/)


## Frontend


### Codemod


 - [https://github.com/facebook/jscodeshift](https://github.com/facebook/jscodeshift) jscodeshift is a toolkit for running codemods over multiple JavaScript or TypeScript files. It provides:
 - [https://github.com/cpojer/js-codemod](https://github.com/cpojer/js-codemod) js-codemod is a Codemod scripts to transform code to next generation JS.
 - [Vue-Codemod](https://github.com/vuejs/vue-codemod)
 - [https://github.com/reactjs/react-codemod](https://github.com/reactjs/react-codemod)
 - [https://github.com/psalaets/vue-jscodeshift-adapter](https://github.com/psalaets/vue-jscodeshift-adapter)

### Parser


 - [CSS Tree](https://github.com/csstree/csstree)
 - [@babel/parser](https://babeljs.io/docs/en/babel-parser)

Benchmarks

| Source | Esprima 4.0.1 | [UglifyJS2](https://github.com/mishoo/UglifyJS2) | [Traceur](https://github.com/google/traceur-compiler) | [Acorn](https://github.com/marijnh/acorn) 8.0.4 | [Shift](https://github.com/shapesecurity/shift-parser-js) | [Shift (no early errors)](https://github.com/shapesecurity/shift-parser-js) |
| --- | --- | --- | --- | --- | --- | --- |
| jQuery.Mobile 1.4.2 | 149.6 ±1.8% | 170.7 ±1.2% | 178.2 ±6.0% | 214.4 ±13.0% | 429.5 ±13.5% | 203.9 ±9.6% |
| Angular 1.2.5 | 125.0 ±2.8% | 138.2 ±2.9% | 134.5 ±2.3% | 113.8 ±2.8% | 251.5 ±1.3% | 147.1 ±1.5% |
| React 0.13.3 | 127.2 ±1.0% | 158.2 ±1.4% | 160.0 ±0.8% | 128.5 ±2.8% | 310.8 ±2.7% | 182.6 ±2.7% |
| **Total** | 401.8 ms | 467.0 ms | 472.7 ms | 456.7 ms | 991.9 ms | 533.5 ms |

### Tools

**[Lemonj](https://github.com/twfe/lemonj)** -  一个面向 CSS/LESS/SCSS 的分析、坏味道检查和自动化重构工具。 

Usage:

```
npm install lemonj -g
lemonj analysis _fixtures
```

Output:

```
Code Smell:  {
  colors: 24,
  importants: 4,
  issues: 8,
  mediaQueries: 1,
  absolute: 0,
  oddWidth: 1
}
```

## Version Control

**[Code Maat](https://github.com/adamtornhill/code-maat)** - Code Maat is a command line tool used to mine and analyze data from version-control systems (VCS).

Outputs:

```csv
statistic,                 value
number-of-commits,           919
number-of-entities,          730
number-of-entities-changed, 3397
number-of-authors,            79
```


**[git-branches-overview](https://github.com/BenoitZugmeyer/git-branches-overview)**  Visualize branches state compared to a base revision or their upstream. 

Output:

![Git Branches Overview](https://raw.githubusercontent.com/BenoitZugmeyer/git-branches-overview/master/git-branches-overview.png)


## Database

### Analysis

 - **[Z PL/SQL Analyzer](https://github.com/felipebz/zpa)** The Z PL/SQL Analyzer (or simply ZPA) is a code analyzer for PL/SQL and Oracle SQL code.
 - **[PLSQLParser](https://github.com/developeron29/PLSQLParser)** - A PLSQL parser built using ANTLR 4

### Database Optimizer

**[Soar](https://github.com/XiaoMi/soar)** 是一个对 SQL 进行优化和改写的自动化工具。 由小米人工智能与云平台的数据库团队开发与维护。

examples:

```
echo 'select * from film' | ./soar
```

### Datbase to Struct

**[xo](https://github.com/xo/xo)** is a Command line tool to generate idiomatic Go code for SQL databases supporting PostgreSQL, MySQL, SQLite, Oracle, and Microsoft SQL Server 


|              | PostgreSQL       | MySQL            | Oracle           | Microsoft SQL Server| SQLite           |
| ------------ |:----------------:|:----------------:|:----------------:|:-------------------:|:----------------:|
| Models       |:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:   |:white_check_mark:|
| Primary Keys |:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:   |:white_check_mark:|
| Foreign Keys |:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:   |:white_check_mark:|
| Indexes      |:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:   |:white_check_mark:|
| Stored Procs |:white_check_mark:|:white_check_mark:|                  |                     |                  |
| ENUM types   |:white_check_mark:|:white_check_mark:|                  |                     |                  |
| Custom types |:white_check_mark:|                  |                  |                     |                  |

**[usql](https://github.com/xo/usql)** is a universal command-line interface for PostgreSQL, MySQL, Oracle Database, SQLite3, Microsoft SQL Server, and many other databases including NoSQL and non-relational databases!

Usage

```bash
# connect to a postgres database
$ usql postgres://booktest@localhost/booktest

# connect to an oracle database
$ usql oracle://user:pass@host/oracle.sid

# connect to a postgres database and run the commands contained in script.sql
$ usql pg://localhost/ -f script.sql
```

**[gormt](https://github.com/xxjwxc/gormt)** -  database to golang struct.

Usage:

```

Flags:
  -d, --database string   数据库名
  -f, --foreign           是否导出外键关联
  -F, --fun               是否导出函数
  -g, --gui               是否ui显示模式
  -h, --help              help for main
  -H, --host string       数据库地址.(注意-H为大写)
  -o, --outdir string     输出目录
  -p, --password string   密码.
      --port int          端口号 (default 3306)
  -s, --singular          是否禁用表名复数
  -b, --table_names string 表名称  
  -l, --url string        url标签(json,url)
  -u, --user string       用户名.
```

**[db2struct](https://github.com/Shelnutt2/db2struct)** - db2struct package produces a usable golang struct from a given database table for use in a `.go` file.

target: Golang

Usage:

```
db2struct --host localhost -d example.com -t users --package example --struct user -p --user exampleUser --guregu --gorm
```

Output

```
package example

type User struct {
  ID              int   `gorm:"column:id"`
  UserName        string `gorm:"column:user_name"`
  NumberOfLogins  null.Int `gorm:"column:number_of_logins"`
  LastName        null.String `gorm:"column:LAST_NAME"`
}
```

## Visual


**[GoCity](https://github.com/rodrigo-brito/gocity)** -  is an implementation of the Code City metaphor for visualizing source code. GoCity represents a Go program as a city, as follows:

 - Folders are districts
 - Files are buildings
 - Structs are represented as buildings on the top of their files.

**[Toxicity](https://github.com/softvis/toxicity-reloaded)** -  A rewrite of the original Toxicity chart in Javascript using D3.js 

**[Blast Radius](https://github.com/28mm/blast-radius)** - s is a tool for reasoning about Terraform dependency graphs with interactive visualizations.

Samples:

![Blast Radius](https://raw.githubusercontent.com/28mm/blast-radius/master/doc/blastradius-interactive.png)

**[CodeFlower](https://github.com/fzaninotto/CodeFlower)** -  Source code visualization utility written in JavaScript with d3.js. Does your code look beautiful? 

Output:

![Examples](https://raw.githubusercontent.com/fzaninotto/CodeFlower/master/images/faker.png)




