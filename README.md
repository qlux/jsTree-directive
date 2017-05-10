jsTree-directive
================

An Angular Directive for jsTree

* [Documentation](http://jstree-directive.herokuapp.com/#/basic)

Install using `bower`

```bash
$ bower i jstree-directive
```

### Tutorial 

[Building a Web Based File Browser with jsTree, Angularjs and Expressjs](http://thejackalofjavascript.com/file-browser-with-jstree-angularjs-and-expressjs)

**_PS : Do note that if you want to make your app 100% Angular, load the jsTree Javascript source using an Angular provider as a dependency to jstree.directive._**

### Basic Example

```
<js-tree tree-id="treeId" tree-data="scope" tree-model="treeData" tree-instance="treeInstance" tree-plugins="checkbox" tree-events="ready:readyCB"></div>
```

### Load a config from the scope
```
<js-tree tree-config="dataTreeConfig"></div>
```
```
$scope.dataTreeConfig = 
    {
        treeId			    :	"treeName",
      	treeInstance	    :	"treeNameInstance",
      	treePlugins		    :	"table,sort,contextmenu",
      	// Default sort function for folders>files
      	sort			    : function(a,b){
      	    return a>b
        },
        treeContextmenu     :   "contextMenu",
        treeEvents          :   "select_node:nodeSelected;ready:selectFirstNode;move_node:moveNode"
    }
```