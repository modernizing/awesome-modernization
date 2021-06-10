# awesome-modernization

Awesome legacy system modernization tools.

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

**[git-branches-overview](https://github.com/BenoitZugmeyer/git-branches-overview)**  Visualize branches state compared to a base revision or their upstream. 

Output:

![Git Branches Overview](https://raw.githubusercontent.com/BenoitZugmeyer/git-branches-overview/master/git-branches-overview.png)


## Database


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


**[CodeFlower](https://github.com/fzaninotto/CodeFlower)** -  Source code visualization utility written in JavaScript with d3.js. Does your code look beautiful? 

Output:

![Examples](https://raw.githubusercontent.com/fzaninotto/CodeFlower/master/images/faker.png)




