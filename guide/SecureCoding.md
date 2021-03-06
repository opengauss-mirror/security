- [1.代码风格](#1%E4%BB%A3%E7%A0%81%E9%A3%8E%E6%A0%BC)
  - [1.1 命名](#11-%E5%91%BD%E5%90%8D)
      - [NAM.01 使用统一的命名风格](#nam01-%E4%BD%BF%E7%94%A8%E7%BB%9F%E4%B8%80%E7%9A%84%E5%91%BD%E5%90%8D%E9%A3%8E%E6%A0%BC)
  - [1.2 注释](#12-%E6%B3%A8%E9%87%8A)
      - [CMT.01 注释符与注释内容间要有1空格](#cmt01-%E6%B3%A8%E9%87%8A%E7%AC%A6%E4%B8%8E%E6%B3%A8%E9%87%8A%E5%86%85%E5%AE%B9%E9%97%B4%E8%A6%81%E6%9C%891%E7%A9%BA%E6%A0%BC)
      - [CMT.02 代码注释置于对应代码的上方或右边](#cmt02-%E4%BB%A3%E7%A0%81%E6%B3%A8%E9%87%8A%E7%BD%AE%E4%BA%8E%E5%AF%B9%E5%BA%94%E4%BB%A3%E7%A0%81%E7%9A%84%E4%B8%8A%E6%96%B9%E6%88%96%E5%8F%B3%E8%BE%B9)
      - [CMT.03 文件头注释包含版权说明](#cmt03-%E6%96%87%E4%BB%B6%E5%A4%B4%E6%B3%A8%E9%87%8A%E5%8C%85%E5%90%AB%E7%89%88%E6%9D%83%E8%AF%B4%E6%98%8E)
      - [CMT.04 不写空有格式的函数头注释](#cmt04-%E4%B8%8D%E5%86%99%E7%A9%BA%E6%9C%89%E6%A0%BC%E5%BC%8F%E7%9A%84%E5%87%BD%E6%95%B0%E5%A4%B4%E6%B3%A8%E9%87%8A)
  - [1.3 格式](#13-%E6%A0%BC%E5%BC%8F)
    - [1.3.1 编码](#131-%E7%BC%96%E7%A0%81)
      - [FMT.01 非纯ASCII码源文件使用 UTF-8 编码](#fmt01-%E9%9D%9E%E7%BA%AFascii%E7%A0%81%E6%BA%90%E6%96%87%E4%BB%B6%E4%BD%BF%E7%94%A8-utf-8-%E7%BC%96%E7%A0%81)
    - [1.3.2 缩进](#132-%E7%BC%A9%E8%BF%9B)
      - [FMT.02 使用空格进行缩进，每次缩进4个空格](#fmt02-%E4%BD%BF%E7%94%A8%E7%A9%BA%E6%A0%BC%E8%BF%9B%E8%A1%8C%E7%BC%A9%E8%BF%9B%E6%AF%8F%E6%AC%A1%E7%BC%A9%E8%BF%9B4%E4%B8%AA%E7%A9%BA%E6%A0%BC)
    - [1.3.3 大括号](#133-%E5%A4%A7%E6%8B%AC%E5%8F%B7)
      - [FMT.03 使用统一的大括号换行风格](#fmt03-%E4%BD%BF%E7%94%A8%E7%BB%9F%E4%B8%80%E7%9A%84%E5%A4%A7%E6%8B%AC%E5%8F%B7%E6%8D%A2%E8%A1%8C%E9%A3%8E%E6%A0%BC)
    - [1.3.4 行宽](#134-%E8%A1%8C%E5%AE%BD)
      - [FMT.04 一行只有一条语句](#fmt04-%E4%B8%80%E8%A1%8C%E5%8F%AA%E6%9C%89%E4%B8%80%E6%9D%A1%E8%AF%AD%E5%8F%A5)
      - [FMT.05 行宽不超过 120 个字符](#fmt05-%E8%A1%8C%E5%AE%BD%E4%B8%8D%E8%B6%85%E8%BF%87-120-%E4%B8%AA%E5%AD%97%E7%AC%A6)
      - [FMT.06 换行时将操作符留在行末，新行缩进一层或进行同类对齐](#fmt06-%E6%8D%A2%E8%A1%8C%E6%97%B6%E5%B0%86%E6%93%8D%E4%BD%9C%E7%AC%A6%E7%95%99%E5%9C%A8%E8%A1%8C%E6%9C%AB%E6%96%B0%E8%A1%8C%E7%BC%A9%E8%BF%9B%E4%B8%80%E5%B1%82%E6%88%96%E8%BF%9B%E8%A1%8C%E5%90%8C%E7%B1%BB%E5%AF%B9%E9%BD%90)
    - [1.3.5 函数](#135-%E5%87%BD%E6%95%B0)
      - [FMT.07 函数的返回类型及修饰符与函数名同行](#fmt07-%E5%87%BD%E6%95%B0%E7%9A%84%E8%BF%94%E5%9B%9E%E7%B1%BB%E5%9E%8B%E5%8F%8A%E4%BF%AE%E9%A5%B0%E7%AC%A6%E4%B8%8E%E5%87%BD%E6%95%B0%E5%90%8D%E5%90%8C%E8%A1%8C)
    - [1.3.6 语句](#136-%E8%AF%AD%E5%8F%A5)
      - [FMT.08 条件、循环语句使用大括号](#fmt08-%E6%9D%A1%E4%BB%B6%E5%BE%AA%E7%8E%AF%E8%AF%AD%E5%8F%A5%E4%BD%BF%E7%94%A8%E5%A4%A7%E6%8B%AC%E5%8F%B7)
      - [FMT.09 case/default 语句相对 switch 缩进一层](#fmt09-casedefault-%E8%AF%AD%E5%8F%A5%E7%9B%B8%E5%AF%B9-switch-%E7%BC%A9%E8%BF%9B%E4%B8%80%E5%B1%82)
      - [FMT.10 指针类型"\*"跟随变量或者函数名](#fmt10-%E6%8C%87%E9%92%88%E7%B1%BB%E5%9E%8B%5C%E8%B7%9F%E9%9A%8F%E5%8F%98%E9%87%8F%E6%88%96%E8%80%85%E5%87%BD%E6%95%B0%E5%90%8D)
    - [1.3.7 空格与空行](#137-%E7%A9%BA%E6%A0%BC%E4%B8%8E%E7%A9%BA%E8%A1%8C)
      - [FMT.11 用空格突出关键字和重要信息](#fmt11-%E7%94%A8%E7%A9%BA%E6%A0%BC%E7%AA%81%E5%87%BA%E5%85%B3%E9%94%AE%E5%AD%97%E5%92%8C%E9%87%8D%E8%A6%81%E4%BF%A1%E6%81%AF)
      - [FMT.12 避免连续3个或更多空行](#fmt12-%E9%81%BF%E5%85%8D%E8%BF%9E%E7%BB%AD3%E4%B8%AA%E6%88%96%E6%9B%B4%E5%A4%9A%E7%A9%BA%E8%A1%8C)
- [2 编程实践](#2-%E7%BC%96%E7%A8%8B%E5%AE%9E%E8%B7%B5)
  - [2.1 预处理](#21-%E9%A2%84%E5%A4%84%E7%90%86)
    - [2.1.1 宏](#211-%E5%AE%8F)
      - [PRE.01 使用函数代替函数式宏](#pre01-%E4%BD%BF%E7%94%A8%E5%87%BD%E6%95%B0%E4%BB%A3%E6%9B%BF%E5%87%BD%E6%95%B0%E5%BC%8F%E5%AE%8F)
      - [PRE.02 定义宏时，要使用完备的括号](#pre02-%E5%AE%9A%E4%B9%89%E5%AE%8F%E6%97%B6%E8%A6%81%E4%BD%BF%E7%94%A8%E5%AE%8C%E5%A4%87%E7%9A%84%E6%8B%AC%E5%8F%B7)
      - [PRE.03 包含多条语句的函数式宏的实现语句必须放在 do-while(0) 中](#pre03-%E5%8C%85%E5%90%AB%E5%A4%9A%E6%9D%A1%E8%AF%AD%E5%8F%A5%E7%9A%84%E5%87%BD%E6%95%B0%E5%BC%8F%E5%AE%8F%E7%9A%84%E5%AE%9E%E7%8E%B0%E8%AF%AD%E5%8F%A5%E5%BF%85%E9%A1%BB%E6%94%BE%E5%9C%A8-do-while0-%E4%B8%AD)
      - [PRE.04 禁止把带副作用的表达式作为参数传递给函数式宏](#pre04-%E7%A6%81%E6%AD%A2%E6%8A%8A%E5%B8%A6%E5%89%AF%E4%BD%9C%E7%94%A8%E7%9A%84%E8%A1%A8%E8%BE%BE%E5%BC%8F%E4%BD%9C%E4%B8%BA%E5%8F%82%E6%95%B0%E4%BC%A0%E9%80%92%E7%BB%99%E5%87%BD%E6%95%B0%E5%BC%8F%E5%AE%8F)
      - [PRE.05 函数式宏定义中慎用 return、goto、continue、break 等改变程序流程的语句](#pre05-%E5%87%BD%E6%95%B0%E5%BC%8F%E5%AE%8F%E5%AE%9A%E4%B9%89%E4%B8%AD%E6%85%8E%E7%94%A8-returngotocontinuebreak-%E7%AD%89%E6%94%B9%E5%8F%98%E7%A8%8B%E5%BA%8F%E6%B5%81%E7%A8%8B%E7%9A%84%E8%AF%AD%E5%8F%A5)
      - [PRE.06 函数式宏要简短](#pre06-%E5%87%BD%E6%95%B0%E5%BC%8F%E5%AE%8F%E8%A6%81%E7%AE%80%E7%9F%AD)
      - [PRE.07 宏的名称不应与关键字相同](#pre07-%E5%AE%8F%E7%9A%84%E5%90%8D%E7%A7%B0%E4%B8%8D%E5%BA%94%E4%B8%8E%E5%85%B3%E9%94%AE%E5%AD%97%E7%9B%B8%E5%90%8C)
      - [PRE.08 禁止宏调用参数中出现预编译指令](#pre08-%E7%A6%81%E6%AD%A2%E5%AE%8F%E8%B0%83%E7%94%A8%E5%8F%82%E6%95%B0%E4%B8%AD%E5%87%BA%E7%8E%B0%E9%A2%84%E7%BC%96%E8%AF%91%E6%8C%87%E4%BB%A4)
      - [PRE.09 宏定义不应以分号结尾](#pre09-%E5%AE%8F%E5%AE%9A%E4%B9%89%E4%B8%8D%E5%BA%94%E4%BB%A5%E5%88%86%E5%8F%B7%E7%BB%93%E5%B0%BE)
      - [PRE.10 宏定义不应依赖宏外部的局部变量名](#pre10-%E5%AE%8F%E5%AE%9A%E4%B9%89%E4%B8%8D%E5%BA%94%E4%BE%9D%E8%B5%96%E5%AE%8F%E5%A4%96%E9%83%A8%E7%9A%84%E5%B1%80%E9%83%A8%E5%8F%98%E9%87%8F%E5%90%8D)
    - [2.1.2 条件编译](#212-%E6%9D%A1%E4%BB%B6%E7%BC%96%E8%AF%91)
      - [PRE.11 \#if或\#elif预处理指令中的常量表达式的值应为布尔值](#pre11-%5Cif%E6%88%96%5Celif%E9%A2%84%E5%A4%84%E7%90%86%E6%8C%87%E4%BB%A4%E4%B8%AD%E7%9A%84%E5%B8%B8%E9%87%8F%E8%A1%A8%E8%BE%BE%E5%BC%8F%E7%9A%84%E5%80%BC%E5%BA%94%E4%B8%BA%E5%B8%83%E5%B0%94%E5%80%BC)
      - [PRE.12 \#if或\#elif预处理指令中的常量表达式被求值前应确保其使用的标识符是有效的](#pre12-%5Cif%E6%88%96%5Celif%E9%A2%84%E5%A4%84%E7%90%86%E6%8C%87%E4%BB%A4%E4%B8%AD%E7%9A%84%E5%B8%B8%E9%87%8F%E8%A1%A8%E8%BE%BE%E5%BC%8F%E8%A2%AB%E6%B1%82%E5%80%BC%E5%89%8D%E5%BA%94%E7%A1%AE%E4%BF%9D%E5%85%B6%E4%BD%BF%E7%94%A8%E7%9A%84%E6%A0%87%E8%AF%86%E7%AC%A6%E6%98%AF%E6%9C%89%E6%95%88%E7%9A%84)
      - [PRE.13 所有\#else、\#elif、\#endif和与之对应的\#if、\#ifdef、\#ifndef预处理指令应出现在同一文件中](#pre13-%E6%89%80%E6%9C%89%5Celse%5Celif%5Cendif%E5%92%8C%E4%B8%8E%E4%B9%8B%E5%AF%B9%E5%BA%94%E7%9A%84%5Cif%5Cifdef%5Cifndef%E9%A2%84%E5%A4%84%E7%90%86%E6%8C%87%E4%BB%A4%E5%BA%94%E5%87%BA%E7%8E%B0%E5%9C%A8%E5%90%8C%E4%B8%80%E6%96%87%E4%BB%B6%E4%B8%AD)
  - [2.2 头文件](#22-%E5%A4%B4%E6%96%87%E4%BB%B6)
    - [INC.01 在头文件中声明需要对外公开的接口](#inc01-%E5%9C%A8%E5%A4%B4%E6%96%87%E4%BB%B6%E4%B8%AD%E5%A3%B0%E6%98%8E%E9%9C%80%E8%A6%81%E5%AF%B9%E5%A4%96%E5%85%AC%E5%BC%80%E7%9A%84%E6%8E%A5%E5%8F%A3)
    - [INC.02 头文件的扩展名只使用.h，不使用非习惯用法的扩展名，如.inc](#inc02-%E5%A4%B4%E6%96%87%E4%BB%B6%E7%9A%84%E6%89%A9%E5%B1%95%E5%90%8D%E5%8F%AA%E4%BD%BF%E7%94%A8h%E4%B8%8D%E4%BD%BF%E7%94%A8%E9%9D%9E%E4%B9%A0%E6%83%AF%E7%94%A8%E6%B3%95%E7%9A%84%E6%89%A9%E5%B1%95%E5%90%8D%E5%A6%82inc)
    - [INC.03 禁止头文件循环依赖](#inc03-%E7%A6%81%E6%AD%A2%E5%A4%B4%E6%96%87%E4%BB%B6%E5%BE%AA%E7%8E%AF%E4%BE%9D%E8%B5%96)
    - [INC.04 禁止包含用不到的头文件](#inc04-%E7%A6%81%E6%AD%A2%E5%8C%85%E5%90%AB%E7%94%A8%E4%B8%8D%E5%88%B0%E7%9A%84%E5%A4%B4%E6%96%87%E4%BB%B6)
    - [INC.05 头文件应当自包含](#inc05-%E5%A4%B4%E6%96%87%E4%BB%B6%E5%BA%94%E5%BD%93%E8%87%AA%E5%8C%85%E5%90%AB)
    - [INC.06 头文件必须用\#define保护，防止重复包含](#inc06-%E5%A4%B4%E6%96%87%E4%BB%B6%E5%BF%85%E9%A1%BB%E7%94%A8%5Cdefine%E4%BF%9D%E6%8A%A4%E9%98%B2%E6%AD%A2%E9%87%8D%E5%A4%8D%E5%8C%85%E5%90%AB)
    - [INC.07 按照合理的顺序包含头文件](#inc07-%E6%8C%89%E7%85%A7%E5%90%88%E7%90%86%E7%9A%84%E9%A1%BA%E5%BA%8F%E5%8C%85%E5%90%AB%E5%A4%B4%E6%96%87%E4%BB%B6)
  - [2.3 数据类型](#23-%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B)
    - [TYP.01 不要重复定义基础类型](#typ01-%E4%B8%8D%E8%A6%81%E9%87%8D%E5%A4%8D%E5%AE%9A%E4%B9%89%E5%9F%BA%E7%A1%80%E7%B1%BB%E5%9E%8B)
    - [TYP.02 使用恰当的基本类型作为操作符的操作数](#typ02-%E4%BD%BF%E7%94%A8%E6%81%B0%E5%BD%93%E7%9A%84%E5%9F%BA%E6%9C%AC%E7%B1%BB%E5%9E%8B%E4%BD%9C%E4%B8%BA%E6%93%8D%E4%BD%9C%E7%AC%A6%E7%9A%84%E6%93%8D%E4%BD%9C%E6%95%B0)
    - [TYP.03 使用合适的类型表示字符](#typ03-%E4%BD%BF%E7%94%A8%E5%90%88%E9%80%82%E7%9A%84%E7%B1%BB%E5%9E%8B%E8%A1%A8%E7%A4%BA%E5%AD%97%E7%AC%A6)
  - [2.4 常量](#24-%E5%B8%B8%E9%87%8F)
    - [CNS.01 禁止使用小写字母“l”作为数值型常量后缀](#cns01-%E7%A6%81%E6%AD%A2%E4%BD%BF%E7%94%A8%E5%B0%8F%E5%86%99%E5%AD%97%E6%AF%8Dl%E4%BD%9C%E4%B8%BA%E6%95%B0%E5%80%BC%E5%9E%8B%E5%B8%B8%E9%87%8F%E5%90%8E%E7%BC%80)
    - [CNS.02 不要使用难以理解的常量](#cns02-%E4%B8%8D%E8%A6%81%E4%BD%BF%E7%94%A8%E9%9A%BE%E4%BB%A5%E7%90%86%E8%A7%A3%E7%9A%84%E5%B8%B8%E9%87%8F)
  - [2.5 变量](#25-%E5%8F%98%E9%87%8F)
    - [VAR.01 禁止读取未经初始化的变量](#var01-%E7%A6%81%E6%AD%A2%E8%AF%BB%E5%8F%96%E6%9C%AA%E7%BB%8F%E5%88%9D%E5%A7%8B%E5%8C%96%E7%9A%84%E5%8F%98%E9%87%8F)
    - [VAR.02 不要在子作用域中重用变量名](#var02-%E4%B8%8D%E8%A6%81%E5%9C%A8%E5%AD%90%E4%BD%9C%E7%94%A8%E5%9F%9F%E4%B8%AD%E9%87%8D%E7%94%A8%E5%8F%98%E9%87%8F%E5%90%8D)
    - [VAR.03 避免大量栈分配](#var03-%E9%81%BF%E5%85%8D%E5%A4%A7%E9%87%8F%E6%A0%88%E5%88%86%E9%85%8D)
    - [VAR.04 慎用全局变量](#var04-%E6%85%8E%E7%94%A8%E5%85%A8%E5%B1%80%E5%8F%98%E9%87%8F)
    - [VAR.05 指向资源句柄或描述符的变量，在资源释放后立即赋予新值](#var05-%E6%8C%87%E5%90%91%E8%B5%84%E6%BA%90%E5%8F%A5%E6%9F%84%E6%88%96%E6%8F%8F%E8%BF%B0%E7%AC%A6%E7%9A%84%E5%8F%98%E9%87%8F%E5%9C%A8%E8%B5%84%E6%BA%90%E9%87%8A%E6%94%BE%E5%90%8E%E7%AB%8B%E5%8D%B3%E8%B5%8B%E4%BA%88%E6%96%B0%E5%80%BC)
    - [VAR.06 禁止将局部变量的地址返回到其作用域以外](#var06-%E7%A6%81%E6%AD%A2%E5%B0%86%E5%B1%80%E9%83%A8%E5%8F%98%E9%87%8F%E7%9A%84%E5%9C%B0%E5%9D%80%E8%BF%94%E5%9B%9E%E5%88%B0%E5%85%B6%E4%BD%9C%E7%94%A8%E5%9F%9F%E4%BB%A5%E5%A4%96)
    - [VAR.07 避免将只在一个函数中使用的变量声明为全局变量](#var07-%E9%81%BF%E5%85%8D%E5%B0%86%E5%8F%AA%E5%9C%A8%E4%B8%80%E4%B8%AA%E5%87%BD%E6%95%B0%E4%B8%AD%E4%BD%BF%E7%94%A8%E7%9A%84%E5%8F%98%E9%87%8F%E5%A3%B0%E6%98%8E%E4%B8%BA%E5%85%A8%E5%B1%80%E5%8F%98%E9%87%8F)
    - [VAR.08 资源不再使用时应予以关闭或释放](#var08-%E8%B5%84%E6%BA%90%E4%B8%8D%E5%86%8D%E4%BD%BF%E7%94%A8%E6%97%B6%E5%BA%94%E4%BA%88%E4%BB%A5%E5%85%B3%E9%97%AD%E6%88%96%E9%87%8A%E6%94%BE)
  - [2.6 表达式](#26-%E8%A1%A8%E8%BE%BE%E5%BC%8F)
    - [EXP.01 执行算术运算或比较操作的两个操作数要求具有相同的基本类型](#exp01-%E6%89%A7%E8%A1%8C%E7%AE%97%E6%9C%AF%E8%BF%90%E7%AE%97%E6%88%96%E6%AF%94%E8%BE%83%E6%93%8D%E4%BD%9C%E7%9A%84%E4%B8%A4%E4%B8%AA%E6%93%8D%E4%BD%9C%E6%95%B0%E8%A6%81%E6%B1%82%E5%85%B7%E6%9C%89%E7%9B%B8%E5%90%8C%E7%9A%84%E5%9F%BA%E6%9C%AC%E7%B1%BB%E5%9E%8B)
    - [EXP.02 含有变量自增或自减运算的表达式中禁止再次引用该变量](#exp02-%E5%90%AB%E6%9C%89%E5%8F%98%E9%87%8F%E8%87%AA%E5%A2%9E%E6%88%96%E8%87%AA%E5%87%8F%E8%BF%90%E7%AE%97%E7%9A%84%E8%A1%A8%E8%BE%BE%E5%BC%8F%E4%B8%AD%E7%A6%81%E6%AD%A2%E5%86%8D%E6%AC%A1%E5%BC%95%E7%94%A8%E8%AF%A5%E5%8F%98%E9%87%8F)
    - [EXP.03 用括号明确表达式的操作顺序，避免过分依赖默认优先级](#exp03-%E7%94%A8%E6%8B%AC%E5%8F%B7%E6%98%8E%E7%A1%AE%E8%A1%A8%E8%BE%BE%E5%BC%8F%E7%9A%84%E6%93%8D%E4%BD%9C%E9%A1%BA%E5%BA%8F%E9%81%BF%E5%85%8D%E8%BF%87%E5%88%86%E4%BE%9D%E8%B5%96%E9%BB%98%E8%AE%A4%E4%BC%98%E5%85%88%E7%BA%A7)
    - [EXP.04 不要向sizeof传递有副作用的操作数](#exp04-%E4%B8%8D%E8%A6%81%E5%90%91sizeof%E4%BC%A0%E9%80%92%E6%9C%89%E5%89%AF%E4%BD%9C%E7%94%A8%E7%9A%84%E6%93%8D%E4%BD%9C%E6%95%B0)
    - [EXP.05 避免对带位域的结构体的布局做任何假设](#exp05-%E9%81%BF%E5%85%8D%E5%AF%B9%E5%B8%A6%E4%BD%8D%E5%9F%9F%E7%9A%84%E7%BB%93%E6%9E%84%E4%BD%93%E7%9A%84%E5%B8%83%E5%B1%80%E5%81%9A%E4%BB%BB%E4%BD%95%E5%81%87%E8%AE%BE)
  - [2.7 控制语句](#27-%E6%8E%A7%E5%88%B6%E8%AF%AD%E5%8F%A5)
    - [2.7.1 判断语句](#271-%E5%88%A4%E6%96%AD%E8%AF%AD%E5%8F%A5)
      - [CTL.01 控制表达式的结果必须是布尔值](#ctl01-%E6%8E%A7%E5%88%B6%E8%A1%A8%E8%BE%BE%E5%BC%8F%E7%9A%84%E7%BB%93%E6%9E%9C%E5%BF%85%E9%A1%BB%E6%98%AF%E5%B8%83%E5%B0%94%E5%80%BC)
      - [CTL.02 &&和||操作符的右侧操作数不应包含副作用](#ctl02-%E5%92%8C%E6%93%8D%E4%BD%9C%E7%AC%A6%E7%9A%84%E5%8F%B3%E4%BE%A7%E6%93%8D%E4%BD%9C%E6%95%B0%E4%B8%8D%E5%BA%94%E5%8C%85%E5%90%AB%E5%89%AF%E4%BD%9C%E7%94%A8)
    - [2.7.2 循环语句](#272-%E5%BE%AA%E7%8E%AF%E8%AF%AD%E5%8F%A5)
      - [CTL.03 循环必须安全退出](#ctl03-%E5%BE%AA%E7%8E%AF%E5%BF%85%E9%A1%BB%E5%AE%89%E5%85%A8%E9%80%80%E5%87%BA)
      - [CTL.04 禁止使用浮点数作为循环计数器](#ctl04-%E7%A6%81%E6%AD%A2%E4%BD%BF%E7%94%A8%E6%B5%AE%E7%82%B9%E6%95%B0%E4%BD%9C%E4%B8%BA%E5%BE%AA%E7%8E%AF%E8%AE%A1%E6%95%B0%E5%99%A8)
    - [2.7.3 goto语句](#273-goto%E8%AF%AD%E5%8F%A5)
      - [CTL.05 慎用 goto 语句](#ctl05-%E6%85%8E%E7%94%A8-goto-%E8%AF%AD%E5%8F%A5)
      - [CTL.06 goto语句只能向下跳转](#ctl06-goto%E8%AF%AD%E5%8F%A5%E5%8F%AA%E8%83%BD%E5%90%91%E4%B8%8B%E8%B7%B3%E8%BD%AC)
    - [2.7.4 switch语句](#274-switch%E8%AF%AD%E5%8F%A5)
      - [CTL.07 switch语句要有default分支](#ctl07-switch%E8%AF%AD%E5%8F%A5%E8%A6%81%E6%9C%89default%E5%88%86%E6%94%AF)
      - [CTL.08 switch语句中至少有两个条件分支](#ctl08-switch%E8%AF%AD%E5%8F%A5%E4%B8%AD%E8%87%B3%E5%B0%91%E6%9C%89%E4%B8%A4%E4%B8%AA%E6%9D%A1%E4%BB%B6%E5%88%86%E6%94%AF)
  - [2.8 声明与初始化](#28-%E5%A3%B0%E6%98%8E%E4%B8%8E%E5%88%9D%E5%A7%8B%E5%8C%96)
    - [DCL.01 不要声明或定义保留的标识符](#dcl01-%E4%B8%8D%E8%A6%81%E5%A3%B0%E6%98%8E%E6%88%96%E5%AE%9A%E4%B9%89%E4%BF%9D%E7%95%99%E7%9A%84%E6%A0%87%E8%AF%86%E7%AC%A6)
  - [2.9 整数](#29-%E6%95%B4%E6%95%B0)
    - [INT.01 确保有符号整数运算不溢出](#int01-%E7%A1%AE%E4%BF%9D%E6%9C%89%E7%AC%A6%E5%8F%B7%E6%95%B4%E6%95%B0%E8%BF%90%E7%AE%97%E4%B8%8D%E6%BA%A2%E5%87%BA)
    - [INT.02 确保无符号整数运算不回绕](#int02-%E7%A1%AE%E4%BF%9D%E6%97%A0%E7%AC%A6%E5%8F%B7%E6%95%B4%E6%95%B0%E8%BF%90%E7%AE%97%E4%B8%8D%E5%9B%9E%E7%BB%95)
    - [INT.03 确保除法和余数运算不会导致除零错误(被零除)](#int03-%E7%A1%AE%E4%BF%9D%E9%99%A4%E6%B3%95%E5%92%8C%E4%BD%99%E6%95%B0%E8%BF%90%E7%AE%97%E4%B8%8D%E4%BC%9A%E5%AF%BC%E8%87%B4%E9%99%A4%E9%9B%B6%E9%94%99%E8%AF%AF%E8%A2%AB%E9%9B%B6%E9%99%A4)
    - [INT.04 整型表达式比较或赋值为一种更大类型之前必须用这种更大类型对它进行求值](#int04-%E6%95%B4%E5%9E%8B%E8%A1%A8%E8%BE%BE%E5%BC%8F%E6%AF%94%E8%BE%83%E6%88%96%E8%B5%8B%E5%80%BC%E4%B8%BA%E4%B8%80%E7%A7%8D%E6%9B%B4%E5%A4%A7%E7%B1%BB%E5%9E%8B%E4%B9%8B%E5%89%8D%E5%BF%85%E9%A1%BB%E7%94%A8%E8%BF%99%E7%A7%8D%E6%9B%B4%E5%A4%A7%E7%B1%BB%E5%9E%8B%E5%AF%B9%E5%AE%83%E8%BF%9B%E8%A1%8C%E6%B1%82%E5%80%BC)
    - [INT.05 只能对无符号整数进行位运算](#int05-%E5%8F%AA%E8%83%BD%E5%AF%B9%E6%97%A0%E7%AC%A6%E5%8F%B7%E6%95%B4%E6%95%B0%E8%BF%9B%E8%A1%8C%E4%BD%8D%E8%BF%90%E7%AE%97)
    - [INT.06 校验外部数据中整数值的合法性](#int06-%E6%A0%A1%E9%AA%8C%E5%A4%96%E9%83%A8%E6%95%B0%E6%8D%AE%E4%B8%AD%E6%95%B4%E6%95%B0%E5%80%BC%E7%9A%84%E5%90%88%E6%B3%95%E6%80%A7)
    - [INT.07 移位操作符的右操作数必须是非负数且小于左操作数的基本类型位宽](#int07-%E7%A7%BB%E4%BD%8D%E6%93%8D%E4%BD%9C%E7%AC%A6%E7%9A%84%E5%8F%B3%E6%93%8D%E4%BD%9C%E6%95%B0%E5%BF%85%E9%A1%BB%E6%98%AF%E9%9D%9E%E8%B4%9F%E6%95%B0%E4%B8%94%E5%B0%8F%E4%BA%8E%E5%B7%A6%E6%93%8D%E4%BD%9C%E6%95%B0%E7%9A%84%E5%9F%BA%E6%9C%AC%E7%B1%BB%E5%9E%8B%E4%BD%8D%E5%AE%BD)
    - [INT.08 表示对象大小的整数值或变量应当使用size_t类型](#int08-%E8%A1%A8%E7%A4%BA%E5%AF%B9%E8%B1%A1%E5%A4%A7%E5%B0%8F%E7%9A%84%E6%95%B4%E6%95%B0%E5%80%BC%E6%88%96%E5%8F%98%E9%87%8F%E5%BA%94%E5%BD%93%E4%BD%BF%E7%94%A8size_t%E7%B1%BB%E5%9E%8B)
    - [INT.09 确保枚举常量映射到唯一值](#int09-%E7%A1%AE%E4%BF%9D%E6%9E%9A%E4%B8%BE%E5%B8%B8%E9%87%8F%E6%98%A0%E5%B0%84%E5%88%B0%E5%94%AF%E4%B8%80%E5%80%BC)
    - [INT.10 确保整数转换不会造成数据截断或符号错误](#int10-%E7%A1%AE%E4%BF%9D%E6%95%B4%E6%95%B0%E8%BD%AC%E6%8D%A2%E4%B8%8D%E4%BC%9A%E9%80%A0%E6%88%90%E6%95%B0%E6%8D%AE%E6%88%AA%E6%96%AD%E6%88%96%E7%AC%A6%E5%8F%B7%E9%94%99%E8%AF%AF)
  - [2.10 指针和数组](#210-%E6%8C%87%E9%92%88%E5%92%8C%E6%95%B0%E7%BB%84)
    - [ARR.01 外部数据作为数组索引时必须确保在数组大小范围内](#arr01-%E5%A4%96%E9%83%A8%E6%95%B0%E6%8D%AE%E4%BD%9C%E4%B8%BA%E6%95%B0%E7%BB%84%E7%B4%A2%E5%BC%95%E6%97%B6%E5%BF%85%E9%A1%BB%E7%A1%AE%E4%BF%9D%E5%9C%A8%E6%95%B0%E7%BB%84%E5%A4%A7%E5%B0%8F%E8%8C%83%E5%9B%B4%E5%86%85)
    - [ARR.02 禁止通过对数组类型的函数参数变量进行sizeof来获取数组大小](#arr02-%E7%A6%81%E6%AD%A2%E9%80%9A%E8%BF%87%E5%AF%B9%E6%95%B0%E7%BB%84%E7%B1%BB%E5%9E%8B%E7%9A%84%E5%87%BD%E6%95%B0%E5%8F%82%E6%95%B0%E5%8F%98%E9%87%8F%E8%BF%9B%E8%A1%8Csizeof%E6%9D%A5%E8%8E%B7%E5%8F%96%E6%95%B0%E7%BB%84%E5%A4%A7%E5%B0%8F)
    - [ARR.03 禁止通过对指针变量进行sizeof操作来获取数组大小](#arr03-%E7%A6%81%E6%AD%A2%E9%80%9A%E8%BF%87%E5%AF%B9%E6%8C%87%E9%92%88%E5%8F%98%E9%87%8F%E8%BF%9B%E8%A1%8Csizeof%E6%93%8D%E4%BD%9C%E6%9D%A5%E8%8E%B7%E5%8F%96%E6%95%B0%E7%BB%84%E5%A4%A7%E5%B0%8F)
    - [ARR.04 避免整数与指针间的互相转化](#arr04-%E9%81%BF%E5%85%8D%E6%95%B4%E6%95%B0%E4%B8%8E%E6%8C%87%E9%92%88%E9%97%B4%E7%9A%84%E4%BA%92%E7%9B%B8%E8%BD%AC%E5%8C%96)
    - [ARR.05 不同类型的对象指针之间不应进行强制转换](#arr05-%E4%B8%8D%E5%90%8C%E7%B1%BB%E5%9E%8B%E7%9A%84%E5%AF%B9%E8%B1%A1%E6%8C%87%E9%92%88%E4%B9%8B%E9%97%B4%E4%B8%8D%E5%BA%94%E8%BF%9B%E8%A1%8C%E5%BC%BA%E5%88%B6%E8%BD%AC%E6%8D%A2)
    - [ARR.06 不要使用变长数组类型](#arr06-%E4%B8%8D%E8%A6%81%E4%BD%BF%E7%94%A8%E5%8F%98%E9%95%BF%E6%95%B0%E7%BB%84%E7%B1%BB%E5%9E%8B)
    - [ARR.07 声明一个带有外部链接的数组时，必须显式指定它的大小](#arr07-%E5%A3%B0%E6%98%8E%E4%B8%80%E4%B8%AA%E5%B8%A6%E6%9C%89%E5%A4%96%E9%83%A8%E9%93%BE%E6%8E%A5%E7%9A%84%E6%95%B0%E7%BB%84%E6%97%B6%E5%BF%85%E9%A1%BB%E6%98%BE%E5%BC%8F%E6%8C%87%E5%AE%9A%E5%AE%83%E7%9A%84%E5%A4%A7%E5%B0%8F)
  - [2.11 字符串](#211-%E5%AD%97%E7%AC%A6%E4%B8%B2)
    - [STR.01 确保字符串存储有足够的空间容纳字符数据和null结束符](#str01-%E7%A1%AE%E4%BF%9D%E5%AD%97%E7%AC%A6%E4%B8%B2%E5%AD%98%E5%82%A8%E6%9C%89%E8%B6%B3%E5%A4%9F%E7%9A%84%E7%A9%BA%E9%97%B4%E5%AE%B9%E7%BA%B3%E5%AD%97%E7%AC%A6%E6%95%B0%E6%8D%AE%E5%92%8Cnull%E7%BB%93%E6%9D%9F%E7%AC%A6)
    - [STR.02 对字符串进行存储操作，确保字符串有null结束符](#str02-%E5%AF%B9%E5%AD%97%E7%AC%A6%E4%B8%B2%E8%BF%9B%E8%A1%8C%E5%AD%98%E5%82%A8%E6%93%8D%E4%BD%9C%E7%A1%AE%E4%BF%9D%E5%AD%97%E7%AC%A6%E4%B8%B2%E6%9C%89null%E7%BB%93%E6%9D%9F%E7%AC%A6)
  - [2.12 断言](#212-%E6%96%AD%E8%A8%80)
    - [AST.01 避免在代码中直接使用assert()](#ast01-%E9%81%BF%E5%85%8D%E5%9C%A8%E4%BB%A3%E7%A0%81%E4%B8%AD%E7%9B%B4%E6%8E%A5%E4%BD%BF%E7%94%A8assert)
    - [AST.02 禁止用断言检测程序在运行期间可能导致的错误，可能发生的错误要用错误处理代码来处理](#ast02-%E7%A6%81%E6%AD%A2%E7%94%A8%E6%96%AD%E8%A8%80%E6%A3%80%E6%B5%8B%E7%A8%8B%E5%BA%8F%E5%9C%A8%E8%BF%90%E8%A1%8C%E6%9C%9F%E9%97%B4%E5%8F%AF%E8%83%BD%E5%AF%BC%E8%87%B4%E7%9A%84%E9%94%99%E8%AF%AF%E5%8F%AF%E8%83%BD%E5%8F%91%E7%94%9F%E7%9A%84%E9%94%99%E8%AF%AF%E8%A6%81%E7%94%A8%E9%94%99%E8%AF%AF%E5%A4%84%E7%90%86%E4%BB%A3%E7%A0%81%E6%9D%A5%E5%A4%84%E7%90%86)
    - [AST.03 禁止在断言内改变运行环境](#ast03-%E7%A6%81%E6%AD%A2%E5%9C%A8%E6%96%AD%E8%A8%80%E5%86%85%E6%94%B9%E5%8F%98%E8%BF%90%E8%A1%8C%E7%8E%AF%E5%A2%83)
    - [AST.04 一个断言只用于检查一个条件](#ast04-%E4%B8%80%E4%B8%AA%E6%96%AD%E8%A8%80%E5%8F%AA%E7%94%A8%E4%BA%8E%E6%A3%80%E6%9F%A5%E4%B8%80%E4%B8%AA%E9%94%99%E8%AF%AF)
  - [2.13 函数设计](#213-%E5%87%BD%E6%95%B0%E8%AE%BE%E8%AE%A1)
    - [2.13.1 输入校验](#2131-%E8%BE%93%E5%85%A5%E6%A0%A1%E9%AA%8C)
      - [FUD.01 对所有外部数据进行合法性检查](#fud01-%E5%AF%B9%E6%89%80%E6%9C%89%E5%A4%96%E9%83%A8%E6%95%B0%E6%8D%AE%E8%BF%9B%E8%A1%8C%E5%90%88%E6%B3%95%E6%80%A7%E6%A3%80%E6%9F%A5)
    - [FUD.02 对象或函数的所有声明必须与定义具有一致的名称和类型限定符](#fud02-%E5%AF%B9%E8%B1%A1%E6%88%96%E5%87%BD%E6%95%B0%E7%9A%84%E6%89%80%E6%9C%89%E5%A3%B0%E6%98%8E%E5%BF%85%E9%A1%BB%E4%B8%8E%E5%AE%9A%E4%B9%89%E5%85%B7%E6%9C%89%E4%B8%80%E8%87%B4%E7%9A%84%E5%90%8D%E7%A7%B0%E5%92%8C%E7%B1%BB%E5%9E%8B%E9%99%90%E5%AE%9A%E7%AC%A6)
    - [FUD.03 设计函数时，优先使用返回值而不是输出参数](#fud03-%E8%AE%BE%E8%AE%A1%E5%87%BD%E6%95%B0%E6%97%B6%E4%BC%98%E5%85%88%E4%BD%BF%E7%94%A8%E8%BF%94%E5%9B%9E%E5%80%BC%E8%80%8C%E4%B8%8D%E6%98%AF%E8%BE%93%E5%87%BA%E5%8F%82%E6%95%B0)
    - [FUD.04 函数避免使用 void\* 类型参数](#fud04-%E5%87%BD%E6%95%B0%E9%81%BF%E5%85%8D%E4%BD%BF%E7%94%A8-void%5C-%E7%B1%BB%E5%9E%8B%E5%8F%82%E6%95%B0)
    - [FUD.05 函数要简短](#fud05-%E5%87%BD%E6%95%B0%E8%A6%81%E7%AE%80%E7%9F%AD)
    - [FUD.06 内联函数要尽可能短，避免超过10行](#fud06-%E5%86%85%E8%81%94%E5%87%BD%E6%95%B0%E8%A6%81%E5%B0%BD%E5%8F%AF%E8%83%BD%E7%9F%AD%E9%81%BF%E5%85%8D%E8%B6%85%E8%BF%8710%E8%A1%8C)
    - [FUD.07 数组作为函数参数时，必须同时将其长度作为函数的参数](#fud07-%E6%95%B0%E7%BB%84%E4%BD%9C%E4%B8%BA%E5%87%BD%E6%95%B0%E5%8F%82%E6%95%B0%E6%97%B6%E5%BF%85%E9%A1%BB%E5%90%8C%E6%97%B6%E5%B0%86%E5%85%B6%E9%95%BF%E5%BA%A6%E4%BD%9C%E4%B8%BA%E5%87%BD%E6%95%B0%E7%9A%84%E5%8F%82%E6%95%B0)
    - [FUD.08 将字符串或指针作为函数参数时，在函数体中应检查参数是否为NULL](#fud08-%E5%B0%86%E5%AD%97%E7%AC%A6%E4%B8%B2%E6%88%96%E6%8C%87%E9%92%88%E4%BD%9C%E4%B8%BA%E5%87%BD%E6%95%B0%E5%8F%82%E6%95%B0%E6%97%B6%E5%9C%A8%E5%87%BD%E6%95%B0%E4%BD%93%E4%B8%AD%E5%BA%94%E6%A3%80%E6%9F%A5%E5%8F%82%E6%95%B0%E6%98%AF%E5%90%A6%E4%B8%BAnull)
    - [FUD.09 避免修改函数参数的值](#fud09-%E9%81%BF%E5%85%8D%E4%BF%AE%E6%94%B9%E5%87%BD%E6%95%B0%E5%8F%82%E6%95%B0%E7%9A%84%E5%80%BC)
  - [2.14 函数使用](#214-%E5%87%BD%E6%95%B0%E4%BD%BF%E7%94%A8)
    - [2.14.1 格式化输入/输出函数](#2141-%E6%A0%BC%E5%BC%8F%E5%8C%96%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA%E5%87%BD%E6%95%B0)
      - [FUU.0.1 调用格式化输入/输出函数时，禁止format参数受外部数据控制](#fuu01-%E8%B0%83%E7%94%A8%E6%A0%BC%E5%BC%8F%E5%8C%96%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA%E5%87%BD%E6%95%B0%E6%97%B6%E7%A6%81%E6%AD%A2format%E5%8F%82%E6%95%B0%E5%8F%97%E5%A4%96%E9%83%A8%E6%95%B0%E6%8D%AE%E6%8E%A7%E5%88%B6)
      - [FUU.0.2 调用格式化输入/输出函数时，使用有效的格式字符串](#fuu02-%E8%B0%83%E7%94%A8%E6%A0%BC%E5%BC%8F%E5%8C%96%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA%E5%87%BD%E6%95%B0%E6%97%B6%E4%BD%BF%E7%94%A8%E6%9C%89%E6%95%88%E7%9A%84%E6%A0%BC%E5%BC%8F%E5%AD%97%E7%AC%A6%E4%B8%B2)
    - [2.14.2 退出类函数](#2142-%E9%80%80%E5%87%BA%E7%B1%BB%E5%87%BD%E6%95%B0)
      - [FUU.0.3 禁用atexit函数](#fuu03-%E7%A6%81%E7%94%A8atexit%E5%87%BD%E6%95%B0)
      - [FUU.0.4 禁止调用kill、TerminateProcess函数直接终止其他进程](#fuu04-%E7%A6%81%E6%AD%A2%E8%B0%83%E7%94%A8killterminateprocess%E5%87%BD%E6%95%B0%E7%9B%B4%E6%8E%A5%E7%BB%88%E6%AD%A2%E5%85%B6%E4%BB%96%E8%BF%9B%E7%A8%8B)
    - [2.14.3 安全函数](#2143-%E5%AE%89%E5%85%A8%E5%87%BD%E6%95%B0)
      - [FUU.0.5 必须检查安全函数返回值，并进行正确的处理](#fuu05-%E5%BF%85%E9%A1%BB%E6%A3%80%E6%9F%A5%E5%AE%89%E5%85%A8%E5%87%BD%E6%95%B0%E8%BF%94%E5%9B%9E%E5%80%BC%E5%B9%B6%E8%BF%9B%E8%A1%8C%E6%AD%A3%E7%A1%AE%E7%9A%84%E5%A4%84%E7%90%86)
      - [FUU.0.6 正确设置安全函数中的destMax参数](#fuu06-%E6%AD%A3%E7%A1%AE%E8%AE%BE%E7%BD%AE%E5%AE%89%E5%85%A8%E5%87%BD%E6%95%B0%E4%B8%AD%E7%9A%84destmax%E5%8F%82%E6%95%B0)
      - [FUU.0.7 禁止封装安全函数](#fuu07-%E7%A6%81%E6%AD%A2%E5%B0%81%E8%A3%85%E5%AE%89%E5%85%A8%E5%87%BD%E6%95%B0)
      - [FUU.0.8 禁止用宏重命名安全函数](#fuu08-%E7%A6%81%E6%AD%A2%E7%94%A8%E5%AE%8F%E9%87%8D%E5%91%BD%E5%90%8D%E5%AE%89%E5%85%A8%E5%87%BD%E6%95%B0)
    - [2.14.4 其他函数](#2144-%E5%85%B6%E4%BB%96%E5%87%BD%E6%95%B0)
      - [FUU.09 禁止外部可控数据作为进程启动函数的参数](#fuu09-%E7%A6%81%E6%AD%A2%E5%A4%96%E9%83%A8%E5%8F%AF%E6%8E%A7%E6%95%B0%E6%8D%AE%E4%BD%9C%E4%B8%BA%E8%BF%9B%E7%A8%8B%E5%90%AF%E5%8A%A8%E5%87%BD%E6%95%B0%E7%9A%84%E5%8F%82%E6%95%B0)
      - [FUU.10 禁止外部可控数据作为dlopen等模块加载函数的参数](#fuu10-%E7%A6%81%E6%AD%A2%E5%A4%96%E9%83%A8%E5%8F%AF%E6%8E%A7%E6%95%B0%E6%8D%AE%E4%BD%9C%E4%B8%BAdlopen%E7%AD%89%E6%A8%A1%E5%9D%97%E5%8A%A0%E8%BD%BD%E5%87%BD%E6%95%B0%E7%9A%84%E5%8F%82%E6%95%B0)
      - [FUU.11 禁止直接使用外部数据拼接SQL命令](#fuu11-%E7%A6%81%E6%AD%A2%E7%9B%B4%E6%8E%A5%E4%BD%BF%E7%94%A8%E5%A4%96%E9%83%A8%E6%95%B0%E6%8D%AE%E6%8B%BC%E6%8E%A5sql%E5%91%BD%E4%BB%A4)
      - [FUU.12 禁止在信号处理例程中调用非异步安全函数](#fuu12-%E7%A6%81%E6%AD%A2%E5%9C%A8%E4%BF%A1%E5%8F%B7%E5%A4%84%E7%90%86%E4%BE%8B%E7%A8%8B%E4%B8%AD%E8%B0%83%E7%94%A8%E9%9D%9E%E5%BC%82%E6%AD%A5%E5%AE%89%E5%85%A8%E5%87%BD%E6%95%B0)
      - [FUU.13 使用库函数时避免竞争条件](#fuu13-%E4%BD%BF%E7%94%A8%E5%BA%93%E5%87%BD%E6%95%B0%E6%97%B6%E9%81%BF%E5%85%8D%E7%AB%9E%E4%BA%89%E6%9D%A1%E4%BB%B6)
      - [FUU.14 禁止使用内存操作类不安全函数](#fuu14-%E7%A6%81%E6%AD%A2%E4%BD%BF%E7%94%A8%E5%86%85%E5%AD%98%E6%93%8D%E4%BD%9C%E7%B1%BB%E4%B8%8D%E5%AE%89%E5%85%A8%E5%87%BD%E6%95%B0)
  - [2.15 文件](#215-%E6%96%87%E4%BB%B6)
    - [FIL.01 创建文件时必须显式指定合适的文件访问权限](#fil01-%E5%88%9B%E5%BB%BA%E6%96%87%E4%BB%B6%E6%97%B6%E5%BF%85%E9%A1%BB%E6%98%BE%E5%BC%8F%E6%8C%87%E5%AE%9A%E5%90%88%E9%80%82%E7%9A%84%E6%96%87%E4%BB%B6%E8%AE%BF%E9%97%AE%E6%9D%83%E9%99%90)
    - [FIL.02 使用文件路径前必须进行规范化并校验](#fil02-%E4%BD%BF%E7%94%A8%E6%96%87%E4%BB%B6%E8%B7%AF%E5%BE%84%E5%89%8D%E5%BF%85%E9%A1%BB%E8%BF%9B%E8%A1%8C%E8%A7%84%E8%8C%83%E5%8C%96%E5%B9%B6%E6%A0%A1%E9%AA%8C)
    - [FIL.03 不要在共享目录中创建临时文件](#fil03-%E4%B8%8D%E8%A6%81%E5%9C%A8%E5%85%B1%E4%BA%AB%E7%9B%AE%E5%BD%95%E4%B8%AD%E5%88%9B%E5%BB%BA%E4%B8%B4%E6%97%B6%E6%96%87%E4%BB%B6)
  - [2.16 内存](#216-%E5%86%85%E5%AD%98)
    - [MEM.01 禁止直接使用malloc申请内存，所以内存申请都需要通过palloc接口从内存上下文申请（工具除外）](#mem01-%E7%A6%81%E6%AD%A2%E7%9B%B4%E6%8E%A5%E4%BD%BF%E7%94%A8malloc%E7%94%B3%E8%AF%B7%E5%86%85%E5%AD%98%E6%89%80%E4%BB%A5%E5%86%85%E5%AD%98%E7%94%B3%E8%AF%B7%E9%83%BD%E9%9C%80%E8%A6%81%E9%80%9A%E8%BF%87palloc%E6%8E%A5%E5%8F%A3%E4%BB%8E%E5%86%85%E5%AD%98%E4%B8%8A%E4%B8%8B%E6%96%87%E7%94%B3%E8%AF%B7%E5%B7%A5%E5%85%B7%E9%99%A4%E5%A4%96)
    - [MEM.02 使用palloc申请内存时，确认通过MemoryContextSwitchTo切换到正确的内存上下文下](#mem02-%E4%BD%BF%E7%94%A8palloc%E7%94%B3%E8%AF%B7%E5%86%85%E5%AD%98%E6%97%B6%E7%A1%AE%E8%AE%A4%E9%80%9A%E8%BF%87memorycontextswitchto%E5%88%87%E6%8D%A2%E5%88%B0%E6%AD%A3%E7%A1%AE%E7%9A%84%E5%86%85%E5%AD%98%E4%B8%8A%E4%B8%8B%E6%96%87%E4%B8%8B)
    - [MEM.03 禁止直接从头TopMemoryContext（g_instance.instance_context，t_thrd.top_mem_cxt，u_sess->top_mem_cxt）上申请内存](#mem03-%E7%A6%81%E6%AD%A2%E7%9B%B4%E6%8E%A5%E4%BB%8E%E5%A4%B4topmemorycontextg_instanceinstance_contextt_thrdtop_mem_cxtu_sess-top_mem_cxt%E4%B8%8A%E7%94%B3%E8%AF%B7%E5%86%85%E5%AD%98)
    - [MEM.04 通过palloc申请的连续内存不能大于1GB，若超过1GB，请使用palloc_huge接口申请内存](#mem04-%E9%80%9A%E8%BF%87palloc%E7%94%B3%E8%AF%B7%E7%9A%84%E8%BF%9E%E7%BB%AD%E5%86%85%E5%AD%98%E4%B8%8D%E8%83%BD%E5%A4%A7%E4%BA%8E1gb%E8%8B%A5%E8%B6%85%E8%BF%871gb%E8%AF%B7%E4%BD%BF%E7%94%A8palloc_huge%E6%8E%A5%E5%8F%A3%E7%94%B3%E8%AF%B7%E5%86%85%E5%AD%98)
    - [MEM.05 u_sess->top_mem_cxt及其子内存上下文上申请的内存，禁止通过t_thrd下的变量引用](#mem05-u_sess-top_mem_cxt%E5%8F%8A%E5%85%B6%E5%AD%90%E5%86%85%E5%AD%98%E4%B8%8A%E4%B8%8B%E6%96%87%E4%B8%8A%E7%94%B3%E8%AF%B7%E7%9A%84%E5%86%85%E5%AD%98%E7%A6%81%E6%AD%A2%E9%80%9A%E8%BF%87t_thrd%E4%B8%8B%E7%9A%84%E5%8F%98%E9%87%8F%E5%BC%95%E7%94%A8)
    - [MEM.06 t_thrd.top_mem_cxt及其子内存上下文上申请的内存，禁止通过u_sess下的变量引用](#mem06-t_thrdtop_mem_cxt%E5%8F%8A%E5%85%B6%E5%AD%90%E5%86%85%E5%AD%98%E4%B8%8A%E4%B8%8B%E6%96%87%E4%B8%8A%E7%94%B3%E8%AF%B7%E7%9A%84%E5%86%85%E5%AD%98%E7%A6%81%E6%AD%A2%E9%80%9A%E8%BF%87u_sess%E4%B8%8B%E7%9A%84%E5%8F%98%E9%87%8F%E5%BC%95%E7%94%A8)
    - [MEM.07 申请的内存需要通过pfree，MemoryContextDelete，MemoryContextReset接口及时释放](#mem07-%E7%94%B3%E8%AF%B7%E7%9A%84%E5%86%85%E5%AD%98%E9%9C%80%E8%A6%81%E9%80%9A%E8%BF%87pfreememorycontextdeletememorycontextreset%E6%8E%A5%E5%8F%A3%E5%8F%8A%E6%97%B6%E9%87%8A%E6%94%BE)
    - [MEM.08 如果需要使用类，需要继承BaseObject类，创建对象是通过接口 New(ContextName) ClassName(..)](#mem08-%E5%A6%82%E6%9E%9C%E9%9C%80%E8%A6%81%E4%BD%BF%E7%94%A8%E7%B1%BB%E9%9C%80%E8%A6%81%E7%BB%A7%E6%89%BFbaseobject%E7%B1%BB%E5%88%9B%E5%BB%BA%E5%AF%B9%E8%B1%A1%E6%98%AF%E9%80%9A%E8%BF%87%E6%8E%A5%E5%8F%A3-newcontextname-classname)
    - [MEM.09 禁止使用c++ STL模板库](#mem09-%E7%A6%81%E6%AD%A2%E4%BD%BF%E7%94%A8c-stl%E6%A8%A1%E6%9D%BF%E5%BA%93)
  - [2.17 C++使用规范](#217-c%E4%BD%BF%E7%94%A8%E8%A7%84%E8%8C%83)
    - [C++.01 推荐使用的C++特性：类、继承、模板、虚函数除此而之外的特性如果使用需要评估风险，并由commiter同意后方可使用。](#c01-%E6%8E%A8%E8%8D%90%E4%BD%BF%E7%94%A8%E7%9A%84c%E7%89%B9%E6%80%A7%E7%B1%BB%E7%BB%A7%E6%89%BF%E6%A8%A1%E6%9D%BF%E8%99%9A%E5%87%BD%E6%95%B0%E9%99%A4%E6%AD%A4%E8%80%8C%E4%B9%8B%E5%A4%96%E7%9A%84%E7%89%B9%E6%80%A7%E5%A6%82%E6%9E%9C%E4%BD%BF%E7%94%A8%E9%9C%80%E8%A6%81%E8%AF%84%E4%BC%B0%E9%A3%8E%E9%99%A9%E5%B9%B6%E7%94%B1commiter%E5%90%8C%E6%84%8F%E5%90%8E%E6%96%B9%E5%8F%AF%E4%BD%BF%E7%94%A8)
    - [C++.02 绝对禁止的C++特性：智能指针、STL模板库这些特性涉及内存分配和释放，与GaussDB Kernel内存管理机制冲突，如果使用会引发内存问题，所以禁止使用。](#c02-%E7%BB%9D%E5%AF%B9%E7%A6%81%E6%AD%A2%E7%9A%84c%E7%89%B9%E6%80%A7%E6%99%BA%E8%83%BD%E6%8C%87%E9%92%88stl%E6%A8%A1%E6%9D%BF%E5%BA%93%E8%BF%99%E4%BA%9B%E7%89%B9%E6%80%A7%E6%B6%89%E5%8F%8A%E5%86%85%E5%AD%98%E5%88%86%E9%85%8D%E5%92%8C%E9%87%8A%E6%94%BE%E4%B8%8Egaussdb-kernel%E5%86%85%E5%AD%98%E7%AE%A1%E7%90%86%E6%9C%BA%E5%88%B6%E5%86%B2%E7%AA%81%E5%A6%82%E6%9E%9C%E4%BD%BF%E7%94%A8%E4%BC%9A%E5%BC%95%E5%8F%91%E5%86%85%E5%AD%98%E9%97%AE%E9%A2%98%E6%89%80%E4%BB%A5%E7%A6%81%E6%AD%A2%E4%BD%BF%E7%94%A8)
    - [C++.03 C++风格结构体vs类仅当只有数据成员时必须使用struct结构体，class仅在数据成员存在函数时并且包含明显的层次关系时才允许使用。](#c03-c%E9%A3%8E%E6%A0%BC%E7%BB%93%E6%9E%84%E4%BD%93vs%E7%B1%BB%E4%BB%85%E5%BD%93%E5%8F%AA%E6%9C%89%E6%95%B0%E6%8D%AE%E6%88%90%E5%91%98%E6%97%B6%E5%BF%85%E9%A1%BB%E4%BD%BF%E7%94%A8struct%E7%BB%93%E6%9E%84%E4%BD%93class%E4%BB%85%E5%9C%A8%E6%95%B0%E6%8D%AE%E6%88%90%E5%91%98%E5%AD%98%E5%9C%A8%E5%87%BD%E6%95%B0%E6%97%B6%E5%B9%B6%E4%B8%94%E5%8C%85%E5%90%AB%E6%98%8E%E6%98%BE%E7%9A%84%E5%B1%82%E6%AC%A1%E5%85%B3%E7%B3%BB%E6%97%B6%E6%89%8D%E5%85%81%E8%AE%B8%E4%BD%BF%E7%94%A8)
    - [C++.04 禁用C++异常机制严禁使用C++的异常机制](#c04-%E7%A6%81%E7%94%A8c%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6%E4%B8%A5%E7%A6%81%E4%BD%BF%E7%94%A8c%E7%9A%84%E5%BC%82%E5%B8%B8%E6%9C%BA%E5%88%B6)
    - [C++.05 禁止使用外部数据拼接SQL命令](#c05-%E7%A6%81%E6%AD%A2%E4%BD%BF%E7%94%A8%E5%A4%96%E9%83%A8%E6%95%B0%E6%8D%AE%E6%8B%BC%E6%8E%A5sql%E5%91%BD%E4%BB%A4)
    - [C++.06 严禁使用string类存储敏感信息](#c06-%E4%B8%A5%E7%A6%81%E4%BD%BF%E7%94%A8string%E7%B1%BB%E5%AD%98%E5%82%A8%E6%95%8F%E6%84%9F%E4%BF%A1%E6%81%AF)
    - [C++.07 禁止通过对指针判空来判断new分配内存是否成功](#c07-%E7%A6%81%E6%AD%A2%E9%80%9A%E8%BF%87%E5%AF%B9%E6%8C%87%E9%92%88%E5%88%A4%E7%A9%BA%E6%9D%A5%E5%88%A4%E6%96%ADnew%E5%88%86%E9%85%8D%E5%86%85%E5%AD%98%E6%98%AF%E5%90%A6%E6%88%90%E5%8A%9F)
  - [2.18 其它](#218-%E5%85%B6%E5%AE%83)
    - [OTH.01 删除无效或永不执行的代码](#oth01-%E5%88%A0%E9%99%A4%E6%97%A0%E6%95%88%E6%88%96%E6%B0%B8%E4%B8%8D%E6%89%A7%E8%A1%8C%E7%9A%84%E4%BB%A3%E7%A0%81)
    - [OTH.02 不要在信号处理函数中访问共享对象](#oth02-%E4%B8%8D%E8%A6%81%E5%9C%A8%E4%BF%A1%E5%8F%B7%E5%A4%84%E7%90%86%E5%87%BD%E6%95%B0%E4%B8%AD%E8%AE%BF%E9%97%AE%E5%85%B1%E4%BA%AB%E5%AF%B9%E8%B1%A1)
    - [OTH.03 禁用rand函数产生用于安全用途的伪随机数](#oth03-%E7%A6%81%E7%94%A8rand%E5%87%BD%E6%95%B0%E4%BA%A7%E7%94%9F%E7%94%A8%E4%BA%8E%E5%AE%89%E5%85%A8%E7%94%A8%E9%80%94%E7%9A%84%E4%BC%AA%E9%9A%8F%E6%9C%BA%E6%95%B0)
    - [OTH.04 禁止在发布版本中输出对象或函数的地址](#oth04-%E7%A6%81%E6%AD%A2%E5%9C%A8%E5%8F%91%E5%B8%83%E7%89%88%E6%9C%AC%E4%B8%AD%E8%BE%93%E5%87%BA%E5%AF%B9%E8%B1%A1%E6%88%96%E5%87%BD%E6%95%B0%E7%9A%84%E5%9C%B0%E5%9D%80)
    - [OTH.05 禁止代码中包含公网地址](#oth05-%E7%A6%81%E6%AD%A2%E4%BB%A3%E7%A0%81%E4%B8%AD%E5%8C%85%E5%90%AB%E5%85%AC%E7%BD%91%E5%9C%B0%E5%9D%80)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# 1.代码风格

代码风格一般包含标识符的命名风格、排版与格式风格，注释风格。一致的编码习惯与风格，会使代码更容易阅读、理解更容易维护。统一的代码风格也是一致性原则最直观的体现。




## 1.1 命名




#### NAM.01 使用统一的命名风格

**【备注】**
社区新增代码使用最新规，老代码暂可保留。

**【描述】**

**驼峰风格(CamelCase)**
大小写字母混用，单词连在一起，不同单词间通过单词首字母大写来分开。
按连接后的首字母是否大写，又分: **大驼峰(UpperCamelCase)**和**小驼峰(lowerCamelCase)**

**内核风格(unix_like)**
又称蛇形风格(snake_case)。单词全小写，用下划线分割。
如：'test_result'

**匈牙利风格**
在“大驼峰”的基础上，加上类型或用途前缀
如：'uiSavedCount', 'bTested'

标识符命名风格的选择由产品自行决策。遵循：
- 推荐使用驼峰风格，具体描述详见下文
- 对于更亲和 Linux/Unix 的代码，可以使用内核风格
- 已使用内核命名风格的代码，可以选择继续使用内核风格
- 基于开源或外部代码进行开发或维护时，可以保持原有命名风格
- 基于产品或版本生命周期以及人力投入考虑，可以保持存量代码的匈牙利风格不变
- 对于仍活跃的使用了匈牙利风格的的产品或版本，建议制定合理可行的整改策略，过渡至驼峰风格
- 不管什么样的命名风格整改策略，都应该保证同一函数或结构体、联合体内的命名风格是一致的

当前条款推荐的“驼峰风格”具体规则如下：

| 类别 | 命名风格 | 形式 |
|-|-|-|
| 函数，结构体类型，枚举类型，联合体类型，typedef 定义的类型 | 大驼峰，或带模块前缀的大驼峰 | AaaBbb, XXX_AaaBbb |
| 局部变量，函数参数，宏参数，结构体中字段，联合体中成员 | 小驼峰 | aaaBbb |
| 全局变量（在函数外部定义的变量） | 带 'g_' 前缀的小驼峰 | g_aaaBbb |
| 宏（不包括函数式宏），枚举值，goto 标签 | 全大写，下划线分割 | AAA_BBB |
| 函数式宏 | 全大写下划线分割，或大驼峰，或带模块前缀的大驼峰 | AAA_BBB, AaaBbb, XXX_AaaBbb |
| 常量（在函数外部定义由const修饰的基本数据类型、枚举类型、字符串类型） | 全大写下划线分割，或带 'g_' 前缀的小驼峰 | AAA_BBB, g_aaaBbb |

**关于“模块前缀”**：
- 仅大驼峰命名风格的符号，可选加模块前缀。
- 模块前缀尽量简短且不超过**2**级（XXX_YYY_AaaBbb, XxxYyyAaaBbb）。
- 应保持风格统一，只选用一种前缀形式（仅选用XXX_AaaBbb，或仅选用XxxAaaBbb）。

**关于“函数式宏”**：
- 函数式宏的命名风格优先与宏一样，采用“全大写下划线分割”。
- 特殊场景，允许将函数式宏的命名风格与函数一样，但这种情况应该是极少的。比如：
```c
#ifdef SOME_DEFINE
void Bar(int);
#define Foo(a) Bar(a) // 特殊场景，用大驼峰风格命名函数式宏
#else
void Foo(int);  // 函数命名风格
#endif
```

**关于单词缩写**：
- 单词缩写应当作单个单词处理，以提高可读性。比如对包含HTTP(HyperText Transfer Protocol)缩写的函数命名如下：
```c
int GetActiveHttpClientCnt(void);
```

**【正例】**
```c
int MyCmp(int a, int b);      // 符合: 函数大驼峰，参数小驼峰（单字符变量也符合小驼峰定义）

enum MyColor {                // 符合：枚举类型，大驼峰
    BLACK,                    // 符合: 枚举值，全大写，下划线分割
    WHITE
} g_bgColor = WHITE;          // 符合: 全局变量，带 g_前缀的小驼峰

int XXX_YYY_FuncName(void);   // 符合: 函数，两级前缀，大模块加小模块

const int NAME_MAX_LEN = 100; // 符合: 符合上述常量定义，用全大写下划线分割
```

## 1.2 注释


#### CMT.01 注释符与注释内容间要有1空格

**【描述】**
注释符使用 `/*` `*/`和 `//` 都是可以的。
注释符与注释内容之间要有1空格。

使用如下的单行、多行注释风格：
```c
// 单行注释
```
```c
/* 另外一种单行注释 */
```
```c
/*
 * 多行注释
 * 第二行
 */
```
```c
// 另外一种多行注释
// 第二行
```

**【注意】**
- 若产品选用如 doxygen 来基于注释生成代码文档，则应由产品制定统一的各类广义的注释符及注释风格。
- “注释内容”有可能也包含空格，比如：

```c
/*
 * 这是一段注释内容也包含空格的例子。
 * XX参数解释如下：
 *     a - 参数 a 说明
 *     b - 参数 b 说明
 */
```




#### CMT.02 代码注释置于对应代码的上方或右边

**【描述】**
针对代码的注释，应该置于对应代码的上方或右方。

代码上方的注释，与代码行间无空行，保持与代码一样的缩进。
例：
```c
// 这是 Foo() 的注释
int Foo(void)
{
    // 这是变量 a 的注释
    int a = INIT_A_VALUE;
    ...
}
```

代码右边的注释，与代码之间，至少留1空格。
例：
```c
int foo = 100;  // 这里是注释内容，与代码至少留1空格
```

右置格式在适当的时候，上下对齐会更美观。
例：
```c
#define A_CONST 100         // 此处两行注释属于同类
#define ANOTHER_CONST 200   // 可保持左侧对齐
```

通常右置注释内容不宜过多；当右置注释超过行宽时，请考虑将注释置于代码上方。




#### CMT.03 文件头注释包含版权说明

**【描述】**
文件头注释应首先包含版权说明。
如果文件头注释需要增加其他内容，可以后面补充。
比如：文件功能说明，作者、创建日期、注意事项等等。

版权许可内容及格式必须如下：
`Copyright (c) 2020 XXX Technologies Co.,Ltd.`

文件头注释举例：
```c
/*
 * Copyright (c) 2020 Huawei Technologies Co.,Ltd.
 *
 * openGauss is licensed under Mulan PSL v2.
 * You can use this software according to the terms and conditions of the Mulan PSL v2.
 * You may obtain a copy of Mulan PSL v2 at:
 *
 *          http://license.coscl.org.cn/MulanPSL2
 *
 * THIS SOFTWARE IS PROVIDED ON AN "AS IS" BASIS, WITHOUT WARRANTIES OF ANY KIND,
 * EITHER EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO NON-INFRINGEMENT,
 * MERCHANTABILITY OR FIT FOR A PARTICULAR PURPOSE.
 * See the Mulan PSL v2 for more details.
 * -------------------------------------------------------------------------
 *
 * dataqueue.cpp
 *
 *
 * IDENTIFICATION
 *    src/gausskernel/storage/replication/dataqueue.cpp
 *
 * -------------------------------------------------------------------------
 */
```

编写文件头注释应注意：
- 文件头注释应该从文件顶头开始。
如果包含“关键资产说明”类注释，则应紧随其后。
- 保持统一格式。
具体格式由项目或更大范围统一制定。格式可参考上面举例。
- 保持版面工整，若内容过长，超出行宽要求，换行时应注意对齐。
对齐可参考上述例子 '注意点'。
- 首先包含“版权许可”，然后包含其他可先选内容。
其他选项按需添加，并保持格式统一。
- 不要空有格式，无内容。
如上述例子，如果 '注意：' 后面无内容。




#### CMT.04 不写空有格式的函数头注释

**【描述】**
要像写代码注释一样**按需**去写函数头注释。

并不是所有的函数都需要函数头注释；
函数原型无法表达的，却又希望读者知道的信息，才需要加函数头注释辅助说明；

函数头注释统一放在函数声明或定义上方。
选择使用如下风格之一：
**使用'//'写函数头**
```c
// 单行函数头
int Func1(void);

// 多行函数头
// 第二行
int Func2(void);
```

**使用'/\*' '\*/' 写函数头**
```c
/* 单行函数头 */
int Func1(void);

/*
 * 单行或多行函数头
 * 第二行
 */
int Func2(void);
```

函数尽量通过函数名自注释，**按需**写函数头注释。
不要写无用、信息冗余的函数头；不要写空有格式的函数头。

函数头注释内容**可选**，但不限于：功能说明、返回值、性能约束、用法、内存约定、算法实现、可重入的要求等等。
模块对外头文件中的函数接口声明，其函数头注释，应当将重要、有用的信息表达清楚。

例：
```c
/*
 * 返回实际写入的字节数，-1表示写入失败
 * 注意，len小于INT_MAX
 */
int WriteData(const unsigned char *buf, size_t len);
```

坏的例子：
```c
/*
 * 函数名：WriteData
 * 功能：写入字符串
 * 参数：
 * 返回值：
 */
int WriteData(const unsigned char *buf, size_t len);
```
上面注释示例中的问题：
- 参数、返回值，空有格式没内容
- 注释中的函数名信息冗余




## 1.3 格式




### 1.3.1 编码




#### FMT.01 非纯ASCII码源文件使用 UTF-8 编码

**【备注】**
非Windows下（DOS格式），建议在Linux下直接开发或使用dos2unix工具进行转换。

**【描述】**
对于非纯 ASCII 源文件，使用 UTF-8 格式。
请正确配置你的编辑器。




### 1.3.2 缩进




#### FMT.02 使用空格进行缩进，每次缩进4个空格

**【描述】**
使用空格而不是制表符('\t')进行缩进，每次缩进为 **4** 个空格。
当前几乎所有的集成开发环境（IDE）和代码编辑器都支持配置将Tab键自动扩展为**4**空格输入，请配置你的代码编辑器支持使用空格进行缩进。




### 1.3.3 大括号




#### FMT.03 使用统一的大括号换行风格

**【描述】**

**K&R风格**
换行时，函数左大括号另起一行放行首，并独占一行；其他左大括号跟随语句放行末。
右大括号独占一行，除非后面跟着同一语句的剩余部分，如 do 语句中的 while，或者 if 语句的 else/else if，或者逗号、分号。

如：
```c
struct MyType { // 跟随语句放行末，前置1空格
    ...
};              // 右大括号后面紧跟分号

int Foo(int a)
{               // 函数左大括号独占一行，放行首
    if (a > 0) {
        ...
    } else {    // 右大括号、"else"、以及后续的左大括号均在同一行
        ...
    }           // 右大括号独占一行
    ...
}
```

**Allman风格**
换行时，左大括另起并独占一行，保持与上一行相同缩进；
右大括号独占一行，除非后面跟着 do 语句中的 while，或者逗号、分号。
如：
```c
struct MyType
{               // 另起并独占一行
    ...
};              // 右大括号后面紧跟分号

int Foo(int a)
{
    if (a > 0)
    {
        ...
    }
    else        // 前后的左右大括号均独占一行，所以 'else' 也只能独占一行
    {
        ...
    }
    ...
}
```




### 1.3.4 行宽




#### FMT.04 一行只有一条语句

**【描述】**
一行只写一条语句。
例：
```c
int Foo(void)
{
    int a = 10; // 符合

    for (int i = 0; i < CNT; i++) { // 符合: 这里有分号，但并不是语句
        Bar();  // 符合
    }

    if (cond) { Func1(); } else { Func2(); } // 不符合： 一行包含两个复合语句

    ...
}
```




#### FMT.05 行宽不超过 120 个字符

**【描述】**
代码行宽不宜过长，否则不利于阅读。
控制行宽长度可以间接的引导开发去缩短函数、变量的命名，减少嵌套的层数，提升代码可读性。
强烈建议和要求每行字符数不要超过 **120** 个；除非超过 **120** 能显著增加可读性，并且不会隐藏信息。
虽然现代显示器分辨率已经很高，但是行宽过长，反而提高了阅读理解的难度；不符合本规范提倡的“清晰”、“简洁”原则。

**【例外】**
如下场景不宜换行，可以例外：
- 换行会导致内容截断，无法被方便查找(grep)的字符串，如命令行或 URL 等等。包含这些内容的代码或注释，可以适当例外。
- \#include / \#error 语句可以超出行宽要求，但是也需要尽量避免。




#### FMT.06 换行时将操作符留在行末，新行缩进一层或进行同类对齐

**【描述】**
当语句过长，或者换行后有更好的可读性时，应根据层次或操作符优级先择合适的断行点进行换行，并将表示未结束的操作符或连接符号留在行末。
操作符、连接符放在行末，表示“未结束，后续还有”。
新行缩进一层，或者保持同类对齐。

长表达式举例：
```c
// 假设下面第一行已经不满足行宽要求
if (currentValue > MIN &&  // 符合：换行后，布尔操作符放在行末
    currentValue < MAX) {  // 符合: 与(&&)操作符的两个操作数同类对齐
    DoSomething();
    ...
}

flashPara.flashEndAddr = flashPara.flashBaseAddr +  // 符合: 加号留在行末
                         flashPara.flashSize;       // 符合: 加法两个操作数对齐
```

函数参数列表举例：
```c
// 符合：函数参数放在一行
ReturnType result = FunctionName(paramName1, paramName2);

ReturnType result = FunctionName(paramName1,
                                 paramName2,
                                 paramName3); // 符合：保持与上方参数对齐

ReturnType result = FunctionName(paramName1, paramName2,
    paramName3, paramName4, paramName5);     // 符合：参数换行，4 空格缩进

ReturnType result = VeryVeryVeryLongFunctionName( // 行宽不满足第1个参数，直接换行
    paramName1, paramName2, paramName3);          // 换行后，4 空格缩进
```

如果函数的参数存在内在关联性，按照可理解性优先于格式排版要求，对参数进行合理分组换行。
```c
// 符合：每行的参数代表一组相关性较强的数据结构，放在一行便于理解
int result = DealWithStructLikeParams(left.x, left.y,    // 表示一组相关参数
                                      right.x, right.y); // 表示另外一组相关参数
```

初始化语句举例：
```c
// 符合: 满足行宽要求时不换行
int arr[4] = { 1, 2, 3, 4 };
```
```c
// 符合: 行宽较长时，换行让可读性更好
const int rank[] = {
    16, 16, 16, 16, 32, 32, 32, 32,
    64, 64, 64, 64, 32, 32, 32, 32
};
```

对于复杂结构数据的初始化，尽量清晰、紧凑。
参考如下格式：
```c
int a[][4] = {
    { 1, 2, 3, 4 }, { 2, 2, 3, 4 }, // 符合
    { 3, 2, 3, 4 }, { 4, 2, 3, 4 }
};

int b[][8] = {
    { 1, 2, 3, 4, 5, 6, 7, 8 },     // 符合
    { 2, 2, 3, 4, 5, 6, 7, 8 }
};
```
```c
int c[][8] = {
    {
        1, 2, 3, 4, 5, 6, 7, 8      // 符合
    }, {
        2, 2, 3, 4, 5, 6, 7, 8
    }
};
```

对于初始化语句中的大括号，遵循：
- 左大括号放行末时，对应的右大括号需另起一行
- 左大括号被内容跟随时，对应的右大括号也应跟随内容




### 1.3.5 函数




#### FMT.07 函数的返回类型及修饰符与函数名同行

**【描述】**
声明定义函数时，函数的返回值类型以及其他修饰符，保持与函数名同一行。

例：
```c
static inline int ShortFunc(int a, int b);         // 符合
static inline int LongFuncName(int longParamName1, // 符合
                               int longParamName2, // 符合: 参数可以与函数名不同行
                               int longParamName3,
                               int longParamName4);
```




### 1.3.6 语句




#### FMT.08 条件、循环语句使用大括号

**【描述】**
包括 if/for/while/do-while 语句应使用大括号，即复合语句。

理由：
- 代码逻辑直观，易读；
- 在已有代码上增加新代码时不容易出错；
- 对于语句中使用函数式宏时，没有大括号保护容易出错（如果宏定义时遗漏了大括号）。

**【正例】**

```c
if (objectIsNotExist) { // 符合：单行条件语句也加大括号
    return CreateNewObject();
}
```
```c
for (int i = 0; i < someRange; i++) { // 符合: 使用了大括号
    DoSomething();
}
```
```c
while (condition) {} // 符合：即使循环体是空，也应使用大括号
```
```c
while (condition) {
    continue;        // 符合：continue 表示空逻辑，使用大括号
}
```

**【反例】**

```c
for (int i = 0; i < someRange; i++)
    DoSomething();  // 不符合： 应该加上括号
```
```c
while (condition);  // 不符合：很容易让人误解循环体是 DoSomething() 调用
DoSomething();
```




#### FMT.09 case/default 语句相对 switch 缩进一层

**【描述】**
合理的缩进使代码块具有层次感，提升可读性。

**【反例】**
```c
switch (var) {
case 0:             // 不符合：case 未缩进
    DoSomething();
    break;
...
default:            // 不符合：default 未缩进
    break;
}
```

**【正例】**
```c
switch (var) {
    case 0:             // 符合: 缩进
        DoSomething1(); // 符合: 缩进
        break;
    case 1: {           // 符合: 带大括号格式
        DoSomething2();
        break;
    }
    default:
        break;
}
```




#### FMT.10 指针类型"\*"跟随变量或者函数名

**【描述】**
声明或定义指针变量或者返回指针类型函数时，"\*" 应该靠右跟随。
例：
```c
int *p1;  // 符合
int* p2;  // 不符合
int*p3;   // 不符合：两边都没空格
int * p4; // 不符合：两边都有空格
```
```c
struct Foo *CreateFoo(void); // 符合: "*"跟随函数名
```

下列情况需要特别注意：
- 当"\*"与变量或函数名之间有其他修饰符，无法跟随时，此时也不要跟随修饰符
```c
char * const VERSION = "V100";    // 符合: 当有 const 修饰符时，"*"两边都有空格
int Foo(const char * restrict p); // 符合: 当有 restrict 修饰符时，"*"两边都有空格
```
任何时候 "\*" 不要紧跟 const 或 restrict 关键字。
- 当右侧没有变量或函数名时，"\*" 可以跟随类型
```c
sz = sizeof(int*); // 符合：右侧没有变量，"*"跟随类型
```




### 1.3.7 空格与空行




#### FMT.11 用空格突出关键字和重要信息

**【描述】**
空格应该突出关键字和重要信息。总体要求如下：
- 行末不应加空格
- if, switch, case, do, while, for 等关键字之后应加空格
- 小括号内部的两侧，不应加空格
- 二元操作符（= + ‐ < > * / % | & ^ <= >= == !=）两侧都应加空格
- 一元操作符（& * + ‐ ~ !）之后不应加空格
- 三元操作符（? :）符号两侧都应加空格
- 结构体中表示位域的冒号，两侧都应加空格
- 前置和后置的自增、自减（++ --）和变量之间不应加空格
- 结构体成员操作符（. ->）前后不应加空格
- 大括号内部两侧有无空格，左右应保持一致
- 逗号、分号、冒号（不含三元操作符和表示位域的冒号）紧跟前面内容无空格，其后需要空格
- 函数参数列表的小括号与函数名之间不应加空格
- 类型强制转换的小括号与被转换对象之间不应加空格
- 数组的中括号与数组名之间不应加空格
- 涉及到换行时，行末的空格可以省去

对于大括号内部两侧的空格，建议如下：
- 一般的，大括号内部两侧建议加空格
- 对于空的，或单个标识符，或单个字面常量，空格不是必须
如：'{}', '{0}', '{NULL}', '{"hi"}' 等
- 连续嵌套的多重括号之间，空格不是必须
如：'{{0}}', '{{ 1, 2 }}' 等
错误示例：'{ 0, {1}}'，不属于连续嵌套场景，而且最外侧大括号左右不一致

注意：可在集成开发环境（IDE）和代码编辑器中设置保存文件时删除行末空格功能。

**【正例】**
1. 变量定义

```c
int i = 0;               // 符合：变量初始化时，= 前后应该有空格，分号前面不要留空格
int buf[BUF_SIZE] = {0}; // 符合：数组初始化时，大括号内空格可选
int arr[] = { 10, 20 };  // 符合: 正常大括号内部两侧建议加空格
```

2. 指针和取地址

```c
x = *p;   // 符合：*操作符和指针p之间不加空格
p = &x;   // 符合：&操作符和变量x之间不加空格
x = r.y;  // 符合：通过.访问成员变量时不加空格
x = r->y; // 符合：通过->访问成员变量时不加空格
```

3. 操作符

```c
x = 0;    // 符合：赋值操作的=前后都要加空格
x = -5;   // 符合：负数的符号之前要加空格
++x;      // 符合：前置和后置的++/--和变量之间不要加空格
x--;

if (x && !y)       // 符合：布尔操作符前后要加上空格，！操作和变量之间不要空格
v = w * x + y / z; // 符合：二元操作符前后要加空格
v = w * (x + z);   // 符合：括号内的表达式前后不需要加空格
```

4. 循环和条件语句

```c
if (condition) { // 符合：if关键字和括号之间加空格，括号内条件语句前后不加空格
    ...
} else {         // 符合：else关键字和大括号之间加空格
    ...
}

// 符合：while关键字和括号之间加空格，括号内条件语句前后不加空格
while (condition) {}

// 符合：for关键字和括号之间加空格，分号之后加空格
for (int i = 0; i < someRange; i++) {
    ...
}

switch (var) { // 符合: switch 关键字后面有1空格
    case 0:    // 符合：case语句条件和冒号之间不加空格
        ...
        break;
    ...
    default:
        ...
        break;
}
```

**【反例】**
函数定义和函数调用的情况

```c
int result = Foo(arg1,arg2);
                      ^         // 不符合： 逗号后面应该有空格

int result = Foo( arg1, arg2 );
                 ^          ^   // 不符合： 小括号内部两侧不应该有空格
```




#### FMT.12 避免连续3个或更多空行

**【描述】**
减少不必要的空行，可以显示更多的代码，方便代码阅读。下面有一些建议遵守的规则：
- 根据上下内容的相关程度，合理安排空行；
- 函数内部、类型定义内部、宏内部、初始化表达式内部，不使用连续空行
- 不使用连续 **3** 个空行，或更多
- 大括号内的代码块行首之前和行末之后不要加空行。

```c
ret = DoSomething();

if (ret != OK) {   // 不符合： 返回值判断应该紧跟函数调用
    return -1;
}
```
```c
int Foo(void)
{
    ...
}



int Bar(void)      // 不符合：最多使用连续2个空行
{
    ...
}
```
```c
int Foo(void)
{

    DoSomething(); // 不符合：大括号内部首尾，不需要空行
    ...

}
```




# 2 编程实践




## 2.1 预处理




### 2.1.1 宏




#### PRE.01 使用函数代替函数式宏

**【描述】**
定义函数式宏前，应考虑能否用函数替代。对于可替代场景，建议用函数替代宏。

函数式宏的缺点如下：
- 函数式宏缺乏类型检查，不如函数调用检查严格。参见示例代码。
- 宏展开时宏参数不求值，可能会产生非预期结果。
- 宏没有独立的作用域，跟控制流语句配合时，可能会产生非预期结果。
- 宏的技巧性太强，例如#的用法和无处不在的括号，影响可读性。
- 在特定场景下必须用特定编译器对宏的扩展，如 gcc 的 statement expression，可移植性也不好。
- 宏在预编译阶段展开后，在其后编译、链接和调试时都不可见；而且包含多行的宏会展开为一行。函数式宏难以调试、难以打断点，不利于定位问题。
- 对于包含大量语句的宏，在每个调用点都要展开。如果调用点很多，会造成代码空间的膨胀。

函数式宏缺乏类型检查的示例代码：

```c
#define MAX(a, b) (((a) < (b)) ? (b) : (a))

int Max(int a, int b)
{
    return (a < b) ? b : a;
}

void TestMacro(void)
{
    unsigned int a = 1;
    int b = -1;

    (void)printf("MACRO: max of a(%u) and b(%d) is %d\n", a, b, MAX(a, b));
    (void)printf("FUNC : max of a(%u) and b(%d) is %d\n", a, b, Max(a, b));
}
```

上面的示例代码由于宏缺乏类型检查，MAX中的a和b的比较提升为无符号数的比较，结果是`a < b`。输出结果是：

```
MACRO: max of a(1) and b(-1) is -1
FUNC : max of a(1) and b(-1) is 1
```

函数没有宏的上述缺点。但是，函数相比宏，最大的劣势是执行效率不高（增加函数调用的开销和编译器优化的难度）。

为此，C99标准引入了内联函数（gcc在标准之前就引入了内联函数）。

内联函数跟宏类似，也是在调用点展开。不同之处在于内联函数是在编译时展开。

内联函数兼具函数和宏的优点：
- 内联函数/函数执行严格的类型检查。
- 内联函数/函数的参数求值只会进行一次。
- 内联函数就地展开，没有函数调用的开销。
- 内联函数比函数优化得更好。

对于性能要求高的产品代码，可以考虑用内联函数代替函数式宏。

函数和内联函数不能完全替代函数式宏，函数式宏在某些场景更适合。比如，在日志记录场景下，使用带可变参和默认参数的函数式宏更方便：

```c
int ErrLog(const char *file, unsigned long line, const char *fmt, ...);
#define ERR_LOG(fmt, ...) ErrLog(__FILE__, __LINE__, fmt, ##__VA_ARGS__)
```




#### PRE.02 定义宏时，要使用完备的括号

**【描述】**
宏展开时只做文本替换，在编译时再求值。文本替换后，宏包含的语句跟调用点代码合并。
合并后的表达式因为操作符的优先级和结合律，可能会导致计算结果跟期望的不同。

比如：
```c
#define C_LEN A_LEN + B_LEN     // 不符合
```
上述宏在展开时，A_LEN 与 B_LEN 的加法并不一定是优先计算。
正确的写法应该是：
```c
#define C_LEN (A_LEN + B_LEN)   // 符合
```

带参数的宏更容易出现问题，比如：
```c
#define SUM(a, b) a + b     // 不符合
```
下面这样调用该宏，执行结果跟预期不符：
`100 / SUM(2, 8)` 将扩展成`(100 / 2) + 8`，而预期结果是`100 / (2 + 8)`。

这个问题的解决方法如下所示：
```c
#define SUM(a, b) ((a) + (b)) // 符合
```

但是要避免滥用括号。如下所示，单独的数字或标识符加括号毫无意义。

```c
#define SOME_CONST  100         // 符合: 单独的数字无需括号
#define ANOTHER_CONST   (-1)    // 符合: 负数需要使用括号
#define THE_CONST   SOME_CONST  // 符合: 单独的标识符无需括号
```

下列情况需要注意：
- 宏参数参与 '#', '##' 操作时，不要加括号
- 宏参数参与字符串拼接时，不要加括号
- 宏参数作为独立部分，在赋值（包括+=, -=等）操作的某一边时，可以不加括号
- 宏参数作为独立部分，在逗号表达式，函数或宏调用列表中，可以不加括号

举例如下：
```c
// x 不要加括号
#define MAKE_STR(x) #x

// obj 不要加括号
#define HELLO_STR(obj) "Hello, " obj

// a, b 需要括号；而 value 可以不加括号
#define UPDATE_VALUE(value, a, b) (value = (a) + (b))

// a 需要括号；而 b 可以不加括号
#define FOO(a, b) Bar((a) + 1, b)
```




#### PRE.03 包含多条语句的函数式宏的实现语句必须放在 do-while(0) 中

**【描述】**
宏本身没有代码块的概念。当宏在调用点展开后，宏内定义的表达式和变量融合到调用代码中，可能会出现变量名冲突和宏内语句被分割等问题。
通过 do-while(0) 显式为宏加上边界，让宏有独立的作用域，并且跟分号能更好的结合而形成单条语句，从而规避此类问题。

如下所示的宏是错误的用法（为了说明问题，示例代码稍不符规范）：

```c
// 不符合
#define FOO(x) \
    (void)printf("arg is %d\n", (x)); \
    DoSomething((x));
```

当像如下示例代码这样调用宏FOO，for 循环只执行了宏的第一条语句，宏的后一条语句只在循环结束后执行一次。

```c
for (i = 1; i < MAX_TIMES; i++)
    FOO(i);
```

用大括号将FOO定义的语句括起来可以解决上面的问题：

```c
#define FOO(x) { \
    (void)printf("arg is %d\n", (x)); \
    DoSomething((x)); \
}
```

但是，如下示例代码，会出现编译报错(else没有与之匹配的if语句)：

```c
if (condition)
    FOO(MAX_MONTH);
else
    FOO(MAX_YEAR);
```

更好的写法是用 do-while(0) 把宏FOO执行体括起来，如下所示：

```c
// 符合
#define FOO(x) do { \
    (void)printf("arg is %d\n", (x)); \
    DoSomething((x)); \
} while (0)
```

**【例外】**
- 包含 break, continue 语句的宏可以例外，使用此类宏务必特别小心。
- 宏中包含不完整语句时，可以例外。比如用宏封装 for 循环的条件部分。
- 非多条语句，或单个 if/for/while/switch 语句，可以例外。





#### PRE.04 禁止把带副作用的表达式作为参数传递给函数式宏

**【描述】**
由于宏只是文本替换，对于内部多次使用同一个宏参数的函数式宏，将带副作用的表达式作为宏参数传入会导致非预期的结果。

**【反例】**
如下所示，宏SQUARE本身没有问题，但是使用时将带副作用的表达式a++传入导致a的值在SQUARE执行后的结果跟预期不符：

```c
#define SQUARE(a) ((a) * (a))

int a = 5;
int b = SQUARE(a++); // 不符合： 展开后表达式中有2个 "a++"，其结果可能是非预期的。
```

SQUARE(a++)展开后为((a++) * (a++))，变量a自增了两次，其值为7，而不是预期的6。

**【正例】**
代码做如下修改：

```c
a++; // 结果：a = 6，只自增了一次
b = SQUARE(a);
```





#### PRE.05 函数式宏定义中慎用 return、goto、continue、break 等改变程序流程的语句

**【描述】**
宏中使用 return、goto、continue、break等改变流程的语句，虽然能简化代码，但同时也隐藏了真实流程，不易于理解，存在过度封装，容易导致资源泄漏等问题。

**【反例】**
如下是宏封装 return 容易导致过度封装和使用的场景：

如下代码，status的判断是主干流程的一部分，用宏封装起来后，变得不直观了，阅读时习惯性把RETURN_IF宏忽略掉了，从而导致对主干流程的理解有偏差。

```c
#define LOG_AND_RETURN_IF_FAIL(ret, fmt, ...) do { \
    if ((ret) != OK) { \
        (void)ErrLog(fmt, ##__VA_ARGS__); \
        return (ret); \
    } \
} while (0)

#define RETURN_IF(cond, ret) do { \
    if (cond) { \
        return (ret); \
    } \
} while (0)

ret = InitModuleA(a, b, &status);
LOG_AND_RETURN_IF_FAIL(ret, "Init module A failed!"); // 符合

RETURN_IF(status != READY, ERR_NOT_READY); // 不符合： 重要逻辑不明显

ret = InitModuleB(c);
LOG_AND_RETURN_IF_FAIL(ret, "Init module B failed!"); // 符合
```

如下是宏封装 return 也容易引发内存泄漏的场景：

```c
#define CHECK_PTR(ptr, ret) do { \
    if ((ptr) == NULL) { \
        return (ret); \
    } \
} while (0)

...

mem1 = MemAlloc(STR_SIZE_MAX);
CHECK_PTR(mem1, ERR_CODE_XXX);

mem2 = MemAlloc(STR_SIZE_MAX);
CHECK_PTR(mem2, ERR_CODE_XXX); // 内存泄漏问题
```

如果 mem2 申请内存失败了，CHECK_PTR 会直接返回，而没有释放 mem1。

除此之外，CHECK_PTR 宏命名也不好，宏名只反映了检查动作，没有指明结果。只有看了宏实现才知道指针为空时返回失败。

综上所述：

不推荐宏定义中封装 return、goto、continue、break 等改变程序流程的语句；

**【例外】**
用于返回值判断等异常处理场景的宏可以包含改变程序流程的语句。

注意：包含 return、goto、continue、break等改变流程语句的宏命名，务必要体现对应关键字。
比如：
```c
#define RETURN_IF(condition, retValue) \
    if (condition) { \
        RecordFailInfo(__FILE__, __LINE__); \
        return retValue; \
    }
```




#### PRE.06 函数式宏要简短

**【描述】**
函数式宏本身的一大问题是比函数更难以调试和定位，特别是宏过长，调试和定位的难度更大。

而且宏扩展会导致目标代码膨胀。建议函数式宏不要超过10行（非空非注释）。





#### PRE.07 宏的名称不应与关键字相同

**【描述】**
使用宏来改变语言关键字（包括用于实现语言扩展的关键字）的含义会导致代码难以理解。如果定义这种宏的同时又包含了标准头文件，则程序会产生未定义行为。

**【反例】**
```c
// 不符合：改变了int的行为，导致后面包含标准头文件时，程序出现未定义的行为
#define int OTHER_TYPE
#include <stdlib.h>

// 不符合：重定义关键字
#define while(x) for (; (x);)
```





#### PRE.08 禁止宏调用参数中出现预编译指令

**【描述】**
这里的宏指函数式宏，其参数不能包括预处理器指令，如#include，#define和#ifdef，这样做会导致未定义的行为。

此规则还适用于在调用标准库函数参数的场景，因为任何标准库函数可作为宏来实现。

**【反例】**
如下代码可能会导致程序出现未定义行为。
```c
#define WRITE_LOG(X)  printf("%s\n", #X)
int Foo(void)
{
    WRITE_LOG(
#ifdef PLATFORM1
    "Notice: Something error."
#else
    "Code: 4567"
#endif
    );
}
```

**【正例】**
```c
#define WRITE_LOG(X)  printf("%s\n", #X)
int Foo(void)
{
#ifdef PLATFORM1
    WRITE_LOG("Notice: Something error.");
#else
    WRITE_LOG("Code: 4567");
#endif
}
```





#### PRE.09 宏定义不应以分号结尾

**【描述】**
当宏定义的结尾有分号时，从代码中难以直观发现语句的结束，降低了程序语句的可读性，并增加了程序员在使用宏时额外增加分号的可能(不小心额外增加的分号可能导致程序流程错误)。因此，宏末尾的分号应由使用者提供，宏定义不应以分号结尾。

**【反例】**
示例用宏定义for语句中的循环头。此宏使用了一个表示循环次数的整数参数，程序员错误地在宏定义的结尾加了分号。

```c
#define LOOP(count)  for (int i = 0; i < (count); i++);

int count = ...;
LOOP(5) {
    puts("In a loop\n");
}
```

程序员希望从代码中获得以下输出：
```c
In a loop
In a loop
In a loop
In a loop
In a loop
```

但是由于宏定义末尾的分号，for程序中的循环具有空语句，因此语句"In a loop"仅被打印一次。本质上，宏定义末尾的分号更改了程序控制流。

**【正例】**
在宏定义的末尾不使用分号，而将是否使用分号的决定权交给宏的使用者：

```c
#define LOOP(count)  for (int i = 0; i < (count); i++)

int count = ...;
LOOP(5) {
    puts("In a loop\n");
}
```




#### PRE.10 宏定义不应依赖宏外部的局部变量名

**【描述】**
宏定义中要使用的变量都要求作为参数传递给宏。
如果宏定义中直接使用宏外部的局部变量名，会导致宏的可重用性差，而且不利于理解。

**【反例】**
```c
#define INIT(x) do { \
    count = (x)->y->length; \
} while (0)

...
int count;
INIT(msg);
```

**【正例】**
```c
#define INIT(x) ((x)->y->length)

...
int count = INIT(msg);
```





### 2.1.2 条件编译




#### PRE.11 \#if或\#elif预处理指令中的常量表达式的值应为布尔值

**【描述】**
`#if`或`#elif`预处理指令中的常量表达式的值应为布尔值。
如果预处理指令中的常量表达式仅是一个开关用途的宏，可以使用数值0或1作为该宏的值。

**【反例】**
```c
#define VERSION 3320

#if 3320    // 不符合

#endif

#if 0       // 不符合

#endif

#if 1       // 不符合

#endif

#if VERSION // 不符合

#endif
```

**【正例】**
```c
#define OLD_VERSION 1000
#define VERSION 3320
#define ENABLE_MMX   1
#define ENABLE_FLOAT 0


#if ENABLE_MMX            // 符合
#endif

#if ENABLE_FLOAT          // 符合
#endif

#if defined(VERSION)      // 符合
#endif

#if VERSION > OLD_VERSION // 符合
#endif
```





#### PRE.12 \#if或\#elif预处理指令中的常量表达式被求值前应确保其使用的标识符是有效的

**【描述】**
在宏扩展之后，如果预处理指令中的常量表达式含有编译器不识别的标识符，则会将这些标识符替换为常量0，存在这种标识符通常认为是编程错误。
因此，良好的做法是在预处理指令中的常量表达式被求值前，使用`#if defined`、`#ifdef`等预处理指令检查标识符是否有效。

**【反例】**
```c
#if VERSION == 4000 // 不符合：VERSION可能未定义
#endif
```

**【正例】**
```c
#if defined(VERSION) && VERSION == 4000 // 符合
...
#endif
```

```c
#ifdef VERSION       // 符合
#if VERSION == 4000  // 符合
...
#endif
#endif
```




#### PRE.13 所有\#else、\#elif、\#endif和与之对应的\#if、\#ifdef、\#ifndef预处理指令应出现在同一文件中

**【描述】**
当使用多个文件来构成这些预处理块时，难以直观发现代码块的关联，增加了阅读和维护的复杂度，从而更容易产生错误。

**【反例】**
如下代码示例中，未在相同文件中闭合预处理块：

```c
// sample.h 开始
#if defined(__VXWORKS__)  // 未在相同文件中闭合该预处理块
#include "vx_config.h"


// 这里结束前，本应当有 #endif 与前面的 #if defined 形成闭合
// sample.h 结束
```

**【正例】**
如下代码示例中，在相同文件中闭合预处理块：

```c
// sample.h 开始
#if defined(__VXWORKS__)    // 在相同文件中闭合该预处理块
#include "vx_config.h"
#endif
// sample.h 结束
```




## 2.2 头文件




### INC.01 在头文件中声明需要对外公开的接口

**【描述】**
通常情况下，每个.c文件都应有一个相应的.h文件（并不一定同名），用于放置对外提供的函数声明、宏定义、类型定义等。

**【正例】**
以下代码中函数Foo是对外提供的接口，函数Bar是内部函数，不对外提供。

foo.h 内容
```c
#ifndef FOO_H
#define FOO_H

void Foo(void); // 符合：头文件中声明对外接口

#endif
```

foo.c 内容
```c
// 符合：只在文件内部使用的函数的声明放在.c文件的头部，并声明为static限制其作用域
static void Bar(void);

void Foo(void)
{
    Bar();
}

static void Bar(void)
{
    ...
}
```

内部使用的函数声明，宏、枚举、结构体等定义不应放在头文件中。被多个源文件调用的内联函数要放在头文件中定义。

有些产品中，习惯一个.c文件对应两个.h文件，一个用于存放对外公开的接口，一个用于存放内部需要用到的定义、声明等，以控制.c文件的代码行数。不提倡这种风格，产生这种风格的根源在于.c过大，应当首先考虑拆分.c文件。另外，一旦把私有定义、声明放到独立的头文件中，就无法从技术上避免别人包含。

本规则反过来并不一定成立（一个.h文件对应一个.c文件）。例如像命令 ID 定义头文件这种特别简单的头文件，不需要有对应的.c存在。

允许出现一个.h对应多个.c文件。

**【例外】**
main函数、单元测试函数所在的.c文件如果不需要提供对外接口，可以没有对应的.h文件。



### INC.02 头文件的扩展名只使用.h，不使用非习惯用法的扩展名，如.inc

**【描述】**
有些产品中使用了 .inc 作为头文件扩展名，这不符合C语言的习惯用法。
在使用 .inc 作为头文件扩展名的产品，习惯上用于标识此头文件为私有头文件。
但是从产品的实际代码来看，这一条并没有被遵守，一个 .inc 文件被多个 .c 包含。
本规范不提倡将私有定义单独放在头文件中，具体见条款 “[在头文件中声明需要对外公开的接口](G.INC.01_在头文件中声明需要对外公开的接口.md)”。  
除此之外，使用 .inc 可能还导致某些IDE工具无法识别其为头文件，造成很多功能不可用，如“跳转到变量定义处”。虽然其中一些可以通过配置强迫IDE识别 .inc 为头文件，但还是有些无法通过配置识别。





### INC.03 禁止头文件循环依赖

**【描述】**
头文件循环依赖，指 a.h 包含 b.h，b.h 包含 c.h，c.h 包含 a.h，导致任何一个头文件修改，都导致所有包含了a.h/b.h/c.h的代码全部重新编译一遍。

而如果是单向依赖，如a.h包含b.h，b.h包含c.h，而c.h不包含任何头文件，则修改a.h不会导致包含了b.h/c.h的源代码重新编译。

头文件循环依赖直接体现了架构设计上的不合理，可通过优化架构去避免。





### INC.04 禁止包含用不到的头文件

**【描述】**
如果当前源文件没有直接引用头文件中的对外接口，则不应该包含。

包含不需要的头文件会引入不必要的依赖，增加了模块或单元之间的耦合度，增加了代码复杂性，可维护性差。

很多系统中头文件包含关系复杂。程序员为了省事起见，直接包含一切想到的头文件，甚至发布了一个god.h，其中包含了所有头文件，然后发布给各个项目组使用。

这种只图一时省事的做法，不仅导致整个系统的编译时间恶化，而且代码的维护成本非常高。





### INC.05 头文件应当自包含

**【描述】**
简单的说，自包含就是任意一个头文件均可独立编译。如果包含某个头文件，会引入对其他头文件的依赖，则会给用户增添不必要的负担。

比如，如果a.h不是自包含的，需要包含b.h才能编译，会带来的危害：
- 每个使用a.h头文件的.c文件，为了让引入的a.h的内容编译通过，都要包含额外的头文件b.h。
- 额外的头文件b.h必须在a.h之前进行包含，这在包含顺序上产生了依赖。

注意：该规则需要与[禁止包含用不到的头文件](G.INC.04_禁止包含用不到的头文件.md)规则一起使用，a.h要刚刚可以自包含，不能在a.h中多包含任何满足自包含之外的其他头文件。





### INC.06 头文件必须用\#define保护，防止重复包含

**【描述】**
为防止头文件被重复包含，所有头文件都应当使用`#define`作为包含保护；不要使用`#pragma once`。

定义包含保护符时，应该遵守如下规则：
- 保护符使用唯一名称；
- 建议考虑项目源代码树顶层以下的文件路径，不要在受保护部分的前后放置代码或者注释，文件头注释除外。

假定 VOS 工程的 timer 模块的 timer.h，其目录为 vos/include/timer.h。其保护符若使用 'TIME_H'很容易不唯一，所以使用项目源代码树的全路径，如：

```c
#ifndef VOS_INCLUDE_TIMER_H
#define VOS_INCLUDE_TIMER_H

...

#endif
```

注意，保护符命名时，避免首尾是下划线(\_)：

```c
#ifndef _VOS_INCLUDE_TIME_H_   // 不符合
```





### INC.07 按照合理的顺序包含头文件

**【描述】**
使用固定的头文件包含顺序可增强可读性,避免隐藏依赖。
建议按稳定度包含头文件，依次顺序为：
C标准库，操作系统库，平台库，项目公共库，自己其他的依赖。

**【正例】**
考虑到C标准库，操作系统库等头文件比项目自研的头文件相对稳定，foo.c中包含头文件的次序如下：

```c
#include <stdlib.h> // C 标准库
#include <string.h>

#include <linux/list.h> // 操作系统库
#include <linux/time.h>

#include "platform/base.h" // 平台库
#include "platform/struct.h"

#include "project/public/log.h" // 项目公共库

#include "bar.h" // foo.c 的依赖 bar.h

#include "foo.h" // foo.c 对应头文件放最后一个，也可以放第一个
```

**【例外】**
当源文件对应的头文件用于验证自包含时，可以作为第一个头文件。




## 2.3 数据类型


**【备注】**
社区已有的数据类型有：数值类型、货币类型、布尔类型、字符类型、二进制类型、日期/时间类型、几何类型、网络地址类型、位串类型、文本搜索类型、UUID类型、JSON类型、对象标识符类型、伪类型、列存表支持的数据类型（详情请参见开发者指南数据类型章节）。

### TYP.01 不要重复定义基础类型

**【描述】**
产品或项目应规划使用相同版本的类型定义，这是一种很好的实践。建议优先使用符合C99，C11标准定义的类型（如：在一个产品中统一使用stdint.h中定义的整数类型）。

避免滥用 `typedef`/`#define` 对基础类型起别名，因为一个产品或项目中如果存在多种类型定义（如同时使用u32，v32，uint32，uint表示unsigned int类型）会使代码变得更加混乱，难以维护和难以编译。使用不同的类型系统，也违反了风格一致原则。

所以除非有明确的必要性，否则不要用 `typedef`/`#define` 对基础类型进行重定义。

下面的场景中重新定义了基础类型为uintptr，其屏蔽了不同平台（CPU/OS）下C语言基本数值类型的位宽差异，是具有必要性的。
```c
#include <bits/wordsize.h>

// __WORDSIZE is defined in wordsize.h
#if __WORDSIZE == 64
typedef unsigned long int uintptr;
#else
typedef unsigned int uintptr;
#endif
```

注意：
当整合其他独立模块代码（如开源代码、第三方代码）时，可增加适配层隔离定义冲突。

- 在可预见的未来，需要提高精度
```c
typedef uint8 DevId;
...
// 若干版本后扩展成 16-bit
typedef uint16 DevId;
```

- 有特殊作用的类型
```c
typedef void *Handle;
```

注意：**能用 typedef 的地方，尽量不用 #define 进行别名定义。**

下面例子是不同模块都使用各自的类型别名，因为历史原因，同名的类型，定义却不同。
```c
// 模块 A
...
typedef unsigned long ULONG;
...
```
```c
// 模块 B
...
#define ULONG UINT32
...
```
模块 B 因为是从 32 位平台移植过来，代码中把 `ULONG` 当作 32 位使用，所以移植时使用 `UINT32` 定义。
当系统运行在 `unsigned long` 为 64 位的平台上时，如果两个模块有接口交互，则这两种类型定义将引起混乱，甚至可能出现严重问题。





### TYP.02 使用恰当的基本类型作为操作符的操作数

**【描述】**
在下面的表格中，"Y"表示该列对应的基本类型可以被该行对应的操作符当作操作数使用，"N"表示该列对应的基本类型被该行对应的操作符当作操作数使用时，是不符合本条款要求的。
"N"的原因有6种，分别以"N1"到"N6"表示，在表格下面的“注”中有具体说明。

<table style="font-size:0.75em">
<tr><th> 操作符 </th><th> 操作数 </th><th> 布尔 </th><th> 字符 </th><th> 枚举 </th><th> 有符号数 </th><th> 无符号数 </th><th> 浮点数 </th><th> 指针 </th></tr>
<tr><td> [ ] </td><td> 操作数 </td><td> N1 </td><td> N2 </td><td> Y </td><td> Y </td><td> Y </td><td> N5 </td><td> N6 </td></tr>
<tr><td> 一元 + </td><td> 操作数 </td><td> N1 </td><td> N2 </td><td> N3 </td><td> Y </td><td> Y </td><td> Y </td><td> N6 </td></tr>
<tr><td> 一元 - </td><td> 操作数 </td><td> N1 </td><td> N2 </td><td> N3 </td><td> Y </td><td> Y </td><td> Y </td><td> N6 </td></tr>
<tr><td> 一元 ++ 一元 -- </td><td> 任意操作数 </td><td> N1 </td><td> Y </td><td> N3 </td><td> Y </td><td> Y </td><td> Y </td><td> Y </td></tr>
<tr><td> += -=  二元 + 二元 - </td><td> 任意操作数 </td><td> N1 </td><td> Y </td><td> N3 </td><td> Y </td><td> Y </td><td> Y </td><td> Y </td></tr>
<tr><td> /= *= / 二元 * </td><td> 任意操作数 </td><td> N1 </td><td> N2 </td><td> N3 </td><td> Y </td><td> Y </td><td> Y </td><td> N6 </td></tr>
<tr><td> %= % </td><td> 任意操作数 </td><td> N1 </td><td> N2 </td><td> N3 </td><td> Y </td><td> Y </td><td> N5 </td><td> N6 </td></tr>
<tr><td> <<= >>= << >> </td><td> 任意操作数 </td><td> N1 </td><td> N2 </td><td> N3 </td><td> N4 </td><td> Y </td><td> N5 </td><td> N6 </td></tr>
<tr><td> > < <= >= </td><td> 任意操作数 </td><td> N1 </td><td> Y </td><td> Y </td><td> Y </td><td> Y </td><td> Y </td><td> Y </td></tr>
<tr><td> == != </td><td> 任意操作数 </td><td> Y </td><td> Y </td><td> Y </td><td> Y </td><td> Y </td><td> N5 </td><td> Y </td></tr>
<tr><td> ~ |= ^= &= | ^ 二元 & </td><td> 任意操作数 </td><td> N1 </td><td> N2 </td><td> N3 </td><td> N4 </td><td> Y </td><td> N5 </td><td> N6 </td></tr>
<tr><td> ! && || </td><td> 任意操作数 </td><td> Y </td><td> N1 </td><td> N1 </td><td> N1 </td><td> N1 </td><td> N1 </td><td> Y </td></tr>
<tr><td> ? : </td><td> 第一操作数 </td><td> Y </td><td> N1 </td><td> N1 </td><td> N1 </td><td> N1 </td><td> N1 </td><td> Y </td></tr>
</table>

注：
- N1：当操作数的语义是数值时，应使用数值类型的值，不应使用布尔类型的值；当操作数的语义是布尔值时，应使用布尔类型的值，不应该使用数值类型的值。
- N2：当操作数的语义是数值时，不应该使用字符类型。字符数据的数值是实现定义的，可能是有符号数也可能是无符号数。
- N3：枚举常量的整数类型是由实现定义的，可能是无符号数也可能是有符号数，参与运算后可能产生非预期的结果。
- N4：对有符号整数进行按位运算的结果是实现定义的，因此位操作符应仅与无符号整数操作数一起使用，但是需要注意整数提升产生的问题。
- N5：计算机中通常因无法精确表示浮点数而进行近似或舍入，因此使用 == 或 != 来比较两个浮点数的结果通常是非预期的，其他为使用浮点数不符合语法约定的情况。
- N6：中括号中使用指针，不符合阅读习惯，其他为使用指针不符合语法约定的情况。

**【例外】**
有符号数类型的非负数常量表达式可以用作移位操作符的右操作数。




### TYP.03 使用合适的类型表示字符

**【描述】**
字符串是一个连续的字符序列，以第一个null字符结束，并且包含第一个null字符。
C编程语言支持窄字符串(包括单字节字符串，多字节字符串)和宽字符字符串。
窄字符串是以第一个null字符（'\0'）结尾的字节字符串。
宽字符串是连续的宽字符序列，以第一个null宽字符（L'\0'）结尾，并包含第一个null宽字符。

字符串可以通过字符数组实现，并且容易遇到与数组相同的问题。因此，对数组的相关条款也适用于字符串。
用于表示字符数据时，窄字符串的每个元素类型都要使用char类型。
由于在不同系统中，char类型可以实现为signed char或unsigned char，因此不要使用char类型来表示整数。
unsigned char可以在当不关心被操作的对象类型，并且需要访问该对象的所有bit位时使用。unsigned char不能表示字符，也不能表示字符串。




## 2.4 常量




### CNS.01 禁止使用小写字母“l”作为数值型常量后缀

**【描述】**
C语言标准允许使用后缀来显式指定数值型常量的类型，例如：整数常量可以使用后缀字母 l 或 L 表示常量类型 `long`，使用字母 ll 或 LL 表示 `long long`。当使用小写字母 l 指定数值型常量类型时，在视觉上容易和数字 1 混淆。为了避免这种混淆带来的误解，应使用大写字母 L 或 LL 作为数值型常量的后缀。

**【反例】**
如下代码示例中，宏 CONSTANT_BARRETT_REDUCTION 的值为 0x1F7011641，但是视觉上像是 0x1F701164111：

```c
#define CONSTANT_BARRETT_REDUCTION 0x1F7011641ll
```

**【正例】**
如下代码示例通过使用大写字母 L 而不是小写字母 l 来消除视觉上的错觉：

```c
#define CONSTANT_BARRETT_REDUCTION 0x1F7011641LL
```





### CNS.02 不要使用难以理解的常量

**【描述】**
难以理解的常量，即看不懂，通过上下文也难以明确含义的数字常量、字符串常量。
难以理解的常量并非一个非黑即白的概念，看不懂也有程度，需要结合代码上下文和业务相关知识来判断。

例如数字 12，在不同的上下文中情况是不一样的：
`type = 12`; 就看不懂，不能明确12代表什么类型；
但 `year = month * 12`; 就能看懂，这里12很明显是指1年有12个月。

数字 0 有时候也是难以理解的常量，比如 `status = 0;`，0 无法明确是什么状态。

解决途径：
- 对于单点使用的难以理解的常量，按需增加注释说明。
- 对于多处使用的难以理解的常量，应该定义宏或 const 变量，并通过符号命名自注释。

禁止出现下列情况：
- 没有通过符号命名来解释数字含义，如 `#define ZERO 0`
- 符号命名限制了其取值，如 `#define XX_TIMER_INTERVAL_300MS 300`

**【反例】**
如下示例代码中，使用了难以理解的常量：

```c
int currentType = psInParam->GetValue("servType");
// 下面使用的数字，不容易理解其具体含义
if (currentType == 1) {
    ...
} else if (currentType == 4) {
    ...
} else {
    ...
}

if (age >= 18) {
    ... // 执行某些操作
} else {
    ... // 执行另外的某些操作
}
```

**【正例】**
如下代码示例中，使用能表达含义的宏或常量：

```c
#define SERV_TYPE_SET 1
#define SERV_TYPE_QUERY 4
#define ADULT_AGE 18

int currentType = psInParam->GetValue("servType");

if (currentType == SERV_TYPE_SET) {
    ...
} else if (currentType == SERV_TYPE_QUERY) {
    ...
} else {
    ...
}

if (age >= ADULT_AGE) {
    ... // 执行某些操作
} else {
    ... // 执行另外的某些操作
}
```

**【反例】**
如下示例代码中的问题在于计算长度时`strlen("V100R01C10")`中，字符串遗漏了一个'1'：

```c
bCond = (strncmp(gSrcDataVer, "V100R011C10", strlen("V100R01C10")) == 0);
```

**【正例】**
如下代码的修改有两个好处：
1.不会出错；
2.如果版本号要修改，修改一次即可：

```c
// 为字符串常量（表示版本号）重定义符号常量
#define    VERSION    "V100R011C10"
bCond = (strncmp(gSrcDataVer, VERSION, strlen(VERSION)) == 0);
```





## 2.5 变量




### VAR.01 禁止读取未经初始化的变量

**【描述】**
这里的变量，指的是局部动态变量，并且还包括内存堆上申请的内存块。
因为他们的初始值都是不可预料的，所以禁止未经有效初始化就直接读取其值。

```c
void Foo(int condVal)
{
    int data;
    Bar(data); // 不符合：未初始化就使用
    ...
}
```

如果有不同分支，要确保所有分支都得到初始化后才能使用：
```c
#define CUSTOMIZED_SIZE 100
void Foo(int condVal)
{
    int data;
    if (condVal > 0) {
        data = CUSTOMIZED_SIZE;
    }
    Bar(data); // 不符合：其他分支中(condVal <= 0)，data值未初始化
    ...
}
```

注意：如果编译器允许，变量应按需定义，避免初始化问题。




### VAR.02 不要在子作用域中重用变量名

**【描述】**
一个作用域包含另一个作用域时，不要在这两个作用域中使用相同的变量名，例如：

- 如果某变量位于全局变量的子作用域内，则这个变量不应与全局变量重名。
- 语句块中定义的变量不能与包含该语句块的任何块中定义的变量重名。

重用变量名会使程序员对正在修改哪个变量感到困惑。此外，如果变量名被重用，则说明该变量名可能太通用，应使用更具有描述性的变量名。

**【反例】**
如下代码示例中，在Func()内声明了数组变量message，并且在if语句块中定义了一个与之重名的message变量，程序员可能是无意间复制了变量名到if代码块中，错误使用了MAX_MESSAGE_LEN，超出了内层局部变量message大小，存在缓冲区溢出风险。

```c
#define MAX_MESSAGE_LEN 100
#define CUSTOMIZED_SIZE 80

void Func(const char *str)
{
    char message[MAX_MESSAGE_LEN];
    ...
    if (str != NULL) {
        char message[CUSTOMIZED_SIZE];   //  使用了与外层相同的变量名
        ...
        // MAX_MESSAGE_LEN 使用错误
        int ret = sprintf_s(message, MAX_MESSAGE_LEN, "Error: %s\n", str);
        ...
    }
    ...
}

int main(void)
{
    ...
    Fun("some error");

    return 0;
}
```

**【正例】**
如下代码示例中，使用了不同的变量名：

```c
#define MAX_MESSAGE_LEN 100
#define CUSTOMIZED_SIZE 80

void Func(const char *str)
{
    char message[MAX_MESSAGE_LEN];
    ...
    if (str != NULL) {
        char msg[CUSTOMIZED_SIZE];
        ...
        int ret = sprintf_s(msg, sizeof(msg), "Error: %s\n", str);
        ...
    }
    ...
}

int main(void)
{
    ...
    Fun("some error");

    return 0;
}
```




### VAR.03 避免大量栈分配

**【描述】**
程序在运行期间，函数内的局部变量存储在栈中，而栈的大小是有限的，局部变量占用的栈空间过大时，可能导致出现栈溢出错误。
建议在定义函数局部变量时(特别是递归调用、循环体中定义变量)，需要充分考虑单个函数及全调用栈的开销，并对函数中的局部变量大小进行一定限制，避免因占用过多的栈空间导致程序运行失败。

例如，linux内核的默认构建配置文件中，限制函数帧的大小不超过1024字节，如果超出限制则出现编译告警。

**【反例】**
如下代码示例中的`buff[MAX_BUFF]` 数组占用空间过大，可能导致栈空间不够，程序发生 stack overflow 异常。

```c
#define MAX_BUFF 0x1000000

char buff[MAX_BUFF] = {0};
...
```
**【正例】**
如下代码示例中，通过动态分配内存的方式，避免栈空间占用过大的问题：

```c
#define MAX_BUFF 0x1000000
char *buf = (char *)malloc(MAX_BUFF);
if (buf == NULL) {
    ... // 错误处理
}
...
```

如上代码中须检查动态分配函数的返回值，如果分配内存大小的来源不可信，则需要注意校验其值的范围。

**【反例】**
递归调用太深也会造成栈分配过大，因此递归函数必须确保调用深度可控。
如下递归函数，没有控制其递归深度，调用深度随m的值增加而增加，所使用的栈大小也随之增加，可能导致栈空间不足：

```c
uint64_t Sum(uint32_t m)
{
    if (m == 0) {
        return 0;
    }
    return Sum(m - 1) + m;
}
```

**【正例】**
重构上面的递归函数，不使用递归算法，所使用的栈大小不会随m的变化而变化：

```c
uint64_t Sum(uint32_t m)
{
    uint64_t n = (uint64_t)m;
    return (n * (n + 1) / 2);
}
```





### VAR.04 慎用全局变量

**【描述】**

不允许私自定义全局变量，全局变量统一放在knl_instance.h里面合适的结构体里，并且根据其他已有变量示意写好初始化语句，全局变量如果被多个线程访问，需要注意多线程并发控制。

**【事例】**
```c
//knl_instance.h
//定义

typedef struct knl_g_reqcheck_context {
    volatile bool g_shutdown_requested;
    volatile ThreadId g_cancel_requested;
    volatile bool g_close_poll_requested;
} knl_g_reqcheck_context;


//knl_instance.cpp
//实例化

static void knl_g_reqcheck_init(knl_g_reqcheck_context* reqcheck_cxt)
{
    Assert(reqcheck_cxt != NULL);
    reqcheck_cxt->g_shutdown_requested = false;
    reqcheck_cxt->g_cancel_requested = 0;
    reqcheck_cxt->g_close_poll_requested = false;
}
```



### VAR.05 指向资源句柄或描述符的变量，在资源释放后立即赋予新值

**【描述】**
指向资源句柄或描述符的变量包括指针、文件描述符、socket描述符以及其它指向资源的变量。
以指针为例，当指针成功申请了一段内存之后，在这段内存释放以后，如果其指针未立即设置为NULL，也未分配一个新的对象，那这个指针就是一个悬空指针。
如果再对悬空指针操作，可能会发生重复释放或访问已释放内存的问题，造成安全漏洞。
消减该漏洞的有效方法是将释放后的指针立即设置为一个确定的新值，例如设置为NULL。对于全局性的资源句柄或描述符，在资源释放后，应该马上设置新值，以避免使用其已释放的无效值；对于只在单个函数内使用的资源句柄或描述符，应确保资源释放后其无效值不被再次使用。

**【反例】**
如下代码示例中，根据消息类型处理消息，处理完后释放掉body指向的内存，但是释放后未将指针设置为NULL。如果还有其他函数再次处理该消息结构体时，可能出现重复释放内存或访问已释放内存的问题。

```c
int Func(void)
{
    SomeStruct *msg = NULL;
    int ret = 0;

    ... // 分配msg，初始化msg->type，分配 msg->body 的内存空间

    if (msg->type == MESSAGE_A) {
        ...
        free(msg->body); // 不符合：释放内存后，未置空
    }
    ...
    if (someError) {
        ...
        goto ERROR_EXIT;
    }
    // 将msg存入全局队列，后续可能使用已释放的body成员
    InsertMsgToQueue(msg);
    return ret;
ERROR_EXIT:
    ...
    free(msg->body);  // 可能再次释放了body的内存
    free(msg);
    return ret;
}
```

**【正例】**
如下代码示例中，立即对释放后的指针设置为NULL，避免重复释放指针。

```c
int Func(void)
{
    SomeStruct *msg = NULL;
    int ret = 0;

    ... // 初始化msg->type，分配 msg->body 的内存空间

    if (msg->type == MESSAGE_A) {
        ...
        free(msg->body);
        msg->body = NULL;
    }
    ...
    if (someError) {
        ...
        goto ERROR_EXIT;
    }
    // 将msg存入全局队列，后续可能使用已释放的body成员
    InsertMsgToQueue(msg);
    return ret;
ERROR_EXIT:
    ...
    free(msg->body); // 马上离开作用域，不必赋值NULL
    free(msg);       // 马上离开作用域，不必赋值NULL
    return ret;
}
```

当free()函数的入参为NULL时，函数不执行任何操作。

**【反例】**
如下代码示例中文件描述符关闭后未赋新值。

```c
SOCKET s = INVALID_SOCKET;
int fd = -1;
...
closesocket(s);
...
close(fd);
...
```

**【正例】**
如下代码示例中，在资源释放后，对应的变量应该立即赋予新值。

```c
SOCKET s = INVALID_SOCKET;
int fd = -1;
...
closesocket(s);
s = INVALID_SOCKET;
...
close(fd);
fd = -1;
...
```

**【反例】**
如下代码示例中，FreeSomeStruct函数中释放p后设置NULL的操作是无效的，导致DoSomeThing函数访问已释放内存。

```c
void FreeSomeStruct(SomeStruct *p)
{
    if (p == NULL) {
        return;
    }
    if (p->content != NULL) {
        free(p->content);
        p->content = NULL;
    }
    free(p);
    p = NULL;
}

void DoSomeThing(void)
{
    SomeStruct *p = ... // 分配结构体内存并初始化
    ...
    if (condition) {
        FreeSomeStruct(p);
    }
    if (p != NULL) {
        // 可能会访问已释放内存
        errno_t ret = memcpy_s(buf, sizeof(buf), p->content, p->contentLen);
        ...
    }
}
```

**【正例】**
如下代码示例中，立即对释放后的指针设置为NULL，避免访问已释放内存。

```c
void FreeSomeStruct(SomeStruct *p)
{
    if (p == NULL) {
        return;
    }
    if (p->content != NULL) {
        free(p->content);
        p->content = NULL;
    }
    free(p);
}

void DoSomeThing(void)
{
    SomeStruct *p = ... // 分配结构体内存并初始化
    ...
    if (condition) {
        FreeSomeStruct(p);
        p = NULL;
    }
    if (p != NULL) {
        errno_t ret = memcpy_s(buf, sizeof(buf), p->content, p->contentLen);
        ...
    }
}
```

**【影响】**

再次使用已经释放的内存，或者再次释放已经释放的内存，或其他使用已释放资源的行为，可能导致拒绝服务或执行任意代码。

**【相关软件CWE编号】** CWE-415，CWE-416

**【业界典型漏洞】** CVE-2015-0057




### VAR.06 禁止将局部变量的地址返回到其作用域以外

**【描述】**
如果对象在其生命周期之外被引用，则程序会产生未定义行为。当指针指向的对象到达其生存期结束时，指针的值将变得不确定。
因此，禁止将局部变量的地址返回到其作用域以外。

**【反例】**
如下代码示例中，Func()函数返回了局部变量的地址，在调用处解引用该指针程序会产生未定义行为：

```c
int *Func(void)
{
    int localVar = 0;
    ...
    return &localVar; // 不符合
}

void Caller(void)
{
    int *p = Func();
    ...
    int x = *p;  // 程序会产生未定义行为
}
```

**【正例】**
如下代码示例中，重构Func()函数返回值类型，使其返回一个整数值：

```c
int Func(void)
{
    int localVar = 0;
    ...
    return localVar;
}

void Caller(void)
{
    int x = Func();
    ...
}
```





### VAR.07 避免将只在一个函数中使用的变量声明为全局变量

**【描述】**
变量如果仅在文件或函数范围内使用，在满足功能的同时，应在最小作用域内声明。
如果变量声明的范围比需要的范围大，则会降低代码的可读性，并可能被意外引用而产生预期之外的错误。 比如，在单个函数作用域内定义的对象减少了不经意间访问函数作用域外部对象的可能性，并明确了不能在其他作用域访问该对象。

**【反例】**
如下代码示例中，变量`g_total`仅在IncreaseNumber函数中使用，该函数功能是访问并递增计数器变量`g_total`，当此变量`g_total`超过最大值`MAX_COUNT`时，重置计数器，并触发相应的业务处理。

```c
unsigned int g_total = 0;

void IncreaseNumber(void)
{
    // 不符合：使用了全局变量g_total。根据场景看到，这里声明的范围太大了
    if (g_total > MAX_COUNT) {
        g_total = 0;
        ...
        return;
    }
    g_total++;
    ...
}
```

**【正例】**
如下解决方案中，在IncreaseNumber()函数内声明`total`为一个静态变量，限制了被其他作用域引用的范围。静态修饰符在程序执行时一直存在，并且不会在函数调用之间消失。

```c
void IncreaseNumber(void)
{
    static unsigned int total = 0;
    if (total > MAX_COUNT) {
        total = 0;
        ...
        return;
    }
    total++;
    ...
}
```
关键字static还防止重新初始化变量。




### VAR.08 资源不再使用时应予以关闭或释放

**【描述】**
这里的资源包括计算机内存、文件描述符、socket描述符。
程序员在创建或分配资源后，如果该资源不再被使用，程序员应将其正确的关闭或释放，尤其要注意所有可能的异常路径，避免遗漏。
以计算机内存为例，当动态分配内存不再使用时应予以释放，否则会发生内存泄漏，如果攻击者可以有意触发该漏洞，则内存资源可能被耗尽，造成拒绝服务。
以文件描述符为例，当打开的文件不再使用时应将指向该文件的描述符关闭，否则会发生该文件描述符泄漏，如果攻击者可以有意触发该漏洞，则可用的文件描述符可能被耗尽，造成拒绝服务。

**【反例】**

```c
#define BLOCK_SIZE_MAX    256

char *GetBlock(int fd)
{
    ...
    char *buf = (char *)malloc(BLOCK_SIZE_MAX);
    if (buf == NULL) {
        return NULL;
    }

    if (read(fd, buf, BLOCK_SIZE_MAX) != BLOCK_SIZE_MAX) {
        return NULL;  // 不符合：在异常路径中返回前未释放buf指向的内存资源，存在内存泄漏。
    }
    return buf;
}
```

**【正例】**

```c
#define    BLOCK_SIZE_MAX    256

char *GetBlock(int fd)
{
    ...
    char *buf = (char *)malloc(BLOCK_SIZE_MAX);
    if (buf == NULL) {
        return NULL;
    }

    if (read(fd, buf, BLOCK_SIZE_MAX) != BLOCK_SIZE_MAX) {
        free(buf);  // 符合：在异常路径中返回前释放buf指向的内存资源，并立即将指针置空。
        buf = NULL;
    }
    return buf;
}
```

**【影响】**

如果资源在结束使用前未正确的关闭或释放，会造成系统的内存泄漏、句柄泄漏等资源泄漏漏洞。如果攻击者可以有意触发资源泄漏，则可能能够通过耗尽资源来发起拒绝服务攻击。


**【相关软件CWE编号】** CWE-401，CWE-404

**【业界典型漏洞】** CVE-2005-3119, CVE-2004-0222, CVE-2002-1372




## 2.6 表达式




### EXP.01 执行算术运算或比较操作的两个操作数要求具有相同的基本类型

**【描述】**
在执行算术运算或者比较操作时，C语言标准允许不同类型操作数之间进行转换，包括显式转换和隐式转换，这对程序员来说自由度是相当大的。
然而，不管是显式转换还是隐式转换，均可能会导致以下几个问题：数值丢失、符号丢失、精度丢失、布局丢失。这就要求程序员必须明确识别类型转换之间的任何潜在风险，而显示转换肯定比隐式转换更容易识别风险，相同的基本类型之间的算术运算或比较操作肯定比显示转换更加容易被识别风险。

说明：自增和自减运算不在此规则约束范围内。

**【反例】**
如下示例代码中，操作符的操作数具有不同的基本类型，因此不符合本规范：

```c
enum EnumA { A1, A2, A3 } a;
enum EnumB { B1, B2, B3 } b;
int x1 = ...;
unsigned int x2 = ...;
char c = ...;
...

x1 += x2;   // 不符合：有符号数 和 无符号数，混合使用
b > A1;     // 不符合：不同枚举类型中的混合使用
a == b;     // 不符合：不同枚举类型中的混合使用
x2 += c;    // 不符合：无符号数和字符，混合使用
```

**【正例】**
如下示例代码中，修改x1的类型为 `unsigned int` 类型，使操作符的操作数具有相同基本数据类型：

```c
enum EnumA { A1, A2, A3 } a;
enum EnumB { B1, B2, B3 } b;
unsigned int x1 = ...;
unsigned int x2 = ...;
...
x1 += x2;
a > A1;
b == B2;
```




### EXP.02 含有变量自增或自减运算的表达式中禁止再次引用该变量

**【描述】**
含有变量自增或自减运算的表达式中，如果再引用该变量，其结果在C语言标准中未明确定义。不同编译器或者同一个编译器不同版本实现可能会不一致。

为了更好的可移植性，不应该对标准未定义的运算次序做任何假设。

注意，运算次序的问题不能使用括号来解决，因为这不是优先级的问题。

示例：

```c
x = b[i] + i++; // 不符合： b[i]运算跟 i++，先后顺序并不明确
```

正确的写法是将自增或自减运算单独放一行：

```c
x = b[i] + i;
i++; // 符合: 单独一行
```

函数参数：

```c
Func(i++, i); // 不符合： 传递第2个参数时，不确定自增运算有没有发生
```

正确的写法：

```c
i++; // 符合: 单独一行
x = Func(i, i);
```





### EXP.03 用括号明确表达式的操作顺序，避免过分依赖默认优先级

**【描述】**
可以使用括号强调表达式操作顺序，防止因默认的优先级与设计思想不符而导致程序出错。
然而过多的括号会分散代码，并降低了可读性，应适度使用。

当表达式包含不常用，优先级易混淆的操作符时，推荐使用括号，比如表达中同时包含位操作符和其他类型操作符。

**【正例】**
```c
c = (a & 0xFF) + b; // 涉及位操作符，需要括号
```





### EXP.04 不要向sizeof传递有副作用的操作数

**【描述】**
不要向sizeof传递有副作用的操作数，因为操作数的副作用不一定会发生。

以sizeof(expr)为例，如果expr表达式的计算结果不影响sizeof(expr)语句的结果，则是否对expr表达式求值是未指定的行为。

**【反例】**
如下代码示例中，sizeof的操作数 `data++` 是一个有副作用的表达式，但是这个表达式的求值不会影响sizeof语句的结果，因此，data可能没有发生自增。

```c
int data = 15;
size_t size = sizeof(data++);
printf("%d, %zu\n", data, size);
```

**【正例】**
如下代码示例中，在 sizeof 表达式之外递增 data。

```c
int data = 15;
size_t size = sizeof(data);
data++;
printf("%d, %zu\n", data, size);
```




### EXP.05 避免对带位域的结构体的布局做任何假设

**【描述】**
结构体中位域的存储布局是与实现相关的，虽然在每种实现中的布局是确定的，但是在不同的实现下通常不具备可移植性：

> 实现可以分配任何足以容纳位域的可寻址存储单元。
> 如果有足够的空间，结构中一个位域之后的相邻位域应被打包到同一单元中。如果没有足够的空间，那么是否将不合适的位域放入下一个单元，或者与相邻单元重叠存放，是由实现定义的。
> 单元内位域的分配顺序(从高阶到低阶或从低阶到高阶)是由实现定义的。可寻址存储单元的对齐方式是未指定的。

因此，不能依赖于位域的分配布局，否则代码将不可移植，并且可能引发难以检测的错误。

**【反例】**
如下代码示例中，依赖位域的存放顺序，代码不可移植：

```c
/*
 * 以int为32bit的系统为例，BitFrame 共32bit。
 * 在低字节序的系统中，BitFrame的可能存储顺序为 offset低位、offset高位、page、dir
 * 在高字节序的系统中，BitFrame的可能存储顺序为 dir、page、offset高位、offset低位
 */

typedef struct {
    unsigned int offset : 16;
    unsigned int page : 8;
    unsigned int dir : 8;
} BitFrame;
...

BitFrame addr = {0};
unsigned char msg[sizeof(BitFrame)];
...
// 在不同系统下msg的内容可能不同的，使用内存复制的方式不可移植
errno_t ret = memcpy_s(&addr, sizeof(addr), msg, sizeof(msg));
...
```

**【正例】**
如下代码示例中，显式指定位域变量的值：

```c
typedef struct {
    unsigned int offset : 16;
    unsigned int page : 8;
    unsigned int dir : 8;
} BitFrame;
...

BitFrame addr = {0};
unsigned char msg[sizeof(BitFrame)];
...
addr.dir = msg[0]; // 显式指定位域变量的值
...
```

**【反例】**
如下代码示例中，依赖位域是跨字节连续存储的，代码不可移植：

```c
typedef struct {
    unsigned int a : 6;
    unsigned int b : 4;
} BitFrame;
...

BitFrame data = {0};
unsigned char *p = (unsigned char *)&data;

// 在低字节序系统下，data.b 的值是与实现相关的，可能是3，也可能没有变化
p[0] = 0xffu;
```

**【正例】**
如下代码示例中，显式指定位域变量的值：

```c
typedef struct {
    unsigned int a : 6;
    unsigned int b : 4;
} BitFrame;
...

BitFrame data = {0};
data.a = 0x3fu;
data.b = 3u; // 显式指定位域变量的值
```




## 2.7 控制语句




### 2.7.1 判断语句




#### CTL.01 控制表达式的结果必须是布尔值

**【描述】**
使用强类型可以减少C语言的编程风险，控制表达式的结果必须是布尔值以及如下表达式的运算结果：
- 关系表达式&ensp;&ensp;&ensp; < &ensp; <= &ensp; >= &ensp; >
- 相等类表达式&ensp; == &ensp; !=
- 逻辑表达式&ensp;&ensp;&ensp; && &ensp; || &ensp; !

控制表达式应用的语句包括：
- if语句
- while语句
- do语句
- for语句

```c
// if语句
if (controlling expression) {
    ...
}

// while语句
while (controlling expression) {
    ...
}

// do语句
do {
    ...
} while (controlling expression);

// for语句
for ( ...; controlling expression; ... ) {
    ...
}
```

**【反例】**

```c
int value = GetValue();
if (value) { // 不符合：不是布尔类型变量
    ...
}
```

**【正例】**

```c
int value = GetValue();
if (value != 0) { // 符合
    ...
}
```

```c
while (true) { // 符合：特殊场景下可以使用布尔类型常量
    ...
}
```

```c
char *p = GetPointer();
if (p != NULL) { // 符合
    ...
}
```

```c
char *p = GetPointer();
if (p == NULL) { // 符合
    ...
}
```

**【例外】**
当判断条件中的表达式是指针时，可以直接使用指针作为表达式。当 p 是一个指针，通常将`if (p)`解读为“如果p有效”，这是程序员意图的直接表达，因此允许写成`if (p)`的形式。

```c
char *p = GetPointer();
if (p) { // 允许使用
    ...
}
```

```c
char *p = GetPointer();
if (!p) { // 允许使用
    ...
}
```




#### CTL.02 &&和||操作符的右侧操作数不应包含副作用

**【描述】**
逻辑与（&&）、逻辑或（||）表达式中的右操作数是否被求值，取决于左操作数的求值结果，当左操作数的求值结果可以得出整个逻辑表达式的结果时，不会再计算右操作数的结果。如果右操作数包含副作用，则不能确定是否确实发生了副作用，因此，本规范中建议逻辑与（&&）、逻辑或（||）操作符的右操作数中不要含有副作用。

副作用是指对执行状态产生影响，包括：修改对象、访问volatile对象、修改文件等。在某些情况下副作用会给程序带来不必要的麻烦，其产生的错误十分难以查找，并降低程序的可读性。

**【反例】**
如下代码示例中，当`flag > 0` 或 `value > 0` 时进入分支处理，但是 value 自减的前提是 `flag <= 0`。尽管代码行为是正确的，也有可能是精心设计的，但是不易阅读理解，并且给维护带来不便, 容易引入问题：

```c
if (flag > 0 || value-- > 0) {
  ...
}
```

**【正例】**
如下代码示例中，明确逻辑行为（可以将公共代码提取成函数在不同分支调用）：

```c
if (flag > 0) {
    ...
} else {
    value--;
    if (value >= 0) {
        ...
    }
}
```

**【反例】**
程序本意是想依据指针p来源不同，执行不同的操作。但是如下代码示例中，逻辑与（&&）表达式的右操作数申请内存，取决于左操作数的判断结果。在后续的执行过程中，无法准确知道p是来自getPtr()还是malloc()。

```c
char *p = getPtr();
if ((p == NULL) && ((p = (char *) malloc(SIZE)) == NULL)) {
    return;
}
...
free(p); // 不确定释放的是否为上面malloc()函数申请的内存
p = NULL;
...
```

**【正例】**
重构上面错误代码，使指针语义准确，无副作用。

```c
char *p = getPtr();
if (p == NULL) {    // 如果p非来自getPtr()，执行本分支。
    p = (char *) malloc(SIZE);
    ... // p判空并初始化，p操作。
} else {
    ...    // 如果p来自getPtr()，执行本分支。
}
free(p);
p = NULL;
...
```

**【反例】**
如下代码示例中，Call()函数中的逻辑与（&&）操作符的右操作数调用了一个导致副作用的函数：

```c
#define FILENAME_LEN 128
static int RemoveFile(unsigned int fileId)
{
    char filename[FILENAME_LEN];
    int ret = sprintf_s(filename, FILENAME_LEN, "/some_dir/%u.txt", fileId);
    if (ret < 0) {
        return -1;
    }
    return unlink(filename); // 该语句具有副作用
}

void Call(void)
{
    ...
    if (isRight && RemoveFile(fileId) != 0) {
        ...
    }
}
```

**【正例】**
如下的一个解决方案是拆分if语句中的表达式：

```c
#define FILENAME_LEN 128
static int RemoveFile(unsigned int fileId)
{
    char filename[FILENAME_LEN];
    int ret = sprintf_s(filename, FILENAME_LEN, "/some_dir/%u.txt", fileId);
    if (ret < 0) {
        return -1;
    }
    return unlink(filename); // 该语句具有副作用
}

void Call(void)
{
    ...
    if (isRight) {
        if (RemoveFile(fileId) != 0) {
            ...
        }
    }
}
```


**【相关软件CWE编号】** CWE-768




### 2.7.2 循环语句




#### CTL.03 循环必须安全退出

**【描述】**
在应用程序中，一个重复提供服务的逻辑循环应当设计退出机制，并且将资源正确释放后安全退出。退出条件的设计，除了让程序逻辑更加完整，也能通过实现优雅退出的代码，显式释放服务循环中分配的资源，避免资源泄漏。

**【反例】**
以下代码，在一个大循环内，ReceiveMsg函数内申请资源，接收外部数据。ParseMsg函数内处理数据，但没有退出条件，会导致循环前申请的资源无法释放，该程序没有安全退出。

```c
...

void DoService(void)
{
    ...
    size_t size = 0;
    unsigned char *pMsg = NULL;

    CreateServiceResource(); // 分配服务资源
    while (true) {
        pMsg = ReceiveMsg(&size);
        if (pMsg != NULL) {
            ParseMsg(pMsg, size);
            FreeMsg(pMsg);
        }
        size = 0;
    }
}
```

**【正例】**
重新设计函数，通过提供服务退出条件，并在资源释放函数ReleaseServiceResource内释放服务循环前申请的资源。

```c
bool ParseMsg(unsigned char *msg, size_t msgLen)
{
    ...
    if (msg->type == EXIT_MESSAGE_TYPE) {
        return false;
    } else {
        return true;
    }
}

void DoService(void)
{
    ...
    size_t size = 0;
    unsigned char *pMsg = NULL;
    bool doRunServiceFlag = true;    // 服务退出条件

    CreateServiceResource(); // 分配服务资源
    while (doRunServiceFlag) {
        pMsg = ReceiveMsg(&size);
        if (pMsg != NULL) {
            doRunServiceFlag = ParseMsg(pMsg, size);
            FreeMsg(pMsg);
        }
        size = 0;
    }
    ReleaseServiceResource(); // 释放服务资源
}
```

**【例外】**

1、操作系统软件的IDLE线程，可能需要无限循环

2、操作系统在不可恢复的错误中，为避免更多错误发生，进入指令无限循环。例如：

```c
void FaultReboot(void)
{
    ...
    reboot(rebootCmd);
    while (1) {
        CoreWait();
    }
}
```

3、嵌入式设备的操作系统或主流程，可能使用无限循环。例如：

```c
void OsTask(void)
{
    ...
    while (1) {
        msgHdl = Receive(OS_WAIT_FOREVER, &msgId, &senderPid);
        if (msgHdl == 0) {
            continue;
        }
        switch (msgId) {
            ...
        }
        (void)Free(msgHdl);
        msgHdl = NULL;
    }
}
```





#### CTL.04 禁止使用浮点数作为循环计数器

**【描述】**
二进制浮点数算数标准ISO/IEEE Std 754-1985中规定了32位单精度和64位双精度浮点类型的表示方法。因为存储二进制浮点的bit位是有限的，所以二进制浮点数的表示范围也是有限的，并且无法精确地表示所有实数。因此，浮点数计算结果也不是精确值，不能将浮点变量用作循环计数器。

**【反例】**
如下代码示例中，使用浮点变量用作循环计数器，在不同实现下循环次数不同，循环可能执行9次也可能执行10次：

```C
float x = 0.1f;
while (x <= 1.0f) {
    // 可能执行9或10次
    x += 0.1f;
}

for (x = 0.1f; x <= 1.0f; x += 0.1f) {
    // 可能执行9或10次
}
```

**【正例】**
如下代码示例中，循环计数器由浮点数修改为整数：

```c
size_t count = 1;
while (count <= 10) {
    float x = count / 10.0f;
    // 执行10次
    count++;
}

for (count = 1; count <= 10; ++count) {
    float x = count / 10.0f;
    // 执行10次
}
```




### 2.7.3 goto语句




#### CTL.05 慎用 goto 语句

**【描述】**
goto语句会破坏程序的结构性，所以除非确实需要，最好不使用goto语句。使用时，也只允许跳转到本函数内 goto 语句之后的标签。

goto语句通常用来实现函数单点返回。

同一个函数体内部存在大量相同的逻辑但又不方便封装成函数的情况下，例如反复执行文件操作，对文件操作失败以后的处理部分代码（例如关闭文件句柄，释放动态申请的内存等等），一般会放在该函数体的最后部分，在需要的地方就goto到那里，这样代码反而变得清晰简洁。

实际也可以将失败处理的代码封装成函数或者封装成宏，但是这么做会让代码变得没那么直接明了。

**【正例】**

```c
// 符合: 使用 goto 实现单点返回
int SomeInitFunc(void)
{
    void *p1 = NULL;
    void *p2 = NULL;
    void *p3 = NULL;

    p1 = malloc(MEM_LEN);
    if (p1 == NULL) {
       goto EXIT;
    }

    p2 = malloc(MEM_LEN);
    if (p2 == NULL) {
        goto EXIT;
    }

    p3 = malloc(MEM_LEN);
    if (p3 == NULL) {
        goto EXIT;
    }

    DoSomething(p1, p2, p3);
    return 0; // 符合

EXIT:
    if (p3 != NULL) {
        free(p3);
    }
    if (p2 != NULL) {
        free(p2);
    }
    if (p1 != NULL) {
        free(p1);
    }
    return -1;
}
```




#### CTL.06 goto语句只能向下跳转

**【描述】**
goto语句会破坏程序的结构性，所以除非确实需要，最好不使用goto语句。使用时，也只允许跳转到本函数内goto语句之后的语句。
不加限制地使用goto语句，特别是使用往回跳的goto语句，会增加代码的复杂性，使程序结构难以理解，在这种情形，应尽量避免使用goto语句。

**【反例】**
```c
void Func(void)
{
    int loopCnt = 0;

LOOP1:
    loopCnt++;
    if (loopCnt < MAX_COUNT) {
        goto LOOP1;     // 不符合：不能往回跳转
    } else {
        ...
    }
    ...

}
```

**【正例】**
```c
void Func(void)
{
    int loopCnt = 0;

    while(loopCnt++) {
        if (loopCnt == MAX_COUNT) {
            goto LOOP2; // 符合：只能向下跳转
        }
        ...
    }
    ...

LOOP2:
    ...
}
```




### 2.7.4 switch语句




#### CTL.07 switch语句要有default分支

**【描述】**
大部分情况下，switch语句中要有default分支，保证在遗漏case标签处理时能够有一个缺省的处理行为。本规范要求统一将default分支放到语句块的最后位置。

**【例外】**

如果switch条件变量是枚举类型，并且 case分支覆盖了所有取值，则可以不要求有default分支。

```c
typedef enum {
    RED,
    GREEN,
    BLUE
} Color;

Color color;
...
// 因为switch条件变量是枚举值，这里可以不用加default处理分支
switch (color) {
    case RED:
        DoRedThing();
        break;
    case GREEN:
        DoGreenThing();
        break;
    case BLUE:
        DoBlueThing();
        ...
        break;
}
```

现代编译器都具备检查是否在switch语句中遗漏了某些枚举值的case分支的能力，会有相应的warning提示。




#### CTL.08 switch语句中至少有两个条件分支

**【描述】**
单个路径的选择语句更适合用`if`语句进行判断；且如果条件分支是布尔值，那么也不合适使用`switch`语句，使用`if`语句更合适。

**【反例】**
如下的代码示例写法都是错误的。

```c
void Foo(void)
{
    ...
    switch (color) {
        default: // 不符合: switch是多余的
            x = 0;
            break;
    }
}
```

```c
void Foo(void)
{
    ...
    switch (color) {
        case RED:
        default: // 不符合: switch是多余的
            x = 0;
            break;
    }
}
```

**【正例】**
如下的代码示例写法是正确的。

```c
void Foo(void)
{
    ...

    switch (lightColor) {
        case RED:
            lastSeconds = 30;    //  红灯保持时间
            break;
        case GREEN:
            lastSeconds = 45;    // 绿灯保持时间
            break;
        default: // 符合: 存在两个分支
            lastSeconds = 3;    // 除了红灯和绿灯，其他（包括黄灯）保持3秒
            break;
    }
}
```




## 2.8 声明与初始化




### DCL.01 不要声明或定义保留的标识符

**【描述】**
如果声明或者定义了一个保留的标识符，那么程序的行为是未定义的。

C11标准7.1.3说明：
    1、双下划线开头，或下划线加一个大写字母开头的所有标识符始终保留使用；
    2、除label名字和结构体、联合的成员外，其他以下划线开头的标识符都在文件范围内有效；
    3、C标准库中已经定义的标识符均保留其用途；
    4、errno和其他C标准库的外部链接标识符始终作为外部链接；
    5、C标准库中具有文件范围的标识符都保留用作宏的名字。

此外，在C11标准7.31中预留了一些将来使用的标识符。

**【反例】**
```c
#undef __LINE__               // 不符合：下划线开头
#define _MODULE_INCLUDE_      // 不符合：下划线开头
int errno;                    // 不符合：errno是标准库中的保留标识符
void *malloc(size_t nbytes);  // 不符合：malloc是标准库中的保留标识符
#define SIZE_MAX 80           // 不符合：SIZE_MAX是标准库中的保留宏定义
```

**【例外】**

作为编译器供应商或标准库程序员，可以使用为编译器保留的标识符。保留的标识符可以由编译器在标准库标头，或标准库标头包含的标头中定义，如在以下示例中来自glibc库实现的声明：

```c
/*
 * The following declarations of reserved identifiers exist in the glibc
 * implementation of <stdio.h>. The original source code may be found at:
 * https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=include/stdio.h
*/

#define __need_size_t
#include <stddef.h>
// Generate a unique file name (and possibly open it).
extern int __path_search (char *__tmpl, size_t __tmpl_len,
              const char *__dir, const char *__pfx,
              int __try_tempdir);
```




## 2.9 整数

C语言中整数类型繁多，包括有符号、无符号以及不同大小的整数类型，在不同实现中相同类型的整数的表示形式可能不同，并且不同整数类型间转换规则非常复杂，因此在使用整数前需要了解整数提升规则，了解不同整数类型间转换规则，了解整数常量/表达式中容易出现的问题，以及算数运算导致的整数溢出（overflow）/整数回绕（wrap）所产生的问题。




### INT.01 确保有符号整数运算不溢出

**【描述】**
有符号整数溢出是C语言标准中说明的一种未定义行为。因此，各种编译器的实现对有符号整数溢出行为有多种处理方式，其程序执行结果不可预料，甚至带来严重安全问题。
出于安全考虑，对外部数据中的有符号整数值在如下场景中使用时，需要确保运算不会导致溢出：

- 指针运算的整数操作数(指针偏移值)
- 数组索引
- 变长数组的长度(及长度运算表达式)
- 内存拷贝的长度
- 内存分配函数的参数
- 循环判断条件

在精度低于int的整数类型上进行运算时，需要考虑整数提升。程序员还需要掌握整数转换规则，包括隐式转换规则，以便设计安全的算术运算。

1）加法

**【反例】**
如下代码示例中，参与加法运算的整数是外部数据，在使用前未做校验，可能出现整数溢出。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int sum = numA + numB;
...
```

**【正例】**
如下代码示例中，按照最大允许值进行校验，防止整数溢出。在编程时可根据具体业务场景做更严格的值域校验。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int sum = 0;
if (((numA > 0) && (numB > (INT_MAX - numA))) ||
    ((numA < 0) && (numB < (INT_MIN - numA)))) {
    ... // 错误处理
}
sum = numA + numB;
...
```

2）减法

**【反例】**
如下代码示例中，参与减法运算的整数是外部数据，在使用前未做校验，可能出现整数溢出，进而造成后续的内存复制操作出现缓冲区溢出。
```c
unsigned char *content = ... // 指向报文头的指针
size_t contentSize = ...     // 缓冲区的总长度
int totalLen = ... // 报文总长度
int skipLen = ...  // 从消息中解析出来的需要忽略的数据长度
// 用 totalLen - skipLen 计算剩余数据长度，可能出现整数溢出
errno_t ret = memmove_s(content, contentSize,
                        content + skipLen, totalLen - skipLen);
...
```

**【正例】**
如下代码示例中，重构为使用`size_t`类型的变量表示数据长度，并校验外部数据长度是否在合法范围内。
```c
unsigned char *content = ... //指向报文头的指针
size_t contentSize = ...     // 缓冲区的总长度
size_t totalLen = ... // 报文总长度
size_t skipLen = ...  // 从消息中解析出来的需要忽略的数据长度
if (skipLen >= totalLen || totalLen > contentSize) {
    ... // 错误处理
}
errno_t ret = memmove_s(content, contentSize,
                        content + skipLen, totalLen - skipLen);
...
```

3）乘法

**【反例】**
如下代码示例中，内核代码对来自用户态的数值范围做了校验，但是由于opt是`int`类型，而校验条件中错误的使用了`ULONG_MAX`进行限制，导致整数溢出。
```c
int opt = ... // 来自用户态
if ((opt < 0) || (opt > (ULONG_MAX / (60 * HZ)))) { // 错误的使用了ULONG_MAX做上限校验
    return -EINVAL;
}
... = opt * 60 * HZ; // 可能出现整数溢出
...
```

**【正例】**
一种改进方案是将opt的类型修改为`unsigned long`类型，这种方案适用于修改了变量类型更符合业务逻辑的场景。
```c
unsigned long opt = ... // 将类型重构为 unsigned long 类型。
if (opt > (ULONG_MAX / (60 * HZ))) {
    return -EINVAL;
}
... = opt * 60 * HZ;
...
```

另一种改进方案是将数值上限修改为INT_MAX。
```c
int opt = ... // 来自用户态
if ((opt < 0) || (opt > (INT_MAX / (60 * HZ)))) { // 修改使用 INT_MAX作为上限值
    return -EINVAL;
}
... = opt * 60 * HZ;
```

4）除法

**【反例】**
如下代码示例中，做除法运算前只检查了是否出现被零除的问题，缺少对数值范围的校验，可能出现整数溢出。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int result = 0;
if (numB == 0) {
    ... // 对除数为0的错误处理
}
result = numA / numB; // 可能出现整数溢出
...
```

**【正例】**
如下代码示例中，按照最大允许值进行校验，防止整数溢出，在编程时可根据具体业务场景做更严格的值域校验。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int result = 0;
// 检查除数为0及除法溢出错误
if ((numB == 0) || ((numA == INT_MIN) && (numB == -1))) {
    ... // 错误处理
}
result = numA / numB;
...
```

5）求余数

许多平台以相同的指令实现求余数和除法运算，因此求余数运算也可能出现算数溢出和除零错误的问题。

**【反例】**
如下代码示例中，缺少对数值范围的校验，可能出现整数溢出。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int result = 0;
if (numB == 0) {
    ... // 对除数为0的错误处理
}
result = numA % numB;  // 可能出现整数溢出
...
```

**【正例】**
如下代码示例中，按照最大允许值进行校验，防止整数溢出。在编程时可根据具体业务场景做更严格的值域校验。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int result = 0;
// 检查除数为0及除法溢出错误
if ((numB == 0) || ((numA == INT_MIN) && (numB == -1))) {
    ... // 错误处理
}
result = numA % numB;
...
```

6）一元减

当操作数等于有符号整数类型的最小值时，在二进制补码一元求反期间会发生溢出。

**【反例】**
如下代码示例中，计算前未校验数值范围，可能出现整数溢出。
```c
int numA = ... // 来自外部数据
int result = -numA; // 可能出现整数溢出
...
```

**【正例】**
如下代码示例中，按照最大允许值进行校验，防止整数溢出。在编程时可根据具体业务场景做更严格的值域校验。
```c
int numA = ... // 来自外部数据
int result = 0;
if (numA == INT_MIN) {
    ... // 错误处理
}
result = -numA;
...
```

**【影响】**

整数溢出可能导致程序拒绝服务、缓冲区溢出、甚至执行任意代码。

**【相关软件CWE编号】** CWE-190，CWE-129
**【业界典型漏洞】** CVE-2019-17041




### INT.02 确保无符号整数运算不回绕

**【描述】**
涉及无符号操作数的计算永远不会溢出，因为超出无符号整数类型表示范围的计算结果会按照结果类型可表示的最大值+1的数值取模。
这种行为更多时候被非正式地称为无符号整数回绕。
在精度低于int的整数类型上进行运算时，需要考虑整数提升。程序员还需要掌握整数转换规则，包括隐式转换规则，以便设计安全的算术运算。
出于安全考虑，对外部数据中的无符号整数值在如下场景中使用时，需要确保运算不会导致回绕：  
- 指针运算的整数操作数(指针偏移值)
- 数组索引
- 变长数组的长度(及长度运算表达式)
- 内存拷贝的长度
- 内存分配函数的参数
- 循环判断条件

1）加法

**【反例】**
如下代码示例中，校验下一个子报文的长度加上已处理报文的长度是否超过了整体报文的最大长度，在校验条件中的加法运算可能会出现整数回绕，造成绕过该校验的问题。
```c
size_t totalLen = ... // 报文的总长度
size_t readLen = 0    // 记录已经处理报文的长度
...
size_t pktLen = ParsePktLen();     // 从网络报文中解析出来的下一个子报文的长度
if (readLen + pktLen > totalLen) { // 可能出现整数回绕
  ... // 错误处理
}
...
readLen += pktLen;
...
```

**【正例】**
由于readLen变量记录的是已经处理报文的长度，必然会小于totalLen，因此将代码中的加法运算修改为减法运算，避免条件绕过。
```c
size_t totalLen = ... // 报文的总长度
size_t readLen = 0;   // 记录已经处理报文的长度
...
size_t pktLen = ParsePktLen(); // 来自网络报文
if (pktLen > totalLen - readLen) {
  ... // 错误处理
}
...
readLen += pktLen;
...
```

2）减法

**【反例】**
如下代码示例中，校验len合法范围的运算可能会出现整数回绕，导致条件绕过。
```c
size_t len = ... // 来自用户态输入
if (SCTP_SIZE_MAX - len < sizeof(SctpAuthBytes)) { // 减法操作可能出现整数回绕
    ... // 错误处理
}
... = kmalloc(sizeof(SctpAuthBytes) + len, gfp); // 可能出现整数回绕
...
```

**【正例】**
如下代码示例中，调整减法运算的位置（需要确保编译期间减法表达式的值不翻转），避免整数回绕问题。
```c
size_t len = ... // 来自用户态输入
if (len > SCTP_SIZE_MAX - sizeof(SctpAuthBytes)) { // 确保编译期间减法表达式的值不翻转
    ... // 错误处理
}
... = kmalloc(sizeof(SctpAuthBytes) + len, gfp);
...
```

3）乘法

**【反例】**
如下代码示例中，使用外部数据计算申请内存长度时未校验，可能出现整数回绕。
```c
size_t width = ... // 来自外部数据
size_t hight = ... // 来自外部数据
unsigned char *buf = (unsigned char *)malloc(width * hight);
```

无符号整数回绕可能导致分配的内存不足。

**【正例】**
如下代码是一种解决方案，校验参与乘法运算的整数数值范围，确保不会出现整数回绕。
```c
size_t width = ... // 来自外部数据
size_t hight = ... // 来自外部数据
if (width == 0 || hight == 0) {
    ... // 错误处理
}
if (width > SIZE_MAX / hight) {
    ... // 错误处理
}
unsigned char *buf = (unsigned char *)malloc(width * hight);
```

**【例外】**
为正确执行程序，必要时无符号整数可能表现出模态（回绕）。建议将变量声明明确注释为支持模数行为，并且对该整数的每个操作也应明确注释为支持模数行为。

**【影响】**

整数回绕可能导致程序缓冲区溢出以及执行任意代码。

**【相关软件CWE编号】** CWE-190

**【业界典型漏洞】** CVE-2007-0776 CVE-2008-3526




### INT.03 确保除法和余数运算不会导致除零错误(被零除)

**【描述】**
整数的除法和取余运算的第二个操作数值为0会导致程序产生未定义的行为，因此使用时要确保整数的除法和余数运算不会导致除零错误(被零除，下同)。

1）除法

**【反例】**
有符号整数类型的除法运算如果限制不当，会导致溢出。
如下示例对有符号整数进行的除法运算做了防止溢出限制，确保不会导致溢出，但不能防止有符号操作数numA和numB之间的除法过程中出现除零错误。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int result = 0;
if ((numA == INT_MIN) && (numB == -1)) {
    ... // 错误处理
}
result = numA / numB; // 可能出现除零错误
...
```

**【正例】**
如下代码示例中，添加numB是否为0的校验，防止除零错误。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int result = 0;
if ((numB == 0) || ((numA == INT_MIN) && (numB == -1))) {
    ... // 错误处理
}
result = numA / numB;
...
```

2）求余数

**【反例】**
如下代码，同除法的错误代码示例一样，可能出现除零错误，因为许多平台以相同的指令实现求余数和除法运算。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int result = 0;
if ((numA == INT_MIN) && (numB == -1)) {
    ... // 错误处理
}
result = numA % numB; // 可能出现除零错误
...
```

**【正例】**
如下代码示例中，添加numB是否为0的校验，防止除零错误。
```c
int numA = ... // 来自外部数据
int numB = ... // 来自外部数据
int result = 0;
if ((numB == 0) || ((numA == INT_MIN) && (numB == -1))) {
    ... // 错误处理
}
result = numA % numB;
...
```

**【影响】**

除零错误可能导致拒绝服务。

**【相关软件CWE编号】** CWE-369




### INT.04 整型表达式比较或赋值为一种更大类型之前必须用这种更大类型对它进行求值

**【描述】**
由于整数在运算过程中可能出现有符号整数溢出、无符号整数回绕等问题，当运算结果赋值给比它更大的类型，或者与比它更大的类型进行比较时，可能会导致实际结果与预期结果不符。

如果将涉及某个操作的整数表达式与较大的整数大小进行比较或分配给较大的整数，则该整数表达式应该通过显式转换其中一个操作数来以较大类型的大小进行计算。

类似的，当组合表达式的运算结果赋值给比它更大类型，或者与比它更大类型进行运算时，应显式转换其中一个操作数为较大的类型。
本规范中组合表达式指的是由如下操作符组成的表达式：

1. 乘除取模（*、 /、 %）
2. 加减（二元+、 二元-）
3. 位运算（&、 |、 ^）
4. 移位（<<、 >>）
5. 三元表达式（?:）如果第二个操作数和第三个操作数都是组合表达式

在int为32位，long long为64位并以二进制补码表示整数的系统中，请观察以下二个代码及其输出，以便了解本规则所解决的问题：
```c
int main(int argc, char *argv[])
{
    unsigned int a = 0x10000000;
    unsigned long long b = a * 0xab;
    printf("b = %llX\n", b);
    return 0;
}
```
输出：
```c
b = B0000000
```

```c
int main(int argc, char *argv[])
{
    unsigned int a = 0x10000000;
    unsigned long long b = (unsigned long long )a * 0xab;
    printf("b = %llX\n", b);
    return 0;
}
```

输出：
```c
b = AB0000000
```

**【反例】**（组合表达式）

以二进制补码表示整数的系统中，如下代码示例，
表达式 `a + b + c` 等同于表达式 `(a + b) + c`，计算组合表达式 `(a + b)` 时先发生整数回绕，其结果为0，再与c相加后得到 x 的值为2。
表达式 `(uint64_t)(a + b) + c` ，计算组合表达式`(a + b)`时先发生整数回绕，其结果为0，然后再转换 `uint64_t` 类型并与 c 相加后得到 y 的值为2。
表达式 `a + c + b` 等同于表达式 `(a + c) + b`，与前面表达式不同点在于，计算`a + c`时发生了隐式类型转换，将 a 隐式提升到了 `uint64_t` 类型后在进行计算，因此最后 z 的值是正确的，但是该代码依赖表达式计算顺序，不利于维护和阅读，应禁止使用该技巧。类似的，t 和 m 的值虽然正确，但是依赖表达式优先级，应禁止使用该技巧。

```c
uint32_t a = 0xffffffffU;
uint32_t b = 1;
uint64_t c = 2;
uint64_t x = a + b + c;   // 结果非预期, x的值为2
uint64_t y = (uint64_t)(a + b) + c; // 结果非预期, y的值为2
uint64_t z = a + c + b;   // 结果正确，但是依赖表达式顺序，禁止使用该技巧
uint64_t t = a + (b + c); // 结果正确，但是依赖表达式优先级，禁止使用该技巧
uint64_t m = a + b * c;   // 结果正确，但是依赖表达式优先级，禁止使用该技巧
```

**【正例】**（组合表达式）

如下的一种解决方案，是显式转换变量 a 和 b 的类型为 `uint64_t` 类型：

```c
uint32_t a = 0xffffffffU;
uint32_t b = 1;
uint64_t c = 2;
uint64_t x = (uint64_t)a + (uint64_t)b + c;
uint64_t y = ((uint64_t)a + (uint64_t)b) + c;
uint64_t z = (uint64_t)a + c + (uint64_t)b;
uint64_t t = (uint64_t)a + ((uint64_t)b + c);
uint64_t m = (uint64_t)a + (uint64_t)b * c;
```

最佳做法是修改变量 a 和 b 的类型为 `uint64_t` 类型，保持表达式中的操作数类型一致（如果表达式的数值不可信，应先校验其范围防止无符号整数回绕）：

```c
uint64_t a = 0xffffffffU;
uint64_t b = 1;
uint64_t c = 2;
uint64_t x = a + b + c;
uint64_t y = a + c + b;
uint64_t z = a + (b + c);
uint64_t t = a + b * c;
```





### INT.05 只能对无符号整数进行位运算

**【描述】**
位运算操作包括~(求反)，&(与)，|(或)，^(异或)，>>(右移位)和<<(左移位)，以及复合赋值运算操作符>>=，<<=，＆=，^=和|=，只能对无符号整数进行位运算，对有符号整数进行按位运算的结果是由编译器实现定义的。

一些操作符（一元操作符~和二元操作符<<，>>，＆，^和|统称为位操作符）应具有整数类型的操作数。对于有符号类型按位运算的返回值取决于整数的内部表示，存在C语言标准中描述的实现定义行为以及未定义行为。

对于数据长度小于int类型的无符号整数做位操作时，编译器会隐式进行整数提升，再对提升后的整数进行位操作，因此对于这类无符号数做位操作时要特别小心，避免出现非预期的结果。

**【反例】**
右移操作可以实现为算术（有符号）移位或逻辑（无符号）移位。如果`E1 >> E2`表达式中E1是有符号类型而且为负值，那么这个表达式结果值是由编译器实现定义的。同样，按位移位数(E2)如果是有符号数，也会导致程序产生未定义行为。

```c
int data = ReadByte();
int value = data >> 24;          //  对有符号整数进行位运算，程序会产生未定义行为

... // 检查 data 的合法范围，代码略

int mask = 1 << data;           //  对有符号整数进行位运算，程序会产生未定义行为
```

**【正例】**
```c
unsigned int data = (unsigned int)ReadByte();
unsigned int value = data >> 24; // 只能对无符号整数进行位运算

... // 检查 data 的合法范围，代码略

unsigned mask  = 1 << data;
```

**【例外】**
<!--<div>仅使用Microsoft C编译器和GCC编译器进行编译的代码中，当使用位操作符对正数进行2的幂的乘除法时，如果已经知道右操作数的大小</div>-->

- 作为位标志的预处理器宏或枚举常量，即使未声明为无符号，也可以作为 & 和 | 操作符的参数。

```c
int fd = open(filename, O_SYNC | O_CREAT | O_EXCL | O_TRUNC, S_IRWXU | S_IRUSR);
```

- 允许使用一个在编译时就可以确定的正的有符号整数，作为移位操作符的右操作数。

```c
#define SHIFT_BITS 3
unsigned int id = ...;
...
unsigned int type = id >> SHIFT_BITS;
```





### INT.06 校验外部数据中整数值的合法性

**【描述】**
对源自外部数据的所有整数值，我们应执行严格评估，以确定它们是否具有可被识别的上限和下限。
对源自污染源的整数值限制其输入在合法范围内有助于防止整数溢出，回绕，截断和其他直接或间接由整数值限定不当引起的风险。
此外，在使用前限制和纠正输入问题要比在后期发生错误时再追溯定位错误的输入更加容易，成本更低。

**【反例】**(无限循环)
如下示例中，由于循环条件受外部输入的报文内容控制，可能进入无限循环：

```c
unsigned char *FindAttr(unsigned char type, const unsigned char *msg, size_t inputMsgLen)
{
    const unsigned char *content = msg;
    ...
    contentLength = content[RD_LEA_PKT_LENGTH]);
    ... // 参考inputMsgLen对contentLength进行校验
    while (contentLength < RD_LEA_PKT_LENGTH + 1) {
        mAttrType = content[0];
        mAttrLength = content[RD_LEA_PKT_LENGTH];
        ...
        contentLength -= mAttrLength;
        content += mAttrLength;
    }
    ...
}
```

此例中，需要检查报文的实际可读长度，报文内容提供的循环增量（避免为0），以防止缓冲区溢出。

**【正例】**
通过检查消息剩余长度，避免后续运算中无符号整数回绕。
```c
unsigned char *FindAttr(unsigned char type, const unsigned char *msg，size_t inputMsgLen)
{
    const unsigned char *content = msg;
    ...
    contentLength = content[RD_LEA_PKT_LENGTH]);
    ... // 参考inputMsgLen对contentLength进行校验
    while (contentLength < RD_LEA_PKT_LENGTH + 1) {
        mAttrType = content[0];
        mAttrLength = content[RD_LEA_PKT_LENGTH];
        ...
        if (contentLength < mAttrLength) {
            ... // 错误处理
            break;
        }
        contentLength -= mAttrLength;
        content += mAttrLength;
    }
    ...
}
```

**【反例】**（分配内存）
下面示例中，maxValue 取自用户定义的环境变量的值，因此是不可信的。该变量的值用于动态分配的大小。代码可以防止无符号整数回绕，但没有对申请内存的大小施加任何合理上限，可能会导致程序使用过多的内存。
```c
char **CreateMap(void)
{
    const char *limitStr = getenv("USER_LIMITS");
    const size_t maxValue =
        (limitStr == NULL) ? strtoul(limitStr, NULL, 10) : 0;

    // 限制未根据实际场景，范围太大，等同于没限制
    if ( (maxValue == 0) || (maxValue > SIZE_MAX / sizeof(unsigned char *))) {
        return NULL;   // 向上层调用函数反馈错误
    }

    const size_t dataSize = maxValue * sizeof(unsigned char *);
    unsigned char **map = (unsigned char **)malloc(dataSize);
    if (map == NULL) {
        return NULL;   // 向上层调用函数反馈错误
    }
    ... // 初始化 map

    return map;
}
```

因为maxValue的值是由用户控制的，所以该值可能会导致分配大量的内存，或者可能导致调用malloc()失败。根据实施错误处理的方式，可能会导致拒绝服务攻击或其他错误。

**【正例】**
如下解决方案定义了可接受的范围maxValue为`[1, MAX_MAP_SIZE]`。该maxValue声明为`size_t`，因此没有必要检查maxValue负值。

```c
#define MAX_MAP_SIZE 1024

char **CreateMap(void)
{
    const char *limitStr = getenv("DATA_MAP_SIZE");
    const size_t maxValue =
        (limitStr == NULL) ? strtoul(limitStr, NULL, 10) : 0;

    // 根据实际场景做出上限限制
    if ( (maxValue == 0) || (maxValue > MAX_MAP_SIZE)) {
        return NULL;   // 返回错误
    }

    const size_t dataSize = maxValue * sizeof(unsigned char *);
    unsigned char **map = (unsigned char **)malloc(dataSize);
    if (map == NULL) {
        return NULL;   // 向上层调用函数反馈错误
    }
    ... // 初始化 map

    return map;
}
```

**【反例】**(数组索引)
如下示例中，污染数据index用于作为数组索引：
```c
const char *GetFruit(void)
{
    static const char *fruit[] = { "apple", "banana", "grape", "orange" };

    // 通过GetUserInputIndex取到的索引值index是受污染的
    int index = 0;
    bool success = GetUserInputIndex(&index);
    if (!success) {
        return NULL;   // 返回错误
    }

    return fruit[index]; // 可能有读取数组索引越界错误
}
```

**【正例】**
如下解决方案将index的可接受范围定义为`[0, ARRAY_NUMBER)`。
```c
#define ARRAY_NUMBER(x) (sizeof(x) / sizeof((x)[0]))

const char *GetFruit(void)
{
    static const char *fruit[] = { "apple", "banana", "grape", "orange" };

    // 通过GetUserInputIndex取到的索引值index是受污染的
    int index = 0;
    bool success = GetUserInputIndex(&index);
    if (!success) {
        return NULL;   // 返回错误
    }
    if ((index < 0) || (index >= ARRAY_NUMBER(fruit))) {
        return NULL;   // 返回错误
    }

    return fruit[index];
}
```

**【反例】**
如下代码片段直接使用了外部传入的数值作为循环拷贝的长度，存在风险。
```c
typedef struct {
    unsigned long octetLen;
    unsigned char *octs;
} AsnOcts;

#define MAX_INT_DIGITS 516
typedef struct {
    unsigned int length;
    unsigned char valueList[MAX_INT_DIGITS];
} BigInt;

BigInt *SAsnOctsToBigInt(const AsnOcts *pAsnOcts) // pAsnOcts来自程序外部数据
{
    BigInt *pBigInt = NULL;
    int ret = 0;

    ... // 检查入参有效性
    pBigInt = malloc(sizeof(BigInt));
    ... // 处理内存分配失败情况

    // 由于拷贝长度受程序外部数据控制且未校验，如下拷贝存在风险
    for (unsigned long i = 0; i < pAsnOcts->octetLen; i++) {
        pBigInt->valueList[i] = pAsnOcts->octs[i];
    }
    ...
}
```

**【正例】**
对外部传入的拷贝长度，需校验后才能使用。
```c
typedef struct {
    unsigned long octetLen;
    unsigned char *octs;
} AsnOcts;

#define MAX_INT_DIGITS 516
typedef struct {
    unsigned int length;
    unsigned char valueList[MAX_INT_DIGITS];
} BigInt;

BigInt *SasnOctsToBigInt(const AsnOcts *pAsnOcts) // pAsnOcts来自程序外部数据
{
    BigInt *pBigInt = NULL;

    ... // 检查入参有效性
    pBigInt = malloc(sizeof(BigInt));
    ... // 处理内存分配失败情况

    // pAsnOcts->octetLen的准确性应由调用方保证，此处仅校验合法性
    if (pAsnOcts->octetLen > MAX_INT_DIGITS) {
        ... // 处理错误
    }

    for (unsigned long i = 0; i < pAsnOcts->octetLen; i++) {
        pBigInt->valueList[i] = pAsnOcts->octs[i];
    }
    ...
}
```

**【影响】**

未对外部数据中的整数值进行限制可能导致拒绝服务，信息泄露，或执行任意代码。




### INT.07 移位操作符的右操作数必须是非负数且小于左操作数的基本类型位宽

**【描述】**
按位偏移包括左移操作(`<<`)和右移操作(`>>`)，是二元操作符，每个操作数都必须是整型。

移位运算时，首先对每个操作数执行整数提升。结果的类型取整数提升后左操作数的类型。如果右操作数的值为负数，或者右操作数的值大于或等于整数提升后左操作数的位宽，那么程序会产生未定义行为。

同时也需要注意到，整数类型的精度是用来表示数值的位数，不包括任何符号位和填充位。对于无符号整数类型，位宽和精度是相同的；而对于有符号整数类型，位宽要比精度大1。通常，我们要求仅应对无符号操作数执行移位。（请参阅规则:[只能对无符号整数进行位运算](#G-INT-05)）

例如：当移位操作的左操作数为32位无符号整数类型时，确保右操作数的取值范围是`[0,31]`。

**【反例】**
```c
uint32_t input = ...
uint32_t value = input << 32;   // 不符合：右操作数的值是32，不满足位宽要求
...
```

**【正例】**
```c
uint32_t input = ...
uint64_t value = (uint64_t)input << 32; // 符合
...
uint32_t count = input >> 24;           // 符合
```

**【相关软件CWE编号】** CWE-682，CWE-758




### INT.08 表示对象大小的整数值或变量应当使用size_t类型

**【描述】**
`size_t`类型是`sizeof`操作符结果的无符号整数类型。具有`size_t`类型的变量能够保证具有足够的精度来表示对象的大小。`size_t`的最大值由`SIZE_MAX`宏表示。类型`size_t`通常能覆盖整个地址空间。

**【反例】**
如下示例中，由于len被定义成`int`类型，其精度不够，当str字符串的长度大于`INT_MAX`值时，SaveStringData()函数未能保存字符串，并返回了失败。

```c
int SaveStringData(const char *str)
{
    int len = strlen(str);

    if (len <= 0) {
        return 0;
    }
    ... // 保存字符串的值

    return len;
}
```

**【正例】**
```c
size_t SaveStringData(const char *str)
{
    size_t len = strlen(str);

    if (len == 0) {
        return 0;
    }
    ... // 保存字符串的值

    return len;
}
```




### INT.09 确保枚举常量映射到唯一值

<!-- 优化了例外的示例，使意图与前面的示例保持一致  -->

**【描述】**
C语言的枚举类型是具有一组有限值的集合，这些值的标识符被称为枚举常量。枚举常量是一个整数常量表达式，其值可表示为`int`。尽管C语言允许相同枚举类型中的多个枚举常量具有相同的值，但是人们普遍期望同一个枚举类型中的枚举常量具有不同的值。因此，将同一个枚举类型中的多个枚举常量定义为相同的值可能会导致一些不易被发现的错误。

**【反例】**
如下代码示例中，在枚举类型`SomeModuleErrCodes`中定义错误码的时候，为两个枚举常量分配了显式值，造成 `ERR_SYS_MODIFY_ERR` 和 `ERR_EMG_INVALID_ERR` 被隐式声明为相同的值（0x3a020010），对于程序员来说，可能并不明显。
这种定义可能导致的错误是尝试将枚举常量用于 `switch` 语句的标签。由于 `switch` 语句中的所有标签都必须是唯一的，因此如下代码违反了此语义约束。

```c
typedef enum {
    ERR_SYS_ARG_ERR = 0x3a020000,
    ERR_SYS_SET_ERR,
    ERR_SYS_OCCUPIED_ERR,
    ERR_SYS_REQFREE_ERR,
    ERR_SYS_NO_REC_ERR,
    ERR_SYS_ACTIVED_ERR,
    ERR_SYS_NO_FILE_ERR,
    ERR_SYS_OPEN_ERR,
    ERR_SYS_ASSIGN_ERR,
    ERR_SYS_ALLOC_ERR,
    ERR_SYS_GET_LIST_ERR,
    ERR_SYS_IGNORE_ERR,
    ERR_SYS_REG_ERR,
    ERR_SYS_CALC_ERR,
    ERR_SYS_SNED_ERR,
    ERR_SYS_RECV_ERR,
    ERR_SYS_MODIFY_ERR,    // 不符合：值与ERR_EMG_INVALID_ERR相同
    ERR_SYS_CHECK_ERR,     // 不符合：值与ERR_EMG_TYPE_ERR相同

    ERR_EMG_INVALID_ERR = 0x3a020010,
    ERR_EMG_TYPE_ERR,
    ...
} SomeModuleErrCodes;
```

**【正例】**
为了防止出现错误代码示例中的问题，枚举类型声明可以采用以下形式之一：

- 不提供显式的整数赋值，如下示例所示

```c
typedef enum {
    ERR_SYS_ARG_ERR,
    ERR_SYS_SET_ERR,
    ERR_SYS_OCCUPIED_ERR,
    ERR_SYS_REQFREE_ERR,
    ERR_SYS_NO_REC_ERR,
    ERR_SYS_ACTIVED_ERR,
    ERR_SYS_NO_FILE_ERR,
    ERR_SYS_OPEN_ERR,
    ERR_SYS_ASSIGN_ERR,
    ERR_SYS_ALLOC_ERR,
    ERR_SYS_GET_LIST_ERR,
    ERR_SYS_IGNORE_ERR,
    ERR_SYS_REG_ERR,
    ERR_SYS_CALC_ERR,
    ERR_SYS_SNED_ERR,
    ERR_SYS_RECV_ERR,
    ERR_SYS_MODIFY_ERR,
    ERR_SYS_CHECK_ERR,

    ERR_EMG_INVALID_ERR,
    ERR_EMG_TYPE_ERR,
    ...
} SomeModuleErrCodes;
```

- 只对第一个成员赋值，如下示例所示

```c
typedef enum {
    ERR_SYS_ARG_ERR      = 0x3a020000,
    ERR_SYS_SET_ERR,
    ERR_SYS_OCCUPIED_ERR,
    ERR_SYS_REQFREE_ERR,
    ERR_SYS_NO_REC_ERR,
    ERR_SYS_ACTIVED_ERR,
    ERR_SYS_NO_FILE_ERR,
    ERR_SYS_OPEN_ERR,
    ERR_SYS_ASSIGN_ERR,
    ERR_SYS_ALLOC_ERR,
    ERR_SYS_GET_LIST_ERR,
    ERR_SYS_IGNORE_ERR,
    ERR_SYS_REG_ERR,
    ERR_SYS_CALC_ERR,
    ERR_SYS_SNED_ERR,
    ERR_SYS_RECV_ERR,
    ERR_SYS_MODIFY_ERR,
    ERR_SYS_CHECK_ERR,

    ERR_EMG_INVALID_ERR,
    ERR_EMG_TYPE_ERR,
    ...
} SomeModuleErrCodes;
```

在上面的两个选项中，除非第一个枚举数必须具有非零值，否则第一种做法是最简单的方法，因此也是首选方法。

**【例外】**
如果枚举类型的多个成员确实需要分配相同的值，需要提供显式的整数赋值，并写一条注释，解释为什么这样做，避免将来的维护人员误认为此代码有问题。
但要清楚此类枚举常量将无法在需要唯一值的上下文中使用（例如在前所述 `switch` 语句中）。




### INT.10 确保整数转换不会造成数据截断或符号错误

**【描述】**
不同整数类型间相互转换时，应确保转换后的结果不会造成数据截断或符号错误。将整数转换为宽度较小的类型会导致高位被截断，有符号/无符号整数间转换可能导致符号错误。因此，无符号数转无符号数或无符号数转有符号数时，确保数值在目标类型的上限范围内；有符号数转有符号数或有符号数转无符号数时，确保数值在目标类型的上限和下限范围内。

将整数值转换为具有同符号的更宽类型，能够保证安全地类型转换：

> 将一个整数类型的值转换为除 _Bool 以外的另一个整数类型时，如果该值可以用新类型表示，则该值不变。
> 否则，如果新类型是无符号的，该值被重复加上或者减去一个新类型所能表示的最大值加1的值，直到该值在新类型的范围内为止。
> 否则，如果新类型是有符号的，并且无法在新类型其中表示其值；结果是实现定义的，或者引发一个由实现定义的信号(signal)。

相同类型的有符号非负数转换为无符号类型时，可以安全地转换：

> 有符号整数类型的非负值范围是相应的无符号整数类型范围的子集，并且每种类型中相同值的表示形式相同。

另外，一些 C 标准函数的参数为 `int` 类型，但是内部实现却将该参数转换为 `unsigned char` 或 `char` 类型后使用。因此，使用这类函数时，应确保传入参数的数值范围在`unsigned char` 或 `char` 类型的值域范围内，常见函数如下：

```c
// 将 c 转换为 unsigned char 类型使用
void *memset(void *s, int c, size_t n);

// 将 c 转换为 unsigned char 类型使用
errno_t memset_s(void *dest, size_t destMax, int c, size_t count);

// ctype.h中列出的所有函数，将 c 转换为 unsigned char 类型使用
int isdigit(int c);

// 将 c 转换为 unsigned char 类型使用
void *memchr(const void *s, int c, size_t n);

// 将 c 转换为 unsigned char 类型使用
int fputc(int c, FILE *stream);

// 将 c 转换为 char 类型使用
char *strchr(const char *s, int c);

// 将 c 转换为 char 类型使用
char *strrchr(const char *s, int c);
```

**【反例】**
如下代码示例中, memset()函数内部会将第二个参数转换为`unsigned char`类型，转换后的结果为0，因此初始化数组的值为0，而非将每个数组元素初始化为0xff00：

```c
#define MAX_LEN 32

int *valueTable = (int *)malloc(sizeof(int) * MAX_LEN);
...
(void)memset(valueTable, 0xff00, sizeof(int) * MAX_LEN);
...
```

**【正例】**
如下代码示例中，仅使用memset()函数将数组初始化为0：

```c
#define MAX_LEN 32

int *valueTable = (int *)malloc(sizeof(int) * MAX_LEN);
...
(void)memset(valueTable, 0, sizeof(int) * MAX_LEN);
...
```

**【反例】**
如下代码示例中，将 long 类型转换为 `size_t` 类型，属于从有符号类型的值转换为无符号类型值，可能会发生类型范围错误，如果 len 的值小于0，会发生符号错误：

```c
void Func(unsigned char *msg, long len)
{
    unsigned char *buffer = NULL;
    if (len == 0) {
        ... // 处理错误
    }
    buffer = (unsigned char *)malloc((size_t)len);
    ...
}
```

**【正例】**
如下代码示例中，优选重构函数 len 参数的类型为 `size_t` 类型。

```c
void Func(unsigned char *msg, size_t len)
{
    unsigned char *buffer = NULL;
    ...
    buffer = (unsigned char *)malloc(len); // len已进行合法性检查
    ...
}
```

**【例外】**
在程序运行的所有架构上，转换后整数类型的值域一定能涵盖被转换的数值时，不需要检查值域范围。例如：在已知 `int` 类型值域范围一定大于 `short` 类型值域的情况下，将 `unsigned short` 转换为一个 `int` 时，没有必要检查是否超出 int 类型的值域范围，可以使用断言检查是否满足条件。


**【相关软件CWE编号】** CWE-192，CWE-197，CWE-681，CWE-704




## 2.10 指针和数组




### ARR.01 外部数据作为数组索引时必须确保在数组大小范围内

**【描述】**
外部数据作为数组索引对内存进行访问时，必须对数据的大小进行严格的校验，确保数组索引在有效范围内，否则会导致严重的错误。
当一个指针指向数组元素时，可以指向数组最后一个元素的下一个元素的位置，但是不能读写该位置的内存：

> 如果指针操作数和指针运算的结果指针指向同一数组对象的元素，或者指向数组对象最后一个元素的后一个元素，则求值不应产生溢出； 否则，行为是不确定的。
> 如果指针指向数组对象最后一个元素的后一个元素，则不应将其用作一元*操作符的操作数。


**【反例】**
如下代码示例中,SetDevId()函数存在差一错误，当 index 等于 `DEV_NUM` 时，恰好越界写一个元素；
同样GetDev()函数也存在差一错误，虽然函数执行过程中没有问题，但是当解引用这个函数返回的指针时，程序会产生未定义行为。

```c
...
#define DEV_NUM 10
#define MAX_NAME_LEN 128
typedef struct {
    int id;
    char name[MAX_NAME_LEN];
} Dev;

static Dev devs[DEV_NUM];

int SetDevId(size_t index, int id)
{
    if (index > DEV_NUM) {    // 不符合：差一错误。
        ... // 错误处理
    }

    devs[index].id = id;
    return 0;
}

static Dev *GetDev(size_t index)
{
    if (index > DEV_NUM) {    // 不符合：差一错误。
        ... // 错误处理
    }

    return devs + index;
}
```

**【正例】**
如下代码示例中，修改校验索引的条件，避免差一错误。

```c
#define DEV_NUM 10
#define MAX_NAME_LEN 128
typedef struct {
    int id;
    char name[MAX_NAME_LEN];
} Dev;

static Dev devs[DEV_NUM];

int SetDevId(size_t index, int id)
{
    if (index >= DEV_NUM) {
        ... // 错误处理
    }
    devs[index].id = id;
    return 0;
}

static Dev *GetDev(size_t index)
{
    if (index >= DEV_NUM) {
        ... // 错误处理
    }
    return devs + index;
}
```

**【影响】**

未对外部数据中的整数值进行限制可能导致拒绝服务，缓冲区溢出，信息泄露，或执行任意代码。

**【相关软件CWE编号】** CWE-119，CWE-123，CWE-125




### ARR.02 禁止通过对数组类型的函数参数变量进行sizeof来获取数组大小

**【描述】**

使用sizeof操作符求其操作数的大小（以字节为单位），其操作数可以是一个表达式或者加上括号的类型名称，例如：`sizeof(int)`或`sizeof(int *)`。

> 当将sizeof应用于具有数组或函数类型的参数时，sizeof操作符将得出调整后的（指针）类型的大小。

函数参数列表中声明为数组的参数会被调整为相应类型的指针。例如：`void Func(int inArray[LEN])`函数参数列表中的inArray虽然被声明为数组，但是实际上会被调整为指向int类型的指针，即调整为`void Func(int *inArray)`。
在这个函数内使用`sizeof(inArray)`等同于`sizeof(int *)`，得到的结果通常与预期不相符。例如：在IA-32架构上，`sizeof(inArray)` 的值是 4，并不是inArray数组的大小。

**【反例】**
如下代码示例中，函数ArrayInit的功能是初始化数组元素。该函数有一个声明为`int inArray[]`的参数，被调用时传递了一个长度为256的int类型数组data。
ArrayInit函数实现中使用`sizeof(inArray) / sizeof(inArray[0])`方法来计算入参数组中元素的数量。
但由于inArray是函数参数，所以具有指针类型，结果，`sizeof(inArray)`等同于`sizeof(int *)`。
无论传递给ArrayInit函数的数组实际长度如何，表达式的`sizeof(inArray) / sizeof(inArray[0])`计算结果均为1，与预期不符。

```c
#define DATA_LEN 256
void ArrayInit(int inArray[])
{
    // 不符合：这里使用sizeof(inArray)计算数组大小
    for (size_t i = 0; i < sizeof(inArray) / sizeof(inArray[0]); i++) {
        ...
    }
}

void FunctionData(void)
{
    int data[DATA_LEN];

    ...
    ArrayInit(data); // 调用ArrayInit函数初始化数组data数据
    ...
}
```

**【正例】**
如下代码示例中，修改函数定义，添加数组长度参数，并在调用处正确传入数组长度。

```c
#define DATA_LEN 256
// 函数说明：入参len是入参inArray数组的长度
void ArrayInit(int inArray[], size_t len)
{
    for (size_t i = 0; i < len; i++) {
        ...
    }
}

void FunctionData(void)
{
    int data[DATA_LEN];

    ArrayInit(data, sizeof(data) / sizeof(data[0]));
    ...
}
```

**【反例】**
如下代码示例中，`sizeof(inArray)`不等于`ARRAY_MAX_LEN * sizeof(int)`，因为将sizeof操作符应用于声明为具有数组类型的参数时，即使参数声明指定了长度，也会被调整为指针，`sizeof(inArray)`等同于 `sizeof(int *)`：

```c
#define ARRAY_MAX_LEN 256

void ArrayInit(int inArray[ARRAY_MAX_LEN])
{
    // 不符合：sizeof(inArray)，得到的长度是指针的大小，不是数组的长度，和预期不符。
    for (size_t i = 0; i < sizeof(inArray) / sizeof(inArray[0]); i++) {
        ...
    }
}

int main(void)
{
    int masterArray[ARRAY_MAX_LEN];

    ...
    ArrayInit(masterArray);

    return 0;
}
```

**【正例】**
如下代码示例中，使用入参len表示指定数组的长度：

```c
#define ARRAY_MAX_LEN 256

// 函数说明：入参len是入参数组的长度
void ArrayInit(int inArray[], size_t len)
{
    for (size_t i = 0; i < len; i++) {
        ...
    }
}

int main(void)
{
    int masterArray[ARRAY_MAX_LEN];

    ArrayInit(masterArray, ARRAY_MAX_LEN);
    ...

    return 0;
}
```





### ARR.03 禁止通过对指针变量进行sizeof操作来获取数组大小

**【描述】**
将指针当做数组进行sizeof操作时，会导致实际的执行结果与预期不符。例如：变量定义 `char *p = array`，其中array的定义为`char array[LEN]`，表达式`sizeof(p)`得到的结果与 `sizeof(char *)`相同，并非array的长度。

**【反例】**
如下代码示例中，buffer和path分别是指针和数组，程序员想对这2个内存进行清0操作，但由于程序员的疏忽，将内存大小误写成了`sizeof(buffer)`，与预期不符。

```c
char path[MAX_PATH];
char *buffer = (char *)malloc(SIZE);
...

...
memset(path, 0, sizeof(path));

// sizeof与预期不符，其结果为指针本身的大小而不是缓冲区大小
memset(buffer, 0, sizeof(buffer));
```

**【正例】**
如下代码示例中，将`sizeof(buffer)`修改为申请的缓冲区大小：

```c
char path[MAX_PATH];
char *buffer = (char *)malloc(SIZE);
...

...
memset(path, 0, sizeof(path));
memset(buffer, 0, SIZE); // 使用申请的缓冲区大小
```





### ARR.04 避免整数与指针间的互相转化

**【描述】**
整数与指针之间相互转换的结果是由实现定义的。在linux下，将指针转换为long类型之后再转换为原类型的做法通常不会丢失信息，但C语言标准并未对此予以保证。

> 指向void的指针可以转换为任何对象类型的指针，也可以从任何对象类型的指针转换为指向void的指针。
> 指向任何对象类型的指针可以转换为指向void的指针并再次转换到原来类型的指针，转换结果应与原始指针相等。
> 整数可能被转换为任何指针类型。除前面所规定的情况，其结果由实现定义，可能未正确对齐，也可能未指向所引用类型的实体。
> 任何指针类型可能被转换为一个整数类型。除前面所规定的情况，其结果由编译器实现定义。如果结果不能用整数类型表示，则程序会产生未定义行为。结果不一定在任何整数类型的取值范围内。
> 任何指向void的有效指针可以转换成intptr_t或uintptr_t类型后再转换成void指针，转换结果应与原始指针相等。

因此，当代码中出现指针和整数互转的情况，首先考虑是否通过修改代码避免转换，如果必须做转换，建议先将指针转换为`void *`后再转换为`uintptr_t`或`intptr_t`类型存放转换后的指针值。

**【反例】**
如下代码示例中，当指针为64位且无符号 int 为32位时，转换后的数值可能不在int类型的值域范围内，导致错误。

```c
char *p = ...;
char *p2 = ...;

// 直接将指针转换为 int 可能会超出int表示范围导致错误
unsigned int number = (unsigned int)p;

// 将uintptr_t转换为int 可能会发生数据截断导致错误
unsigned int number2 = (unsigned int)(uintptr_t)p2;
```

**【正例】**
如下代码示例中，使用uintptr_t类型接收转换后的指针，先转换为`void *`的原因是因为C语言标准中只规定了`void *`转换`intptr_t`或`uintptr_t`的行为是确定的。

```c
char *p = ...;
char *p2 = ...;
uintptr_t number = (uintptr_t)(void *)p;
uintptr_t number2 = (uintptr_t)(void *)p2;
```

**【例外】**
值为0的整数字面量或者编译期间可确定的值为0的常量表达式可以转换为指针类型，其结果是空指针。
将一个表示地址的整数常量转换为指针时,行为是由实现定义的，可能未正确对齐，也可能未指向所引用类型的实体。
但是在某些应用中可能需要通过此类转换来读写特定硬件地址的内容，在这些情况下，本规范仅允许在特定平台（包括硬件、操作系统、编译器和标准C库）中使用此类转换。
编写代码前需充分分析和验证转换结果的正确性，示例代码如下：

```c
#define FIXED_MEMORY_ADDR   硬件有效地址
uintptr_t mid = (uintptr_t)FIXED_MEMORY_ADDR; // 也可以使用intptr_t

/*
 * 注意：下面代码不具备可移植性，仅在特定平台下使用。
 * 转换结果可能未正确对齐，也可能未指向所引用类型的实体。
 */
TargetType *p = (TargetType *)(void *)mid;
```

**【相关软件CWE编号】** CWE-758，CWE-704，CWE-587




### ARR.05 不同类型的对象指针之间不应进行强制转换

**【描述】**
不同的对象类型可能有不同的对齐要求，如果在不同类型的对象指针之间做强制转换，或转化为void指针后再转换为不同类型的对象指针，对象的对齐方式可能被改变，从而导致程序产生未定义行为。

> 指向的对象或者不完整类型的指针，可能被转换为指向不同对象或者其他不完整类型的指针。若结果指针没有正确地对齐，就会导致程序产生未定义行为。

另外，从void指针转换为特定类型的指针是允许的，但需要满足如下要求：
    1、确保转换后的指针正确对齐；
    2、void指针指向的数据长度必须满足目标类型大小的要求。

**【反例】**

如下代码示例中，`char`类型指针`&c` 被转换为更严格对齐的`int`类型指针`intPtr`再被强制转换为`char`类型指针`charPtr`。在某些实现上，`charPtr`将不匹配`&c`。因此，如果将一个对象类型的指针转​​换为另一个对象类型的指针，则第二个对象类型的对齐要求不能比第一个更加严格。

```c
char c = 'x';         // 变量c的地址可能不在int对齐(通常为4字节对齐)的内存边界上
int *intPtr = (int *)&c;  // 不兼容的转换
char *charPtr = (char *)intPtr;

ASSERT(charPtr == &c);     // 在一些系统下会因地址不对齐失败
```
**【正例】**
如下代码示例中，`char` 类型值被保存在一个类型为 `int` 的对象中，这样指针的值会被正确对齐。

```c
char c = 'x';
int i = c;
int *intPtr = &i;

ASSERT(intPtr == &i);
```

**【反例】**
C标准允许将任何对象指针和 `void *` 相互转换。因此，一种指针类型可以转换为 `void *` 后再转换为另一种类型，即使类型不兼容也不会出现编译告警。
如下代码示例中，向 Func() 函数传入了 `char` 类型指针，但是函数将其转换为 `int` 类型指针返回，intPtr 可能比 charPtr 对齐更严格。

```c
int *Func(void *ptr)
{
    ...
    return ptr;
}

void Caller(char *charPtr)
{
    int *intPtr = Func(charPtr);  // 程序可能产生未定义行为
    ...
}
```


**【正例】**
如下代码示例中，重构函数参数类型为 `int` 类型指针，避免出现类型转换。

```c
int *Func(int *ptr)
{
    ...
    return ptr;
}

void Caller(int *ptr)
{
    int *intPtr = Func(ptr);
    ...
}
```

**【反例】**
有些架构要求访问大于一个字节的对象时指针正确对齐，然而，在系统代码中，未对齐数据（例如网络栈）往往必须复制到正常对齐的内存位置，见如下代码示例：

```c
typedef struct {
    int len;
    ...
} Header;

int ProcessMessage(unsigned char *data, size_t length)
{
    Header header;
    Header *tmp = NULL;
    unsigned int offset;

    ... // 校验入参合法性
    offset = data[OFFSET_VALUE];
    tmp = (Header *)(data + offset);  // 如果指针不对齐，程序会产生未定义行为
    memcpy(&header, tmp, sizeof(header));
    ...
}
```

将未对齐的值对齐到引用需要对齐类型的指针时，程序会产生未定义行为。例如，编译器可能注意到 tmp 和 header 必须对齐，于是使用内联的memcpy()，在该函数中使用假定已对齐数据的指令。

**【正例】**
如下代码示例中，避免使用Header指针做类型转换：

```c
typedef struct {
    int len;
    ...
} Header;

int ProcessMessage(unsigned char *data, size_t length)
{
    Header header;
    unsigned int offset;

    ... // 校验入参合法性
    offset = data[OFFSET_VALUE];
    memcpy(&header, data + offset, sizeof(header));
    ...
}
```

**【例外】**
允许将对象类型指针转换为`char、signed char`或`unsigned char`对象类型的指针。

> 当指向对象的指针转换为指向字符类型的指针时，结果指向对象的最低地址字节。结果的连续增量（直到对象的大小）会产生指向对象剩余字节的指针。




### ARR.06 不要使用变长数组类型

**【描述】**
在C99中新加入了对变长数组的支持，即数组的长度可以由某个非const变量来定义，变长数组的空间大小直到程序运行时才能确定。
由于要在运行时才能确定数组的大小，因此分配空间的起始地址也是不确定的（例如要在栈上分配两个可变长数组的情况）。这种不确定性会给程序执行带来非常大的风险。

当变长度数组的大小超大时，可能会导致堆栈混乱而引发异常，如果大小为负数或零，那么程序会产生未定义行为。

**【反例】**
如下代码示例中使用变长数组是不符合规范的。

```c
int ReadAndProcess(size_t n)
{
    int array[n]; // 不符合：使用变长数组类型
    ...
}
```

```c
void Func(size_t n)
{
    int val[n];       // 不符合
    size_t count = 10;
    int array[count]; // 不符合: 可维护性不好

    count = 20;       // 以为修改了array 的大小，但是实际上并未修改 array 的大小

    ...
}
```

```c
// 不符合: 该声明中的 array 会被调整为指针参数, 并不代表 array 的大小是 n
void Func2(int n, int array[n])
{
    ...
}
```

**【正例】**
解决方案是使用malloc动态分配一段内存，或者在能够明确数组大小时，显式指定其长度。

```c
int ReadAndProcess(size_t n)
{
    // 校验n是否合法

    // 解决方案，使用malloc分配大小
    int *array = (int *)malloc(n * sizeof(int));
    // array判空及初始化，此处略
    ...
}
```

```c
#define ARRAY_LEN 16

void Func(void)
{
    // 解决方案，明确array的大小，满足此处场景需求。
    int array[ARRAY_LEN];
    ...
}
```




### ARR.07 声明一个带有外部链接的数组时，必须显式指定它的大小

**【描述】**
在**声明**具有外部链接的数组时，明确指定其大小会使代码更加安全。明确声明外部链接数组的大小可以方便在编写代码时，校验数组索引是否越界；而且还有利于静态分析工具做数组边界检查。

此规则仍然允许通过初始化列表隐式指定大小的方式来定义一个数组，但在将其声明为一个带有外部链接的数组时，必须显式指定它的大小。

在声明同时也要遵从规则[禁止通过声明的方式引用外部函数接口、变量](G.INC.07_禁止通过声明的方式引用外部函数接口、变量.md)

**【反例】**
如下代码示例中，在头文件中声明了全局数组g_array，但是未显式指定其大小。

```c
// in foo.h
extern int g_array[];     // 不符合：没有显式指定数组大小
```

**【正例】**
如下是正确的代码示例，在头文件中声明全局数组`g_array`时，显式指定了数组的大小为`MAX_LEN`。

```c
// in foo.h
extern int g_array[MAX_LEN];   // 符合：显式指定了数组大小
```

**【正例】**
当使用初始化列表隐式指定外部链接数组的大小时，可以定义独立的记录数组长度的常量来使用该数组。
```c
// foo.h
const size_t g_privLen;
const char g_priv[];

// foo.c
const char g_priv[] = {'x', 'w', 'r'};
const size_t g_privLen = sizeof(priv) / sizeof(priv[0]);
```




## 2.11 字符串




### STR.01 确保字符串存储有足够的空间容纳字符数据和null结束符

**【描述】**
将数据复制到不足以容纳数据的缓冲区，会导致缓冲区溢出。缓冲区溢出经常发生在字符串操作中。为了避免这种错误，截断拷贝的数据以限制字符串的字节长度是一种防御方法，但是最好的措施是确保目的缓冲区的大小足以容纳复制数据和null结束符。当字符串存储在堆空间时，确保分配内存时已分配了足够的空间。
部分字符串处理函数由于设计时安全考虑不足，或者存在一些隐含的目的缓冲区长度要求，容易被误用，导致缓冲区写溢出。此类典型函数包括不在C标准库函数中的itoa()，realpath()函数。

**【反例】**(itoa)
有些函数如itoa(), realpath()需要在对传入的缓冲区指针位置进行写入操作，但函数并没有提供缓冲区长度。因此，在调用这些函数前，必须提供足够的缓冲区。
如下代码示例中，试图将数字转为字符串，但是目标存储空间的预留长度不足：

```c
int num = ...
char str[8];
itoa(num, str, 10);  // 10进制整数的最大存储长度是12个字节
```
**【正例】**
使用安全函数实现整数转换为10进制形式的字符串。
```c
int num = ...
char str[16]; // 有时会考虑字节对齐定义冗余的长度，这里选择了16
int ret = sprintf_s(str, sizeof(str), "%d", num);
...  // 处理错误
```

**【反例】**(realpath)
如下代码示例中，试图将路径标准化，但是目标存储空间的长度不足：

```c
#define MAX_PATH_LEN 100
char  resolvedPath[MAX_PATH_LEN];

/*
 * realpath函数的存储缓冲区长度是由PATH_MAX常量定义，
 * 或是由_PC_PATH_MAX系统值配置的，通常都大于100字节
 */
char *res = realpath(path, resolvedPath);
...
```

**【正例】**
可以将realpath的第二个参数传入NULL, 以让系统自动分配合适的内存。
```c
char *resolvedPath = NULL;

resolvedPath = realpath(path, NULL);
if (resolvedPath == NULL) {
    ... // 处理错误
}
...
if (resolvedPath != NULL) {
    free(resolvedPath);
    resolvedPath = NULL;
}
...
```

**【反例】**
如下代码示例中，在对外部数据进行解析并将内容保存到name中，未考虑name的大小：
```c
int ProcessMessage(unsigned char *msg, size_t length)
{
    ...
    char name[MAX_NAME];
    size_t i = 0;
    // 必须考虑msg不包含预期的字符'\n'
    while (i < length &&
           msg[i] != '\0' &&
           msg[i] != '\n') {
        name[i] = msg[i];
        i++;
    }
    name[i] = '\0';
    ...
}
```

**【正例】**
如下代码示例中，在对外部数据进行解析并将内容保存到name中，考虑了name的大小：

```c
int ProcessMessage(unsigned char *msg, size_t length)
{
    ...
    char name[MAX_NAME];
    size_t i = 0;
    // 必须考虑msg不包含预期的字符'\n'
    while (i < length &&
           msg[i] != '\0' &&
           msg[i] != '\n' &&
           i < MAX_NAME - 1) { // 使用 MAX_NAME - 1 保留结束符空间
        name[i] = msg[i];
        i++;
    }
    name[i] = '\0';
    ...
}
```

**【反例】**（差一错误）
如下代码示例中，展现了一个差一错误。代码中的循环将数据从src复制到dest。但是因为循环没有考虑'\0'结束符，它可能错误的写入dest缓冲区结束位置之后的一个字节。

```c
...
char dest[ARRAY_SIZE];
char src[ARRAY_SIZE];
...
size_t i;
for (i = 0; src[i] != '\n' && i < ARRAY_SIZE; i++) {
    dest[i] = src[i];
}
dest[i] = '\0'; // 不符合：越界写了一个字节
```

**【正例】**（差一错误）
如下代码示例中，修改了循环条件，避免差一错误导致的写越界。

```c
...
char dest[ARRAY_SIZE];
char src[ARRAY_SIZE];
...
size_t i;
for (i = 0; src[i] != '\n' && i < ARRAY_SIZE - 1; i++) {
    dest[i] = src[i];
}
dest[i] = '\0';
```

**【反例】**（gets函数）
gets函数在C99技术勘误3中被弃用，从C11标准中删除，它本是不安全的，绝不应该使用，因为它没有提供任何控制从stdin读取缓冲区数据量的办法。
如下代码示例中，假设gets函数不会读取超过`(BUFFER_SIZE - 1)`个字符，但是这是个无效的假设，可能造成缓冲区溢出。
gets函数从stdin中读取字符写入目标数组，直到遇到文件结束符或换行符结束，并将换行符丢弃，在读入数组的最后一个字符后面写入'\0'结束符。

```c
#define BUFFER_SIZE 128

char buf[BUFFER_SIZE];
if (gets(buf) == NULL) {
    ... // 错误处理
}
```

**【正例】**（fgets函数）
如下代码示例中，fgets函数从流中读取到数组的字符数最多不超过第二个参数减一，并保证目标字符串有'\0'结束符，因此不会造成缓冲区溢出。

```c
#define BUFFER_SIZE 128

char buf[BUFFER_SIZE];
...
if (fgets(buf, sizeof(buf), stdin) == NULL) {
    ... // 错误处理
}
... // 继续处理换行符等
```
fgets函数不是gets函数的严格替代品，这是因为fgets函数会保留换行符（如果读到的话），也可能返回一个不完整的行。使用fgets函数安全地处理太长而无法保存在目标数组中的行是可能的，但是由于性能原因，不建议这么做。

**【正例】**（gets_s函数）

gets_s函数最多从stdin流读取指定数量 - 1个字符到目标数组，丢弃换行符并保证有'\0'结束符。 
如下代码示例中，使用gets_s读取数据，避免缓冲区溢出：

```c
#define BUFFER_SIZE 128

char buf[BUFFER_SIZE];
if (gets_s(buf, sizeof(buf)) == NULL) {
    ... // 错误处理
}
```

**【反例】**(getchar函数)

一次读取一个字符提供了控制行为的更大灵活性，但是需要附加的性能开销。如下代码示例中，一次读一个字符直到遇到文件结束或换行符为止，丢弃换行符，并在最后一个读到的字符之后添加'\0'结束符，但是这段代码存在缓冲区溢出风险，没有校验指针是否超出了buf的有效范围：

```c
#define BUFFER_SIZE 128

char buf[BUFFER_SIZE];
char *p = buf;
int ch;

while ((ch = getchar()) != '\n' && ch != EOF) {
    *p = (char)ch;
    p++;
}
*p = '\0';
...
```

**【正例】**(getchar函数)

如下代码示例中，添加了校验代码。当`count == BUFFERSIZE - 1`时，字符不会再复制到buf，并为结束符留出空间。循环将继续读取字符值直到遇到换行或文件结束为止：

```c
#define BUFFER_SIZE 128

char buf[BUFFER_SIZE];
size_t count = 0;
int ch;

while ((ch = getchar()) != '\n' && ch != EOF) {
    if (count < sizeof(buf) - 1) {
        buf[count] = (char)ch;
        count++;
    }
    ...
}
buf[count] = '\0';  // 设置字符串结束符
...
```

**【反例】**(scanf函数)
如下代码示例中，scanf函数调用可能造成写入到字符数组buf之外：

```c
#define BUFFERSIZE 128

char buf[BUFFER_SIZE];
if (scanf("%s", buf) != 1) {
    ... // 错误处理
}
... // 函数实现其它部分
```

**【正例】**(scanf函数)
如下代码示例中，调用`scanf_s`函数以避免缓冲区溢出：

```c
#define BUFFER_SIZE 128

char buf[BUFFER_SIZE];
if (scanf_s("%s", buf, sizeof(buf)) != 1) {
    ... // 错误处理
}
... // 函数实现其它部分
```

**【反例】**(strcpy)

```c
#define MAX_ENV_LENGTH 256

char buff[MAX_ENV_LENGTH];
char *editor = getConfig("EDITOR");
if (editor == NULL) {
    ...
} else {
    strcpy(buff, editor);
}
...
```

**【正例】**(strcpy)
复制环境变量时限制其长度，避免出现缓冲区溢出：

```c
#define MAX_ENV_LENGTH 256

char buff[MAX_ENV_LENGTH];
char *editor = getConfig("EDITOR");
if (editor == NULL) {
    ...
} else {
    if (strcpy_s(buff, sizeof(buff), editor) ！= EOK) {
        ... // 错误处理
    }
}
...
```

**【反例】**(sprintf函数)

在如下代码示例中，name引用一个外部字符串；它可能来自用户输入、文件系统或者网络。程序从这个字符串构造一个文件名，准备打开该文件：

```c
#define MAX_NAME_LEN 128

char filename[MAX_NAME_LEN];
sprintf(filename, "%s.txt", name);
...
```

**【正例】**(sprintf函数)

一个解决方案是使用安全函数`sprintf_s`替代sprintf函数，避免出现缓冲区溢出：

```c
#define MAX_NAME_LEN 128

char filename[MAX_NAME_LEN];
int ret = sprintf_s(filename, sizeof(filename),"%s.txt", name);
if (ret < 0) {
     ... // 错误处理
}
...
```

**【影响】**

违反本条款可能导致拒绝服务，缓冲区溢出，信息泄露，或执行任意代码。

**【相关软件CWE编号】** CWE-119，CWE-120，CWE-123，CWE-125，CWE-676

**【历史漏洞】** CAN-2003-0352




### STR.02 对字符串进行存储操作，确保字符串有null结束符

**【描述】**
部分字符串处理函数操作字符串时，将截断超出指定长度的字符串，如strncpy()函数最多复制n个字符到目的缓冲区，如果源字符串长度大于n，则目的缓冲区的内容为n个被复制的字符，null结束符不会被写入到目的缓冲区。使用这类函数时，可能会无意截断导致数据丢失，并在某些情况下会导致软件漏洞。
因此，对字符串进行存储操作，必须确保字符串有null结束符（如使用字符串安全函数生成字符串，或显式对字符数组赋null结束符），否则在后续的调用strlen等操作中，可能会导致内存越界访问漏洞。

**【反例】**
在如下代码示例中，使用strncpy函数复制字符串时可能会发生截断（发生条件为：`strlen(name) > sizeof(filename) - 1`）。当发生截断时，filename的内容是不完整的，并且缺少'\0'结束符，后续对filename的操作可能会导致软件漏洞：

```c
#define FILENAME_LEN 128

char filename[FILENAME_LEN];
strncpy(filename, name, sizeof(filename) - 1);
...
```

**【正例】**
使用安全函数`strcpy_s`复制字符串，并检查安全函数返回值，如果成功，则确保filename字符串是完整的并且包含'\0'结束符：

```c
#define FILENAME_LEN 128

char filename[FILENAME_LEN];
errno_t ret = strcpy_s(filename, sizeof(filename), name);
if (ret != EOK) {
     ... // 处理错误
}
...
```

**【相关软件CWE编号】** CWE-170，CWE-464




## 2.12 断言

断言是一种调试诊断机制，用于验证代码是否符合程序员的预期。程序员在开发期间应该对函数的参数、代码中间执行结果合理地使用断言机制，确保程序的缺陷尽量在测试阶段被发现。

断言可以用于代码中说明各种假定，包括前提条件(preconditions)和后置条件(postconditions)。例如，可以对仅在模块内部使用的函数体内，用断言来声明调用该函数的前提条件，以帮助模块内的调用者正确传入参数。对于模块对外提供的接口函数，由于其实现对外是不可见的，因此不能通过断言来告知调用者需要遵循的约定，也不能通过使用断言来减少对接口函数参数的实际校验。

在调试版本中，断言被触发后，说明程序出现了不应该出现的严重错误，程序会立即提示错误，并终止执行。典型的严重错误如参数在同一模块的上层函数已经校验过，但传递到下层函数后参数不正确，或程序模块内部发送的状态值未定义。

断言必须用宏进行定义，只在调试版本有效，最终发布版本不允许出现assert函数，例如可以按下面的代码实现：

```c
#include <assert.h>
#ifdef DEBUG
#define ASSERT(f)  assert(f)
#else
#define ASSERT(f)  ((void)0)
#endif
```

如下的函数VerifyUser，上层调用者会保证传进来的参数是合法的字符串，不可能出现传递非法参数的情况。因此，在该函数的开头，加上4个ASSERT进行校验。

```c
bool VerifyUser(const char *userName, const char *password)
{
    ASSERT(userName != NULL);
    ASSERT(strlen(userName) > 0);
    ASSERT(password != NULL);
    ASSERT(strlen(password) > 0);
    ...
}
```




### AST.01 避免在代码中直接使用assert()

**【描述】**
使用assert()会使代码发布版本与NDEBUG宏发生直接联系。为避免发布版本定义的宏受限于NDEBUG，在代码中不应直接使用assert()。建议使用内部函数Assert()。

【反例】

```c
int Foo(int *array, size_t size)
{
    /*
     * 违反本条规范: 当发布版本的编译选项中未指定NDEBUG时，
     * 该代码会被编译到二进制文件中，因此避免在代码中直接使用assert()
     */
    assert(array != NULL);
    ...
}
```





### AST.02 禁止用断言检测程序在运行期间可能导致的错误，可能发生的错误要用错误处理代码来处理

**【描述】**
断言主要用于调试期间，在发布版本中应将其关闭。因此，断言应该用于防止不正确的程序员假设，而不能用在发布版本上检查程序运行过程中发生的错误。

断言永远不应用于验证是否存在运行时（与逻辑相对）错误，包括但不限于：
- 无效的用户输入（例如：命令行参数和环境变量）
- 文件错误（例如：打开、读取或写入文件时出错）
- 网络错误（例如：网络协议错误）
- 内存不足的情况（例如：malloc()类似的故障）
- 系统资源耗尽（例如：文件描述符、进程、线程）
- 系统调用错误（例如：执行文件、锁定或解锁互斥锁时出错）
- 无效的权限（例如：文件、内存、用户）

例如，防止缓冲区溢出的代码不能使用断言实现，因为该代码必须编译到发布版本的可执行文件中。
如果服务器程序在网运行时由恶意用户触发断言失败，会导致拒绝服务攻击。在这种情况下，更适合使用软故障模式，例如写入日志文件和拒绝请求。

**【反例】**
以下代码的所有ASSERT的用法都是错误的。例如，错误的使用ASSERT宏来验证内存分配是否成功，因为内存的可用性取决于系统的整体状态，并且在程序运行的任何时候都可能耗尽，所以必须以具有韧性的方式来妥善处理并将程序从内存耗尽中恢复。因此，使用ASSERT宏来验证内存分配是否成功将是不合适的，因为这样做可能导致进程突然终止，从而开启了拒绝服务攻击的可能性。

```c
FILE *fp = fopen(path, "r");
ASSERT(fp != NULL);  // 不符合：文件有可能打开失败
char *str = (char *)malloc(MAX_LINE);
ASSERT(str != NULL); // 不符合：内存有可能分配失败
ReadLine(fp, str);
char *p = strstr(str, "age="");
ASSERT(p != NULL);   // 不符合：文件中不一定存在该字符串
char *end = NULL;
long age = strtol(p + 4, &end, 10);
ASSERT(age > 0);     // 不符合：文件内容不一定符合预期
```

**【正例】**
下面代码演示了如何重构上面的错误代码
```c
FILE *fp = fopen(path, "r");
if (fp == NULL) {
    ... // 错误处理
}
char *str = (char *)malloc(MAX_LINE);
if (str == NULL) {
    ... // 错误处理
}
ReadLine(fp, str);
char *p = strstr(str, "age=");
if (p == NULL) {
    ... // 错误处理
}
char *end = NULL;
long age = strtol(p + 4, &end, 10);
if (age <= 0) {
    ... // 错误处理
}
```


**【相关软件CWE编号】** CWE-190




### AST.03 禁止在断言内改变运行环境

**【描述】**
在程序正式发布阶段，断言不会被编译进去，为了确保调试版和正式版的功能一致性，严禁在断言中使用任何赋值、修改变量、资源操作、内存申请等操作。

例如，以下的断言方式是错误的：

```c
ASSERT(p1 = p2);        // p1被修改
ASSERT(i++ > 1000);     // i被修改
ASSERT(close(fd) == 0); // fd被关闭
```




### AST.04 一个断言只用于检查一个条件

**【描述】**
为了更加准确地发现错误的位置，每一条断言只校验一个错误。

**【反例】**
下面的断言同时校验多个错误，在断言触发的时候，无法判断到底是哪一个错误触发了断言：

```c
int Foo(int *array, size_t size)
{
    ASSERT(array != NULL && size > 0 && size <= ARRAY_SIZE_MAX);
    ...
}
```

**【正例】**
应该将每个错误检查分开，可以修改如下：

```c
int Foo(int *array, size_t size)
{
    ASSERT(array != NULL);
    ASSERT(size > 0);
    ASSERT(size <= ARRAY_SIZE_MAX);
    ...
}
```

**【正例】**
如果一个错误检查是由逻辑或组合而成，那么可以写在一个断言中。代码略。





## 2.13 函数设计

权限、并发、资源管理策略的编程设计方法，设计模式的最佳实践由于其描述的复杂性，需要单独的文档说明，下面将尽量不涉及有关内容。




### FUD.01 对所有外部数据进行合法性检查

**【描述】**
外部数据的来源包括但不限于：网络、用户输入、命令行、文件（包括程序的配置文件）、环境变量、用户态数据（对于内核程序）、进程间通信（包括管道、消息、共享内存、socket、RPC等，特别需要注意的是设备内部不同单板间通讯也属于进程间通信）、API参数、全局变量。

来自程序外部的数据通常被认为是不可信的，在使用这些数据之前，需要进行合理的检查。
如果不对这些外部数据进行检查，将可能导致不可预期的安全风险。

对来自程序外部的数据要校验处理后才能使用。典型的使用场景包括：

**作为数组索引**
    将不可信的数据作为数组索引，可能导致超出数组上限，从而造成非法内存访问。
**作为内存偏移地址**
    将不可信数据作为指针偏移访问内存，可能造成非法内存访问，并可以造成进一步的危害，如任意地址读/写。
**作为内存分配的尺寸参数**
    例如进行0字节长度分配可能造成非法内存访问，或未限制分配内存大小造成的过度资源消耗。
**作为循环条件**
    将不可信数据作为循环限定条件，可能会引发缓冲区溢出、内存越界读/写、死循环等问题。
**作为除数**
    参见除零错误(被零除)。
**作为命令行参数**
    参见“禁止外部可控数据作为进程启动函数的参数”。
**作为数据库查询语句的参数**
    参见“禁止直接使用外部数据拼接SQL命令”。
**作为输入/输出格式化字符串**
    参见“调用格式化输入/输出函数时，禁止format参数受外部数据控制”。
**作为内存拷贝长度**
    当作为拷贝长度时，可能造成目标缓冲区溢出。
**作为文件路径**
    直接打开不可信路径，可能会导致目录遍历攻击，操作了攻击者无权操作的文件，使得系统被攻击者所控制。

输入校验包括但不局限于：
- 校验数据长度
- 校验数据范围
- 校验数据类型和格式
- 校验输入只包含可接受的字符（“白名单”形式），尤其需要注意一些特殊情况下的特殊字符。

**外部数据校验原则**
**1.信任边界**
由于外部数据不可信，因此系统在运行过程中，如果数据传输与处理跨越不同的信任边界，为了防止攻击蔓延，必须对来自信任边界外的其他模块的数据进行合法性校验。
（a）so（或者dll）之间
so或dll作为独立的第三方模块，用于对外导出公共的api函数，供其他模块进行函数调用。so/dll无法确定上层调用者是否传递了合法参数，因此so/dll的公共函数需要检查调用者提供的参数合法性。so/dll应该设计成低耦合、高复用性，尽管有些软件的so/dll当前设计成只在本软件中使用，但仍然应该将不同的so/dll模块视为不同的信任边界。
（b）进程与进程之间
为防止通过高权限进程提权，进程与进程之间的IPC通信（包括单板之间的IPC通信、不同主机间的网络通信），应视为不同信任边界。
（c）应用层进程与操作系统内核
操作系统内核具有比应用层更高的权限，内核向应用层提供的接口，应该将来自应用层的数据作为不可信数据处理。
（d）可信执行环境内外环境
为防止攻击蔓延至可信执行环境，TEE、SGX等对外提供的接口，应该将来自外部的数据作为不可信数据处理。



**2.外部数据校验**
外部数据进入到本模块后，必须经过合法性校验才能使用。被校验后的合法数据，在本模块内，其他内部子函数中不需要重复校验。
下面的例子，函数Foo处理外部数据，由于buffer不一定是’\0’结尾， strlen 的返回值 nameLen 有可能超过 len，导致越界读取数据。本例中采用 strnlen 进行字符串长度计算，随后解析出 name 字符串，在后续的 Foo2 调用中可以直接使用 strlen。

**【反例】**

```c
void Foo(const unsigned char *buffer, size_t len)
{
    if (buffer == NULL) { // 必须做参数合法性检查
        // 错误处理
        ...
    }

    // buffer不一定是'\0'结尾
    size_t nameLen = strlen((const char *)buffer);
    char *name = (char *)malloc(nameLen + 1);
    if (name != NULL) {
        errno_t ret = memcpy_s(name, nameLen + 1, buffer, nameLen);
        name[nameLen] = '\0';
    }
    ...
}
```

**【正例】**
应该是调用 strnlen 避免读越界

```c
void Foo(const unsigned char *buffer, size_t len)
{
    if (buffer == NULL || len >= MAX_BUFFER_LEN) { // 必须做参数合法性检查
        // 错误处理
        ...
    }

    // buffer不一定是'\0'结尾
    size_t nameLen = strnlen((const char *)buffer, len);
    char *name = (char *)malloc(nameLen + 1);
    if (name != NULL) {
        memcpy_s(name, nameLen + 1, buffer, nameLen);
        name[nameLen] = '\0';
        foo2(name);    // foo2内可以直接使用 strlen
    }
    ...
}
```
下面的代码处理外部数据，数据格式如下:

MODULE_A_Foo 和MODULE_A_Foo2是MODULE_A的二个函数，MODULE_A_Foo处理外部数据，将name解析出来，传递给MODULE_A_Foo2处理，MODULE_A_Foo2又调用外部模块MODULE_B的MODULE_B_Foo处理。
```c
// MODULE_A_Foo2 为 MODULE_A 模块的内部函数，约定为由调用者保证参数的合法性
static void MODULE_A_Foo2(const char *name)
{
    // 如果以下的ASSERT触发，表示调用处违反了约定，调用处必须进行修改
    ASSERT(name != NULL);

    size_t nameLen = strlen(name);     //不需要检查name合法性
    MODULE_B_Foo(name);                //调用MODULE_B中的函数
}

void MODULE_A_Foo(const unsigned char *buffer, size_t len)
{
    if (buffer == NULL || len <= sizeof(int)) { // 必须做参数合法性检查
        // 错误处理
        ...
    }
    int nameLen = *(int *)buffer;
    // nameLen 是不可信数据，必须检查合法性
    if (nameLen <= 0 || (size_t)nameLen > len - sizeof(int)) {
        // 错误处理
        ...
    }
    char *name = (char *)malloc(nameLen + 1);
    if (name == NULL) {
        // 内存分配失败，错误处理
        ...
    }
    errno_t err = memcpy_s(name, nameLen + 1, buffer + sizeof(int), nameLen);
    if (err != EOK) {
        // 错误处理
        ...
    }
    name[nameLen] = '\0';   // 此时name是一个具有\0结尾的合法字符串
    MODULE_A_Foo2(name);    // 调用本模块内内部函数
    ...
}
```
以下是MODULE_B模块中的代码：
```c
/*
 * MODULE_B_Foo 为 MODULE_B 模块的公共函数，
 * 其约定为，如果参数name不为NULL,那么必须是一个具有’\0’结尾的合法字符串并且长度大于0
 */
void MODULE_B_Foo(const char *name)
{
    if (name == NULL || name[0] == '\0') { // 必须做参数合法性检查
        // 错误处理
        ...
    }
    size_t nameLen = strlen(name);    // 不需要使用strnlen
    ...
}
```
对于模块A来说， buffer 是外部不可信输入，必须做严格的校验，从 buffer 解析出来的 name，在解析过程中进行了合法性检查，在模块A内部属于合法数据，作为参数传递给内部子函数时不需要再做合法性检查（如果要继续对 name 内容进行解析，那么仍然必须对 name 内容进行校验）。
如果模块A中的 name 继续跨越信任面传递给其他模块（在本例中是直接调用模块B的公共函数，也可以是通过文件、管道、网络等方式），那么对于B模块来说， name 属于不可信数据，必须做合法性检查。




### FUD.02 对象或函数的所有声明必须与定义具有一致的名称和类型限定符

**【描述】**
在函数或对象的声明和定义中应使用一致的类型和限定符，声明和定义之间的不一致可能存在编程错误，参数名可以提供关于函数接口的有用信息。本规则要求如下：

- 函数声明中的参数应该包含参数名，并且函数定义与其声明中的参数类型以及参数名需要保持一致。
- 如果一个函数声明中没有参数，则在其原型中使用关键字void，否则将导致调用方和被调用方之间的功能接口模糊。
- 同一个对象的声明和定义应保持一致，包括类型、限定符等。

> 引用同一对象或函数的所有声明应具有一致的类型，否则程序会产生未定义行为。

**【反例】**
如下代码示例中，在func.c中定义了函数，但是在func.h中对该函数的声明存在名称或类型限定符上的不一致，错误的地方已通过注释的方式标识出来。

```c
// In func.h
void Func1(const int num);    // 不符合：参数的限定符与函数定义不一致
void Func2(int);              // 不符合：缺少参数名，应修改为void Func2(int num)

// 不符合： 参数名不匹配，应修改为 void Func3(int num, int count)
void Func3(int count, int num);

void Func4();                  // 不符合：空参数列表，应修改为void Func4(void)

void (*Fp1)();                 // 不符合：空参数列表，应修改为void (*Fp1)(void)
typedef void (*Fp2)(int);      // 不符合：缺少参数名

// In func.c
int g_a = 0;
int g_array[4] = {0};

void Func1(int num) // 不符合： 参数的限定符与函数声明不一致
{
    ...
}
void Func2(int num)
{
    ...
}
void Func3(int num, int count)
{
    ...
}
void Func4() // 不符合： 应修改为 void Func4(void)
{
    ...
}

// In caller.c
#include "func.h"
extern short g_a;    // 不符合： 类型不一致，应在func.h中声明
extern int *g_array; // 不符合： 类型不一致，应在func.h中声明

void Caller(void)
{
    Func4(3);        // 不符合： 由于兼容性原因，可以编译通过，但是传入了无用的参数
}
```

**【正例】**
如下代码示例中，保持声明和定义一致：

```c
// In func.h
extern int g_a;
extern int g_array[4];
void Func1(int num);
void Func2(int num);
void Func3(int num, int count);

typedef int Width;
typedef int Height;

void Func4(void)
void (*Fp1)(void);
typedef void (*Fp2)(int num);
typedef void (*Fp3)(int n); // 该规则不要求函数指针中的参数名与其指向函数参数名相同

// In func.c
int g_a = 0;
int g_array[4] = {0};

void Func1(int num)
{
　  ...
}
void Func2(int num)
{
    ...
}
void Func3(int num, int count)
{
    ...
}
void Func4(void)
{
    ...
}
```





### FUD.03 设计函数时，优先使用返回值而不是输出参数

**【描述】**
使用返回值而不是输出参数，可以提高可读性，并且通常能够提供相同或更优的性能。

如：函数名为 GetXxx、FindXxx 或直接用名词作函数名的函数，直接返回对应对象，可读性更好。





### FUD.04 函数避免使用 void\* 类型参数

**【描述】**
函数参数应尽量避免使用 `void *` 类型，尽量让编译器在编译阶段就检查出类型不匹配的问题。

**【反例】**
使用强类型便于编译器帮我们发现错误，如下代码中注意函数 FooListAddNode 的使用：

```c
typedef struct {
    struct List link;
    int foo;
} FooNode;

typedef struct {
    struct List link;
    int bar;
} BarNode;

void FooListAddNode(void *node) // 不符合： 这里用 void * 类型传递参数
{
    ASSERT(node != NULL);
    FooNode *foo = (FooNode *)node;
    ListAppend(&g_fooList, &foo->link);
}

void MakeTheList(void)
{
    FooNode *foo = NULL;
    BarNode *bar = NULL;
    ...
    FooListAddNode(bar); // 不符合：这里本意是想传递参数 foo，但错传了bar，却没有报错
}
```

上述问题有可能很隐晦，不易轻易暴露，从而破坏性更大。

**【正例】**
如果明确 FooListAddNode 的参数类型，而不是 `void *`，则在编译阶段就能发现上述问题。

```c
// 其他部分同上
void FooListAddNode(FooNode *foo)
{
    ListAppend(&g_fooList, &foo->link);
}
```

**【例外】**

某些通用泛型接口，需要传入不同类型指针的，可以用 void * 入参。





### FUD.05 函数要简短

**【描述】**
函数要简短。复杂过长的函数不利于阅读理解，难以维护。 过长的函数往往意味着函数功能不单一，过于复杂，或过分呈现细节，未进行进一步拆分或分层。

产品可从如下维度间接约束函数的尺寸和复杂度：
- 函数行数建议不超过50行（非空非注释）。
- 函数的参数个数。建议不超过5个。
- 函数最大代码块嵌套深度。建议不超过4层。





### FUD.06 内联函数要尽可能短，避免超过10行

**【描述】**

将函数定义成内联一般希望提升性能，但是实际并不一定能提升性能。

如果函数体短小，则函数内联可以有效的缩减目标代码的大小，并提升函数执行效率。

反之，函数体比较大，内联展开会导致目标代码的膨胀，特别是当调用点很多时，膨胀得更厉害，反而会降低执行效率。

内联函数规模建议控制在 10 行（非空非注释）以内。

不要为了提高性能而滥用内联函数。不要过早优化。一般情况，当有实际测试数据证明内联性能更高时，再将函数定义为内联。

对于类似 setter/getter 短小而且调用频繁的函数，可以定义为内联。




### FUD.07 数组作为函数参数时，必须同时将其长度作为函数的参数

**【描述】**
通过函数参数传递数组，函数参数必须同时传递数组可容纳元素的个数，而不是以字节为单位的数组最大大小；同样，通过函数参数传递一块内存进行读写操作时，必须同时传递内存块大小，否则在函数内访问该内存偏移时，无法判断偏移的合法范围，产生越界访问的漏洞。例如，直接使用strlen计算外部报文中的字符串长度时，可能读越界，此时应结合报文长度使用strnlen函数避免读取字符串越界。

在本规则中所说的“数组”不仅局限为数组类型变量，还包括字符串和指向连续内存块的指针。

**【反例】**
如下代码示例中，函数ParseMsg不知道msg的范围，容易产生内存越界访问漏洞。

```c
int ParseMsg(unsigned char *msg)
{
    ...
}

void Func(void)
{
    size_t len = GetMsgLen();
    ...
    unsigned char *msg = (unsigned char *)malloc(len);
    ...
    ParseMsg(msg);
    ...
}
```

**【正例】**
正确的做法是将msg的大小作为参数传递到ParseMsg中，如下代码：

```c
int ParseMsg(unsigned char *msg, size_t msgLen)
{
    ASSERT(msg != NULL);
    ASSERT(msgLen != 0);
    ...
}

void Func(void)
{
    size_t len = GetMsgLen();
    ...
    unsigned char *msg = (unsigned char *)malloc(len);
    ...
    ParseMsg(msg, len);
    ...
}
```

如下代码，msg是固定长度的数组，也必须将数组的最大元素数作为函数的参数，对于char类型的数组可以sizeof计算元素数：

```c
int ParseMsg(unsigned char *msg, size_t msgLen)
{
    ASSERT(msg != NULL);
    ASSERT(msgLen != 0);
    ...
}
void Func(void)
{
    unsigned char msg[MAX_MSG_LEN];
    ...
    ParseMsg(msg, sizeof(msg));
    ...
}
```

如果参数是`char *`，且参数作为写内存的缓冲区，那么必须传入其缓冲区长度。如：

```c
int SaveName(char *name, size_t size, const char *inputName)
{
    ...
    ret = strcpy_s(name, size, inputName);
    ...
}

void Func(void)
{
    char name[NAME_MAX];
    ...
    int ret = SaveName(name, sizeof(name), inputName);
    ...
}
```

**【例外】**

可以通过运行时约束处理程序保证不发生越界读或写的函数可以忽略最大元素参数。例如，安全函数`strcpy_s`的 src 参数不需要 size 参数。

```c
errno_t strcat_s(char *dest, size_t destMax, const char *src);
errno_t strcpy_s(char *dest, size_t destMax, const char *src);
```
strcpy_s函数没有显式为 src 提供元素个数参数。但是，它要求 src 有字符串结束符，这种情况下，函数内部通过strlen获得src的长度是合理的，并且 destMax > strlen(src)，从而保证功能正确。

**【影响】**

不遵循此条款可能会导致不正确的内存访问和缓冲区溢出问题。




### FUD.08 将字符串或指针作为函数参数时，在函数体中应检查参数是否为NULL

**【描述】**
如果字符串或者指针作为函数参数，为了防止空指针引用错误，在引用前必须确保该参数不为NULL。如果该函数仅用于处理模块内部的可信数据，需要由上层调用者保证该参数不能为NULL，那么在函数开始处可以加断言说明这个参数使用的前提条件。

**【正例】**
例如下面的代码，因为int *p有可能为NULL，因此在使用前需要进行判断。

```c
#define MAX_COUNT ...
int Func(int *p, size_t count)
{
    if (p == NULL || count == 0 || count > MAX_COUNT) {
        ... // 错误处理
    }
    int c = p[0];
    ...
}
int Caller(void)
{
    int *arr = ...
    size_t count = ...
    Func(arr, count);
    ...
}
```

下面的代码，由于p的合法性由调用者保证，对于 Func() 函数，不可能出现p为NULL的情况，因此加上断言进行校验。

```c
int Func(int *p, size_t count)
{
    ASSERT(p != NULL); // 由调用者保证p不为空
    ASSERT(count > 0);
    ASSERT(count <= MAX_COUNT);
    int c = p[0];
    ...
}

int Caller(void)
{
    int *arr = ...
    size_t count = ...
    ...
    if (arr != NULL && count > 0 && count <= MAX_COUNT) {
        Func(arr, count);
    }
    ...
}
```

**【影响】**

解引用空指针会导致程序产生未定义行为，通常会造成程序异常终止。在某些情况下，解引用空指针会导致任意代码执行漏洞。


**【相关软件CWE编号】** CWE-20，CWE-476




### FUD.09 避免修改函数参数的值

**【描述】**
虽然语法上允许修改函数参数的值，但这种修改可能会混淆或改变了参数本身的含义，其执行结果可能与程序员的期望不一致，会给代码开发、维护带来潜在的风险。

**【反例】**
如下代码示例中，不合理地修改了参数的值：

```c
void Func(int input, int *output)
{
    ...  // 包含input的合法性校验，确保不会在引起函数中的整数运算溢出问题
    input += Add(input);     // 不符合：修改参数的值，给后边的代码开发、维护造成迷惑
    threshold *= Multiplier(input);
    ...
    if (input > threshold) { // 这里本意是使用原始入参值，导致bug
        DoExtraOperation();
        ...
    }

    *output = input;         // input 已被修改，给阅读、维护代码造成迷惑
}
```

**【正例】**
如下代码示例中，使用单独的局部变量作为工作变量：

```c
void Func(int input, int *output)
{
    ...  // 包含input的合法性校验，确保不会在引起函数中的整数运算溢出问题
    int workVar = input;     // 符合：使用局部变量代替

    workVar += Add(workVar);
    threshold *= Multiplier(workVar);
    ...
    if (input > threshold) { // 原始入参值没变，和期望一致
        DoExtraOperation();
        ...
    }

    *output = workVar;       // 符合本规则要求，没有修改函数参数的值
}
```




## 2.14 函数使用




### 2.14.1 格式化输入/输出函数




#### FUU.0.1 调用格式化输入/输出函数时，禁止format参数受外部数据控制

**【描述】**
调用格式化函数时，如果format参数由外部数据提供，或由外部数据拼接而来，会造成格式化字符串漏洞。

攻击者如果能够完全或者部分控制格式字符串内容，可以使被攻击的进程崩溃、查看栈内容、查看内存内容或者在任意内存位置写入数据。结果是，攻击者能够以被攻击进程的权限执行任意代码。

格式化输出函数特别危险，这是因为许多程序员没有意识到它们是具有攻击能力的。比如：格式化输出函数可以使用%n转换符，向指定地址写入一个整数值。

这些格式化函数有：
    格式化输出函数: xxxprintf;
    格式化输入函数: xxxscanf;
    格式化错误消息函数: err(), verr(), errx(), verrx(), warn(), vwarn(), warnx(), vwarnx(), error(), error_at_line();
    格式化日志函数: syslog(), vsyslog().

**【反例】**
如下代码示例中的IncorrectPassword()函数的功能是在身份验证无效时（指定用户没有找到或者密码不正确），显示一条错误信息。
该函数接受一个源自用户的字符串数据user，而user是未验证的，是外部可控的。
该函数将user构造一条错误信息，然后用C语言标准函数fprintf打印到stderr。
```c
// 调用者需保证入参user的长度被限制为256个字节或者更少
void IncorrectPassword(const char *user)
{
    int ret = -1;
    static const char msgFormat[] = "%s cannot be authenticated.\n";

    size_t len = strlen(user) + 1 + sizeof(msgFormat);
    char *msg = (char *)malloc(len);
    if (msg == NULL) {
        ... // 错误处理
    }

    ret = snprintf_s(msg, len, len - 1, msgFormat, user);
    if (ret == -1) {
        ... // 错误处理
    } else {
        fprintf(stderr, msg); // msg中有来自未验证的外部数据，存在格式化字符串漏洞
    }

    free(msg);
}
```
示例代码中首先计算了消息的长度，然后分配内存，接着利用`snprintf_s()`函数拼接了消息内容。因此消息内容中包含了msgFormat的内容和用户的内容。
当入参user中含有用户输入的格式符（如`%s,%p,%n`等）后，`fprintf()`在执行时，会将msg作为一个格式化字符串来进行解析，而不是直接输出消息内容。
也就是说此时msg中的内容不会被直接打印到stderr中，反而会将一些未知的数据打印到stderr，引发程序产生未定义行为。这是一个非常严重的格式化字符串漏洞。

**【正例】**
下面是第一种推荐做法，代码中使用fputs()来代替fprintf()函数，fputs()会直接将msg的内容输出到stderr中，而不会去解析它。
```c
// 入参user的长度被限制为256个字节或者更少
void IncorrectPassword(const char *user)
{
    int ret = -1;
    static const char msgFormat[] = "%s cannot be authenticated.\n";

    // 这里加法运算不会整数溢出，因为user有限制
    size_t len = strlen(user) + 1 + sizeof(msgFormat);
    char *msg = (char *)malloc(len);
    if (msg == NULL) {
        ... // 错误处理
    }

    ret = snprintf_s(msg, len, len - 1, msgFormat, user);
    if (ret == -1) {
        ... // 错误处理
    } else {
        fputs(stderr, msg); // 使用fputs函数代替fprintf函数
    }
    free(msg);
}
```

**【正例】**
下面是第二种推荐做法，代码中将不受信任的用户输入user作为fprintf()的可选参数之一，用“%s”将user以字符串的形式固定下来，然后输出到stderr中，而不作为格式字符串的一部分，这样就消除了格式化字符串漏洞出现的可能性。
```c
void IncorrectPassword(const char *user)
{
    static const char msgFormat[] = "%s cannot be authenticated.\n";
    fprintf(stderr, msgFormat, user);
}
```

**【反例】**
如下代码示例中，使用了POSIX函数syslog()[IEEE Std 1003.1：2013]函数，但是syslog()函数也可能出现格式化字符串漏洞。
```c
void Foo(void)
{
    char *msg = GetMsg();
    ...
    syslog(LOG_INFO, msg); // 存在格式化字符串漏洞
}
```

**【正例】**
下面是推荐做法，代码中将不受信任的用户输入msg作为syslog()的可选参数之一，用“%s”将msg以字符串的形式固定下来，然后输出到系统日志中，而不作为格式字符串的一部分，这样就消除了格式化字符串漏洞出现的可能性。
```c
void Foo(void)
{
    static const char msgFormat[] = "%s cannot be authenticated.\n";
    char *msg = GetMsg();
    ...
    syslog(LOG_INFO, msgFormat, msg); // 这里没有格式化字符串漏洞
}
```

**【影响】**

如果格式串被外部可控，攻击者可以使进程崩溃、查看栈内容、查看内存内容或者在任意内存位置写入数据，进而以被攻击进程的权限执行任意代码。




#### FUU.0.2 调用格式化输入/输出函数时，使用有效的格式字符串

**【描述】**
格式化输入/输出函数（如fscanf()/fprintf()及相关函数）在format字符串控制下进行转换、格式化、打印其实参。

在创建格式化字符串时的常见错误包括：

- format中参数个数与实参个数不一致；
- 使用无效的转换指示符；
- 使用与转换指示符不兼容的标志字符；
- 使用与转换指示符不兼容的长度修饰符；
- format中转换指示符与实参类型不匹配；
- 使用实参指定宽度或者精度时，实参的类型不是int类型；

不要为格式化输入/输出函数提供未知的或者无效的转换规格，以及标志字符、精度、长度修饰符、转换指示符的无效组合。同样，不要提供与格式化字符串中的转换指示符类型不匹配的实参。这可能会使程序产生未定义行为。

**【反例】**
如下代码示例中，printf()的实参infoLevel类型与对应的转换指示符's'不匹配，正确的转换指示符要使用'd'。同样，实参infoMsg类型与对应的转换指示符'd'不匹配，正确的转换指示符要使用's'。
这些用法会使程序产生未定义行为，比如：printf()将把infoLevel实参解释为指针，试图从infoLevel包含的地址中读取一个字符串，从而发生非法访问。
```c
void Foo(void)
{
    const char *infoMsg = "Information seed to user.";
    int infoLevel = 3;

    ...

    printf("infoLevel: %s, infoMsg: %d\n", infoLevel, infoMsg);

    ...
}
```

**【正例】**
正确的做法是确保printf()函数的实参匹配format的转换指示符。
```c
void Foo(void)
{
    const char *infoMsg = "Information seed to user.";
    int infoLevel = 3;

    ...

    printf("infoLevel: %d, infoMsg: %s\n", infoLevel, infoMsg);

    ...
}
```

**【影响】**

错误的格式串可能造成内存破坏或者程序异常终止。




### 2.14.2 退出类函数




#### FUU.0.3 禁用atexit函数

**【描述】**
atexit函数使用有严格限制：在一个程序中最多只能注册32个例程；例程必须通过return返回，不允许调用退出函数（如exit()）或调用longjmp()等方式返回，否则例程可能得不到正确执行，还会造成程序产生未定义行为。同时对于所有的退出处理程序来说，程序员应该主动清理不再使用的资源，而不应该在最终程序退出后通过使用atexit函数事先注册的例程被动地清理资源。

**【反例】**
在如下代码示例中，ProcessExit()函数由atexit()事先注册，在程序终止时执行必要的资源清理操作。但是如果g_someResource条件为真，则exit()被第二次调用，造成程序产生未定义行为。

```c
...
int g_someResource = 1;

void ProcessExit(void)
{
    if (g_someResource == 0) {
        ... // g_someResource，在这里清理程序资源，代码省略

        exit(0); // 不符合：在本例程中调用exit，导致程序产生未定义行为
    }

    return;
}

int main(void)
{
    // 不符合：注册atexit()例程ProcessExit()，清理资源
    if (atexit(ProcessExit) != 0) {
        ... // 错误处理
    }

    ...

    // main函数退出
    return 0;
}
```

**【正例】**
重构代码，禁止使用atexit()函数

```c
...
void ProcessExit(void)
{
    if (g_someResource == 0) {
        ... // g_someResource，在这里清理程序资源，代码省略
    }

    return;
}

int main(void)
{
    ...

    // main函数退出
    ProcessExit(); // 符合：主动调用资源清理函数
    return 0;
}
```

**【例外】**

作为服务维测监控功能，为定位程序异常退出原因的模块，可以作为例外使用atexit()函数。

**【影响】**

在程序调用\_Exit()、\_exit()、quick_exit()等函数退出时，atexit()注册的函数得不到执行，产生非预期的结果。




#### FUU.0.4 禁止调用kill、TerminateProcess函数直接终止其他进程

**【描述】**
调用kill、TerminateProcess等函数直接强行终止其他进程(如kill -SIGKILL，kill -SIGSTOP)，会导致被终止的进程中的资源得不到清理。

进程终止时，进程特有的资源将由系统自动释放，而其他资源(尤其是不属于进程的系统资源)在程序退出前难以得到有效地清理。

对于进程/线程间通信，应该主动发送一个停止命令，通知对方安全退出。接收到停止命令的进程应尽快完成进程资源和不再使用的系统资源的清理和释放。

当发送给对方进程/线程退出信号后，在等待一定时间内如果对方仍然未退出，可以调用kill、TerminateProcess函数强行终止目标进程。

**【反例】**
```c
if (isFatalStatus) {

    ...

    kill(pid, SIGKILL); // 不符合：直接调用kill强行结束目标进程
}
```

**【正例】**
正确的做法是通知对方进程停止，在等待一定时间内如果对方仍然未退出，再强行终止目标进程。

```c
if (isFatalStatus) {

    ...

    kill(pid, SIGUSR1); // 符合：目标进程将SIGUSR1定义为停止命令

    ...

    if (WaitForRemoteProcessExit() == TIME_OUT) {
        kill(pid, SIGKILL); // 目标进程在限定时间内仍然未退出，强行结束目标进程
    }
}
```

**【影响】**

强行终止程序，会导致被终止的程序中的资源得不到清理。





### 2.14.3 安全函数

**一、安全函数设计初衷**

安全函数的设计初衷是为了帮助程序员在编写代码时增加安全意识，在编程过程中时刻保持将外部数据当作不可信数据的思想，小心谨慎地处理外部的数据，并且在万一传入不正确的参数的情况下清空destBuff，安全退出，降低程序被进一步攻击的风险。
要正确用好安全函数，发挥安全函数的价值，必须比使用原有的memcpy等不安全函数更加谨慎，在对参数的使用上应该更加严格。

安全函数引入destMax的目的，是为了让程序员非常清晰地知道当前destBuff的大小，以免destBuff写溢出，导致程序出现安全问题。

安全函数的返回值是errno_t错误码。如果安全函数返回失败，很可能是程序受到了攻击，因此需要对安全函数的返回结果进行判断，对返回的错误值进行相应的处理。

安全函数必须正确使用，不正确的使用方法无法发挥出安全函数的价值。正确使用安全函数有助于提升代码的安全性，包括正确指定安全函数的参数，处理返回值等。

例如：memcpy_s函数的destMax参数大小必须与dest实际大小保持一致，count参数不能大于源缓冲区的实际长度。

**二、使用前提**

安全函数的使用前提：srcBuffer/count或者destBuffer/destMax是一段合法的内存空间。
    合法的内存空间是指：
    （1）堆
    （2）栈
    （3）程序静态数据区
    （4）mmap分配出来的内存页
对于不属于合法内存空间范围内的内存，例如已释放的堆内存、不可访问的内存、跨越未映射内存页的内存等等，安全函数不对合法性进行检查，在执行过程中，安全函数内部本身执行过程可能会出错。




#### FUU.0.5 必须检查安全函数返回值，并进行正确的处理

**【描述】**
原则上，如果使用了安全函数，需要进行返回值检查。如果返回值表示错误，那么本函数一般情况下应该立即返回，不能继续执行。

安全函数有多个错误返回值，如果安全函数返回失败，在本函数返回前，根据产品具体场景的不同，执行以下一个或多个措施：

- 记录日志
- 返回错误
- 调用abort立即退出程序

**【正例】**

```c
bool ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...
    if (destBuff == NULL || destMax == 0) {
        return false; // 返回失败
    }
    errno_t ret = memcpy_s(destBuff, destMax, src, srcLen);
    if (ret != EOK) {
        Log("memcpy_s failed, err = %d\n", err);
        return false; // 返回失败
    }
    ...
    return true;
}
```

**【例外1】**

[禁止使用内存操作类不安全函数](G.FUU.21_禁止使用内存操作类不安全函数.md) 中的例外场景中描述了允许继续使用不安全函数的场景，场景(1)-(5)对应的代码如果使用了安全函数，可以不进行返回值检查。

**【例外2】**

在安全函数返回值检查错误处理代码中，如果又调用了安全函数，可以不进行返回值检查。

例如，在以下代码中，调用strcpy_s失败后，错误处理代码试图记录日志，在错误处理代码内又调用了sprintf_s安全函数，此时不需要进行返回值检查。（程序员需要仔细检查该语句不会产生安全问题）

```c
errno_t ret = strcpy_s(dest, sizeof(dest), src);
if (ret != EOK) {
    char buff[MAX_BUFF];
    sprintf_s(buff, sizeof(buff), ...);
    Log(buff);
    return -1;
}
...
```

**【影响】**

忽略检查安全函数返回值，可能会导致程序执行了错误流程以及处理了错误的数据。





#### FUU.0.6 正确设置安全函数中的destMax参数

**【描述】**
安全函数的destMax参数设置应当准确，有效。

**【反例】**

以下代码，destBuff跨越到不可访问内存，属于误用：
```c
#define BUFF_SIZE 100
...
char destBuff[BUFF_SIZE];
char *src = ...
size_t srcLen = ...
memcpy_s(destBuff, 0x7fffffff, src, srcLen); // 不符合
```

**destMax参数设置原则**

（为聚焦于说明destMax的用法，示例代码中省略了安全函数的返回值检查以及其他检查）

**1. destBuff 为 char destBuff[BUFF_SIZE] 形式的局部变量的情况**

**1.1 使用时，destMax必须设置为 sizeof(destBuff) 或 BUFF_SIZE**

**【反例】**

```c
#define BUFF_SIZE 100
...
char destBuff[BUFF_SIZE];
char *src = ...
size_t srcLen = ...
...
memcpy_s(destBuff, 100, src, srcLen);       // 不符合
memcpy_s(destBuff, srcLen, src, srcLen);    // 不符合
```

**【正例】**

```c
#define BUFF_SIZE 100
...
char destBuff[BUFF_SIZE];
char *src = ...
size_t srcLen = ...
char strDest[BUFF_SIZE];
...
memcpy_s(destBuff, sizeof(destBuff), src, srcLen);   // 符合
memcpy_s(destBuff, BUFF_SIZE, src, srcLen);          // 符合
sprintf_s(strDest, sizeof(strDest), "Hello, world"); // 符合
...
memset_s(strDest, BUFF_SIZE, 0, BUFF_SIZE);          // 符合
scanf_s("%s", strDest, sizeof(strDest));             // 符合
```

**1.2 如果 destBuff 作为参数跨函数传递，必须将 destBuff 的实际大小作为参数进行传递**

**【反例】**

```c
#define BUFF_SIZE 100

int Foo(void)
{
    char destBuff[BUFF_SIZE];
    ...
    ParseBuff(destBuff, 100);   // 不符合
    ParseBuff2(destBuff);       // 不符合：必须增加destMax参数
    ...
}

int ParseBuff(char *destBuff, size_t destMax)
{
    char *src = ...
    size_t srcLen = ...

    memcpy_s(destBuff, BUFF_SIZE, src, srcLen);        // 不符合
    memcpy_s(destBuff, sizeof(destBuff), src, srcLen); // 不符合
    memcpy_s(destBuff, 100, src, srcLen);              // 不符合
    memcpy_s(destBuff, srcLen, src, srcLen);           // 不符合
    ...
}
```

**【正例】**

```c
#define BUFF_SIZE 100

int Foo(void)
{
    char destBuff[BUFF_SIZE];
    ...
    ParseBuff(destBuff, BUFF_SIZE); // 符合：传递BUFF_SIZE
    ...
}

int ParseBuff(char *destBuff, size_t destMax)
{
    char *src = ...
    size_t srcLen = ...
    memcpy_s(destBuff, destMax, src, srcLen);   // 符合
    ...
}
```

**2. destBuff为动态分配的堆内存的情况**

使用时，destMax应设置为当初分配时的内存大小

**【反例】**

```c
#define BUFF_SIZE 100
...
unsigned char *destBuff = (unsigned char *)malloc(BUFF_SIZE);
if (destBuff == NULL) {
    ... // 错误处理
}
...
unsigned char *src = ...
size_t srcLen = ...

memcpy_s(destBuff, 100, src, srcLen);       // 不符合
memcpy_s(destBuff, srcLen, src, srcLen);    // 不符合
```

**【正例】**

```c
#define BUFF_SIZE 100
...
unsigned char *destBuff = (unsigned char *)malloc(BUFF_SIZE);
if (destBuff == NULL) {
    ... // 错误处理
}
...
unsigned char *src = ...
size_t srcLen = ...

memcpy_s(destBuff, BUFF_SIZE, src, srcLen); // 符合
```

**2.1 如果 destBuff 的大小通过动态计算获得**

**【反例】**

```c
...
size_t destMax = ...
...
if (destMax > BUFF_SIZE) {
    ...
}
unsigned char *destBuff = (unsigned char *)malloc(destMax);
...
unsigned char *src = ...
size_t srcLen = ...

memcpy_s(destBuff, srcLen, src, srcLen);  // 不符合
```

**【正例】**

```c
...
size_t destMax = ...
...
if (destMax > BUFF_SIZE) {
    ...
}
unsigned char *destBuff = (unsigned char *)malloc(destMax);
...
unsigned char *src = ...
size_t srcLen = ...

memcpy_s(destBuff, destMax, src, srcLen);   // 符合
```

**2.2 如果 destBuff 的大小与 srcLen 相同**

**【正例】**

```c
...
unsigned char *src = ...
size_t srcLen = ...
...
unsigned char *destBuff = (unsigned char *)malloc(srcLen);
if (destBuff == NULL) {
    ... // 错误处理
}
...
memcpy_s(destBuff, srcLen, src, srcLen);    // 符合
```

**2.3 如果 destBuff 作为参数跨函数传递，必须将 destBuff 的实际大小作为参数进行传递**

**【反例】**

```c
int Foo(void)
{
    ...
    size_t destMax = ...
    ...
    unsigned char *destBuff = (unsigned char *)malloc(destMax);
    if (destBuff == NULL) {
        ... // 错误处理
    }

    ParseBuff(destBuff);    // 不符合：未传递destBuff的大小
    ...
}

int ParseBuff(unsigned char *destBuff)
{
    unsigned char *src = ...
    size_t srcLen = ...
    
    memcpy_s(destBuff, srcLen, src, srcLen);  // 不符合
    ...
}
```

**【反例】**

```c
int Foo(void)
{
    ...
    size_t destMax = ...
    ...
    unsigned char *destBuff = (unsigned char *)malloc(destMax);
    if (destBuff == NULL) {
        ... // 错误处理
    }

    ParseBuff(destBuff, destMax);
    ...
}

int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...

    memcpy_s(destBuff, srcLen, src, srcLen);  // 不符合：未使用正确的destMax
    ...
}
```

**【正例】**

```c
int Foo(void)
{
    ...
    size_t destMax = ...
    ...
    unsigned char *destBuff = (unsigned char *)malloc(destMax);
    if (destBuff == NULL) {
        ... // 错误处理
    }

    ParseBuff(destBuff, destMax); // 符合
    ...
}

int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...
    
    memcpy_s(destBuff, destMax, src, srcLen); // 符合
    ...
}
```

**3. destBuff 为struct结构的局部变量的情况**

使用时，destMax必须设置为 sizeof(变量名称) 或 sizeof(结构名称)。

**【反例】**

```c
typedef struct {
    int a;
    int b;
    int c;
} SomeStru;
...
SomeStru destBuff;
unsigned char *src = ...
size_t srcLen = ...

memcpy_s(&destBuff, 12, src, srcLen);                // 不符合
memcpy_s(&destBuff, srcLen, src, srcLen);            // 不符合
```

**【正例】**

```c
typedef struct {
    int a;
    int b;
    int c;
} SomeStru;
...
SomeStru destBuff;
unsigned char *src = ...
size_t srcLen = ...

memcpy_s(&destBuff, sizeof(destBuff), src, srcLen);  // 符合
memcpy_s(&destBuff, sizeof(SomeStru), src, srcLen);  // 符合
```

**4. struct结构作为子函数参数的情况**

如果参数类型是结构体指针，可以不传递destMax参数，否则必须将destBuff的实际大小作为参数进行传递。

**【反例】**

```c
typedef struct {
    int a;
    int b;
    int c;
} SomeStru;
...
int Foo(void)
{
    SomeStru destBuff;

    ParseBuff((unsigned char *)&destBuff, 12);  // 不符合
    ParseBuff2((unsigned char *)&destBuff);     // 不符合，必须传递DestMax
    ParseBuff3(&destBuff);
}

int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...

    memcpy_s(destBuff, sizeof(destBuff), src, srcLen);  // 不符合
    memcpy_s(destBuff, sizeof(SomeStru), src, srcLen);  // 不符合
    memcpy_s(destBuff, 12, src, srcLen);                // 不符合
    memcpy_s(destBuff, srcLen, src, srcLen);            // 不符合
    ...
}

// 不符合：unsigned char *作为参数时，必须传递destMax
int ParseBuff2(unsigned char *destBuff)
{
    unsigned char *src = ...
    size_t srcLen = ...
    
    memcpy_s(destBuff, sizeof(destBuff), src, srcLen);  // 不符合
    memcpy_s(destBuff, sizeof(SomeStru), src, srcLen);  // 不符合
    memcpy_s(destBuff, 12, src, srcLen);                // 不符合
    memcpy_s(destBuff, srcLen, src, srcLen);            // 不符合
    ...
}

// 函数的参数类型是结构体指针
int ParseBuff3(SomeStru *destBuff)
{
    unsigned char *src = ...
    size_t srcLen = ...
    
    memcpy_s(destBuff, sizeof(destBuff), src, srcLen);  // 不符合
    memcpy_s(destBuff, 12, src, srcLen);                // 不符合
    memcpy_s(destBuff, srcLen, src, srcLen);            // 不符合
    ...
}
```

**【正例】**

```c
typedef struct {
    int a;
    int b;
    int c;
} SomeStru;
...
int Foo(void)
{
    SomeStru destBuff;

    ParseBuff((unsigned char *)&destBuff, sizeof(destBuff));  // 符合
    ParseBuff((unsigned char *)&destBuff, sizeof(SomeStru));  // 符合
    ParseBuff3(&destBuff);  // 符合：结构体指针作为函数参数时，不需要传递destMax
}

int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...
    
    memcpy_s(destBuff, destMax, src, srcLen);   // 符合
    ...
}

// 结构体指针作为函数参数时，不需要传递destMax
int ParseBuff3(SomeStru *destBuff)
{
    unsigned char *src = ...
    size_t srcLen = ...

    memcpy_s(destBuff, sizeof(SomeStru), src, srcLen);  // 符合
    ...
}
```

**5. struct结构数组作为子函数参数的情况**

如果参数类型是结构体指针，必须指定数组的数量，否则必须将destBuff的实际大小作为参数进行传递。

**【反例】**

```c
typedef struct {
    int a;
    int b;
    int c;
} SomeStru;
...
int Foo(void)
{
    size_t count = ...
    ...
    SomeStru *destBuff = (SomeStru *)malloc(sizeof(SomeStru) * count);
    if (destBuff == NULL) {
        ... // 错误处理
    }
    ...
    ParseBuff((unsigned char *)destBuff, sizeof(SomeStru) * count);
    ParseBuff2((unsigned char *)destBuff);  // 不符合
}

int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...

    memcpy_s(destBuff, srcLen, src, srcLen);  // 不符合
}

// 不符合：unsigned char *作为参数时，必须传递destMax
int ParseBuff2(unsigned char *destBuff)
{
    ...
}


```

**【正例】**

```c
typedef struct {
    int a;
    int b;
    int c;
} SomeStru;
...
int Foo(void)
{
    size_t count = ...
    ...
    SomeStru *destBuff = (SomeStru *)malloc(sizeof(SomeStru) * count);
    if (destBuff == NULL) {
        ... // 错误处理
    }
    ...
    ParseBuff((unsigned char *)destBuff, sizeof(SomeStru) * count); // 符合
    ParseBuff2(destBuff, count);    // 符合
}

// 符合：非结构体指针时，传递destBuff的实际大小
int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...
    
    memcpy_s(destBuff, destMax, src, srcLen); // 符合
}

// 符合：结构体指针时，必须传递结构体数组数量，如：此处count为SomeStru的数量
int ParseBuff2(SomeStru *destBuff, size_t count)
{
    unsigned char *src = ...
    size_t srcLen = ...
    ...
    memcpy_s(destBuff, sizeof(SomeStru) * count, src, srcLen); // 符合
}
```

**6. destBuff为struct结构中的成员变量的情况**

destMax必须设置为该成员变量的实际大小，而不是整个结构体大小。

**【反例】**

```c
#define BUFF_SIZE 100
typedef struct {
    int a;
    int b;
    int c;
    unsigned char buffer[BUFF_SIZE];
} SomeStru;
...

SomeStru destBuff;
unsigned char *src = ...
size_t srcLen = ...
memcpy_s(destBuff.buffer, sizeof(destBuff), src, srcLen);        // 不符合
memcpy_s(destBuff.buffer, 100, src, srcLen);                     // 不符合
memcpy_s(destBuff.buffer, srcLen, src, srcLen);                  // 不符合
```

**【正例】**

```c
#define BUFF_SIZE 100
typedef struct {
    int a;
    int b;
    int c;
    unsigned char buffer[BUFF_SIZE];
} SomeStru;
...

SomeStru destBuff;
unsigned char *src = ...
size_t srcLen = ...
memcpy_s(destBuff.buffer, sizeof(destBuff.buffer), src, srcLen); // 符合
memcpy_s(destBuff.buffer, BUFF_SIZE, src, srcLen);               // 符合
```

**7. destBuff为变长struct结构中的变长成员变量**

destMax必须设置为该成员变量的实际大小，结构体中必须有描述变长部分长度的成员变量。

**【反例】**

```c
typedef struct {
    int a;
    int b;
    int c;
    size_t buffLen;
    unsigned char buff[0];
} SomeStru;
...
size_t buffLen = ...
unsigned char *src = ...
size_t srcLen = ...
SomeStru *destBuff = (SomeStru *)malloc(sizeof(SomeStru) + buffLen);
...
destBuff->buffLen = buffLen;
...
memcpy_s(destBuff->buff, srcLen, src, srcLen);  // 不符合
```

**【正例】**

```c
typedef struct {
    int a;
    int b;
    int c;
    size_t buffLen;
    unsigned char buff[0];
} SomeStru;
...
size_t buffLen = ...
unsigned char *src = ...
size_t srcLen = ...
SomeStru *destBuff = (SomeStru *)malloc(sizeof(SomeStru) + buffLen);
...
destBuff->buffLen = buffLen;
...
memcpy_s(destBuff->buff, destBuff->buffLen, src, srcLen); // 符合
```

如果要将变长成员变量作为子函数的参数进行传递，必须将buffLen作为参数一起传递。具体用例“6. destBuff为struct结构中的成员变量的情况”。

**8. struct结构中的成员变量作为子函数参数的情况**

destMax必须设置为该成员变量的实际大小，而不是整个结构体大小。

**【反例】**

```c
#define BUFF_SIZE 100
typedef struct {
    int a;
    int b;
    int c;
    unsigned char buffer[BUFF_SIZE];
} SomeStru;

int Foo(void)
{
    ...
    SomeStru destBuff;

    ParseBuff(destBuff.buffer, sizeof(destBuff));   // 不符合：入参大小有误
    ParseBuff2(destBuff.buffer);    // 不符合：函数入参缺少buffer的实际大小
    ...
}

int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...

    memcpy_s(destBuff, BUFF_SIZE, src, srcLen);        // 不符合
    memcpy_s(destBuff, sizeof(SomeStru), src, srcLen); // 不符合
    memcpy_s(destBuff, srcLen, src, srcLen);           // 不符合
    ...
}

int ParseBuff2(unsigned char *destBuff)
{
    ...
}
```

**【正例】**

```c
#define BUFF_SIZE 100
typedef struct {
    int a;
    int b;
    int c;
    unsigned char buffer[BUFF_SIZE];
} SomeStru;

int Foo(void)
{
    ...
    SomeStru destBuff;
    ParseBuff(destBuff.buffer, BUFF_SIZE);  // 符合：入参是该成员变量的实际大小
    ParseBuff(destBuff.buffer, sizeof(destBuff.buffer)); // 符合
    ...
}

int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...
    memcpy_s(destBuff, destMax, src, srcLen);   // 符合
    ...
}
```

**9. struct结构中的struct结构成员变量作为子函数参数的情况**

destMax必须设置为该成员变量的实际大小，而不是整个结构体大小。以下面struct结构体为例：

```c
#define BUFF_SIZE 100
typedef struct {
    int a1;
    int b1;
    int c1;
} SomeStru1;

typedef struct {
    int a2;
    int b2;
    int c2;
} SomeStru2;

typedef struct {
    SomeStru1 s1;
    int a;
    int b;
    int c;
    unsigned char buffer[BUFF_SIZE];
    SomeStru2 s2;
} SomeStru;
```

**【反例】**

```c
int Foo(void)
{
    ...
    SomeStru destBuff;

    ParseBuff((unsigned char *)&destBuff.s2, sizeof(destBuff)); // 不符合：xx
    ParseBuff((unsigned char *)&destBuff.s1, sizeof(destBuff)); // 不符合：xx
    ...
}

int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...

    memcpy_s(destBuff, BUFF_SIZE, src, srcLen);         // 不符合：xx
    memcpy_s(destBuff, sizeof(SomeStru), src, srcLen);  // 不符合：xx
    memcpy_s(destBuff, srcLen, src, srcLen);            // 不符合：xx
}

int ParseBuff2(SomeStru2 *destBuff)
{
    unsigned char *src = ...
    size_t srcLen = ...

    memcpy_s(destBuff, srcLen, src, srcLen);    // 不符合：xx
}
```

**【正例】**

```c
int Foo(void)
{
    ...
    SomeStru destBuff;
    ParseBuff((unsigned char *)&destBuff.s2, sizeof(destBuff.s2)); // 符合
    ParseBuff((unsigned char *)&destBuff.s2, sizeof(SomeStru2));   // 符合
    ParseBuff2(&destBuff.s2);                                      // 符合
    ...
}

int ParseBuff(unsigned char *destBuff, size_t destMax)
{
    unsigned char *src = ...
    size_t srcLen = ...
    memcpy_s(destBuff, destMax, src, srcLen);   // 符合
    ...
}

int ParseBuff2(SomeStru2 *destBuff)
{
    unsigned char *src = ...
    size_t srcLen = ...
    memcpy_s(destBuff, sizeof(SomeStru2), src, srcLen); // 符合
    ...
}
```

**10.对destBuff的局部范围进行操作**

原则上，destMax必须设置为destBuff操作范围的内存大小，如果计算过程比较复杂，允许将destMax设置为destBuffer最初分配的大小，例如：

```c
...
int destMax = ...
...
if (destMax <= 0 || destMax > ...) {
    ...
}
// 以下代码分别将src1和src2复制到destBuff进行拼接
unsigned char *destBuff = (unsigned char *)malloc(destMax);
if (destBuff == NULL) {
    ...
}
...
unsigned char *src1 = ...
size_t srcLen1 = ...
unsigned char *src2 = ...
size_t srcLen2 = ...
...
// count为外部传入的src1中的整数元素最大个数
if (count > ...) {
    ...
}
size_t offset = sizeof(int) * count;
...
if (offset >= destMax) {
    ...
}
memcpy_s(destBuff, offset, src1, srcLen1);   // 符合
memcpy_s(destBuff, srcLen1, src1, srcLen1);  // 不符合
memcpy_s(destBuff + offset, destMax - offset, src2, srcLen2); // 符合
memcpy_s(destBuff + offset, srcLen2, src2, srcLen2);          // 不符合

// 将destMax设置为destBuffer最初分配的大小，不建议使用
memcpy_s(destBuff, destMax, src1, srcLen1);
```

**【影响】**

安全函数预防缓冲区溢出的前提是正确设置deatMax参数，如果该参数不正确，则可能导致缓冲区溢出，在某些情况下可以造成任意代码执行漏洞。





#### FUU.0.7 禁止封装安全函数

**【描述】**
保留所有安全检查和返回值信息的封装，不必要的增加了函数调用开销；对入参检查及返回值进行修改的封装，丢失了安全函数的部分安全特性。因此安全函数不允许进行封装。

以函数封装的形式重新封装安全函数或不安全函数时，忽略安全函数的destMax参数，或用count参数直接代替destMax参数，具有额外的安全风险。

**【反例】**
错误示例1：使用类似不安全函数的接口封装安全函数，destMax与count参数使用相同参数

```c
void *XXX_memcpy(void *dest, const void *src, size_t count)
{
    ...
    memcpy_s(dest,  count,  src, count);
    ...
}
```

错误示例2：使用类似安全函数的接口封装安全函数，调用安全函数时，忽略了destMax入参，调用安全函数时destMax与count参数使用相同参数。

```c
errno_t XXX_memcpy_s(void *dest, size_t destMax, const void *src, size_t count)
{
    ...
    memcpy_s(dest,  count,  src, count);
    ...
}
```

错误示例3：使用类似安全函数的名字的函数，但是参数与安全函数不同

```c
errno_t XXX_memcpy_s(void *dest, const void *src, size_t count)
{
    ...
}
```

错误示例4：使用类似安全函数的接口封装不安全函数，忽略了destMax参数

```c
errno_t XXX_memcpy_s(void *dest, size_t destmax, const void *src, size_t count)
{
    ...
    memcpy(dest, src, count);
    ...
}
```

错误示例5：用函数实现自定义不安全函数

```c
errno_t XXX_strncpy(char *dest, size_t destMax, const char *src)
{
    ...
}
```

**【影响】**

不正确的封装或自实现安全函数，使安全函数的安全增强功能丧失，可能导致缓冲区溢出，在某些情况下可以造成任意代码执行漏洞。





#### FUU.0.8 禁止用宏重命名安全函数

**【描述】**
使用宏重命名安全函数不利于静态代码扫描工具（非编译型）定制针对安全函数误用的规则，同时，由于命名风格多样，也不利于提示程序员函数的真实用途，容易造成对代码的误解及重命名安全函数的误用。重命名安全函数不会改变安全函数本身的检查能力。

错误示例1：代码中未直接调用安全函数，而是以宏的方式调用安全函数

```c
#define XXX_memcpy_s  memcpy_s
#define SEC_MEM_CPY   memcpy_s
#define XX_memset_s(dst, dstMax, val, n) memset_s((dst), (dstMax), (val), (n))
```

以宏的方式重定义安全函数时，忽略安全函数的destMax参数，或用count参数直接代替destMax参数，或者用不安全函数仿冒安全函数，这些编程方式具有额外的安全风险。

错误示例2：使用类似不安全函数接口的宏，重定义安全函数，destMax与count参数使用相同参数

```c
#define XXX_memcpy(dst, src, count) memcpy_s(dst, count, src, count)
```

错误示例3：使用类似安全函数接口的宏，重定义安全函数，destMax与count参数使用相同参数

```c
#define XXX_memcpy_s(dst, destMax, src, count) memcpy_s(dst, count, src, count)
```

错误示例4：使用类安全函数接口的宏，重定义不安全函数，忽略了destMax参数

```c
#define XXX_memcpy(dst, destMax, src, count) memcpy(dst, src, count)
```

错误示例5：使用类似安全函数的名字的宏或者函数，但是参数与安全函数不同

```c
#define XXX_memcpy_s(dst, src, count) ...
```

错误示例6：宏定义伪安全函数，名称为安全函数，对应的函数实际不是安全函数

```c
#define my_snprintf_s snprintf
```

错误示例7：用宏实现自定义不安全函数

```c
#define XXX_strncpy(dst, destMax, src) ...
```

**【影响】**

不正确的封装或自实现安全函数，使安全函数的安全增强功能丧失，可能导致缓冲区溢出，在某些情况下可以造成任意代码执行漏洞。





### 2.14.4 其他函数




#### FUU.09 禁止外部可控数据作为进程启动函数的参数

**【描述】**
本条款中进程启动函数包括system、popen、execl、execlp、execle、execv、execvp等。
system()、popen()等函数会创建一个新的进程，如果外部可控数据作为这些函数的参数，会导致注入漏洞。
使用execl()等函数执行新进程时，如果使用shell启动的新进程，则同样存在命令注入风险。
使用execlp()、execvp()、execvpe()函数依赖于系统的环境变量PATH来搜索程序路径，使用它们时应充分考虑外部环境变量的风险，或避免使用这些函数。
因此，总是优先考虑使用C标准函数实现需要的功能。如果确实需要使用这些函数，请使用白名单机制确保这些函数的参数不受任何外来数据的影响。 

**【反例】**
如下代码示例中，使用 system() 函数执行 cmd 命令串来自外部，攻击者可以执行任意命令：

```c
char *cmd = GetCmdFromRemote();
if (cmd == NULL) {
    ... // 处理错误
}
system(cmd);
```

如下代码示例中，使用 system() 函数执行 cmd 命令串的一部分来自外部，攻击者可能输入 'some dir;useradd xxx'字符串，创建一个xxx的用户：

```c
char cmd[MAX_LEN];
int ret = 0;
char *name = GetDirNameFromRemote();
if (name == NULL) {
    ... // 处理错误
}
...
ret = sprintf_s(cmd, sizeof(cmd), "ls %s", name)
...
system(cmd);
```

使用exec系列函数来避免命令注入时，注意exec系列函数中的path、file参数禁止使用命令解析器(如/bin/sh)。

```c
int execl(const char *path, const char *arg, ...);
int execlp(const char *file, const char *arg, ...);
int execle(const char *path, const char *arg, ...);
int execv(const char *path, char *const argv[]);
int execvp(const char *file, char *const argv[]);
int execvpe(const char *file, char *const argv[], char *const envp[]);
```

例如，禁止如下使用方式：

```c
char *cmd = GetDirNameFromRemote();
execl("/bin/sh", "sh", "-c", cmd, NULL);
```

**【反例】**  (使用库函数)

在Linux下的部分命令有对应的库函数，或者可以通过少量的编码来避免使用system函数调用命令，如mkdir()函数可以实现mkdir命令的功能。下面实现了一个文件内容拷贝的功能，不必要的通过system函数调用了系统 cat 命令。
```c
int WriteDataToFile(const char *dstFile, const char *srcFile)
{
    ...
    ...  // 入参的合法性检查
    ret = sprintf_s(buffer, bufLen, "cat %s > %s", context, filepath);
    if (ret < 0) {
        ...
    }
    system(buffer);
    ...
}
```

**【正例】**  (使用库函数)

一些命令功能可以通过少量的编码来实现。如下代码实现了文件拷贝的功能，避免了对 cat 或 cp 命令的调用。需要注意的是，为简化描述，下面代码未考虑信号中断的影响。

```c
#define OPEN_SRC_FILE_ERROR -1
#define OPEN_DST_FILE_ERROR -2
#define WRITE_DST_FILE_ERROR -3
#define READ_DST_FILE_ERROR -4

int WriteDataToFile(const char *dstFile, const char *srcFile)
{
    int ret = 0;
    ssize_t len = 0;
    unsigned char buf[MAX_BUF_SIZE];

    ... // 入参的合法性检查
    int sourceFile = open(srcFile, O_RDONLY);
    if (sourceFile < 0) {
        return OPEN_SRC_FILE_ERROR;
    }
    int destFile = open(dstFile,
                        O_CREAT | O_WRONLY | O_EXCL,
                        S_IRUSR | S_IWUSR);
    if (destFile <0) {
        ret = OPEN_DST_FILE_ERROR;
        goto EXIT2;
    }
    while ((len = read(sourceFile, buf, sizeof(buf))) > 0) {
        if (write(destFile, buf, (size_t)len) != len) {
            ret = WRITE_DST_FILE_ERROR;
            goto EXIT1;
        }
    }
    if (len < 0) {
        ret = READ_DST_FILE_ERROR;
    }
EXIT1:
    close(destFile);
EXIT2:
    close(sourceFile);
    return ret;
}
```

**【正例】**  (使用exec系列函数)
可以通过库函数简单实现的功能（如上例），需要避免调用命令处理器来执行外部命令。如果确实需要调用单个命令，应使用exec*函数来实现参数化调用，并对调用的命令实施白名单管理。应避免使用execlp、execvp、execvpe函数。

```c
pid_t pid;
char * const envp[] = { NULL };
...
char *filename = GetDirNameFromRemote();
if (filename == NULL) {
    ... // 处理错误
}
...
if ((pid = fork()) < 0) {
    ...
} else if (pid == 0) {
    // 使用some_tool对指定文件进行加工
    execle("/bin/some_tool", "some_tool", filename, NULL, envp);
    _Exit(-1);
}
...
int status;
waitpid(pid, &status, 0);
FILE *fp = fopen(filename, "r");
...
```
此时，外部输入的filename仅作为some_tool命令的参数，没有命令注入的风险。

**【正例】**  (使用白名单)

对输入的文件名基于合理的白名单检查，避免命令注入。
```c
char *cmd = GetCmdFromRemote();
if (cmd == NULL) {
    ... // 处理错误
}

// 使用白名单检查命令是否合法，仅允许"some_tool_a", "some_tool_b"命令，外部无法随意控制
if (!IsValidCmd(cmd)) {
    ... // 处理错误
}
system(cmd);
...
```

**【影响】**

如果传递给system()、popen()或其他命令处理器函数的命令字符串是外部可控的，则攻击者可能会以被攻击进程的权限执行系统上存在的任意命令。


**【相关软件CWE编号】**  CWE-676，CWE-88




#### FUU.10 禁止外部可控数据作为dlopen等模块加载函数的参数

**【建议】**
建议使用pg_dlopen代替dlopen。

**【描述】**
这些函数会加载外部模块，如果外部可控数据作为这些函数的参数，有可能会加载攻击者事先预制的模块。

如果要使用这些函数，可以采用如下措施之一：
- 使用白名单机制，确保这些函数的参数不受任何外来数据的影响；
- 使用数字签名机制保护要加载的模块，充分保证其完整性；
- 在设备本地加载的动态库通过权限与访问控制措施保证了本身安全性后，通过特定目录自动被程序加载；
- 在设备本地的配置文件通过权限与访问控制措施保证了本身安全性后，自动加载配置文件中指定的动态库。

**【反例】**
以下代码从外部获取数据后直接作为LoadLibrary函数的参数，有可能导致程序被植入木马。

```c
char *msg = GetMsgFromRemote();
LoadLibrary(msg);
```

**【影响】**

如果动态库文件是外部可控的，则攻击者可替换该库文件，在某些情况下可以造成任意代码执行漏洞。





#### FUU.11 禁止直接使用外部数据拼接SQL命令

**【描述】**
SQL注入是指SQL查询被恶意更改成一个与程序预期完全不同的查询。执行更改后的查询可能会导致信息泄露或者数据被篡改。而SQL注入的根源就是使用外部数据来拼接SQL语句。C/C++语言中常见的使用外部数据拼接SQL语句的场景有（包括但不局限于）：

- 连接MySQL时调用mysql_query()，Execute()时的入参
- 连接SQL Server时调用db-library驱动的dbsqlexec()的入参
- 调用ODBC驱动的SQLprepare()连接数据库时的SQL语句的参数
- C++程序调用OTL类库中的otl_stream()，otl_column_desc()时的入参
- C++程序连接Oracle数据库时调用ExecuteWithResSQL()的入参

防止SQL注入的方法主要有以下几种：

- 参数化查询（通常也叫作预处理语句）：参数化查询是一种简单有效的防止SQL注入的查询方式，应该被优先考虑使用。支持的数据库有MySQL，Oracle（OCI）。
- 参数化查询（通过ODBC驱动）：支持ODBC驱动参数化查询的数据库有Oracle、SQLServer、PostgreSQL和GaussDB。
- 对外部数据进行校验（对于每个引入的外部数据推荐“白名单”校验）。
- 对外部数据中的SQL特殊字符进行转义。

**【反例】**
下列代码拼接用户输入，没有进行输入检查，存在SQL注入风险：

```c
char name[NAME_MAX];
char sqlStatements[SQL_CMD_MAX];
int ret = GetUserInput(name, NAME_MAX);
...
ret = sprintf_s(sqlStatements,
                SQL_CMD_MAX,
                "SELECT childinfo FROM children WHERE name= ‘%s’",
                name);
...
ret = mysql_query(&myConnection, sqlStatements);
...
```

**【正例】**
使用预处理语句进行参数化查询可以防御SQL注入攻击：

```c
char name[NAME_MAX];
...
MYSQL_STMT *stmt = mysql_stmt_init(myConnection);
char *query = "SELECT childinfo FROM children WHERE name= ?";
if (mysql_stmt_prepare(stmt, query, strlen(query))) {
    ...
}
int ret = GetUserInput(name, NAME_MAX);
...
MYSQL_BIND params[1];
(void)memset_s(params, sizeof(params), 0, sizeof(params));
...
params[0].bufferType = MYSQL_TYPE_STRING;
params[0].buffer = (char *)name;
params[0].bufferLength = strlen(name);
params[0].isNull = 0;

bool isCompleted = mysql_stmt_bind_param(stmt, params);
...
ret = mysql_stmt_execute(stmt);
...
```

**【影响】**

如果拼接SQL语句的字符串是外部可控的，则攻击者可以通过注入特定的字符串欺骗程序执行恶意的SQL命令，造成信息泄露、权限绕过、数据被篡改等问题。





#### FUU.12 禁止在信号处理例程中调用非异步安全函数

**【描述】**
在信号处理程序中只调用异步安全函数：

> 如果信号是通过调用abort()或raise()函数产生的，则信号处理程序中不能调用raise()函数。
> 如果信号不是通过调用abort()或raise()函数产生的，则如下情况，程序的行为是未定义的：
> ...信号处理程序中调用了标准库中除abort()函数，_Exit()函数，quick_exit()函数、 signal()函数(其第一个参数等于触发信号处理程序的信号编号)之外的任何函数，...。

除了C语言标准函数以外，其他系统函数也提供了一些的异步安全函数，在信号处理程序中使用这些函数之前，应确保调用的函数在所有可能的执行环境下均是异步安全的。

**【反例】**
如下代码示例中，信号处理函数中调用了非异步安全函数printf()：

```c
void Handler(int num)
{
    printf("receive signal = %d\n", SIGINT);
}
int main(int argc, char **argv)
{
    if (signal(SIGINT, Handler) == SIG_ERR) {
        ... // 错误处理
    }
    while (true) {
        ... // 程序主循环代码
    }
    return 0;
}
```
**【正例】**
如下代码示例中，尽量不在信号处理函数中调用其他函数，仅在信号处理程序中修改volatile sig_atomic_t的变量：

```c
static volatile sig_atomic_t g_flag = 0;

void Handler(int num)
{
    g_flag = 1;
}

int main(int argc, char **argv)
{
    if (signal(SIGINT, Handler) == SIG_ERR) {
        ... // 错误处理
    }
    while (true) {
        if (g_flag != 0) {
            printf("receive signal = %d\n", SIGINT);
        }
        ... // 程序主循环代码
    }
    ...
    return 0;
}
```

**【影响】**

从信号处理函数中调用非异步信号安全函数会导致程序产生未定义行为。


**【相关软件CWE编号】** CWE-479




#### FUU.13 使用库函数时避免竞争条件

**【描述】**
C语言标准库中有一些函数是不可重入函数。不可重入函数在多线程环境下的执行结果可能不能达到预期效果，需谨慎使用。
例如strtok()和asctime()等函数对每个进程返回一个保存结果的指针，保存在函数分配的内存中。另外的一些函数（如rand()）会基于每个进程在该函数分配的内存中存储状态信息。多个线程调用相同函数可能造成条件竞争问题，这种问题常常导致异常行为，并且可能造成更严重的漏洞，例如异常终止、拒绝服务攻击、损害数据完整性。

下表中左列给出的库函数是不可重入的，在多线程中被调用时，可能存在条件竞争问题。

| 函数 | 安全措施 |
| :-- | :-- |
| rand(), srand() | 禁用rand函数产生用于安全用途的伪随机数 |
| getenv(), getenv_s() | 不要存储函数返回的指针 |
| strtok() | C11标准中的strtok_s()， POSIX中的strtok_r() |
| strerror() | C11标准中的strerror_s()，POSIX中的strerror_r() |
| asctime(), ctime(), localtime(), gmtime() | C11标准中的asctime_s(), ctime_s(), localtime_s(), gmtime_s() |
| setlocale() | 使用互斥方法保护区域特定API的多线程访问 |
| ATOMIC_VAR_INIT, atomic_init() | 不要试图从多个线程初始化一个原子变量 |
| tmpnam() | C11标准中的tmpnam_s()，POSIX中的tmpnam_r() |
| mbrtoc16(), c16rtomb(), mbrtoc32(), c32rtomb() | 调用时，参数mbstate_t *禁止为空 |

另外还需要注意的函数有：gethostbyaddr(), gethostbyname(), inet_ntoa(), localeconv()等。
localeconv()返回的结果必须视为const限定类型，或者返回的指针所指向对象状态需要立即使用，重复调用函数会导致保存的状态丢失。

**【反例】**
以下示例是期望通过getenv函数取到TABLE_WX_ENV和TABLE_BD_ENV两个环境变量的值，再判断这两个值是否相同。
但是由于getenv()是不可重入的，在第二次调用该函数时，可能会覆盖上一次取到的字符串内容，所以即使两个环境变量是不同的，但是最终两者wxEnv和bdEnv在比较时可能相同。

```c
void Foo(void)
{
    char *wxEnv = NULL;
    char *bdEnv = NULL;

    wxEnv = getenv("TABLE_WX_ENV");
    if (wxEnv == NULL) {
        ... // 错误处理
        return;
    }

    bdEnv = getenv("TABLE_BD_ENV");
    if (bdEnv == NULL) {
        ... // 错误处理
        return;
    }

    if (strcmp(wxEnv, bdEnv) == 0) {
        printf("They are the same.\n");
    } else {
        printf("They are NOT the same.\n");
    }
}
```

**【正例】**
如下代码示例中，先将取到的环境变量保存起来，然后再比较。

```c
// 函数是将srcEnv复制一份。成功返回复制之后的首地址，失败返回NULL
char *TransEnv(const char *srcEnv)
{
    ... // 具体实现略。strcpy_s...
}

void Function(void)
{
    char *wxEnv = NULL;
    char *bdEnv = NULL;

    const char *envVal = getenv("TABLE_WX_ENV");
    if (envVal != NULL) {
        wxEnv = TransEnv(envVal);
        ... // 判断TransEnv函数返回值并正确处理异常
    } else {
        ... // 错误处理
        return;
    }

    envVal = getenv("TABLE_BD_ENV");
    if (envVal != NULL) {
        bdEnv = TransEnv(envVal);
        ... // 判断TransEnv函数返回值并正确处理异常
    } else {
        ... // 错误处理
        return;
    }

    // 比较两个副本
    if (strcmp(wxEnv, bdEnv) == 0) {
        printf("They are the same.\n");
    } else {
        printf("They are NOT the same.\n");
    }

    ... // 退出前清理资源
}
```

**【影响】**

多线程调用同一个库函数引起的条件竞争可能导致应用程序异常终止、损害数据完整性或者造成拒绝服务。


**【相关软件CWE编号】** CWE-330，CWE-377，CWE-676




#### FUU.14 禁止使用内存操作类不安全函数

**【描述】**
C语言标准的许多函数，要求程序员提供足够大的数组（内存空间）以容纳函数产生的结果。但是根据历史漏洞分析，程序员在使用一些内存操作类函数时，容易因使用不当而造成缓冲区溢出等安全漏洞。因此本规范中禁止使用内存操作类不安全函数。为避免遗漏对不安全函数的检查，同时禁止封装这些不安全函数。

基于缓冲区溢出漏洞触发的历史情况分析并统计，发现有很大一部分缓冲区溢出漏洞是因为调用了这些内存操作类函数但未考虑目标缓冲区大小而导致的。

以下列出了部分内存操作类不安全函数：

- 内存拷贝函数：memcpy(), wmemcpy(), memmove(), wmemmove()
- 内存初始化函数：memset()
- 字符串拷贝函数：strcpy(), wcscpy(), strncpy(), wcsncpy()
- 字符串拼接函数：strcat(), wcscat(), strncat(), wcsncat()
- 字符串格式化输出函数：sprintf(), swprintf(), vsprintf(), vswprintf(), snprintf(), vsnprintf()
- 字符串格式化输入函数：scanf(), wscanf(), vscanf(), vwscanf(), fscanf(), fwscanf(), vfscanf(), vfwscanf(), sscanf(), swscanf(), vsscanf(), vswscanf()
- stdin流输入函数：gets()

**【例外】**

在下列情况下，由于未涉及到外部数据处理，不存在被攻击的场景，内存操作完全在本函数内完成，不存在因外部控制而失败的可能性，可以保留使用不安全函数：

（1）对固定长度的数组进行初始化，或对固定长度的结构体进行内存初始化：

```c
unsigned char g_array[ARRAY_SIZE];
void Foo(void)
{
    char destBuff[BUFF_SIZE];
    ...
    memset(g_array, c1, sizeof(g_array));   // 对全局固定长度的数据赋值
    ...
    memset(destBuff, c2, sizeof(destBuff)); // 对局部固定长度的数据赋值
    ...
}
```

```c
typedef struct {
    int type;
    int data;
} Tag;

Tag g_tag = {1, 2};

void Foo(void)
{
    Tag dest;
    ...
    // 对固定长度结构体赋值
    memcpy(&dest, &g_tag, sizeof(Tag));
    ...
}
```

（2）函数参数中有指向内存的指针参数和对应的内存大小的参数时，对该内存进行初始化：

```c
void Foo(unsigned char *buff1, size_t len1, unsigned char *buff2, size_t len2)
{
    ...
    memset(buff1, 0, len1); // 对buff1清0
    memset(buff2, 0, len2); // 对buff2清0
    ...
}
```

（3）从堆中分配内存后，赋予初值：

```c
size_t len = ...
char *str = (char *)malloc(len);
if (str != NULL) {
    memset(str, 0, len);
    ...
}
```

（4）根据源内存的大小进行同等大小的内存复制：

以下代码基于srcSize分配了一块相同大小的内存，并复制过去：

```c
unsigned char *src = ...
size_t srcSize = ...
unsigned char *destBuff = malloc(srcSize);

if (destBuff == NULL) {
    ... // 错误处理
}
memcpy(destBuff, src, srcSize);
```

以下代码根据源字符串的大小分配一块相同的内存，并复制过去：

```c
char *src = ...
size_t len = strlen(src);
if (len > BUFF_SIZE) {
    ...
}
char *destBuff = malloc(len + 1);
if (destBuff == NULL) {
    ... // 错误处理
}
strcpy(destBuff, src);
```

（5）源内存全部是静态字符串常量（编写代码时需要检查目标内存是否足够的存储空间）：

以下代码直接将字符串常量“hello”复制到数组中：

```c
char destBuff[BUFF_SIZE];
strcpy(destBuff, "hello");
```

以下代码对静态字符串常量进行拼接：

```c
const char *g_List[] = {"red", "green", "blue"};
char destBuff[BUFF_SIZE];
sprintf(destBuff, "hello %s", g_List[i]);
```

**【影响】**

使用内存操作类的标准库函数时，易受常见编程错误的影响，经常出现缓冲区溢出问题，可能导致严重的可利用漏洞。




## 2.15 文件

自UNIX开始引入文件等概念后，输入输出操作可以独立于具体设备进行。输入输出模型的细节被隐藏在文件结构之下。因此，不应当访问FILE指针的成员，C语言标准还禁止复制文件对象。

在并发系统上访问文件可能存在竞争问题。访问文件时，应尽量避免条件竞争。




### FIL.01 创建文件时必须显式指定合适的文件访问权限

**【描述】**
创建文件时，如果不显式指定合适访问权限，可能会让未经授权的用户访问该文件，造成信息泄露，文件数据被篡改，文件中被注入恶意代码等风险。

虽然文件的访问权限也依赖于文件系统，但是当前许多文件创建函数（例如POSIX open函数）都具有设置（或影响）文件访问权限的功能，所以当使用这些函数创建文件时，必须显式指定合适的文件访问权限，以防止意外访问。

**【反例】**
使用POSIX open()函数创建文件但未显示指定该文件的访问权限，可能会导致文件创建时具有过高的访问权限。这可能会导致漏洞（例如CVE-2006-1174）。

```c
void Foo(void)
{
    int fd = -1;
    char *filename = NULL;

    ... // 初始化 filename

    fd = open(filename, O_CREAT | O_WRONLY); // 没有显式指定访问权限
    if (fd == -1) {
        ... // 错误处理
    }
    ...
}
```

**【正例】**
应该在open的第三个参数中显式指定新创建文件的访问权限。可以根据文件实际的应用情况设置何种访问权限。

```c
void Foo(void)
{
    int fd = -1;
    char *filename = NULL;

    ... // 初始化 filename 和指定其访问权限

    // 此处根据文件实际需要，显式指定其访问权限
    int fd = open(filename, O_CREAT | O_WRONLY, S_IRUSR | S_IWUSR);
    if (fd == -1) {
        ... // 错误处理
    }
    ...
}
```

**【影响】**

创建访问权限弱的文件，可能会导致对这些文件的非法访问。





### FIL.02 使用文件路径前必须进行规范化并校验

**【描述】**
当文件路径来自外部数据时，必须对其做合法性校验，如果不校验，可能造成系统文件的被任意访问。但是禁止直接对其进行校验，正确做法是在校验之前必须对其进行路径规范化处理。这是因为同一个文件可以通过多种形式的路径来描述和引用，例如既可以是绝对路径，也可以是相对路径；而且路径名、目录名和文件名可能包含使校验变得困难和不准确的字符（如：“.”、“..”）。此外，文件还可以是符号链接，这进一步模糊了文件的实际位置或标识，增加了校验的难度和校验准确性。所以必须先将文件路径规范化，从而更容易校验其路径、目录或文件名，增加校验准确性。

因为规范化机制在不同的操作系统和文件系统之间可能有所不同，所以最好使用符合当前系统特性的规范化机制。例如：在linux下，使用realpath函数，在windows下，使用PathCanonicalize函数进行文件路径的规范化。

一个简单的案例说明如下：

```c
当文件路径来自外部数据时，需要先将文件路径规范化，如果没有作规范化处理，攻击者就有机会通过恶意构造文件路径进行文件的越权访问。
例如，攻击者可以构造“../../../etc/passwd”的方式进行任意文件访问。
```

**【反例】**
在此错误的示例中，inputFilename包含一个源于受污染源的文件名，并且该文件名已打开以进行写入。在使用此文件名操作之前，应该对其进行验证，以确保它引用的是预期的有效文件。
不幸的是，inputFilename引用的文件名可能包含特殊字符，例如目录字符，这使验证变得困难，甚至不可能。而且，inputFilename中可能包含可以指向任意文件路径的符号链接，即使该文件名通过了验证，也会导致该文件名是无效的。
这种场景下，对文件名的直接验证即使被执行也是得不到预期的结果，对fopen()的调用可能会导致访问一个意外的文件。

```c
...

if (!verify_file(inputFilename) {    // 没有对inputFilename做规范化，直接做校验
    ... // 错误处理
}

if (fopen(inputFilename, "w") == NULL) {
    ... // 错误处理
}

...
```

**【正例】**
规范化文件名是具有一定难度的，因为这需要了解底层文件系统。
POSIX realpath()函数可以帮助将路径名转换为规范形式。
- 该realpath()函数应从所指向的路径名派生一个filename的绝对路径名，两者指向同一文件，绝对路径其文件名不涉及“ .”，“ ..”或符号链接。
在规范化路径之后，还必须执行进一步的验证，例如确保两个连续的斜杠或特殊文件不会出现在文件名中。有关如何执行路径名解析的更多详细信息。
使用realpath()函数有许多需要注意的地方，详细可以翻看Linux程序员手册。
在了解了以上原理之后，对上面的错误代码示例，我们采用如下解决方案：

```c
char *realpathRes = NULL;

...

// 在校验之前，先对inputFilename做规范化处理
realpathRes = realpath(inputFilename, NULL);
if (realpathRes == NULL) {
    ... // 规范化的错误处理
}

// 规范化以后对路径进行校验
if (!verify_file(realpathRes) {
    ... // 校验的错误处理
}

// 使用
if (fopen(realpathRes, "w") == NULL) {
    ... // 实际操作的错误处理
}

...

free(realpathRes);
realpathRes = NULL;
...
```

**【正例】**
根据我们的实际场景，我们还可以采用的第二套解决方案，说明如下：
如果`PATH_MAX`被定义为 limits.h 中的一个常量，那么使用非空的`resolved_path`调用realpath()也是安全的。
在本例中realpath()函数期望`resolved_path`引用一个字符数组，该字符数组足够大，可以容纳规范化的路径。
如果定义了PATH_MAX，则分配一个大小为`PATH_MAX`的缓冲区来保存realpath()的结果。正确代码示例如下：

```c
char *realpathRes = NULL;
char *canonicalFilename = NULL;
size_t pathSize = 0;

...

pathSize = (size_t)PATH_MAX;

if (VerifyPathSize(pathSize) == true) {
    canonicalFilename = (char *)malloc(pathSize);

    if (canonicalFilename == NULL) {
        ... // 错误处理
    }

    realpathRes = realpath(inputFilename, canonicalFilename);
}

if (realpathRes == NULL) {
    ... // 错误处理
}

if (VerifyFile(realpathRes) == false) {
    ... // 错误处理
}

if (fopen(realpathRes, "w") == NULL ) {
    ... // 错误处理
}

...

free(canonicalFilename);
canonicalFilename = NULL;
...
```

**【反例】**
下面的代码场景是从外部获取到文件名称，拼接成文件路径后，直接对文件内容进行读取，导致攻击者可以读取到任意文件的内容：

```c
char *filename = GetMsgFromRemote();
...
int ret = sprintf_s(untrustPath, sizeof(untrustPath), "/tmp/%s", filename);
...
char *text = ReadFileContent(untrustPath);
```

**【正例】**
正确的做法是，对路径进行规范化后，再判断路径是否是本程序所认为的合法的路径：

```c
char *filename = GetMsgFromRemote();
...
sprintf_s(untrustPath, sizeof(untrustPath), "/tmp/%s", filename);
char path[PATH_MAX];
if (realpath(untrustPath, path) == NULL) {
    ... // 处理错误
}
if (!IsValidPath(path)) {    // 检查文件的位置是否正确
    ... // 处理错误
}
char *text = ReadFileContent(path);
```

**【例外】**

运行于控制台的命令行程序，通过控制台手工输入文件路径，可以作为本条款例外。

```c
int main(int argc, char **argv)
{
    int fd = -1;

    if (argc == 2) {
        fd = open(argv[1], O_RDONLY);
        ...
    }

    ...
    return 0;
}

```

**【影响】**

未对不可信的文件路径进行规范化和校验，可能造成对任意文件的访问。




### FIL.03 不要在共享目录中创建临时文件

**【描述】**
共享目录是指其它非特权用户可以访问的目录。程序的临时文件应当是程序自身独享的，任何将自身临时文件置于共享目录的做法，将导致其他共享用户获得该程序的额外信息，产生信息泄露。因此，不要在任何共享目录创建仅由程序自身使用的临时文件。

临时文件通常用于辅助保存不能驻留在内存中的数据或存储临时的数据，也可用作进程间通信的一种手段（通过文件系统传输数据）。例如，一个进程在共享目录中创建一个临时文件，该文件名可能使用了众所周知的名称或者一个临时的名称，然后就可以通过该文件在进程间共享信息。这种通过在共享目录中创建临时文件的方法实现进程间共享的做法很危险，因为共享目录中的这些文件很容易被攻击者劫持或操纵。这里有几种缓解策略：

1. 使用其他低级IPC（进程间通信）机制，例如套接字或共享内存。
2. 使用更高级别的IPC机制，例如远程过程调用。
3. 使用仅能由程序本身访问的安全目录(多线程/进程下注意防止条件竞争)。

同时，下面列出了几项临时文件创建使用的方法，产品根据具体场景执行以下一项或者几项，同时产品也可以自定义合适的方法。

1. 文件必须具有合适的权限，只有符合权限的用户才能访问
2. 创建的文件名是唯一的、或不可预测的
3. 仅当文件不存在时才创建打开(原子创建打开)
4. 使用独占访问打开，避免竞争条件
5. 在程序退出之前移除

同时也需要注意到，当某个目录被开放读/写权限给多个用户或者一组用户时，该共享目录潜在的安全风险远远大于访问该目录中临时文件这个功能的本身。

在共享目录中创建临时文件很容易受到威胁。例如，用于本地挂载的文件系统的代码在与远程挂载的文件系统一起共享使用时可能会受到攻击。安全的解决方案是不要在共享目录中创建临时文件。

**【反例】**
如下代码示例，程序在Linux系统的共享目录/tmp下创建临时文件来保存临时数据，且文件名是硬编码的。
由于文件名是硬编码的，因此是可预测的，攻击者只需用符号链接替换文件，然后链接所引用的目标文件就会被打开并写入新内容。

```c
void ProcData(const char *filename)
{
    FILE *fp = fopen(filename, "wb+");
    if (fp == NULL) {
        ... // 错误处理
    }

    ... // 写文件

    fclose(fp);
}

int main(void)
{
    // 不符合：1.在系统共享目录中创建临时文件；2.临时文件名硬编码
    char *pFile = "/tmp/data";
    ...

    ProcData(pFile);

    ...
    return 0;
}
```

**【正确案例】**
```c
Linux下的/tmp目录是一个所有用户都可以访问的共享目录，不应在该目录下创建仅由程序自身使用的临时文件。
```

**【影响】**

不安全的创建临时文件，可能导致文件非法访问，并造成本地系统上的权限提升。


**【业界典型漏洞】**CVE-2004-2502





## 2.16 内存




### MEM.01 禁止直接使用malloc申请内存，所以内存申请都需要通过palloc接口从内存上下文申请（工具除外）

**【正例】**
```c
char* Buffer = (char*)palloc(BUFFER_SIZE);
```

**【反例】**
```c
char* Buffer = (char*)malloc(BUFFER_SIZE);
```


### MEM.02 使用palloc申请内存时，确认通过MemoryContextSwitchTo切换到正确的内存上下文

**【正例】**
```c
MemoryContext oldContext = MemoryContextSwitchTo(u_sess->cache_mem_cxt);
char* Buffer = (char*)palloc(BUFFER_SIZE);
...
(void)MemoryContextSwitchTo(oldContext);
```




### MEM.03 禁止直接从头TopMemoryContext（g_instance.instance_context，t_thrd.top_mem_cxt，u_sess->top_mem_cxt）上申请内存

**【反例】**
```c
MemoryContext oldContext = MemoryContextSwitchTo(u_sess->top_mem_cxt);
char* Buffer = (char*)palloc(BUFFER_SIZE);
...
(void)MemoryContextSwitchTo(oldContext);
```


### MEM.04 通过palloc申请的连续内存不能大于1GB，若超过1GB，请使用palloc_huge接口申请内存

**【正例】**
```c
g_instance.ckpt_cxt_ctl->dirty_page_queue = (DirtyPageQueueSlot *)palloc_huge(CurrentMemoryContext, queue_mem_size);
```


### MEM.05 u_sess->top_mem_cxt及其子内存上下文上申请的内存，禁止通过t_thrd下的变量引用

**【反例】**
```c
MemoryContext oldContext = MemoryContextSwitchTo(u_sess->cache_mem_cxt);
t_thrd.log_cxt.plog_md_read_entry = (char*)palloc0(PLOG_ENTRY_MAX_SIZE);
...
(void)MemoryContextSwitchTo(oldContext);
```



### MEM.06 t_thrd.top_mem_cxt及其子内存上下文上申请的内存，禁止通过u_sess下的变量引用

**【反例】**
```c
u_sess->storage_cxt.LocalBufferDescriptors = (BufferDesc*)MemoryContextAllocZero(THREAD_GET_MEM_CXT_GROUP(MEMORY_CONTEXT_STORAGE), (unsigned int)nbufs * sizeof(BufferDesc));
```


### MEM.07 申请的内存需要通过pfree，MemoryContextDelete，MemoryContextReset接口及时释放

**【正例】**
```c
MemoryContext oldContext = MemoryContextSwitchTo(u_sess->cache_mem_cxt);
char* Buffer = (char*)palloc(BUFFER_SIZE);
...
(void)MemoryContextSwitchTo(oldContext);
...
pfree(Buffer);
//or
MemoryContextDelete(top_transaction_mem_cxt);
```



### MEM.08 如果需要使用类，需要继承BaseObject类，创建对象是通过接口 New(ContextName) ClassName(..)

**【正例】**
```c
New(ContextName) ClassName(..)
class ThreadPoolListener : public BaseObject {
...
}
m_listener = New(CurrentMemoryContext) ThreadPoolListener(this);
...
delete m_listener;
```



## 2.17 C++使用规范




### C++.01 推荐使用的C++特性：类、继承、模板、虚函数除此而之外的特性如果使用需要评估风险，并由commiter同意后方可使用。





### C++.02 绝对禁止的C++特性：智能指针、STL模板库这些特性涉及内存分配和释放，与GaussDB Kernel内存管理机制冲突，如果使用会引发内存问题，所以禁止使用。





### C++.03 C++风格结构体vs类仅当只有数据成员时必须使用struct结构体，class仅在数据成员存在函数时并且包含明显的层次关系时才允许使用。

**【反例】**
```c
typedef struct CFileNode : public BaseObject
{
	RelFileNode m_rnode;
	ForkNumber  m_fork_num;
	int		m_attid;
	
	CFileNode(RelFileNode rnode, ForkNumber fork_num = MAIN_FORKNUM)
	{
		m_rnode = rnode;
		m_fork_num = fork_num;
		m_attid = -1;
	}

	CFileNode(RelFileNode rnode, int attid, ForkNumber fork_num = MAIN_FORKNUM)
	{
		m_rnode = rnode;
		m_fork_num = fork_num;
		m_attid = attid;
	}

	CFileNode(const CFileNode& cfile_node)
	{
		m_rnode = cfile_node.m_rnode;
		m_forkNum = cfile_node.m_fork_num;
		m_attid = cfile_node.m_attid;
	}
}CFileNode;
```



### C++.04 禁用C++异常机制严禁使用C++的异常机制

**【描述】**
所有的错误都应该通过错误值在函数之间传递并做相应的判断, 而不应该通过异常机制进行错误处理。编码人员必须完全掌控整个编码过程，建立攻击者思维，增强安全编码意识，主动把握有可能出错的环节。而使用C++异常机制进行错误处理，会削弱编码人员的安全意识。异常机制会打乱程序的正常执行流程，使程序结构更加复杂，原先申请的资源可能会得不到有效清理。异常机制导致代码的复用性降低，使用了异常机制的代码，不能直接给不使用异常机制的代码复用。异常机制在实现上依赖于编译器、操作系统、处理器，使用异常机制，导致程序执行性能降低。在二进制层面，程序被加载后，异常处理函数增加了程序的被攻击面，攻击者可以通过覆盖异常处理函数地址，达到攻击的效果。

**【例外】**
在接管C++语言本身抛出的异常（例如new失败、STL）、第三方库（例如IDL）抛出的异常时，可以使用异常机制
```c
int len = ...;
char *p = NULL;
try {
    p = new char[len];
}
catch (bad_alloc) {
    ...
    abort();
}
```

**【相关指南】**
Google C++ Style Guide.Exceptions: We do not use C++ exceptions.




### C++.05 禁止使用外部数据拼接SQL命令

**【描述】**
SQL注入是指SQL查询被恶意更改成一个与程序预期完全不同的查询。执行更改后的查询可能会导致信息泄露或者数据被篡改。而SQL注入的根源就是使用外部数据来拼接SQL语句。C/C++语言中常见的使用外部数据拼接SQL语句的底层场景有（包括但不局限于）：
•	连接MySQL时调用mysql_query(),Execute()时的入参
•	连接SQL Server时调用db-library驱动的dbsqlexec()的入参
•	调用ODBC驱动的SQLprepare()连接数据库时的SQL语句参数
•	C++程序调用OTL类库中的otl_stream()，otl_column_desc()时的入参
•	C++程序连接Oracle数据库时调用ExecuteWithResSQL()的入参





### C++.06 严禁使用string类存储敏感信息





### C++.07 禁止通过对指针判空来判断new分配内存是否成功

**【描述】**
标准C++使用new分配内存失败时，会抛出异常std::bad_alloc而非返回NULL，因此检查返回值是否为NULL判断分配是否成功是徒劳的，需使用异常捕获。

**【正例】**
```c
try
{
    master_context = new _master_context();
}
catch(std::bad_alloc)
{
    return -1;
}
```

### C++.08 禁止使用c++ STL模板库

**【反例】**
```c
Map<int, int> indexMap;
indexMap[1]=2;
...
```

## 2.18 其它




### OTH.01 删除无效或永不执行的代码

**【描述】**
无效或永不执行的代码（即无效代码或无法访问的代码）通常是编程错误的结果，并且可能导致意外行为。通常在编译时，编译器会对此类代码进行优化。但是，为了提高可读性并确保解决逻辑错误，应该主动对其进行识别，理解和消除。

虽然大多数现代编译器在许多情况下可以对无效或从不执行的代码告警，但程序员还是应该主动识别无效的语句或表达式，并将其从代码中删除。

**【反例】**
下面代码中，最后的 if 条件语句永远无法成立，应该删除或重新优化代码。
```c
int Func(int condVal)
{
    char *s = NULL;
    if (condVal == 1) {
        s = (char *)malloc(ALLOC_SIZE);
        if (s == NULL) {
           ... // 错误处理
        }
        ... // 处理 s
        return 0;
    }
    ...
    if (s != NULL) {
        ... // 此处代码不可达
    }
    return 0;
}
```

**【正例】**
删除无效代码取决于程序员的意图，下面代码是一种改进方案。
```c
int Func(int condVal)
{
    if (condVal == 1) {
        char *s = (char *)malloc(ALLOC_SIZE);
        if (s == NULL) {
           ... // 错误处理
        }
        ... // 处理 s
        free(s);
        return 0;
    }
    ...
    return 0;
}
```

**【反例】**
下面代码进行了a与b的比较，没有任何效果。
```c
int a = ...;
int b = ...;
...
a == b; // 不符合： 这一行代码没有任何作用
```

该代码可能是程序员错误的使用相等操作符(`==`)而不是赋值操作符(`=`)的情况。

**【正例】**
```c
int a = ...;
int b = ...;
...
a = b;
```

**【反例】**
如下代码示例中，对指针进行解引用后，指针值增加了，但解引用没有任何作用。
```c
int *p = NULL;
...
*p++;
```

**【正例】**
更正此示例取决于程序员的意图。例如，如果解引用p是错误的，则p不应解引用。
```c
int *p = NULL;
...
p++;
```

**【反例】**
从上到下评估一串`if/else if`语句。最多只执行该链的一个分支：第一个分支的条件求值为true。因此，在if/else if语句序列中复制条件会自动导致无效代码。
```c
if (param == 1) {
    DoSomething1();
} else if (param == 2) {
    DoSomething2();
} else if (param == 1) {  // 条件重复，永远不成立，预期是3？
    DoSomething3();
} else {
    ...
}
```

**【正例】**
```c
if (param == 1) {
    DoSomething1();
} else if (param == 2) {
    DoSomething2();
} else if (param == 3) {
    DoSomething3();
} else {
    ...
}
```

**【例外1】**
在某些情况下，看似无效的代码可能会使软件更具弹性。一个示例是语句中的`default`标签，该`switch`语句的控制表达式具有枚举类型，并且为该类型的所有枚举指定标签。
```c
typedef enum {
    RED,
    GREEN,
    BLUE
} Color;

const char *FuncB(Color c)
{
    switch (c) {
        case RED:
            return "Red";
        case GREEN:
            return "Green";
        case BLUE:
            return "Blue";
        default:
            return "Unknown color";   // 不是无效代码
    }
}

void FuncA(void) {
    Color unknown = (Color)123;
    puts(FuncB(unknown));
}
```

**【例外2】**

公共库中未使用的函数和变量不违反该准则。同样，由于因`#ifdef`而没有编译的代码可能会随后在另一个应用程序中使用或在其他平台上构建，因此也不会违反该准则。

**【影响】**

存在无效的代码或从未执行的代码，可能代表逻辑错误，可能会导致意外的行为和漏洞。





### OTH.02 不要在信号处理函数中访问共享对象

**【描述】**
如果在信号处理程序中访问和修改共享对象，可能会造成竞争条件，使数据处于不确定的状态。
这条规则有两个不适用的场景：

- 读写不需要加锁的原子对象;
- 读写volatile sig_atomic_t类型的对象，因为具有volatile  sig_atomic_t类型的对象即使在出现异步中断的时候也可以作为一个原子实体访问，是异步安全的。

此外，在信号处理程序中，如果要调用函数，请仅调用异步信号安全函数。

**【反例】**
在这个信号处理过程中，程序打算将`g_msg`作为共享对象，当产生SIGINT信号时更新共享对象的内容，但是该`g_msg`变量类型不是`volatile sig_atomic_t`，所以不是异步安全的。

```c
#define MAX_MSG_SIZE 32
static char g_msgBuf[MAX_MSG_SIZE] = {0};
static char *g_msg = g_msgBuf;

void SignalHandler(int signum)
{
    // 下面代码操作g_msg不合规，因为不是异步安全的
    (void)memset_s(g_msg, MAX_MSG_SIZE, 0, MAX_MSG_SIZE);
    errno_t ret = strcpy_s(g_msg, MAX_MSG_SIZE, "signal SIGINT received.");
    ... // 处理 ret
}

int main(void)
{
    errno_t ret = strcpy_s(g_msg, MAX_MSG_SIZE, "No msg yet."); // 初始化消息内容
    ... // 处理 ret

    signal(SIGINT, SignalHandler); // 设置SIGINT信号对应的处理函数

    ... // 程序主循环代码

    return 0;
}
```
**【正例】**
如下代码示例中，在信号处理函数中仅将`volatile sig_atomic_t`类型作为共享对象使用。

```c
#define MAX_MSG_SIZE 32
volatile sig_atomic_t g_sigFlag = 0;

void SignalHandler(int signum)
{
    g_sigFlag = 1; // 符合
}

int main(void)
{
    signal(SIGINT, SignalHandler);
    char msgBuf[MAX_MSG_SIZE];
    errno_t ret = strcpy_s(msgBuf, sizeof(msgBuf), "No msg yet."); // 初始化消息内容
    ... // 处理 ret

    ... // 程序主循环代码

    if (g_sigFlag == 1) {  // 在退出主循环之后，根据g_sigFlag状态再刷新消息内容
        ret = strcpy_s(msgBuf, sizeof(msgBuf), "signal SIGINT received.");
        ... // 处理 ret
    }

    return 0;
}
```

**【影响】**

在信号处理程序中访问或修改共享对象，可能造成以不一致的状态访问数据。


**【相关软件CWE编号】** CWE-662，CWE-828




### OTH.03 禁用rand函数产生用于安全用途的伪随机数

**【描述】**
C语言标准库rand()函数生成的是伪随机数，所以不能保证其产生的随机数序列质量。根据C11标准，rand()函数产生的随机数范围是`[0, RAND_MAX(0x7FFF)]`，因为范围相对较短，所以这些数字可以被预测。
所以禁止使用rand()函数产生的随机数用于安全用途，必须使用安全的随机数产生方式，如：类Unix平台的/dev/random文件，Windows平台的BCryptGenRandom。

典型的安全用途场景包括(但不限于)以下几种：

- 会话标识SessionID的生成；
- 挑战算法中的随机数生成；
- 验证码的随机数生成；
- 用于密码算法用途（例如用于生成IV、盐值、密钥等）的随机数生成。

**【反例】**
程序员期望生成一个唯一的不可被猜测的HTTP会话ID，但该ID是通过调用rand()函数产生的数字随机数，它的ID是可猜测的，并且随机性有限。

**【正例】(POSIX)**
在类Unix平台上，可以使用/dev/random文件得到随机数。需要注意的是，设备刚启动时，由于硬件输入的熵可能不足，读取该接口可能产生阻塞问题。

**【影响】**

使用rand()函数可能造成可预测的随机数。





### OTH.04 禁止在发布版本中输出对象或函数的地址

**【描述】**
禁止在发布版本中输出对象或函数的地址，如：将变量或函数的地址输出到客户端、日志、串口中。

当攻击者实施高级攻击时，通常需要先获取目标程序中的内存地址（如变量地址、函数地址等），再通过修改指定内存的内容，达到攻击目的。
如果程序中主动输出对象或函数的地址，则为攻击者提供了便利条件，可以根据这些地址以及偏移量计算出其他对象或函数的地址，并实施攻击。
另外，由于内存地址泄露，也会造成地址空间随机化的保护功能失效。

为降低地址泄露造成漏洞的风险，高版本linux内核代码中的printk函数已经将%p格式由打印地址数值修改为打印地址的hash值。
同时也提供了%pK %px等格式，应对特殊场景，因此内核中打印指针的策略可参考业界CVE修改漏洞的方法。

**【反例】**
如下代码中，使用%p格式将指针指向的地址记录到日志中。

```c
int Encode(unsigned char *in, size_t inSize, unsigned char *out, size_t maxSize)
{
    ...
    Log("in=%p, in size=%zu, out=%p, max size=%zu\n", in, inSize, out, maxSize);
    ...
}
```

备注：这里仅用%p打印指针作为示例，代码中将指针转换为整数再打印也存在同样的风险。

**【正例】**
如下代码中，删除打印地址的代码。

```c
int Encode(unsigned char *in, size_t inSize, unsigned char *out, size_t maxSize)
{
    ...
    Log("in size=%zu, max size=%zu\n", inSize, maxSize);
    ...
}
```

**【例外】**
当程序崩溃退出时，在记录崩溃的异常信息中可以输出内存地址等信息。

**【影响】**

内存地址信息泄露，为攻击者实施攻击提供有利信息，可能造成地址空间随机化防护失效。


**【相关软件CWE编号】** CWE-200

**【业界典型漏洞】** CVE-2019-9444





### OTH.05 禁止代码中包含公网地址

**【描述】**

代码或脚本中包含用户不可见，不可知的公网地址，可能会引起客户质疑。

对产品发布的软件（包含软件包/补丁包）中包含的公网地址（包括公网IP地址、公网URL地址/域名、邮箱地址）要求如下：
1、禁止包含用户界面不可见、或产品资料未描述的未公开的公网地址。
2、已公开的公网地址禁止写在代码或者脚本中，可以存储在配置文件或数据库中。

对于开源/第三方软件自带的公网地址必须至少满足上述第1条公开性要求。

**【例外】**
- 对于标准协议中必须指定公网地址的场景可例外，如soap协议中函数的命名空间必须指定的一个组装的公网URL、http页面中包含w3.org网址等。