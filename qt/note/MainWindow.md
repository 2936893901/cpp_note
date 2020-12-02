# `MainWindow`
## `QMenubar`
1. 创建菜单栏（只能最多有一个，且不需要放在对象树上），头文件<QMenuBar>
```c++
QMenuBar *bar = menuBar();
```
2. 将菜单栏放入窗口
```c++
setMenuBar(bar);
```
3. 创建菜单
```c++
QMenu *firstMenu = bar->addMenu("first");
```
4. 创建菜单项
```c++
firstMenu->addAction("one");
// 添加分隔符
firstMenu->addSeparator();
```
## `QToolBar`
1. 创建工具栏，头文件<QToolBar>
```c++
QToolBar *toolBar = new QToolBar(this);
```
2. 添加到窗口中
```c++
// 工具栏停靠的位置(第一个参数可以是Qt::TopToolBarArea, Qt::LeftToolBarArea, Qt::RightToolBarArea, Qt::BottomToolBarArea)
addToolBar(Qt::ToolBarArea area = Qt, toolBar);
```
3. 设置停靠
```c++
// 设置左右停靠
toolBar->setAllowedAreas(Qt::LeftToolBarArea | Qt::RightToolBarArea);
```
4. 设置浮动
```c++
// 设置不浮动
toolBar->setFloatable(false);
```
5. 设置移动（总开关）
```c++
// 设置不能移动
toolBar->setMovable(false);
```