- [1.代码风格](#1代码风格)
  - [1.1 命名](#11-命名)
      - [G.NAM.01 使用统一的命名风格【建议】](#gnam01-使用统一的命名风格建议)
      - [G.NAM.02 命名要有明确含义，以提升代码的可读性【建议】](#gnam02-命名要有明确含义以提升代码的可读性建议)
      - [G.NAM.03 "self"应是实例方法的第一个参数，"cls"应是类方法的第一个参数【建议】](#gnam03-self应是实例方法的第一个参数cls应是类方法的第一个参数建议)
      - [G.NAM.04 避免在无关的标识符或无关的概念之间重用名字， 避免因重名而导致的意外赋值和错误引用【建议】](#gnam04-避免在无关的标识符或无关的概念之间重用名字-避免因重名而导致的意外赋值和错误引用建议)
      - [G.NAM.05 除了需要重写魔法函数、对象之外，不推荐使用双下划线开头且双下划线结尾的标识符来命名一般对象【建议】](#gnam05-除了需要重写魔法函数对象之外不推荐使用双下划线开头且双下划线结尾的标识符来命名一般对象建议)
  - [1.2 注释](#12-注释)
      - [G.CMT.01 模块文档字符串写在文件的顶部，Shebang和文件编码声明之后，导入(imports) 部分之前的位置，不需要缩进【建议】](#gcmt01-模块文档字符串写在文件的顶部shebang和文件编码声明之后导入imports-部分之前的位置不需要缩进建议)
      - [G.CMT.02 类的文档字符串写在类声明(class ClassName:)所在行的下一行，并向后缩进4个空格【建议】](#gcmt02-类的文档字符串写在类声明class-classname所在行的下一行并向后缩进4个空格建议)
      - [G.CMT.03 公共函数的文档字符串写在函数声明(def function\_name(param):)所在行的下一行，并向后缩进4个空格【建议】](#gcmt03-公共函数的文档字符串写在函数声明def-function_nameparam所在行的下一行并向后缩进4个空格建议)
      - [G.CMT.04 代码的注释位置和格式应该在项目内保持统一【建议】](#gcmt04-代码的注释位置和格式应该在项目内保持统一建议)
      - [G.CMT.05 正式交付给客户的代码不应包含TODO/FIXME注释【建议】](#gcmt05-正式交付给客户的代码不应包含todofixme注释建议)
      - [G.CMT.06 文件头注释应该包含版权许可信息【建议】](#gcmt06-文件头注释应该包含版权许可信息建议)
  - [1.3 格式](#13-格式)
      - [G.FMT.01 程序块应该采用4个空格缩进风格编写【建议】](#gfmt01-程序块应该采用4个空格缩进风格编写建议)
      - [G.FMT.02 行宽不超过120个字符【建议】](#gfmt02-行宽不超过120个字符建议)
      - [G.FMT.03 合理安排空行【建议】](#gfmt03-合理安排空行建议)
      - [G.FMT.04 用空格突出关键字和重要信息【建议】](#gfmt04-用空格突出关键字和重要信息建议)
      - [G.FMT.05 导入部分(imports)应该置于模块注释和文档字符串之后，模块全局变量和常量声明之前【建议】](#gfmt05-导入部分imports应该置于模块注释和文档字符串之后模块全局变量和常量声明之前建议)
      - [G.FMT.06 每行只能导入一个模块【建议】](#gfmt06-每行只能导入一个模块建议)
      - [G.FMT.07 导入部分(imports)应该按照标准库、第三方库、应用程序自定义模块的顺序排列导入【建议】](#gfmt07-导入部分imports应该按照标准库第三方库应用程序自定义模块的顺序排列导入建议)
      - [G.FMT.08 一行只写一条语句【建议】](#gfmt08-一行只写一条语句建议)
      - [G.FMT.09 合理的运用换行和缩进【建议】](#gfmt09-合理的运用换行和缩进建议)
      - [G.FMT.10 代码行的行尾结束符LF和CRLF不应该混用【建议】](#gfmt10-代码行的行尾结束符lf和crlf不应该混用建议)
- [2.编程实践](#2编程实践)
  - [2.1 数据模型](#21-数据模型)
      - [G.TYP.01 需要精确数值计算的场景，应使用decimal模块，且不要用浮点数构造Decimal【建议】](#gtyp01-需要精确数值计算的场景应使用decimal模块且不要用浮点数构造decimal建议)
      - [G.TYP.02 浮点型数据判断相等不要直接使用==【要求】](#gtyp02-浮点型数据判断相等不要直接使用要求)
      - [P.02 合理使用字符串格式化](#p02-合理使用字符串格式化)
      - [P.03 合理使用字符串引号](#p03-合理使用字符串引号)
      - [P.17 不要使用难以理解的字面量](#p17-不要使用难以理解的字面量)
      - [G.TYP.04 建议使用if seq或if not seq的方式判断序列是否为空【建议】](#gtyp04-建议使用if-seq或if-not-seq的方式判断序列是否为空建议)
      - [G.TYP.05 对序列使用切片操作时，不建议使用负步进值进行切片【建议】](#gtyp05-对序列使用切片操作时不建议使用负步进值进行切片建议)
      - [G.TYP.06 同一个字典表达式中各个键值不要相同【要求】](#gtyp06-同一个字典表达式中各个键值不要相同要求)
      - [G.TYP.07 使用dict\[key\]获取 value 时需要注意保证 key 在有效的范围内【建议】](#gtyp07-使用dictkey获取-value-时需要注意保证-key-在有效的范围内建议)
      - [G.TYP.08 必须使用isinstance判断变量类型【要求】](#gtyp08-必须使用isinstance判断变量类型要求)
      - [G.TYP.09 建议优先使用对应的内置函数来判断对象的类型或行为【建议】](#gtyp09-建议优先使用对应的内置函数来判断对象的类型或行为建议)
  - [2.2 运算符和表达式](#22-运算符和表达式)
      - [G.OPR.01 对除法运算和模运算中的除数为0的情况做相应保护【要求】](#gopr01-对除法运算和模运算中的除数为0的情况做相应保护要求)
      - [G.OPR.02 与None作比较要使用is或is not，不要使用等号【要求】](#gopr02-与none作比较要使用is或is-not不要使用等号要求)
      - [G.OPR.03 禁止使用is运算符做值相等性比较【要求】](#gopr03-禁止使用is运算符做值相等性比较要求)
      - [G.OPR.04 不建议使用海象运算符【建议】](#gopr04-不建议使用海象运算符建议)
      - [G.OPR.05 应该使用 is not 运算符而不是not ... is【建议】](#gopr05-应该使用-is-not-运算符而不是not--is建议)
      - [G.OPR.06 应该使用 not in 测试成员关系【建议】](#gopr06-应该使用-not-in-测试成员关系建议)
      - [G.EXP.01 尽可能使用隐式布尔值【建议】](#gexp01-尽可能使用隐式布尔值建议)
      - [G.EXP.02 如果lambda表达式的内容超过一行，建议定义为常规函数【建议】](#gexp02-如果lambda表达式的内容超过一行建议定义为常规函数建议)
      - [G.EXP.03 不应将lambda表达式赋值给变量，应该使用常规函数【建议】](#gexp03-不应将lambda表达式赋值给变量应该使用常规函数建议)
      - [G.EXP.04 推导式和生成器表达式仅用于简单的逻辑表达【建议】](#gexp04-推导式和生成器表达式仅用于简单的逻辑表达建议)
  - [2.3 控制语句](#23-控制语句)
      - [G.CTL.01 同一个函数所有分支的返回值类型和个数保持一致【要求】](#gctl01-同一个函数所有分支的返回值类型和个数保持一致要求)
      - [G.CTL.02 所有的代码都必须是逻辑可达的【要求】](#gctl02-所有的代码都必须是逻辑可达的要求)
      - [G.CTL.03 避免在条件/循环控制语句中包含过多的条件【建议】](#gctl03-避免在条件循环控制语句中包含过多的条件建议)
      - [G.CTL.04 建议使用 for x in iterable 的方式循环处理可迭代对象【建议】](#gctl04-建议使用-for-x-in-iterable-的方式循环处理可迭代对象建议)
      - [G.CTL.05 建议使用单个下划线代替循环体中未使用的循环变量【建议】](#gctl05-建议使用单个下划线代替循环体中未使用的循环变量建议)
      - [G.CTL.06 避免出现死循环【建议】](#gctl06-避免出现死循环建议)
  - [2.4 函数与方法](#24-函数与方法)
      - [G.FNM.01 禁止使用可变对象作为参数默认值【要求】](#gfnm01-禁止使用可变对象作为参数默认值要求)
      - [G.FNM.02 函数和lambda表达式不应该使用外部的循环代码中定义的变量【建议】](#gfnm02-函数和lambda表达式不应该使用外部的循环代码中定义的变量建议)
      - [G.FNM.03 当函数参数个数较多且有相关性时，建议通过class/namedtuple/dataclass等具名形式进行封装【建议】](#gfnm03-当函数参数个数较多且有相关性时建议通过classnamedtupledataclass等具名形式进行封装建议)
      - [G.FNM.04 不要将没有返回值的函数调用结果赋值给变量【要求】](#gfnm04-不要将没有返回值的函数调用结果赋值给变量要求)
      - [G.FNM.05 当函数返回值个数较多时，建议通过class/namedtuple等具名形式进行封装【建议】](#gfnm05-当函数返回值个数较多时建议通过classnamedtuple等具名形式进行封装建议)
      - [G.FNM.06 使用return代替StopIteration来结束生成器【要求】](#gfnm06-使用return代替stopiteration来结束生成器要求)
      - [G.FNM.07 建议妥善处理函数的返回值和异常【建议】](#gfnm07-建议妥善处理函数的返回值和异常建议)
  - [2.5 变量作用域](#25-变量作用域)
      - [P.04 合理使用全局变量【建议】](#p04-合理使用全局变量建议)
      - [G.VAR.01 禁止在变量的生命周期内修改其类型【要求】](#gvar01-禁止在变量的生命周期内修改其类型要求)
      - [G.VAR.02 禁止使用global关键字声明不存在的外部变量【要求】](#gvar02-禁止使用global关键字声明不存在的外部变量要求)
      - [G.VAR.03 禁止覆盖外部作用域中的标识符【要求】](#gvar03-禁止覆盖外部作用域中的标识符要求)
  - [2.6 类与面向对象](#26-类与面向对象)
      - [G.CLS.01 如果子类和父类中都有\_\_init\_\_ 方法，则子类中的\_\_init\_\_ 方法必须正确调用其父类\_\_init\_\_ 方法【要求】](#gcls01-如果子类和父类中都有__init__-方法则子类中的__init__-方法必须正确调用其父类__init__-方法要求)
      - [G.CLS.02 重写方法的方法签名应该和被重写的方法一致【建议】](#gcls02-重写方法的方法签名应该和被重写的方法一致建议)
      - [G.CLS.03 建议避免在继承内置类型的同时重写其魔法函数【建议】](#gcls03-建议避免在继承内置类型的同时重写其魔法函数建议)
      - [G.CLS.04 建议在实现抽象类时使用abc模块【建议】](#gcls04-建议在实现抽象类时使用abc模块建议)
      - [G.CLS.05 子类调用父类初始化方法的方式，建议使用super类辅助【建议】](#gcls05-子类调用父类初始化方法的方式建议使用super类辅助建议)
      - [G.CLS.06 类的方法建议统一按照一种规则进行排列【建议】](#gcls06-类的方法建议统一按照一种规则进行排列建议)
      - [G.CLS.07 类的方法不需要访问实例时，建议定义为staticmethod或classmethod【建议】](#gcls07-类的方法不需要访问实例时建议定义为staticmethod或classmethod建议)
      - [G.CLS.08 禁止在\_\_init\_\_ 方法外定义实例属性【建议】](#gcls08-禁止在__init__-方法外定义实例属性建议)
      - [G.CLS.09 重写类的魔法函数时必须返回其原型指定的类型【要求】](#gcls09-重写类的魔法函数时必须返回其原型指定的类型要求)
      - [G.CLS.10 未实现的数值运算类型魔法函数必须返回NotImplemented而不是抛出NotImplementedError【要求】](#gcls10-未实现的数值运算类型魔法函数必须返回notimplemented而不是抛出notimplementederror要求)
      - [G.CLS.11 避免在类外或者子类中访问父类受保护的成员【建议】](#gcls11-避免在类外或者子类中访问父类受保护的成员建议)
      - [G.CLS.12 类实例较多时，推荐使用\_\_slots\_\_来加强管理类的成员属性【建议】](#gcls12-类实例较多时推荐使用__slots__来加强管理类的成员属性建议)
  - [2.7 异常处理](#27-异常处理)
      - [G.ERR.01 try代码块内只包含可能抛出异常的代码段【建议】](#gerr01-try代码块内只包含可能抛出异常的代码段建议)
      - [G.ERR.02 用异常来表示异常，而不是用返回值表示异常【建议】](#gerr02-用异常来表示异常而不是用返回值表示异常建议)
      - [G.ERR.03 异常的类型定义必须继承自Exception【要求】](#gerr03-异常的类型定义必须继承自exception要求)
      - [G.ERR.04 对异常做类型转换时要保留原始异常的错误调用栈信息【建议】](#gerr04-对异常做类型转换时要保留原始异常的错误调用栈信息建议)
      - [G.ERR.05 使用有明确业务属性的异常类型【要求】](#gerr05-使用有明确业务属性的异常类型要求)
      - [G.ERR.06 raise语句必须包含异常实例【要求】](#gerr06-raise语句必须包含异常实例要求)
      - [G.ERR.07 避免抑制或忽略异常【建议】](#gerr07-避免抑制或忽略异常建议)
      - [G.ERR.08 禁止通过异常泄露敏感数据【要求】](#gerr08-禁止通过异常泄露敏感数据要求)
      - [G.ERR.09 在单个except代码块内，禁止重复捕获同类异常【要求】](#gerr09-在单个except代码块内禁止重复捕获同类异常要求)
      - [G.ERR.10 同时使用多个except语句时，要注意异常捕获的顺序【要求】](#gerr10-同时使用多个except语句时要注意异常捕获的顺序要求)
      - [G.ERR.11 避免使用SystemExit和sys.exit()，主进程入口中例外【建议】](#gerr11-避免使用systemexit和sysexit主进程入口中例外建议)
      - [G.ERR.12 合理地使用object.__exit__ 处理异常【建议】](#gerr12-合理地使用objectexit-处理异常建议)
      - [G.ERR.13 捕获异常后避免直接重新抛出【建议】](#gerr13-捕获异常后避免直接重新抛出建议)
      - [G.ERR.14 不要使用return、break、continue或抛出异常使finally块非正常结束【要求】](#gerr14-不要使用returnbreakcontinue或抛出异常使finally块非正常结束要求)
  - [2.8 并行与并发](#28-并行与并发)
      - [P.06 不要依赖于内置类型的原子性【建议】](#p06-不要依赖于内置类型的原子性建议)
      - [P.07 Python多线程适用于阻塞式IO场景，不适用于并行计算场景【建议】](#p07-python多线程适用于阻塞式io场景不适用于并行计算场景建议)
      - [G.CNP.01 建议为communicate传入超时参数来防止子进程死锁或失去响应【建议】](#gcnp01-建议为communicate传入超时参数来防止子进程死锁或失去响应建议)
  - [2.9 包与模块](#29-包与模块)
      - [P.08 使用package对module分层管理【建议】](#p08-使用package对module分层管理建议)
      - [P.09 使用\_\_all\_\_声明允许外部访问的变量、函数和类【建议】](#p09-使用__all__声明允许外部访问的变量函数和类建议)
      - [G.IMP.01 使用绝对路径导入模块【建议】](#gimp01-使用绝对路径导入模块建议)
      - [G.IMP.02 使用 from ... import ... 语句的注意事项【建议】](#gimp02-使用-from--import--语句的注意事项建议)
      - [G.IMP.03 避免使用\_\_import\_\_ 函数【建议】](#gimp03-避免使用__import__-函数建议)
  - [2.10 标准库](#210-标准库)
      - [P.10 注意根据场景选用copy或deepcopy完成浅拷贝或深拷贝](#p10-注意根据场景选用copy或deepcopy完成浅拷贝或深拷贝)
      - [G.PSL.01 避免使用已经被标记为弃用并有明确替代的方法【建议】](#gpsl01-避免使用已经被标记为弃用并有明确替代的方法建议)
      - [G.PSL.02 在datetime的使用过程中注意时区的影响，时区敏感的场景建议显式指定时区【建议】](#gpsl02-在datetime的使用过程中注意时区的影响时区敏感的场景建议显式指定时区建议)
      - [G.PSL.03 修改sys.path时注意避免模块重名问题【建议】](#gpsl03-修改syspath时注意避免模块重名问题建议)
      - [G.PSL.04 建议用functools.wraps定义函数装饰器【建议】](#gpsl04-建议用functoolswraps定义函数装饰器建议)
  - [2.11 代码工程](#211-代码工程)
      - [P.11 建议尽量使用标准库中的功能来替代直接调用操作系统的系统命令【建议】](#p11-建议尽量使用标准库中的功能来替代直接调用操作系统的系统命令建议)
      - [G.PRJ.01 建议为启动文件添加启动文件头【建议】](#gprj01-建议为启动文件添加启动文件头建议)
      - [G.PRJ.02 建议为启动文件设置执行入口【建议】](#gprj02-建议为启动文件设置执行入口建议)
      - [G.PRJ.03 产品代码不要包含任何调试入口点【要求】](#gprj03-产品代码不要包含任何调试入口点要求)
      - [G.PRJ.04 建议同一项目内的编码方式保持一致，推荐使用UTF-8【建议】](#gprj04-建议同一项目内的编码方式保持一致推荐使用utf-8建议)
      - [G.PRJ.05 不用的代码段直接删除，不要注释掉【要求】](#gprj05-不用的代码段直接删除不要注释掉要求)
      - [G.PRJ.06 正式发布的代码及注释内容不应包含开发者个人信息【要求】](#gprj06-正式发布的代码及注释内容不应包含开发者个人信息要求)
      - [G.PRJ.07 禁止代码中包含公网地址【要求】](#gprj07-禁止代码中包含公网地址要求)
  - [2.12 文件](#212-文件)
      - [P.12 使用open打开文件时应注意使用正确的模式和编码【要求】](#p12-使用open打开文件时应注意使用正确的模式和编码要求)
      - [G.FIO.01 在多用户系统中创建文件时应根据需要指定合适的权限【要求】](#gfio01-在多用户系统中创建文件时应根据需要指定合适的权限要求)
      - [G.FIO.02 校验文件路径之前应该先对其进行规范化处理【要求】](#gfio02-校验文件路径之前应该先对其进行规范化处理要求)
      - [G.FIO.03 禁止使用tempfile.mktemp创建临时文件【要求】](#gfio03-禁止使用tempfilemktemp创建临时文件要求)
      - [G.FIO.04 临时文件使用完毕应及时删除【要求】](#gfio04-临时文件使用完毕应及时删除要求)
      - [G.FIO.05 构造文件路径时应屏蔽操作系统的差异，建议使用库函数辅助构造【建议】](#gfio05-构造文件路径时应屏蔽操作系统的差异建议使用库函数辅助构造建议)
      - [G.FIO.06 解压文件必须进行安全检查【要求】](#gfio06-解压文件必须进行安全检查要求)
  - [2.13 序列化](#213-序列化)
      - [G.SER.01 禁止使用pickle.load、\_pickle.load和shelve模块加载外部数据【要求】](#gser01-禁止使用pickleload_pickleload和shelve模块加载外部数据要求)
      - [G.SER.02 禁止序列化未加密的敏感数据【要求】](#gser02-禁止序列化未加密的敏感数据要求)
      - [G.SER.03 禁止使用yaml模块的load函数【要求】](#gser03-禁止使用yaml模块的load函数要求)
      - [G.SER.04 禁止使用jsonpickle模块的encode/decode或dumps/loads函数【要求】](#gser04-禁止使用jsonpickle模块的encodedecode或dumpsloads函数要求)
      - [G.SER.05 在序列化操作时建议使用较为安全的json模块【建议】](#gser05-在序列化操作时建议使用较为安全的json模块建议)
  - [2.14 外部数据校验](#214-外部数据校验)
      - [P.13 检验跨信任边界传递的外部数据【要求】](#p13-检验跨信任边界传递的外部数据要求)
      - [G.EDV.01 禁止使用eval和exec函数执行不可信代码【要求】](#gedv01-禁止使用eval和exec函数执行不可信代码要求)
      - [G.EDV.02 禁止使用OS命令解析器或"危险函数"调用系统命令【要求】](#gedv02-禁止使用os命令解析器或危险函数调用系统命令要求)
      - [G.EDV.03 避免在命令解析器中使用通配符【要求】](#gedv03-避免在命令解析器中使用通配符要求)
      - [G.EDV.04 禁止使用subprocess模块中的shell=True选项【要求】](#gedv04-禁止使用subprocess模块中的shelltrue选项要求)
      - [G.EDV.05 调用外部可执行程序时建议使用绝对路径【建议】](#gedv05-调用外部可执行程序时建议使用绝对路径建议)
      - [G.EDV.06 禁止直接使用外部数据来拼接SQL语句【要求】](#gedv06-禁止直接使用外部数据来拼接sql语句要求)
      - [G.EDV.07 不受信任的外部数据禁止使用.format()进行格式化【要求】](#gedv07-不受信任的外部数据禁止使用format进行格式化要求)
      - [G.EDV.08 防止正则表达式引起的ReDos攻击【要求】](#gedv08-防止正则表达式引起的redos攻击要求)
      - [G.EDV.09 禁止直接使用外部数据来拼接XML【要求】](#gedv09-禁止直接使用外部数据来拼接xml要求)
      - [G.EDV.10 禁止在处理XML数据时解析不可信的实体【要求】](#gedv10-禁止在处理xml数据时解析不可信的实体要求)
  - [2.15 日志](#215-日志)
      - [G.LOG.01 logging模块应尽量使用懒插值的能力记录日志【建议】](#glog01-logging模块应尽量使用懒插值的能力记录日志建议)
      - [G.LOG.02 使用日志记录工具实现日志功能【建议】](#glog02-使用日志记录工具实现日志功能建议)
      - [G.LOG.03 禁止直接使用外部数据记录日志【要求】](#glog03-禁止直接使用外部数据记录日志要求)
  - [2.16 性能与资源管理](#216-性能与资源管理)
      - [P.14 在try代码块内如果修改了资源，需要在except子句内将对应的资源还原【建议】](#p14-在try代码块内如果修改了资源需要在except子句内将对应的资源还原建议)
      - [P.15 合并大量字符串时建议根据需求选择合适的方式【建议】](#p15-合并大量字符串时建议根据需求选择合适的方式建议)
      - [P.16 在内存敏感的场景下建议使用生成器代替一次性生成数据的容器【建议】](#p16-在内存敏感的场景下建议使用生成器代替一次性生成数据的容器建议)
      - [G.PRM.01 在list成员个数可以预知的情况下，创建list时建议预留容纳所有成员的空间【建议】](#gprm01-在list成员个数可以预知的情况下创建list时建议预留容纳所有成员的空间建议)
      - [G.PRM.02 在成员个数及内容皆不变的场景下建议使用tuple代替list【建议】](#gprm02-在成员个数及内容皆不变的场景下建议使用tuple代替list建议)
      - [G.PRM.03 资源的申请和释放需要成对使用，包括正常和异常场景【建议】](#gprm03-资源的申请和释放需要成对使用包括正常和异常场景建议)
  - [2.17 代码测试](#217-代码测试)
      - [G.TES.01 禁止在生产版本的业务代码中使用assert【要求】](#gtes01-禁止在生产版本的业务代码中使用assert要求)
      - [G.TES.02 使用对应的方法做值断言【建议】](#gtes02-使用对应的方法做值断言建议)
  - [2.18 数据安全处理](#218-数据安全处理)
      - [G.DSP.01 将敏感对象发送出信任区域前进行签名并加密【要求】](#gdsp01-将敏感对象发送出信任区域前进行签名并加密要求)
      - [G.DSP.02 安全场景下必须使用密码学意义上的安全随机数【要求】](#gdsp02-安全场景下必须使用密码学意义上的安全随机数要求)
      - [G.DSP.03 必须使用ssl.SSLSocket代替socket.Socket来进行安全数据交互【要求】](#gdsp03-必须使用sslsslsocket代替socketsocket来进行安全数据交互要求)
      - [G.DSP.04 禁止在用户界面、日志中暴露不必要信息【要求】](#gdsp04-禁止在用户界面日志中暴露不必要信息要求)


# 1.代码风格

代码风格一般包含标识符的命名风格、排版与格式风格，注释风格。一致的编码习惯与风格，会使代码更容易阅读、理解更容易维护。统一的代码风格也是一致性原则最直观的体现。

## 1.1 命名

#### G.NAM.01 使用统一的命名风格【建议】

**【描述】**
在标识符命名时，应使用统一的命名风格，如果标识符命名不规范，会出现代码可读性问题。

**【修改建议】**
1. 常用标识符类型的命名风格推荐表：

| 类别  | 公有  |  私有 |
| ------------ | ------------ | ------------ |
|Modules |lower_with_under |_lower_with_under|
|Packages|lower_with_under   |   |
|Classes   |  CapWords |   |
| Exceptions  |   CapWords|   |
|Functions  |lower_with_under() | _lower_with_under() |
|Global/Class Constants  |  CAPS_WITH_UNDER |  _CAPS_WITH_UNDER  |
| Global/Class Variables   |  lower_with_under |  _lower_with_under |
|Instance Variables   |lower_with_under |_lower_with_under or __lower_with_under (当需要名字修饰时)  |
|Method Names   |  lower_with_under()|  _lower_with_under() or __lower_with_under() (当需要名字修饰时)|
|Function/Method Parameters   |  lower_with_under  |     |
|Local Variables|lower_with_under|  |

2. 如果项目不遵循本条款规范命名风格，此规则不适用，建议取消该规则的检查。
   - 基于开源或外部代码进行开发或维护时，可以保持原有命名风格，
   - 本条款未明确要求的标识符命名风格，由项目组自行选择，并保持风格统一。

**【正例】**
1：包和模块的命名风格
- 修复示例：包（Package）、模块（Module）名使用意义完整的英文描述，采用小写加下划线的风格命名
```python
from example_package import example_module  # 符合
from example_module import MyClass  # 符合
```
2：类的命名风格
- 修复示例：类（Class）名使用意义完整的英文描述，采用大写字母开头的单词（CapWords）风格命名
```python
class MyClass:  # 符合
    def __init__(self):
    ....
```
3：函数的命名风格
- 修复示例：函数、方法使用意义完整的英文描述，采用小写加下划线（lower_with_under）的风格命名
```python
def my_method():  # 符合
    ....
```
4：类或对象的保护成员、私有成员的命名风格
- 修复示例：类或对象的保护成员一般用单下划线`_`开头，私有成员一般用双下划线`__`开头
```python
class MyClass:
    def __init__(self):
        self._member = 1  # 符合，单下划线开头，暗示此成员仅供类的内部操作使用，外部不应该访问

    def my_method(self):
        self._member += 1

    def _my_protected_method(self):  # 符合，单下划线开头，暗示此方法仅供类的内部操作使用，外部不应该访问
        pass

class Mapping:
    def __init__(self, iterable):
        self.items_list = []
        self.__update(iterable)

    # 双下划线开头，会被解释器改名为_Mapping__update，外部如果使用修改后的名字仍可访问
    def __update(self, iterable):
        for item in iterable:
            self.items_list.append(item)

class MappingSubclass(Mapping):
    # 双下划线开头，会被解释器改名为_MappingSubclass__update，不会跟基类成员重名
    def __update(self, keys, values):
        for item in zip(keys, values):
            self.items_list.append(item)
```
5：变量（Variable）、类的数据成员（Data Member）、函数的参数(Parameter)的命名风格
- 修复示例：变量（Variable）、类的数据成员（Data Member）、函数的参数(Parameter)采用小写加下划线 （lower_with_under）的风格命名
```python
class FileEntry:
    def __init__(fd, buffer_size, buffer_offset):  # 符合
        self.file_descriptor = fd  # 符合
        self.buffer_size = buffer_size  # 符合
        self.buffer_offset = buffer_offset  # 符合
```
6：常量（Constant）命名风格
- 修复示例：常量（Constant） 采用大写加下划线（CAPS_WITH_UNDER）的风格命名
```python
import enum

class State(enum.Enum):
    '''The internal state used for parsing the input file.'''
    NORMAL = 0  # 符合
    IGNORE = 1  # 符合
```

**【反例】**
1：包和模块的命名风格
- 错误示例：
```python
from EXAMPLE_PACKAGE import example_module  # 不符合
from examplemodule import MyClass  # 不符合
```
2：类的命名风格
- 错误示例：
```python
class myclass:  # 不符合
    def __init__(self):
    ....
```
3：函数的命名风格
- 错误示例：
```python
def myMethod():  # 不符合
    ....
```
4：类或对象的保护成员、私有成员的命名风格
- 错误示例：
```python
class Example:
    def __init__(self):
        self._bad_public_name = 10  # 不符合，公开属性变保护属性
        self.__bad_protect_name = 10  # 不符合，保护属性变私有属性
        self.bad_private_name = 11  # 不符合，私有属性变公开
        self.protect_name = 12  # 不符合，保护属性变公开

    def __public_method(self):  # 不符合，公开方法设置成私有，难以或者无法正常调用
        pass

    def private_method(self):  # 不符合，私有方法公开
        pass
```
5：变量（Variable）、类的数据成员（Data Member）、函数的参数(Parameter)的命名风格
- 错误示例：
```python
class FileEntry:
    def __init__(fd, buffersize, bufferoffset):  # 不符合
        self.filedescriptor = fd  # 不符合
        self.buffersize = buffersize  # 不符合
        self.bufferoffset = bufferoffset  # 不符合
```
6：常量（Constant）命名风格
- 错误示例：
```python
import enum

class State(enum.Enum):
    '''The internal state used for parsing the input file.'''
    normal = 0  # 不符合
    ignore = 1  # 不符合
```

#### G.NAM.02 命名要有明确含义，以提升代码的可读性【建议】

**【描述】**
对于单个字符命名的场景，不应该使用字符"l"("L"的小写形式)，"I"("i"的大写形式)，"o"等命名。在某些字体中，这些字符与数字1和0很难辨认。

**【修改建议】**
不要使用`l`,`I`,`o`等难以辨认的单个字符命名变量，建议使用其他有明确含义的标识符。

**【正例】**
1：使用"l"("L"的小写形式)，"I"("i"的大写形式)，"o"作为变量名
- 修复示例：变量名使用有意义的单词
```python
class Student:
    pass

def example_function():
    student_chen = Student()  # 符合
    number_list = [i for i in range(10)]  # 符合，局部循环变量使用i
```

**【反例】**
1：使用"l"("L"的小写形式)，"I"("i"的大写形式)，"o"作为变量名
- 错误示例：
```python
class Student:
    pass

def example_function():
    I = Student()  # 不符合，使用I作为变量名，影响可读性
    o = [l for l in range(1)]  # 不符合，字符l和数字1很容易混淆，字符o和数字0容易混淆
```

#### G.NAM.03 "self"应是实例方法的第一个参数，"cls"应是类方法的第一个参数【建议】

**【描述】**
类方法（被@classmethod装饰的函数）的第一个参数是“cls”，这是Python语言常规约定。虽然也可以使用任意形参名字来代替“cls”，但这会破坏常规约定，降低代码的可读性。

**【修改建议】**
类方法的第一个参数名应是“cls”，不应使用其它参数名。

**【正例】**
1：类方法total使用其他参数来代替约定的cls参数
- 修复示例：类方法total的第一个位置参数是cls
```python
class Student:
    @classmethod
    def total(cls):   # 符合,类方法用cls参数
        print("total count")
```

**【反例】**
1：类方法total使用其他参数来代替约定的cls参数
- 错误示例：类方法total的第一个参数是ptr
```python
class Student:
    @classmethod
    def total(ptr):   # 不符合，类方法total缺少cls参数
        print("total count")
```

**【描述】**
实例方法的第一个参数是“self”，这是Python语言常规约定。虽然也可以使用任意形参名字来代替“self”，但这会破坏常规约定，从而降低代码的可读性。

**【修改建议】**
实例方法的第一个参数应使用“self”，不能使用其它参数代替。

**【正例】**
1：实例方法第一个参数不为"self"
- 修复示例：实例方法的第一个参数是self
```python
class Student:
    def set_information(self, name, age, sex):  # 符合
        print("student information")

    def add_information(self, rank):  # 符合，实例方法的第一个参数是self
        print(rank)
```

**【反例】**
1：实例方法第一个参数不为"self"
- 错误示例：实例方法中使用student代替self，可读性降低
```python
class Student:
    def set_information(student, name, age, sex):  # 不符合
        print("student information")

    def add_information(rank):  # 不符合，该实例方法忘记写self参数
        print(rank)

if __name__ == '__main__':
    monitor = Student()
    monitor.set_information('lucy', 18, 0)  # 调用成功
    monitor.add_information(1)  # 调用实例方法出错
```

**【描述】**
实例方法的第一个参数是“self”，不能缺失。

**【修改建议】**
实例方法的第一个参数应是“self”，不应缺失。

**【正例】**
1：实例方法缺失self参数
- 修复示例1：实例方法的第一个位置参数是self
```python
class MyClass(object):
    def method(self):    # 符合，表示实例方法
        """A method with a self argument."""
```
- 修复示例2：使用静态方法
```python
class MyClass(object):
    @staticmethod
    def method():    # 符合，表示静态方法
        """A method with a self argument."""
```

**【反例】**
1：实例方法缺失self参数
- 错误示例：
```python
class MyClass(object):
    def method():  # 不符合
        """A method without a self argument."""
```

#### G.NAM.04 避免在无关的标识符或无关的概念之间重用名字， 避免因重名而导致的意外赋值和错误引用【建议】

**【描述】**
重复定义一个函数/类的名字很容易掩盖编码问题，让同 一个名字的函数/类在不同的执行阶段具有不同的含义，不利于可读性，应予以禁止。
在代码修改时，同名的变量容易导致错误的引用，也不利于代码可读性，应当尽量避免。

**【修改建议】**
应避免重用名字的场景如下：
  1. 标识符的命名避免和内置函数、内置类以及Python关键字重复。
  2. 避免重复定义函数、类方法或类。
  3. 标识符命名避免与当前导入的模块名称重名。
  4. 避免在函数中定义与参数名称相同的变量，这可能导致潜在的错误。

**【正例】**
1：参数和内建函数重名
- 修复示例：修改参数名避免和内建函数重名
```python
def function(para, typename):    # 符合
    ...
    para_type = type(para) 
```
2：变量和导入对象重名
- 修复示例：修改变量名避免和导入对象重名
```python
from os import path

for file_name in ['file1.py', 'file2.py']:     # 符合
    print(file_name)
```
3：变量名和函数参数名重名
- 修复示例：修改变量名避免和函数参数重名
```python
from os import path

def redefine_argument(file_name):     
    with open('file.py') as some_file:      # 符合
        pass
```

**【反例】**
1：参数和内建函数重名
- 错误示例：参数名遮盖了builtin函数type
```python
def function(para, type):  
    ...
    para_type = type(para)  # 不符合，type被遮盖为函数参数，不是builtin的实现
```
2：变量和导入对象重名
- 错误示例：循环变量path与导入的对象path重名
```python
from os import path

for path in ['file1.py', 'file2.py']:    # 不符合，path变量和导入模块名重名
    print(path)
```
3：变量名和函数参数名重名
- 错误示例：file_name变量与函数参数名称重名，可能导致潜在的错误
```python
def not_redefine_argument(file_name):    
    with open('file.py') as file_name:          # 不符合，file_name变量名和参数名称重名
        pass
```

#### G.NAM.05 除了需要重写魔法函数、对象之外，不推荐使用双下划线开头且双下划线结尾的标识符来命名一般对象【建议】

**【描述】**
魔法函数是以双下划线开头且双下划线结尾的标识符，用来命名Python内部特殊的魔法函数或对象，如类成员的`__init__`、`__len__`、`__add__`等。
普通成员方法不能以双下划线开头且双下划线结尾，否则会和魔法函数混淆。

**【修改建议】**
除魔法函数外，不要使用双下划线开头且双下划线结尾的标识符命名一般函数或对象。如果是私有方法，可以仅以双下划线开头，但不能以双下划线结尾。

**【正例】**
1：使用双下划线开头且结尾定义成员函数
- 修复示例：以双下划线开头的方法，属于对象私有的方法
```python
class MyClass:
    def __init__(self):
        pass

    def my_function(self, param):  # 符合
        pass

    def __my_private_function(self, param):  # 符合，仅以双下划线开头的方法，属于对象私有的方法
        pass
```

**【反例】**
1：使用双下划线开头且结尾定义成员函数
- 错误示例：以双下划线开头且双下划线结尾的方式命名
```python
class MyClass:
    def __init__(self):
        pass

    def __myfunction__(self, param):  # 不符合，这是自定义方法，不应该采用以双下划线开头且双下划线结尾的方式命名
        pass
```

## 1.2 注释

尽量通过清晰的软件架构、良好的标识符命名来提高代码的可读性；在需要的时候，才辅以注释说明。
对晦涩难懂的代码、命名，应该进行重构而不是添加注释
注释要从读者的角度出发，按需注释，内容要简洁明了，无歧义，信息全面且不冗余，不要简单地复制接口或方法的名字
修改代码的同时也要保证其注释的一致性
使用通顺的英文进行注释

#### G.CMT.01 模块文档字符串写在文件的顶部，Shebang和文件编码声明之后，导入(imports) 部分之前的位置，不需要缩进【建议】

**【描述】**
模块文档字符串应写在文件开始处，顶格不缩进，整体位置在Shebang和文件编码声明之后，导入(import) 部分之前。
文档字符串缩进会导致文档排版混乱，代码可读性差。

**【修改建议】**
模块文档字符串应写在文件开始处，顶格不缩进，整体位置在Shebang和文件编码声明之后，导入(import) 部分之前。
文档字符串使用三引号作为定界符，以前导三引号开头，结束三引号要自成一行。

**【正例】**
1：模块文档字符串格式错误
- 修复示例：模块文档字符串放在了Shebang和文件编码声明之后，导入(import) 部分之前
```python
#!/usr/bin/env python
# coding: utf-8
# 版权所有 (c) 华为技术有限公司 2012-2020
"""这是一个模块文档字符串的总体描述。
详细的功能描述建议和上面的总体描述空一行分隔。
可列出该模块导出的类，函数（以及任何其他对象）、异常等信息，并以每个一段的形式摘要描述。
（这些摘要通常比对象的docstring中的摘要行提供的细节少。）
包的docstring（即，包的__init__.py模块的docstring ）也应列出该包导出的模块和子包。
"""

from __future__ import barry_as_FLUFL

__all__ = []

import os
import sys
```

**【反例】**
1：模块文档字符串格式错误
- 错误示例：模块文档字符串写在了导入部分之后
```python
#!/usr/bin/env python
# coding: utf-8
# 版权所有 (c) 华为技术有限公司 2012-2020
from __future__ import barry_as_FLUFL
__all__ = []
import os
import sys
"""这是一个模块文档字符串的总体描述。
详细的功能描述建议和上面的总体描述空一行分隔。
可列出该模块导出的类，函数（以及任何其他对象）、异常等信息，并以每个一段的形式摘要描述。
（这些摘要通常比对象的docstring中的摘要行提供的细节少。）
包的docstring（即，包的__init__.py模块的docstring ）也应列出该包导出的模块和子包。
"""
```

#### G.CMT.02 类的文档字符串写在类声明(class ClassName:)所在行的下一行，并向后缩进4个空格【建议】

**【描述】**
类的文档字符串应位于类定义头部的下一行，相对于class关键字缩进4个空格，与内部定义的方法、数据成员具有相同的缩进量。

**【修改建议】**
类的文档字符串应位于类定义头部的下一行，相对于class关键字缩进4个空格，与内部定义的方法、数据成员具有相同的缩进量。
1.使用单行文档字符串时，前导三引号和结束三引号保持在同一行。
2.使用多行文档字符串时，以前导三引号开头，结束三引号要自成一行。

**【正例】**
1：类的文档字符串格式
- 修复示例：单行文档字符串
```python
class ErrorClass(Exception):
    """Base class for I/O related errors."""
    def __init__(self, *args, **kwargs): 
        pass
```
- 修复示例：多行文档字符串
```python
class ExampleClass:
    """The summary line for a class docstring should fit on one line.

    If the class has public attributes, they may be documented here
    in an ``Attributes`` section and follow the same formatting as a
    function's ``Args`` section. Alternatively, attributes may be documented
    inline with the attribute's declaration (see __init__ method below).

    Properties created with the ``@property`` decorator should be documented
    in the property's getter method.

    Attributes:
        attr1 (str): Description of `attr1`.
        attr2 (:obj:`int`, optional): Description of `attr2`.

    """
    def __init__(self, param1, param2, param3):
        """Example of docstring on the __init__ method.

        The __init__ method may be documented in either the class level
        docstring, or as a docstring on the __init__ method itself.

        Either form is acceptable, but the two should not be mixed. Choose one
        convention to document the __init__ method and be consistent with it.

        Note:
            Do not include the `self` parameter in the ``Args`` section.

        Args:
            param1 (str): Description of `param1`.
            param2 (:obj:`int`, optional): Description of `param2`. Multiple
                lines are supported.
            param3 (:obj:`list` of :obj:`str`): Description of `param3`.

        """
        self.attr1 = param1
        self.attr2 = param2
```

**【反例】**
1：类的文档字符串格式
- 错误示例：类的文档字符串缩进不一致
```python
class Six:  # error
    """
功能描述：
接口：
"""
```

#### G.CMT.03 公共函数的文档字符串写在函数声明(def function_name(param):)所在行的下一行，并向后缩进4个空格【建议】

**【描述】**
公共函数的文档字符串写在函数声明(def function_name(param):)所在行的下一行，并向后缩进4个空格。

**【修改建议】**
公共函数的文档字符串写在函数声明(def function_name(param):)所在行的下一行，并向后缩进4个空格。
1.使用单行文档字符串时，使用三引号作为定界符，前导三引号和结束三引号应该保持在同一行。
2.使用多行文档字符串时，使用三引号作为定界符，以前导三引号开头，结束三引号要自成一行。

**【正例】**
1：函数的文档字符串缩进
- 修复示例：单行文档字符串
```python
def get_freeze_count(*args, **kwargs): # real signature unknown
    """ Return the number of objects in the permanent generation. """
    pass
```
- 修复示例：多行文档字符串的示例是采用的Google风格，也可以采用Pycharm reStructedText风格，只要项目组内的注释风格保持一致就可以
```python
def select_function(rlist, wlist, xlist, timeout=None):
    """Wait until one or more file descriptors are ready for some kind of I/O.

    If only one kind of condition is required, pass [] for the other lists.
    A file descriptor is either a socket or file object, or a small integer
    gotten from a fileno() method call on one of those.

    Args:
        rlist: wait until ready for reading
        wlist: wait until ready for writing
        xlist: wait for an ``exceptional condition''
    Return: 
        a tuple of three lists corresponding to the first three
        arguments; each contains the subset of the corresponding file descriptors
        that are ready.
    Optional parameters：
        specifies a timeout in seconds; it may be 
        a floating point number to specify fractions of seconds.  If it is absent
        or None, the call will never time out.

    Raises:
         IOErrorr:  An error...
    """
    pass
```

**【反例】**
1：函数的文档字符串缩进
- 错误示例：文档字符串内容缩进不一致
```python
def func1(): 
    """
    功能描述：
    参数：
    返回值：
    异常描述：
    :return:
    """
    print("class three func 1")
```

#### G.CMT.04 代码的注释位置和格式应该在项目内保持统一【建议】

**【描述】**
代码的注释位置和格式应该在项目内保持统一风格，否则会导致代码很难维护，可读性差。

**【修改建议】**
1. 注释应该与其描述的代码保持同样的缩进，放在被注释代码块的上方相邻位置，使用#开头，#后面一个空格然后写注释文本。
2. 代码行的行尾添加注释，为了提高可读性，行尾注释应该至少离开代码2个空格，#后面一个空格然后写注释文本。

**【正例】**
1：注释在代码段的上方
- 修复示例：注释放在语句块上方，并和被注释代码段保持同样的缩进。#后面空一格写注释内容
```python
 # Create command line to call pylint
 epylint_part = [executable, "-c", "from pylint import epylint;epylint.Run()"]
```
2：注释在行尾
- 修复示例：注释放在行尾，与代码尾部间隔至少两个空格
```python
repssn_ind = ssn_data[index].repssn_index  # Get replicate sub system index and net indicator
```

**【反例】**
1：注释在代码段的上方
- 错误示例：注释虽然放在代码段的上方，但没有和被注释代码段保持同样的缩进。
```python
      # Get replicate sub system index and net indicator   
repssn_ind = ssn_data[index].repssn_index
repssn_ni = ssn_data[index].ni
```
2：注释在行尾
- 错误示例：注释放在了被注释代码段的下方。
```python
 epylint_part = [executable, "-c", "from pylint import epylint;epylint.Run()"]
 # Create command line to call pylint
```

#### G.CMT.05 正式交付给客户的代码不应包含TODO/FIXME注释【建议】

**【描述】**
TODO注释一般用来描述已知待改进、待补充的修改点。
FIXME注释一般用来描述已知缺陷。
它们都应该有统一风格，方便文本搜索统一处理。如：
```python
# TODO: 补充XX处理
# FIXME: XX缺陷
```
在版本开发阶段，可以使用此类注释用于突出标注；交付前应该全部处理掉。

**【修改建议】**
版本发布之后，应该删除TODO/FIXME注释。

**【正例】**
版本发布之前，可以保留TODO/FIXME注释
```python
# TODO: 版本发布之前可以保留
# FIXME: 版本发布之前可以保留
```

**【反例】**
版本正式发布之后仍然保留TODO/FIXME注释
```python
# TODO: 版本发布之后应该删除
# FIXME: 版本发布之后应该删除
```

#### G.CMT.06 文件头注释应该包含版权许可信息【建议】

**【描述】**
文件头注释应放在模块文档字符串之前，应包含版权许可信息，版权许可信息建议放在shebang和文件编码声明之后。如果需要在文件头注释中增加其他内容，可以在版权说明的后面进行补充。

**【修改建议】**
版权许可内容及格式如下，其内容可根据实际情况做调整：
- 中文版：`版权所有 (c) 华为技术有限公司 2012-2020`
- 英文版：`Copyright (c) Huawei Technologies Co., Ltd. 2012-2020. All rights reserved.`

关于版本许可信息，应注意：
- 2012-2020 根据实际需要可以修改。
2012 是文件首次创建年份，而 2020 是最后文件修改年份。二者可以一样，如 "2020-2020"。
 对文件有重大修改时，必须更新后面年份，如特性扩展，重大重构等。
- 版权说明可以使用华为子公司。
 如：版权所有 (c) 海思半导体 2012-2020
或英文：Copyright (c) Hisilicon Technologies Co., Ltd. 2012-2020. All rights reserved.
- 同一项目内，版本许可信息的位置和风格应保持一致。

**【正例】**
1：版权注释信息格式
- 修复示例：(中文版)
```python
#!/usr/bin/python3.7
# -*- coding: utf-8 -*-
# 版权所有 (c) 华为技术有限公司 2012-2020
```
- 修复示例：(英文版)
```python
#!/usr/bin/python3.7
# -*- coding: utf-8 -*-
# Copyright (c) Huawei Technologies Co., Ltd. 2012-2020. All rights reserved.
```

**【反例】**
1：版权注释信息格式
- 错误示例：错误版权申明(中文版)
```python
#!/usr/bin/python3.7
# -*- coding: utf-8 -*-
# 版权 (c) 华为技术有限公司 2012-2020
```
- 错误示例：错误版权申明(英文版)
```python
#!/usr/bin/python3.7
# -*- coding: utf-8 -*-
# Huawei Technologies Co., Ltd. 2012-2020. All rights reserved.
```

## 1.3 格式

#### G.FMT.01 程序块应该采用4个空格缩进风格编写【建议】

**【描述】**
程序块采用缩进风格编写，以4个空格为缩进单位，缩进量必须是4的倍数。
建议以4个空格作为缩进量，如果不以4个空格作为缩进，会导致代码格式混乱，运行时可能会出现缩进错误。
选择结构、循环结构、异常处理结构、函数定义、类定义、成员方法定义、类方法定义、静态方法定义、with块等语法结构，代码块相对于头部应该有4个空格的缩进。
相同级别的代码应具有相同的缩进量，虽然不影响程序运行，也不允许在逻辑上具有相同缩进层次的代码在视觉上具有不同的缩进量。
使用空格（space）和跳格（Tab），虽然视觉效果一样，但禁止在缩进时混合使用跳格和空格，否则程序无法运行，提示错误'SyntaxError: inconsistent use of tabs and spaces in indentation'。
因此，新项目必须使用纯空格(spaces)来代替跳格(Tab) 。

**【修改建议】**
程序块采用4个空格缩进风格，不能使用tab键。

**【正例】**
1：代码混合空格和tab缩进
- 修复示例：语句缩进使用4个空格
```python
class Seven:  # 符合
    """
    功能描述:
    接口:
    """
```

2：程序块缩进小于4个空格
- 修复示例：缩进4个空格
```python
for _, value in x_dict.items():
    if value < 100:
        print('value小于100')
    elif value > 100:
        print('value大于100')
    else:
        print('value等于100')
```

**【反例】**
1：代码混合空格和tab缩进
- 错误示例：代码同时使用空格和tab键缩进
```python
class Seven:  # 不符合
	"""
    功能描述：
    接口：
	"""
```

2：代码使用tab键
- 错误示例：使用tab键代替空格缩进
```python
class Seven:  # 不符合
	"""
    功能描述：
    接口：
	"""
```

3：程序块缩进小于4个空格
- 错误示例：语句缩进2个空格
```python
for key, value in x_dict.items():
    if value == 98:
      print(key)                 # 不符合，该语句缩进太少，只有2个空格
```

4：语句缩进超过4个空格
- 错误示例：语句缩进8个空格
```python
class Seven:  # 错误
	   """
    功能描述：
    接口：
	   """
```

#### G.FMT.02 行宽不超过120个字符【建议】

**【描述】**
行宽包含代码以及注释等，行宽不宜过长，否则不利于阅读。

该规则有可配置参数，具体配置详见规则集中该规则的选项配置。

**【修改建议】**
1. 代码行长度超过120，需在合适的地方换行。一般情况可使用`\\`。
2. 调用函数时，长度超过120，可以让调用的函数分成多行写，可以有效减少代码行长度。
3. 列表，字典元素过多，可以使用多行的方式分行写元素。

**【正例】**
1：代码行长度过长
- 修复示例：函数调用长度超过120，使用`\\`换行连接符换行
```python
var_sum = long_var_int_one + long_var_int_two + long_var_int_three + \\
          long_var_int_four + long_var_int_five + long_var_int_six
```
- 修复示例：函数调用代码长度超过120，使用规范化的格式
```python
if __name__ == '__main__':
    # 符合，代码行过长，使用规范化格式换行写
    local_min = simulated_annealing(
        prob, 
        find_max=True, 
        max_x=100,
        min_x=5,
        max_y=5340,
        min_y=-5,
        visualization=True,
        max_z=120,
        allow_edit=False
    )
    p = Person()
```

**【反例】**
1：代码行长度过长
- 错误示例：函数调用代码长度超过120
```python
var_sum = long_var_int_one + long_var_int_two + long_var_int_three + long_var_int_four + long_var_int_five + long_var_int_six
```

#### G.FMT.03 合理安排空行【建议】

**【描述】**
顶级的类定义或函数定义之间，需要2个空行，使用空行可以凸显出代码块的相关程度，能提升代码可读性。

**【修改建议】**
顶级的类定义或函数定义之间，需要2个空行。

**【正例】**
1：顶级的函数定义与类之间空行
- 修复示例：顶级的函数定义与类定义之间空两个空行
```python
def function_name():
    do_something()
# 空行
# 空行
class Example:   # 符合
    ...
```

**【反例】**
1：顶级的函数定义与类之间空行
- 错误示例：顶级的函数定义与类定义之间空4个空行
```python
def function_name(): 
    ...
# 空行
# 空行
# 空行
# 空行
class Example:  # 不符合，顶级的函数定义与类定义之间应该空两个空行
    ...
```

**【描述】**
类中的方法定义之间需间隔一个空行，使用空行可以凸显出代码块的相关程度，能提升代码可读性。

**【修改建议】**
类中的方法定义之间空一行。

**【正例】**
1：类中的方法之间空行
- 修复示例：类中的方法定义之间空一行
```python
class Animal:
    def eat(self):
        print("Can i eat?")
    # 空行
    def sleep(self):   # 符合，类中的方法定义之间空一行
        print("i want to sleep.")
```

**【反例】**
1：类中的方法之间空行
- 错误示例：类中的方法定义之间没有空行
```python
class Animal:
    def eat(self):
        print("Can i eat?")
    def sleep(self):   # 不符合，类中的方法定义之间空0行
        print("i want to sleep.")
```

**【描述】**
嵌套定义前应有 1 个空行，使用空行可以凸显出代码块的相关程度，能提升代码可读性。

**【修改建议】**
嵌套定义前应有 1 个空行。

**【正例】**
1：嵌套定义前没有加空行
- 修复示例：嵌套定义前应有 1 个空行
```python
def outer():

    def inner():
        pass
```

**【反例】**
1：嵌套定义前没有加空行
- 错误示例：
```python
def outer():
    def inner():
        pass
```

**【描述】**
空格应该突出关键字和重要信息。

**【修改建议】**
建议加空格的场景：
- 逗号、分号、冒号（假如用到的话）只在后面加空格。 
- 比较操作符">"、">="、"<"、"<="、"=="，赋值操作符"="、"+="，算术操作符"+"、"-"、"%"，逻辑 操作符"and"、"or"等双目操作符的前后加空格。
- "*"、"**"等作为操作符时，前后可以加空格，但若和更低优先级的操作符同时使用并且不涉及括号，则建议前后不加空格。
- 函数参数类型定义时，冒号前不应使用空格，冒号后需要加空格。函数返回值类型定义"->"前后建议添加空格。

不建议加空格的场景：
- 函数定义语句中的参数默认值，调用函数传递参数时使用的等号，建议不加空格。
- 对于包含关系的两个对象用"."连接时，前后不应加空格。
- 括号内侧，左括号后面和右括号前面，不需要加空格，多重括号间不必加空格。
- 紧贴索引切片或被调用函数名，开始的括号前，不需要加空格。
- 切片的3个参数之间的冒号前后不需要加空格，例如seq[start:stop:stride]。
- 行尾不建议加空格。

**【正例】**
1：关键字之后的空格
- 修复示例：def关键字之后有1个空格
```python
def func(): 
    pass
```

2：左括号后面的空格
- 修复示例：左括号后面没有空格
```python
with open('file.dat') as f:    # 符合，函数调用左括号后面没有空格
    contents = f.read()
```

3：右括号前面的空格
- 修复示例：右括号前面没有空格
```python
with open('file.dat') as f:    # 符合，函数调用右括号前面没有空格
    contents = f.read()
```

4：冒号前面的空格
- 修复示例：冒号前面没有空格
```python
with open('file.dat') as f:    # 符合
    contents = f.read()
```

5：括号之前的空格
- 修复示例：括号之前有0个空格
```python
with open('file.dat') as f:   # 符合
    contents = f.read()
```

6：算术操作符之后的空格
- 修复示例：乘号之后有1个空格
```python
doubled = num * 2
```

7：算术操作符之前的空格
- 修复示例：乘号之前有1个空格
```python
doubled = num * 2
```

8：操作符前后的空格
- 修复示例：操作符前后有1个空格
```python
if age > 15:   # 符合
    print('Can drive')
```

9：逗号之后的空格
- 修复示例：逗号之后有1个空格
```python
my_tuple = 1, 2
```

10：函数默认参数等于号前后的空格
- 修复示例：函数默认参数等于号前后没有空格
```python
def func(key1='val1',    # 符合，函数默认参数等于号前后没有空格
         key2='val2'): 
    return key1, key2
```

11：类型标注默认参数等于号前后的空格
- 修复示例：类型标注默认参数等于号前后有1个空格
```python
def func(a: int = 1):   # 符合
    pass
```

12：关键字之前的空格
- 修复示例：in关键字之前有1个空格
```python
def func():
    if 1 in [1, 2, 3]:   # 符合
        print('yep!')
```

**【反例】**
1：关键字之后的空格
- 错误示例：def关键字之后有2个空格
```python
def  func(): 
    pass
```

2：左括号后面的空格
- 错误示例：左括号后面有空格
```python
with open( 'file.dat') as f:   # 不符合，函数调用左括号后面有空格
    contents = f.read()
```

3：右括号前面的空格
- 错误示例：右括号前面有空格
```python
with open('file.dat' ) as f:    # 不符合，函数调用右括号前面有空格
    contents = f.read()
```

4：冒号前面的空格
- 错误示例：冒号前面有空格
```python
with open('file.dat') as f :  # 不符合，冒号前面有空格
    contents = f.read()
```

5：括号之前的空格
- 错误示例：括号之前有1个空格
```python
with open ('file.dat') as f:   # 不符合，括号之前有1个空格
    contents = f.read()
```

6：算术操作符之后的空格
- 错误示例：算术操作符之后的空格
```python
doubled = num *  2 
```

7：算术操作符之前的空格
- 错误示例：乘号之前有2个空格
```python
doubled = num  * 2
```

8：操作符前后的空格
- 错误示例：操作符前后没有空格
```python
if age>15:   #  不符合，操作符前后没有空格
    print('Can drive')
```

9：逗号之后的空格
- 错误示例：逗号之后有2个空格
```python
my_tuple = 1,  2
```

10：函数默认参数等于号前后的空格
- 错误示例：函数默认参数等于号前后有空格
```python
def func(key1 = 'val1',     # 不符合，函数默认参数等于号前后有空格
         key2 = 'val2'): 
    return key1, key2
```

11：类型标注默认参数等于号前后的空格
- 错误示例：类型标注默认参数等于号前后没有空格
```python
def func(a: int=1):    # 不符合
    pass
```

12：关键字之前的空格
- 错误示例：in关键字之前有2个空格
```python
def func():
    if 1  in [1, 2, 3]:     # 不符合
        print('yep!')
```

#### G.FMT.04 用空格突出关键字和重要信息【建议】

**【描述】**
标点符号后面没有空格，应该要有1个空格。

**【修改建议】**
标点符号后面要有1个空格。

**【正例】**
1：标点符号后面的空格
- 修复示例：标点符号后面有1个空格
```python
my_tuple = 1, 2, 3
```

**【反例】**
1：标点符号后面的空格
- 错误示例：标点符号后面没有空格
```python
my_tuple = 1,2,3
```

**【描述】**
关键字后面没有空格，应该要有1个空格。

**【修改建议】**
关键字后面要有1个空格。

**【正例】**
1：关键字后面的空格
- 修复示例：关键字后面有1个空格
```python
from collections import (namedtuple, defaultdict)
```

**【反例】**
1：关键字后面的空格
- 错误示例：关键字后面没有空格
```python
from collections import(namedtuple, defaultdict)
```

**【描述】**
模运算符前后没有空格，应该有一个空格。

**【修改建议】**
模运算符前后有1个空格。

**【正例】**
1：模运算符前后的空格
- 修复示例：模运算符前后有1个空格
```python
remainder = 10 % 2 
```

**【反例】**
1：模运算符前后的空格
- 错误示例：模运算符前后没有空格
```python
remainder = 10%2 
```

**【描述】**
空格应该突出关键字和重要信息。

**【修改建议】**
建议加空格的场景：
- 逗号、分号、冒号（假如用到的话）只在后面加空格。 
- 比较操作符">"、">="、"<"、"<="、"=="，赋值操作符"="、"+="，算术操作符"+"、"-"、"%"，逻辑 操作符"and"、"or"等双目操作符的前后加空格。
- "*"、"**"等作为操作符时，前后可以加空格，但若和更低优先级的操作符同时使用并且不涉及括号，则建议前后不加空格。
- 函数参数类型定义时，冒号前不应使用空格，冒号后需要加空格。函数返回值类型定义"->"前后建议添加空格。

不建议加空格的场景：
- 函数定义语句中的参数默认值，调用函数传递参数时使用的等号，建议不加空格。
- 对于包含关系的两个对象用"."连接时，前后不应加空格。
- 括号内侧，左括号后面和右括号前面，不需要加空格，多重括号间不必加空格。
- 紧贴索引切片或被调用函数名，开始的括号前，不需要加空格。
- 切片的3个参数之间的冒号前后不需要加空格，例如seq[start:stop:stride]。
- 行尾不建议加空格。

**【正例】**
```python
print(current, data, data_list) 
```

```python
total = addend + added_data
addend += 2
if current_time >= MAX_TIME_VALUE: 
    pass
```

```python
total = multiplier * multiplicand   # 符合，操作符"*"、"**"，前后可以加空格
total = radix ** power_nums
total = radix*2 - 1  # 符合，这里的操作符"*"前后不建议加空格
```

```python
def create(self, name=None):    # 符合，参数默认值以及调用函数传递参数时使用的等号，前后不加空格
    self.create(name="mike")
``` 

```python
result.write_log()  # 符合，"."后面不加空格
```

```python
a = ((b + c) * d - 5) * 6  # 符合
```

```python
def sample(constant: int = 1) -> str:  # 符合
    pass
```

```python
my_dict[key] = my_list[index]   # 符合
conn = Telnet.connect(ip_address) 
```

**【反例】**
```python
print(current,data,data_list)  # 不符合，逗号后面没有加空格
```
```python
total=addend + added_data   # 不符合，赋值操作符"="的前后没有加空格
addend+=2   # 不符合，赋值操作符"+="的前后没有加空格
if current_time>=MAX_TIME_VALUE:   # 不符合，比较操作符">="的前后没有加空格
```

```python
result. write_log()  # 不符合，"."后面添加了空格
```

```python
a = ( (b + c) * d - 5) * 6  # 不符合，多重括号间添加了空格
```

```python
def sample(constant : int=1)->str:  # 不符合，":"前添加了空格 ，参数类型定义时赋值操作符"="的前后没有加空格，"->"前后没有添加空格
    pass  

```

```python
my_dict [key] = my_list [index]   # 不符合，紧贴索引切片或被调用函数名，开始的括号前，添加了空格。
conn = Telnet.connect (ip_address)
```

**【描述】**
移位操作符或者位操作符前后没有空格，应该要有1个空格。

**【修改建议】**
移位操作符或者位操作符前后要有1个空格。

**【正例】**
1：移位操作符或者位操作符前后的空格
- 修复示例：移位操作符或者位操作符前后有1个空格
```python
x = 128 << 1
```

**【反例】**
1：移位操作符或者位操作符前后的空格
- 错误示例：移位操作符或者位操作符前后没有空格
```python
x = 128<<1
```

#### G.FMT.05 导入部分(imports)应该置于模块注释和文档字符串之后，模块全局变量和常量声明之前【建议】

**【描述】**
导入部分(imports)应该置于模块注释和文档字符串之后，模块全局变量和常量声明之前，否则会影响程序阅读和代码结构。

**【修改建议】**
1. 导入语句应该置于模块注释和文档字符串之后，模块全局变量和常量声明之前。
2. 非导入语句如全局变量等应置于导入语句之后，更改环境路径为目的的代码如sys.path.append以及猴子补丁等可以视作导入代码。
3. 如果文件中定义了类似`__all__`、`__version__`这种全局变量（以两个下划线开头、以两个下划线结尾），那么导入部分应该放在这类定义的后面，但`__future__`模块的导入例外，`__future__`模块的导入必须放在文档字符串之后，其他内容之前。
故放置顺序为：
     - `__future__`模块
     - `__all__`、`__version__`这种全局变量
     - 导入模块语句

**【正例】**
1：导入语句的位置错误
- 修复示例：导入部分位于文档字符串之后，全局变量之前
```python
"""This is a module
Functions of this module
"""
import os      # 符合，导入位置正确
import sys   # 符合，导入位置正确

sample_global_variable = 0
M_SAMPLE_GLOBAL_CONSTANT = 0
```

**【反例】**
1：导入语句的位置错误
- 错误示例：导入部分位于文档字符串和全局变量之后
```python
"""This is a module
Functions of this module
""" 
sample_global_variable = 0
M_SAMPLE_GLOBAL_CONSTANT = 0
import os   # 不符合，导入位置错误
import sys   # 不符合，导入位置错误
```

#### G.FMT.06 每行只能导入一个模块【建议】

**【描述】**
禁止一行导入多个模块语句，否则会影响程序阅读。

**【修改建议】**
1. 每行只能导入一个模块
2. 如果导入语句太长，可以放到元组中，然后换行。

**【正例】**
1：一行导入多个库
- 修复示例1：一行导入了一个库
```python
import os  # 符合
import sys
```
- 修复示例2：如果一行代码太长，可以放到元组中，然后换行
```python
from moviepy.editor import (VideoFileClip, TextClip,  # 符合
                            CompositeVideoClip, ColorClip)
```

**【反例】**
1：一行导入多个库
- 错误示例：一行导入了两个库
```python
import os, sys  # 不符合
```

#### G.FMT.07 导入部分(imports)应该按照标准库、第三方库、应用程序自定义模块的顺序排列导入【建议】

**【描述】**
导入部分(imports)应按照标准库，第三方库，应用程序自定义模块的顺序排列导入，否则会影响代码结构。

**【修改建议】**
导入部分应该按照如下分组顺序导入，每个分组之间应该留一个空行：
1. 标准库
2. 第三方库
3. 应用程序自定义模块
4. 如果文件中包含`__future__`模块的导入，那么该语句应该被放在所有导入的最前面

**【正例】**
1：导入顺序错误
- 修复示例1：按照标准库，第三方库，应用程序自定义模块的顺序导入
```python
import os   # 符合，标准模块放在前面
import sys  # 符合，标准模块放在前面

from oslo_config import cfg
from oslo_log import log as logging

from cinder import context
from cinder import db
```
- 修复示例2：`__future__`模块放在导入语句最前面
```python
from __future__ import print_function   # __future__模块放在导入语句最前面

import os
import sys
from time import sleep
```

**【反例】**
1：导入顺序错误
- 错误示例：标准库导入在应用程序自定义模块导入之后
```python
from oslo_config import cfg
from oslo_log import log as logging

from cinder import context
from cinder import db

import os    # 不符合，标准模块应放在最前面
import sys   # 不符合，标准模块应放在最前面
```

#### G.FMT.08 一行只写一条语句【建议】

**【描述】**
类、方法定义、控制语句冒号后面应换行，否则影响代码结构和程序阅读。

**【修改建议】**
类、方法定义、控制语句冒号后面应换行。

**【正例】**
1：循环语句
- 修复示例：循环语句头部和循环体起独立行
```python
for i in range(10): 
    print(i)  # 符合
```

**【反例】**
1：循环语句
- 错误示例：循环语句头部和循环体共用1行
```python
for i in range(10): print(i)  # 不符合
```

**【描述】**
def函数定义部分和函数体不能共用一行，否则会影响程序阅读。

**【修改建议】**
函数体要单起一行，不能和函数定义部分共用一行。

**【正例】**
1：函数定义方式
- 修复示例：函数定义和函数体部分分开
```python
def main6():  # 符合
    a = 1  
    print(a)
```

**【反例】**
1：函数定义方式
- 错误示例：函数定义和函数体部分合用一行
```python
def main6(): a = 1; print(a)  # 不符合
```

**【描述】**
不能在一行使用分号分隔多条语句，不是python的代码风格，影响程序阅读。

**【修改建议】**
一行只写一条语句。

**【正例】**
1：一行写多条语句
- 修复示例：一行只写一条语句
```python
rect.length = 0  # 符合
rect.width = 0
```

**【反例】**
1：一行写多条语句
- 错误示例：单行使用分号分隔多条语句
```python
rect.length = 0; rect.width = 0;  # 不符合
```

#### G.FMT.09 合理的运用换行和缩进【建议】

**【描述】**
当语句过长，或者可读性不佳时，需要在合适的地方换行。否则会导致一行语句过长，不利于程序阅读和维护。

**【修改建议】**
1. 如果一条语句过长，且其中有函数调用、方法调用、类调用或类似的语法，可以采用隐式续行的写法，左括号应跟函数名在同一行，右括号应跟最后一个参数在同一行，
然后在圆括号内某个参数后面逗号位置换行，换行后后面几行开始的位置，与同组表达式的第一个左对齐。
2. 如果列表、元组、字典、集合类似的对象的语句过长，建议要么左括号与右括号在同一行，要么在左括号后进行第一次换行，右括号单独成一行。
3. 不建议复杂且较长的表达式，如果一定要使用，建议在每一段（map，generator，filter）后面进行换行，也就是说，每一段分别独立一行。

**【正例】**
1：字典，列表赋值
- 修复示例：字典的左括号和右括号在同一行，键值对齐
```python
data = {'key1': 12, 'key2': 23}  # 符合

data = {
    'key1': 12,
    'key2': 23,
}   # 符合，左括号后面换行，右括号和左括号所在行的第一列对齐，且最后一个元素后面保留逗号

foo = [
    'hello', 'world',
]  # 符合，左括号后面换行，右括号和左括号所在行的第一列对齐
```
2：列表表达式
- 修复示例：复杂且较长的表达式，每一段换行
```python
[
    x * y
    for x in range(20)
    for y in range(20)
    if x * y > 200
]
```

**【反例】**
1：字典，列表赋值
- 错误示例：字典的键没有对齐，并且在左括号后没有换行
```python
data = {'key1': 12,  # 不符合，'key1'没有和'key2'对齐
       'key2': 23,
}

data = {'key1': 12,
       'key2': 23}   # 不符合，右括号没有单独成一行

data = {'hello',
        'world'}
```
2：列表表达式
- 错误示例：复杂且较长的表达式，没有在每一段换行
```python
[x*y for x in range(20)
for y in range(20) if x*y > 200]
```

#### G.FMT.10 代码行的行尾结束符LF和CRLF不应该混用【建议】

**【描述】**
项目文件中，代码行的行尾结束符LF和CRLF不应该混用。UNIX系统应使用LF作为行尾结束符，Window系统应使用CRLF作为行尾结束符。

**【修改建议】**
统一使用\n作为代码文件的换行符。

# 2.编程实践
## 2.1 数据模型

#### G.TYP.01 需要精确数值计算的场景，应使用decimal模块，且不要用浮点数构造Decimal【建议】

**【描述】**
在需要精确数值计算的情况下，使用浮点数不仅无法得到精确的计算结果，而且会导致程序出现意想不到的结果。

**【修改建议】**
涉及精确的数值计算（货币、金融等），建议使用decimal模块。且不要用浮点数构造`Decimal`，应该使用字符串格式的数值构造`Decimal`。

**【正例】**
1：浮点数使用
- 修复示例：使用Decimal模块，使用字符串格式的数值构造`Decimal`
```python
from decimal import Decimal

print(Decimal('12.3') * Decimal('0.1'))  # 符合，输出1.23
print(Decimal('3.14'))  # 符合，输出3.14
```
- 修复示例：使用Decimal模块，使用字符串格式的数值构造`Decimal`
```python
from decimal import Decimal

print(Decimal('6') / Decimal('3.14'))  # 符合
print(Decimal(1) / Decimal(7))  # 符合
print(Decimal('1') / Decimal('7'))  # 符合
```

**【反例】**
1：浮点数使用
- 错误示例：使用浮点数无法得到精确的计算结果
```python
print(12.3 * 0.1)  # 不符合，输出1.2300000000000002
print('{0:.20f}'.format(3.14))  # 不符合，输出3.14000000000000012434
```
- 错误示例：使用浮点数构造`Decimal`
```python
Decimal.from_float(12.222)   # 不符合
Decimal(3.14).adjusted()  # 不符合
print(Decimal(6) / Decimal(3.14))   # 不符合
```

#### G.TYP.02 浮点型数据判断相等不要直接使用==【要求】

**【描述】**
由于浮点数在计算机表示中存在精度的问题，数学上相等的数字，经过运算后，其浮点数表示可能不再相等，从而会导致程序出现不是预期的结果，因而禁止使用相等运算符 == 来比较浮点数是否相等。

**【修改建议】**
浮点型数据判断相等不要直接使用==，使用math.isclose方法来处理，不要把浮点数作为HashMap的Key使用。

**【正例】**
1：浮点数的比较
- 修复示例：考虑浮点数的精度问题，可在一定的误差范围内判定两个浮点数值是否相等。这个误差应根据实际需要进行定义
```python
first = 1.0 - 0.8
last = 0.8 - 0.6
EPSILON = 1e-15
if abs(first - last) < EPSILON:    # 符合，预期会进入这里
    pass
```
- 修复示例：Python3.5以后的版本新增了math.isclose()方法，可以实现两个浮点数的比较，如果指接近相等则返回True，否则返回False
```python
import math

first = 3.0
last = 2.99998
print(math.isclose(first, last, rel_tol=1e-5))  # 符合，输出结果为True
```

**【反例】**
1：浮点数的比较
- 错误示例：使用浮点数比较数值是否相等
```python
first = 1.0 - 0.8
last = 0.8 - 0.6
if first == last:    
    do_something_true()  # 不符合，预期进入此代码块，执行其他业务逻辑，但事实上data1 == data2的结果在很多情况下可能为False
else:    
    do_something_false()  # 不符合，实际上会进入这里
```

#### P.02 合理使用字符串格式化

**【描述】**
字符串格式应遵循以下原则：
1. 对于简单的字符串串联，使用`+`操作符即可，对于复杂的字符串格式化方法，优先推荐使用`formate()`方法或f-字符串
2. 尽量避免使用运算符%进行格式化和连接字符串

**【正例】**
```python
name = "Alice"
greeting = "Hello, " + name + "!"
print(greeting)  # 输出: Hello, Alice!
```

```python
name = "Bob"
age = 25
message = "My name is {} and I am {} years old.".format(name, age)
print(message)  # 输出: My name is Bob and I am 25 years old.
```

```python
name = "Charlie"
age = 30
message = f"My name is {name} and I am {age} years old."
print(message)  # 输出: My name is Charlie and I am 30 years old.
```

**【反例】**
```python
# 不推荐
name = "Dave"
age = 35
message = "My name is %s and I am %d years old." % (name, age)
print(message)  # 输出: My name is Dave and I am 35 years old.
```

#### P.03 合理使用字符串引号

**【描述】**
字符串引号的使用应遵循以下原则：
1. 在同一个文件中，要保证字符串引号使用的一致性。使用单引号或者双引号引用字符串，并在同一文件中沿用
2. 在字符串内需要使用引号的情况推荐使用另一种引号，避免使用反斜线进行转义
3. 多行字符串建议使用三重双引号`"""`而不是三重单引号`'''`。当且仅当项目中使用单引号`'`引用字符串时，才可能会使用三重单引号`'''`为非文档字符串的多行字符串来标识引用。文档字符串必须使用三重双引号`"""`

**【正例】**
```python
# 规则1：统一使用双引号（假设项目约定用双引号）
name = "Alice"
message = "Hello, world!"

# 规则2：字符串内需用引号时，外层用另一种引号
quote = 'She said, "Python is awesome!"'  # 内层双引号无需转义
html_tag = "<div class='header'>"         # 内层单引号无需转义

# 规则3：多行字符串用三重双引号
multiline_text = """
This is a multi-line string.
It preserves line breaks and indentation.
"""

# 文档字符串必须用三重双引号
def calculate_sum(a, b):
    """Calculate the sum of two numbers."""
    return a + b
```

**【反例】**
```python
# 反例1：同一文件中混用单双引号（违反一致性）
bad_name = 'Bob'
bad_message = "Hi there!"  # 风格不一致

# 反例2：用相同引号导致需要转义
bad_quote = "She said, \"Python is hard!\""  # 不推荐，转义降低了可读性
bad_tag = '<div class=\"header\">'           # 同上

# 反例3：随意使用三重单引号（非文档字符串）
bad_multiline = '''
This is a multi-line string.
But it uses triple single quotes inconsistently.
'''

# 反例4：文档字符串用三重单引号（禁止）
def bad_docstring(a, b):
    '''Calculate the difference.'''  # 错误！文档字符串必须用 """
    return a - b
```

#### P.17 不要使用难以理解的字面量

**【描述】**
难以理解的字面量是指通过代码的上下文难以明确业务含义的字面量，包括整型字面量、浮点数字面量、布尔字面量和字符串字面量等。使用难以理解的字面量，会导致代码难以维护和阅读。

**【修改建议】**
对于多处使用的难以理解的字面量，应该定义为常量或者变量，并通过符号命名自注释。

**【正例】**
1：多处使用的难以理解的字面量
- 修复示例1：下代码中，提取出了能表达含义的常量并通过标识符命名来解释字符串含义
```python
ACTION_1 = "action1"  # 行为模式1

def run():
    prepare(ACTION_1)  # 符合
    execute(ACTION_1)
    release(ACTION_1)
```

**【反例】**
1：多处使用的难以理解的字面量
- 错误示例：使用重复字符串
```python
def run():
    prepare("this is a duplicate")  # 不符合 ，字符串"this is a duplicate" 多次使用，且难以理解信息
    execute("this is a duplicate")
    release("this is a duplicate")
```

#### G.TYP.04 建议使用if seq或if not seq的方式判断序列是否为空【建议】

**【描述】**
在条件表达式中虽然可以直接使用len()判断序列是否为空，但Python语言本身有非常简单而高效的方式来推断字符串、列表、元组、字典、集合的隐式布尔值，
使用if seq 或if not seq判断序列是否为空，是一种非常Pythonic的编程方式，同时也是PEP8推荐的方式。

**【修改建议】**
使用if seq或if not seq的方式判断序列是否为空。

**【正例】**
使用if seq或if not seq的方式判断序列是否为空
```python
if seq:
    pass

if not seq:
    pass
```

**【反例】**
通过列表长度来判断序列是否为空
```python
if len(seq):
    pass

if not len(seq):
    pass

if len(seq) == 0:
    pass

if len(seq) != 0:
    pass

```

#### G.TYP.05 对序列使用切片操作时，不建议使用负步进值进行切片【建议】

**【描述】**
不建议使用负步进值进行切片。

Python提供了example_list[start : end : stride]形式的写法，以实现步进切割，也就是从每stride个元素中取一个出来。但如果stride值为负，则会使代码难以理解，特定使用场景下还会造成错误。

**【修改建议】**
尽量使用stride为正数，并且尽量不要同时使用start、 end 、 stride。如果确实要执行这种操作，建议将“步进”切割过程和“范围”切割过程分开，使代码更清晰。

**【正例】**
1：对序列使用了负步进值进行切片
- 修复示例：使用正步进值切片
```python
list_one = [1, 2, 3, 4, 5, 6, 7, 8]

# 符合，结果明确
list_two = list_one[::2]
print(list_two)  # [1, 3, 5, 7] 
list_three = list_two[1:-1]
print(list_three)  # [3, 5]
```

**【反例】**
1：对序列使用了负步进值进行切片
- 错误示例：
```python
my_list = [1, 2, 3, 4, 5, 6, 7, 8]

# 不符合，难以理解，且容易出错
print(my_list[-2::-2])  # [7, 5, 3, 1] 
print(my_list[-2:2:-2])  # [7, 5]
print(my_list[2:2:-2])  # []
```

#### G.TYP.06 同一个字典表达式中各个键值不要相同【要求】

**【描述】**
同一个字典表达式中的各个键值不要重复，如果存在重复的键值，后面的键值对会覆盖前面的键值对，会导致程序出现意想不到的结果。

**【修改建议】**
字典表达式不能包含相同的键值。

**【正例】**
1：字典初始化键值
- 修复示例：字典的键值各不相同

```python

dict_duplicate_values = {"lilei": 20, "hanmeimei": 30, "wangqiang": 45}    # 符合，键值没有重复的

print(dict_duplicate_values)  # {'lilei': 20, 'hanmeimei': 30, 'wangqiang': 45}

```

**【反例】**
1：字典初始化键值
- 错误示例：字典变量包含相同的键值，并且对应的值不相同
```python
dict_duplicate_values = {"lilei": 20, "hanmeimei": 30, "wangqiang": 45, "lilei": 23}    # 不符合，键值有2个`lilei`
print(dict_duplicate_values)  # {'lilei': 23, 'hanmeimei': 30, 'wangqiang': 45}
```

#### G.TYP.07 使用dict[key]获取 value 时需要注意保证 key 在有效的范围内【建议】

**【描述】**
Python的字典dict可以使用key获取其对应的value。但是当key在dict的key值列表中不存在时，直接使用dict[key]获取value会报KeyError。从而会导致程序异常崩溃，
因此需要注意从代码层面保证 key 在有效的范围内。

**【修改建议】**
1. 尽量避免直接使用dict[key]的方式从字典中获取value，如果一定要使用，需要注意对key not in dict的情况做异常处理。
2. 使用dict.get(key)方法获取value，并且在使用dict.get方法时应设置默认值并对返回值进行检查，如果不设置默认值的话则默认为None。
3. 对于性能要求不高的场景，推荐使用collections模块中defaultdict类，当取一个字典中不存在的key值时，它不会报错或者取到的值为None，而是会返回一个设定的默认值。

**【正例】**
1：使用KeyError捕获字典key的取值异常
- 修复示例：对key不存在的情况做异常处理
```python
example_dict = dict()
example_key = 'example_key'
try:
    example_value = example_dict[example_key]
except KeyError:
    ...  # 符合，对key不存在的情况做异常处理
```
2：使用dict.get()的方法来代替直接取值
- 修复示例：使用dict.get()的方法，设置默认值为'Not exist'
```python
example_dict = dict()
example_key = 'example_key'
example_value = example_dict.get(example_key,  'Not exist')  # 符合，使用dict.get()的方法，设置默认值为'Not exist'

# 无论是否设置默认值，在使用的时候都应该进行判断，以保证安全性
if example_value == 'Not exist':
    pass
else:
    pass
```
3：使用defaultdict类来代替直接取值
- 修复示例：使用defaultdict类，默认值为空字符串' '
```python
from collections import defaultdict

example_dict = defaultdict(str)  # 符合，使用defaultdict类，默认值为空字符串' '
example_key = 'example_key'
print(example_dict[example_key])
```

**【反例】**
1：使用KeyError捕获字典key的取值异常
- 错误示例：没有判断key是否在字典变量中存在
```python
example_dict = dict()
example_key = 'example_key'
example_value = example_dict[example_key]   # 不符合，字典取值时没有判断键值是否存在
```
2：使用dict.get()的方法来代替直接取值
- 错误示例：没有判断key是否在字典变量中存在
```python
example_dict = dict()
example_key = 'example_key'
example_value = example_dict[example_key]   # 不符合，字典取值时没有判断键值是否存在
```
3：使用defaultdict类来代替直接取值
- 错误示例：没有判断key是否在字典变量中存在
```python
example_dict = dict()
example_key = 'example_key'
example_value = example_dict[example_key]   # 不符合，字典取值时没有判断键值是否存在
```

#### G.TYP.08 必须使用isinstance判断变量类型【要求】

**【描述】**
使用`isinstance`代替`type`比较来判断变量类型；判断一个对象的类型是否在多个类型中，尽量使用单次`isinstance`调用。

**【修改建议】**
使用isinstance而不是type来判断变量类型。

**【正例】**
`isinstance`不仅会判断对象是否是目标类型的实例，还会判断对象是否是目标类型子类的实例，或者是否能通过目标类型的`__instancecheck__`校验。
```Python
is_integer = isinstance(obj, int)

is_integer_or_float = isinstance(obj, (int, float))
```
```Python
class B:
     pass

class C(B):
     pass

isinstance(C(), B)
```
```Python
class ABC(type):
    def __instancecheck__(cls, inst):
        return any(cls.__subclasscheck__(c)
                   for c in {type(inst), inst.__class__})

    def __subclasscheck__(cls, sub):
        candidates = cls.__dict__.get("__subclass__", set()) | {cls}
        return any(c in candidates for c in sub.mro())

class Integer(metaclass=ABC):
    __subclass__ = {int}

isinstance(1, Integer)
```

**【反例】**
使用type判断对象类型
```Python
is_integer = type(obj) is type(1)
```

#### G.TYP.09 建议优先使用对应的内置函数来判断对象的类型或行为【建议】

**【描述】**
使用hasattr判断对象的类型或行为属于通过对象特征间接判断。如果存在对应的内置函数来判断对象的类型或行为，则建议优先使用这些内置函数，比如，推荐使用callable()、isinstance()等内置函数来代替hasattr()判断对象的类型或行为。
因为对应的内置函数可以更好地覆盖各种场景，并且不会随着语言的演进而失效。
如果没有对应的内置函数，则仍可使用hasattr()函数判断对象是否具有特定的行为。

**【修改建议】**
使用内置函数，包含(callable, isinstance)来判断对象的类型或行为。

**【正例】**
```Python
from collections.abc import Container, Iterable

callable(obj)  # 判断是否是callable

isinstance(obj, Container)  # 判断是否是容器

isinstance(obj, Iterable)  # 判断是否可迭代。另外因为历史原因，仅实现了__getitem__是"可迭代的"对象，但是无法通过isinstance去判断
```

**【反例】**
```Python
hasattr(obj, '__call__')  # 判断是否是callable

hasattr(obj, '__contains__')  # 判断是否是容器

hasattr(obj, '__iter__')  # 判断是否可迭代
```

## 2.2 运算符和表达式

#### G.OPR.01 对除法运算和模运算中的除数为0的情况做相应保护【要求】

**【描述】**
对除法运算和模运算中的除数为0的情况做相应保护。

如果除法或模运算中的除数为零可能会导致程序终止，因此需要对除数为0的情况做相应保护。

**【修改建议】**
1. 在除法运算前，对除数是否为0进行判断。
2. 通过捕获除0异常ZeroDivisionError的方式，来防止程序意外终止。

**【正例】**
1：未对除数进行非零判断
- 修复示例1：对除数进行非零判断
```python
dividen_num = 0
divisor_num = 0

# 符合：在进行除法运算前，先对除数做非0判断
if divisor_num != 0:
  division_result = dividen_num / divisor_num
  remainder_result = dividen_num % divisor_num
else:
  ...
```
- 修复示例2：捕获除零异常

```python
dividen_num = 0
divisor_num = 0

# 符合：通过捕获除0异常ZeroDivisionError的方式，来防止程序意外终止
try:
  division_result = dividen_num / divisor_num
except ZeroDivisionError:
  ...
else:
  ...
```

**【反例】**
1：未对除数进行非零判断
- 错误示例：未对除数进行非零判断
```python
dividen_num = 0
divisor_num = 0

# 不符合：未对除数进行非0判断
division_result = dividen_num / divisor_num
remainder_result = dividen_num % divisor_num
```

#### G.OPR.02 与None作比较要使用is或is not，不要使用等号【要求】

**【描述】**
`is`判断是否指向同一个对象（判断两个对象的id是否相等），`==`会调用`__eq__`方法判断是否等价（判断两个对象的值是否相等）。None是python中的一个特殊的常量，表示一个空的对象。一个变量如果是None，它一定和None指向同一个内存地址。因此，判断实例为None时，与None作比较应该使用`is`或`is not`。

注意：None和空值不是一个东西，空值是Python中的一个特殊值，数据为空并不代表是空对象，例如`[]`, `{}`, `()`, `''`等都不是None。

**【修改建议】**
与None作比较要使用`is`或`is not`。

**【正例】**
1：对象与None的比较
- 修复示例：同一个实例，使用`is`和`==`的判断结果不同
```python
class PersonMetaClass(object):
    def __init__(self, name, age, gender):
        self.name = name
        self.age = age
        self.gender = gender

    def __eq__(self, other):
        if hasattr(other, 'gender'):
            return self.gender == other.gender
        else:
            return 'The assertion property does not exist'

student1 = PersonMetaClass('Xiao li', 17, 'female')
student2 = PersonMetaClass('Han Hong', 18, 'female')
print(student2 is None)  # 符合，判断两个对象的id是否相等，结果为False
print(student2 is student1)  # False
```

**【反例】**
1：对象与None的比较
- 错误示例：对象与None用等于号做比较
```python
class PersonMetaClass(object):
    def __init__(self, name, age, gender):
        self.name = name
        self.age = age
        self.gender = gender

    def __eq__(self, other):
        if hasattr(other, 'gender'):
            return self.gender == other.gender
        else:
            return 'The assertion property does not exist'

student1 = PersonMetaClass('Xiao li', 17, 'female')
student2 = PersonMetaClass('Han Hong', 18, 'female')
print(student2 == None)  # 不符合，判断两个对象的值是否相等，结果为The assertion property does not exist
print(student2 == student1)  # True
```

#### G.OPR.03 禁止使用is运算符做值相等性比较【要求】

**【描述】**
`is`和`is not`是用来检查两个实例是否引用同一个对象的，禁止用`is`或`is not`运算符在内置类型之间作比较，否则程序会出现`SyntaxWarning`语句警告信息：`SyntaxWarning: "is" with a literal. Did you mean "=="?`。内置类型有int、float、complex、list、tuple、set、frozenset、dict、str、bytes，建议用`==`或`!=`运算符替代。针对于内置类型比较地址的情况，建议使用`id()`判断代替`is`和`is not`。

**【修改建议】**
内置类型数值之间用`==`或`!=`来比较。

**【正例】**
1：内置类型之间作比较
- 修复示例：
```python
def literal_comparison(param):
    return param == 2000   # 符合，整数比较用==

literal_comparison(2000)  # True
literal_comparison(int("2000"))  # True
print(() == tuple())  # 符合，元组比较用==，结果为True
print((1,) == tuple([1]))  # 符合，元组比较用==，结果为True
```

**【反例】**
1：内置类型之间作比较
- 错误示例：
```python
def literal_comparison(param):
    return param is 2000   # 不符合，整数比较用is

literal_comparison(2000)  # True
literal_comparison(int("2000"))  # False
print(() is tuple())  # 不符合，元组比较用is，结果为True
print((1,) is tuple([1]))  # 不符合，元组比较用is，结果为False
```

#### G.OPR.04 不建议使用海象运算符【建议】

**【描述】**
不建议使用海象运算符`:=`， 一般人难以理解海象运算符，它会使代码更难理解与维护。

**【修改建议】**
用赋值语句`=`替代海象运算符`:=`。

**【正例】**
1：赋值
- 修复示例：用等于号代替海象运算符
```python
v = f(p)  # 符合
v0 = f(p)  # 符合
v1 = f(p)  # 符合

value = f(p)  # 符合
func(a=value)  # 符合
func(value, b=2)  # 符合

def func(param=21):  # 符合
    p = 21

x = 10  # 符合
f'{x}'
```

**【反例】**
1：赋值
- 错误示例：使用海象运算符
```python
(v := f(p))  # 不符合
v0 = (v1 := f(p))  # 不符合

func(a=(b := f(p)))  # 不符合
func(a := f(p), b=2)  # 不符合

def func(param=(p := 21)):  # 不符合
    pass

def func(param: (p := 21) = 3):  # 不符合
    pass

f'{(x := 10)}'  # 不符合
```

#### G.OPR.05 应该使用 is not 运算符而不是not ... is【建议】

**【描述】**
`x is not None`和`not x is None`虽然有相同的功能，但是前者的可读性更强，后者易产生歧义，导致代码可读性变差。

**【修改建议】**
使用 is not 运算符而不是not ... is。

**【正例】**
1：判断对象是否为None
- 修复示例：使用`x is not None`判断对象是否为None
```python
if foo is not None:    # 符合
    pass
```

**【反例】**
1：判断对象是否为None
- 错误示例：使用`not x is None`判断对象是否为None
```python
if not foo is None:   # 不符合
    pass
```

#### G.OPR.06 应该使用 not in 测试成员关系【建议】

**【描述】**
使用`x not in the_list`而不是`not x in the_list`来测试成员关系，这样可以提升代码可读性和一致性，后者会导致代码可读性变差。

**【修改建议】**
使用 not in和in来测试成员关系。

**【正例】**
1：测试成员关系
- 修复示例：通过not in来测试成员关系
```python
if item not in items:
    ...
```

**【反例】**
1：测试成员关系
- 错误示例：通过not取反来测试成员关系
```python
if not item in items:
    ...
```

#### G.EXP.01 尽可能使用隐式布尔值【建议】

**【描述】**
当表达式与True、False或None等单例值进行比较时，应该使用is或者is not，如果使用==判断会导致意外的判断结果。

**【修改建议】**
使用is或者is not来比较True、False或None等单例值。

**【正例】**
1：与bool值比较相等
- 修复示例：与False比较使用is关键字
```python
def DFS(self):
    # visited array for storing already visited nodes
    visited = [False] * len(self.vertex)

    # call the recursive helper function
    for i in range(len(self.vertex)):
        # 符合，与False比较使用用is符号
        if visited[i] is False:
            self.DFSRec(i, visited)
```
2：与bool值比较不相等
- 修复示例：与False比较使用is not符号
```python
def DFS(self):
    # visited array for storing already visited nodes
    visited = [False] * len(self.vertex)

    # call the recursive helper function
    for i in range(len(self.vertex)):
        # 符合，与False比较使用用is not符号
        if visited[i] is not False:
            self.DFSRec(i, visited)
```

**【反例】**
1：与bool值比较相等
- 错误示例：与False比较使用==符号
```python
def DFS(self):
    # visited array for storing already visited nodes
    visited = [False] * len(self.vertex)

    # call the recursive helper function
    for i in range(len(self.vertex)):
        # 不符合，与False比较不能用==符号
        if visited[i] == False:
            self.DFSRec(i, visited)
```
2：与bool值比较不相等
- 错误示例：与False比较使用!=符号
```python
def DFS(self):
    # visited array for storing already visited nodes
    visited = [False] * len(self.vertex)

    # call the recursive helper function
    for i in range(len(self.vertex)):
        # 不符合，与False比较不能用!=符号
        if visited[i] != False:
            self.DFSRec(i, visited)
```

#### G.EXP.02 如果lambda表达式的内容超过一行，建议定义为常规函数【建议】

**【描述】**
如果lambda表达式的内容太复杂的话，代码可读性会变差，使人难以理解，建议使用常规函数来代替。

**【修改建议】**
建议定义为常规函数的场景如下：
1. lambda表达式的内容较长，例如超过120个字符的lambda表达式建议改为常规函数。
2. lambda表达式的结构较复杂，例如lambda parameter: exp1 if condition1 else (exp2 if condition2 else exp3)类似或更多层嵌套的lambda表达式建议改为常规函数。
3. 标准库operator中已提供的简单运算，不建议再通过重新定义lambda表达式的方法实现，建议直接使用operator中的现有方法。

**【正例】**
1：单个列表处理
- 修复示例：使用函数来处理列表元素
```python
def division(x):
    if x % 5 == 0:
        return x
    elif x % 6 == 0:
        return x
    else:
        return 0

mylist = [3, 4, 36, 25, 56]
# 符合，使用函数代替lambda
mylist_division = map(division, mylist)
```
2：多个列表处理
- 修复示例：使用标准库operator中的mul方法
```python
from operator import mul

vector_first = [1, 2, 3, 4, 5]
vector_last = [5, 4, 3, 2, 1]
# 符合
sum(map(mul, vector_first, vector_last))
```

**【反例】**
1：单个列表处理
- 错误示例：对列表的元素处理，使用过于复杂的lambda表达式
```python
mylist = [3, 4, 36, 25, 56]
# 不符合，lambda表达式过于复杂
mylist_division = map(lambda x: x if x % 5 == 0 else (x if x % 6 == 0 else 0), mylist)
```
2：多个列表处理
- 错误示例：处理2个列表的元素，使用lambda表达式
```python
vector_first = [1, 2, 3, 4, 5]
vector_last = [5, 4, 3, 2, 1]
# 不符合
sum(map(lambda x, y: x*y, vector_first, vector_last))
```

#### G.EXP.03 不应将lambda表达式赋值给变量，应该使用常规函数【建议】

**【描述】**
把lambda表达式赋给一个变量，lambda表达式就可以和其他常规函数一样被调用，但是通过type()查看函数的类型是`<class 'function'>`。
```python
f = lambda x: 2 * x
print(f(3))  # 6
print(type(f))  # <class 'function'>
```
lambda表达式赋值给变量，返回的错误堆栈信息中，显示也是`<lambda>`，从而会导致调试困难。

**【修改建议】**
不要把lambda表达式赋值给变量。

**【正例】**
1：表达式赋值
- 修复示例：把函数赋值给变量，然后调用
```python
def exact_division(x):
    return 10 // x

func = exact_division
# 符合
print(func(0))  # 可以显示出错方法的堆栈信息
```

**【反例】**
1：表达式赋值
- 错误示例：把lambda表达式赋值给变量，然后调用
```python
# 不符合
exact_division = lambda x: 10 // x
print(exact_division(0))  # 此处异常不好调试
```

#### G.EXP.04 推导式和生成器表达式仅用于简单的逻辑表达【建议】

**【描述】**
复杂的推导式和生成器表达式，会伤害代码的易读性，难于阅读，难于理解，难于维护，且不易调试。

**【修改建议】**
慎用复杂的推导式和生成器表达式，可以拆分成多个简单的推导式和生成器表达式。

**【正例】**
1：推导式和生成器表达式的使用
- 修复示例：简单易懂的推导表达式

```python
# 符合
result = [{'key': value} for value in range(10000) if is_odd(value)]

# 符合
result = [{'key': key, 'value': value}
          for key, value in generate_iterable(some_input)
          if predicate(key, value)]

return {key: value
        for x in generate_iterable(parameter)
        if predicate(key, value)}

squares_generator = (x**2 for x in range(10))

unique_names = {user.name for user in users if user}
```

**【反例】**
1：推导式和生成器表达式的使用
- 错误示例：有多个子句，多重循环的推导表达式
```python
# 不符合，多个子句的推导表达式
result = [
(x, y) for x in range(10) for y in range(5) if x * y > 10]

# 不符合，多个循环的推导表达式
return ((x, y, z)
        for x in range(5)
        for y in range(5)
        if x != y
        for z in range(5)
        if y != z)
```

## 2.3 控制语句

#### G.CTL.01 同一个函数所有分支的返回值类型和个数保持一致【要求】

**【描述】**
Python的函数/方法没有显式的返回语句`return`时，会默认返回`None`。如果一个函数/方法的多个分支有的使用显式`return`语句，有的不使用显式`return`，那么对于调用者来说就无法使用一个统一的类型来处理这个函数的返回对象，可能在返回对象的后续处理过程中发生错误。
因此，要求函数/方法要么所有分支都显式地使用`return`语句，要么所有分支都隐式地不使用`return`语句，即默认返回`None`。
另外，当函数/方法的所有分支返回语句都采用显式的时候，建议非None返回值的分支返回值类型和个数保持一致。

**【修改建议】**
同一个函数所有分支的返回值类型和个数保持一致。

**【正例】**
```python
INVALID_VALUE = -1

def function_with_return_statement(x):
    if x >= 0:
        return x + 1
    else:
        return INVALID_VALUE  

def function_return_type_consistent(x):
    if x < 0:
        return INVALID_VALUE  
    return x + 1
```

也可以使用类型注解，显式地提示出函数/方法预期的返回对象类型。需要注意的是，类型注解并不真正检查返回值类型和参数类型，只是一种预期。
```python
INVALID_VALUE = -1

def function_with_return_statement(x: int) -> int:
    if x >= 0:
        return x + 1
    else:
        return INVALID_VALUE 

def function_return_type_consistent(x: int) -> int:
    if x < 0:
        return INVALID_VALUE 
    return x + 1
```

**【反例】**
下面的函数都包含`if`条件分支，但多分支的返回对象类型不一致。
```python
def function_with_no_else_return_statement(x):
    if x >= 0:
        return x + 1

def function_return_type_inconsistent(x):
    if x < 0:
        return
    return  x + 1
```

#### G.CTL.02 所有的代码都必须是逻辑可达的【要求】

**【描述】**
跳转语句（return, break, continue 和 raise）将会使程序执行跳出当前代码块。跳转语句所在代码块中，在它之后的代码及代码块将永远无法执行到。
这类代码虽然一时无法被执行到，但后续附近代码的修改有可能会触发到它们的执行，存在潜在风险。因此，这类逻辑不可达的代码需要删除掉。

**【修改建议】**
必须保持代码逻辑可达。

**【正例】**
修改方法：要么清理无法执行到的代码，要么调整代码位置，把逻辑修改正确。
```python
def function_with_return_no_dead_code(a):
    i = 10
    return i + a
```

```python
def function_with_raise_no_dead_code(a):
    if a:
        return a
    else:
        do_something_else()  # 如果do_something_else确实需要执行，那么调整它的位置
        raise Exception("invalid value")
```

**【反例】**
下面的几段代码都存在一些无法被执行到的代码。
```python
def function_with_return_dead_code(a):
    i = 10
    return i + a
    i += 1  # 这里的代码无法被执行到
```

```python
def function_with_raise_dead_code(a):
    if a:
        return a
    else:
        raise Exception("invalid value")
        do_something_else()  # 这里的处理将永远无法被执行
```

#### G.CTL.03 避免在条件/循环控制语句中包含过多的条件【建议】

**【描述】**
控制性条件表达式if语句中如果包含过多的条件，会对阅读者造成理解与记忆上的困难，也会在修改时更容易出错，使代码不易维护，可读性差。因此，避免在条件/循环控制语句中包含过多的条件，建议在if语句中的表达式尽量清晰直接，避免陷入具体的条件判断细节。

**【修改建议】**
1. if语句中的表达式应清晰直接，并且建议不超过3个，可以根据具体逻辑决定。
2. 条件判断细节可以在使用`if`条件判断之前用`bool`变量代替或`封装函数/方法`。

**【正例】**
1：if判断语句条件过多
- 修复示例：将if语句判断条件合并，用`bool`变量代替
```python
is_activity_valid = activity.is_active and activity.remaining > 10
is_user_valid = user.is_active and (user.sex == 'female' or user.level > 3)
if is_activity_valid and is_user_valid:  # 符合，此处的逻辑应清晰直接，建议在同一抽象层次上，不要陷入细节
    user.add_coins(1024)
```

**【反例】**
1：if判断语句条件过多
- 错误示例：
```python
if activity.is_active and activity.remaining > 10 and \\
        user.is_active and (user.sex == 'female' or user.level > 3):  # 不符合，此处的逻辑非常多，阅读困难，修改容易出错
    user.add_coins(1024)
```

#### G.CTL.04 建议使用 for x in iterable 的方式循环处理可迭代对象【建议】

**【描述】**
使用`for i in range(x):`语句，然后在循环体内对序列用下标[i]获取元素是一种较为传统的编程习惯，它有很多缺点：容易越界；在循环体内修改i容易出错；可读性差。因此，建议尽量使用`for x in iterable:`的方式，直接取序列中的每一个对象进行处理。

**【修改建议】**
1. 使用 for x in iterable 的方式循环处理可迭代对象。
2. 有些场合下，需要在处理时使用每个元素的序号，这时可以使用`enumerate`内置函数来给元素加上序号形成元组。

**【正例】**
1：遍历列表
- 修复示例1：使用 for x in iterable 的方式直接循环遍历列表
```python
for x in my_list:  # 符合，使用迭代器直接循环遍历列表
    do_something(x)
```
- 修复示例2：有些场合下，需要在处理时使用每个元素的序号，这时可以使用`enumerate`内置函数来给元素加上序号形成元组：
```python
my_list = ['a', 'b', 'c'] 

for i, x in enumerate(my_list):  # 符合
    print(i, x)
```

**【反例】**
1：遍历列表
- 错误示例：通过遍历列表长度来遍历列表
```python
for i in range(len(my_list)):  # 不符合，遍历列表使用长度遍历
    do_something(my_list[i])
```

#### G.CTL.05 建议使用单个下划线代替循环体中未使用的循环变量【建议】

**【描述】**
在for循环代码块中定义未使用的循环变量，虽然并不会造成功能问题，但是会导致代码中出现冗余变量，可能会导致性能降低。

**【修改建议】**
保证循环里的变量被使用，如果不使用，使用单个下划线`_`或双下划线`__`代替。

**【正例】**
1：循环变量未使用
- 修复示例：用下划线代替循环未使用变量
```python
def function_loop_with_underscore():
    # 符合，未使用的循环变量用_下划线代替
    for _ in range(32):
        do_something_several_times()
```

**【反例】**
1：循环变量未使用
- 错误示例：定义了一些冗余变量
```python
def function_loop_with_unused_loop_variable():
    # 不符合，i是冗余的循环变量
    for i in range(32):
        do_something_several_times()
```

#### G.CTL.06 避免出现死循环【建议】

**【描述】**
死循环会导致程序卡死，建议不要使用存在"死循环"风险的迭代或循环。
包括但不限于以下情况：
- 存在循环变量不被修改的情况或修改循环变量的路径不可达。
- 无退出条件的循环。

**【修改建议】**
1. 保证循环变量的路径可达并且可以被修改。
2. while条件语句永真的情况下，保证循环代码中存在退出条件。也可以使用异常退出循环。

**【正例】**
1：循环变量的路径不可达
- 修复示例：保证循环变量的路径总是可达
```python
condition = 0

while condition < 5:
    ...
    condition += 1  # 符合
```
2：循环变量不被修改
- 修复示例：保证循环变量可以被修改
```python
condition = 0
count = 0

while condition < 5:
    ...
    count += 1  
    condition += 1  # 符合
```
3：无退出条件的循环
- 修复示例1：采用条件退出
```python
while True:
    if timeout:  # 符合，条件退出
        break
```
- 修复示例2：采用异常退出
```python
try:
    while True:
        ...
        # raise EOFError
except EOFError as e:
    ...  # 符合，采用异常退出
```

**【反例】**
1：循环变量的路径不可达
- 错误示例：
```python
condition = 0

while condition < 5:
    ...
    if False:  # 不符合，循环变量的路径不可达
        condition += 1 
```
2：循环变量不被修改
- 错误示例：
```python
condition = 0
count = 0

while condition < 5:
    count += 1  # 不符合，循环变量不被修改
```
3：无退出条件的循环
- 错误示例：
```python
while True:
    ...  # 不符合，无退出条件的循环
```

## 2.4 函数与方法

#### G.FNM.01 禁止使用可变对象作为参数默认值【要求】

**【描述】**
在Python程序中，函数的参数默认值只会被初始化一次，并且被重复利用，当参数默认值为可变对象时，若函数调用时不传入参数值，则对该参数的默认值进行的任何操作实际上操作的是同一个对象，这可能会引发一些不可预知的错误。

**【修改建议】**
仅可使用不可变对象作为参数默认值，例如：bool、int、float、complex、tuple、str、bytes、frozenset、None。

**【正例】**
1：函数列表参数
- 修复示例：使用None作为默认值，在程序中重新初始化为空列表
```python
#  符合，函数参数使用None作为默认值，在函数体中初始化列表
def fun(arg_a, list_arg=None):
    list_arg = list_arg or []
    list_arg.append(arg_a)
    print(list_arg)

fun(1)  # 打印[1]
fun(1)  # 打印[1]
fun(1, [])  # 打印[1]
fun(1, {})  # 打印[1]
fun(1, ())  # 打印[1]
fun(1, False)  # 打印[1]
```
2：函数字典参数
- 修复示例：使用None作为默认值，在程序中重新初始化为空字典
```python
# 符合，函数参数使用None作为默认值，在函数体中初始化字典
def fun(arg_a, list_arg=None):
    list_arg = {} if list_arg is None else list_arg
    list_arg[arg_a] = arg_a
    print(list_arg)
```

**【反例】**
1：函数列表参数
- 错误示例：使用空列表作为默认值 
```python
# 不符合，函数参数使用空列表作为默认值
def fun(arg_a, list_arg=[]):
    list_arg.append(arg_a)
    print(list_arg)

fun(1)      # 打印[1]
fun(1)      # 打印[1, 1]
fun(1, [])  # 打印[1]
```
2：函数字典参数
- 错误示例：使用空字典作为默认值
```python
# 不符合，函数参数使用空字典作为默认值
def fun(arg_a, list_arg={}):
    list_arg[arg_a] = arg_a
    print(list_arg)

fun(1)      # 打印{1: 1}
fun(2)      # 打印{1: 1, 2: 2}
fun(3, {})  # 打印{3: 3}
```

#### G.FNM.02 函数和lambda表达式不应该使用外部的循环代码中定义的变量【建议】

**【描述】**
如果在循环体中定义了函数/lambda并引用了循环变量，则在循环体外调用该函数时，将始终获取到该循环变量的终值，导致结果与预期不一致。

**【修改建议】**
lambda表达式不能引用循环变量，如果在循环中立即调用函数或使用lambda表达式，而不是循环结束之后才调用或使用，可以在函数或lambda表达式中使用外部循环中的变量。

**【正例】**
1：lambda表达式使用外部循环变量
- 修复示例：如果在循环中立即调用函数或使用lambda表达式，而不是循环结束之后才调用或使用，可以在函数或lambda表达式中使用外部循环中的变量。
下述代码示例中，list是强制进行计算并转为list格式，是立即执行的。
```python
for i in range(5):
    print(list(map(lambda j: i + j, range(5))))  # 符合

执行结果：
 [0, 1, 2, 3, 4]
 [1, 2, 3, 4, 5]
 [2, 3, 4, 5, 6]
 [3, 4, 5, 6, 7]
 [4, 5, 6, 7, 8]
```
2：函数中使用外部循环变量
- 修复示例：嵌套函数不引用循环变量，将函数与参数值同时保存，形成[(函数,参数)]的映射列表。
```python
def test():
    """循环打印出0到4"""
    func_list = []
    def func(value):
        return value

    for i in range(5):
        func_list.append((func, i)  # 符合

    for func, arg in func_list:
        print(func(arg))

test()
```

**【反例】**
1：lambda表达式使用外部循环变量
- 错误示例：第一个for循环使用的是map，map是延期执行的
```python
map_list = []
for i in range(5):
    # 不符合，循环中使用lambda，延迟调用
    map_list.append(map(lambda j: i + j, range(5)))

for unit in map_list:
    print(list(unit))

执行结果：
[4, 5, 6, 7, 8]
[4, 5, 6, 7, 8]
[4, 5, 6, 7, 8]
[4, 5, 6, 7, 8]
[4, 5, 6, 7, 8]
```
2：函数中使用外部循环变量
- 错误示例：嵌套函数中采用了外部循环体的循环变量。
代码本意：循环打印出0~4
实际结果：重复打印4
```python
def test():
    """循环打印出0到4"""
    func_list = []
    for i in range(5):
        def func():
            return i  # 不符合

        func_list.append(func)

    for func in func_list:
        print(func())

test()
```

#### G.FNM.03 当函数参数个数较多且有相关性时，建议通过class/namedtuple/dataclass等具名形式进行封装【建议】

**【描述】**
函数参数过多，会导致代码可读性差，难以理解。

**【修改建议】**
当函数参数个数较多(一般多于5个)，并且参数之间有一定相关性时，建议通过class/namedtuple(具名元组)/dataclass等具名形式进行封装。

**【正例】**
1：函数参数个数较多
- 修复示例：采用dataclass进行数据封装，适用于Python3.7以上版本
```python
from dataclasses import dataclass

@dataclass
class Student:
    name: str
    age: int
    gender: str
    height: int

#  符合，函数参数过多，使用dataclass进行封装
def process_student_info(student):
    print(student.name)

freshman = Student("nn", 12, "male", None)
process_student_info(freshman)
```
- 修复示例：采用具名元组进行数据封装
```python
import collections

Student = collections.namedtuple('Student', ['name', 'age', 'gender', 'height', 'weight', 'education', 'religion'])

# 符合，函数参数过多，使用namedtuple进行封装
def process_student_info(student):
    # do something here
    ...

freshmen = Student("bob", 12, "male", None, None, None, None)
process_student_info(freshmen)
```
- 修复示例：采用类进行数据封装
```python
class Student:
    def __init__(self, name, age, gender, height=None, weight=None, education=None, religion=None): 
        self.name = name
        self.age = age
        self.gender = gender
        self.height = height
        ...

# 符合，函数参数过多，使用类进行封装
def add_freshmen(student):
    # do something here
    ...

freshmen = Student("bob", 19, "male")
add_freshmen(freshmen)
```

**【反例】**
1：函数参数个数较多
- 错误示例：函数参数超过5个
```python
#  不符合，函数参数超过5个
def add_freshmen(name, age, gender, height, weight, education, religion):
    ...

#  不符合，函数参数超过5个
add_freshmen("bob", 19, "male", None, None, None, None)
```

#### G.FNM.04 不要将没有返回值的函数调用结果赋值给变量【要求】

**【描述】**
将没有返回值的函数调用赋值给变量时，变量实际被赋值为None，没有意义，会导致代码冗余。

**【修改建议】**
不要将没有返回值的函数调用结果赋值给变量。

**【正例】**
1：没有返回值的函数赋值给变量
- 修复示例：有返回值的函数赋值给变量
```python
def division_if_success_return_true(x, y):
    try:
        print(x / y)
    except ZeroDivisionError:
        return False
    return True

# 符合，函数返回值赋值给变量
result = division_if_success_return_true(1, 2)
```

**【反例】**
1：没有返回值的函数赋值给变量
- 错误示例：没有返回值的函数赋值给变量
```python
def division(x, y):
    try:
        print(x / y)
    except ZeroDivisionError:
        print('除数不能为0')

# 不符合，函数没有返回值
result = division(1, 2)
```

#### G.FNM.05 当函数返回值个数较多时，建议通过class/namedtuple等具名形式进行封装【建议】

**【描述】**
函数返回值过多，会导致代码可读性差，代码复杂度增加，难以理解。

**【修改建议】**
函数返回值最好不要超过3个，超过时通过class/namedtuple/dataclass等具名形式进行封装。

**【正例】**
1：函数返回值个数较多
- 修复示例：采用类进行数据封装
```python
class Student:
    def __init__(self, name, age, gender, height=None, weight=None, education=None, religion=None):
        self.name = name
        self.age = age
        self.gender = gender
        self.height = height
        ...

def get_student_info(id):
    # get info from database
    ...
    # 符合，返回值使用类封装
    student = Student("bob", 19, "male")
    return student
```
- 修复示例：采用具名元组进行数据封装
```python
import collections

Student = collections.namedtuple("Student", ["name", "age", "gender", "height", "weight", "education", "religion"])

def get_student_info(id):
    # get info from database
    ...
    # 符合，返回值使用元组封装
    student = Student("bob", 12, "male", None, None, None, None)
    return student
```
- 修复示例：采用dataclass进行数据封装
```python
from dataclasses import dataclass

@dataclass
class Student:
    name: str
    age: int
    gender: str
    height: int

def get_student_info(id):
    # get info from database
    ...
    # 符合，返回值使用dataclass封装
    student = Student("jack", 18, "male", 170)
    return student
```

**【反例】**
1：函数返回值个数较多
- 错误示例：函数返回值超过3个
```python
def get_student_info(id):
    # get info from database
    ...
    # 不符合，函数返回值超过3个
    return name, age, gender, height, weight, education, religion
```

#### G.FNM.06 使用return代替StopIteration来结束生成器【要求】

**【描述】**
使用return代替StopIteration来结束生成器。

使用`return`代替`raise StopIteration`来结束生成器的迭代。从Python3.7开始，生成器退出时的`StopIteration`将会被解释器转换成`RuntimeError`。

**【修改建议】**
用`return`代替`raise StopIteration`来结束生成器的迭代

**【正例】**
1：raise StopIteration 结束生成器
- 修复示例：用 return 来结束生成器的迭代
```python
def correct_example():
    for i in range(100):
        if i == 10:
            return  # 符合，当函数执行到return时候，__next__()会抛出异常，直接终止当前生成器
        yield i

for i in correct_example():
    print(i)  # for循环会自动捕获该异常，直接停止遍历
```

**【反例】**
1：raise StopIteration 结束生成器
- 错误示例：
```python
def wrong_example():
    for i in range(100):
        if i == 10:
            raise StopIteration()  # 不符合，i等于10时，这里抛出一个异常
        yield i

for i in wrong_example():
    print(i)  # for循环并不会自动捕获该异常，程序将报错，这显然不是我们所预期的
```

#### G.FNM.07 建议妥善处理函数的返回值和异常【建议】

**【描述】**
当函数的调用没有产生任何作用同时忽略了函数的返回值，即函数返回值既未参与程序业务逻辑处理，函数的调用也无需进行预期异常和相应返回值的处理，在这种情况下函数无需调用，应及时删除。当函数通常通过返回值返回数据或执行结果时，调用者应该在函数调用之后，对返回数据及执行结果进行有效、正确的合法性检出和处理。

**【反例】**
```python
import sys

def test():
    return "shjayei"

if __name__ == "__main__":
    test()
    sys.exit(0)
```

```python
import sys

def test():
    ...
    try:
        ...
    except UserDefined.UnrecoverableException as e:
        do_something(e)
        raise e  # 重新抛出异常UserDefined.UnrecoverableException

if __name__ == "__main__":
    test()
    sys.exit(0)
```

```python
def get_api():
    status_code = to_be_called()
    if status_code >= 0:
        ...
    # 缺少失败场景返回值的检查
```

**【正例】**
```python
import sys

def test(x, y):
    x, y = map(int, [x, y])
    return x / y

if __name__ == "__main__":
    try:
        test(sys.argv[1], sys.argv[2])
    except ZeroDivisionError:
        sys.exit(1)
    sys.exit(0)
```

```python
def get_api():
    status_code = to_be_called()
    if status_code == -1: # 失败场景返回值检查
        ...
    if status_code >= 0:
        ...
```

## 2.5 变量作用域

#### P.04 合理使用全局变量【建议】

**【描述】**
全局变量使用建议遵守以下原则：
1. 使用全局变量会导致业务代码和全局变量之间产生数据耦合，且很难跟踪数据的变化，建议避免使用全局变量
2. 建议使用模块级的常量，并将有相关关系的常量设计为枚举或者类常量，而不是分散在全局。但是不建议将所有的常量定义到一个常量类或者模块中，避免出现“口袋”类和模块
3. 如果需要定义模块级全局变量，应该通过命名（以_开头）将全局变量声明为模块的内部变量，并且将其排除在__all__之外
4. 如果需要定义模块外可以访问的全局变量，不应该使用以`_, __`开头的命名，并应包含在`__all__`内
5. 变量或者常量都应该放在与它表达的业务相关的地方

**【正例】**
```python
# 模块内全局变量
_global = object()

# 全局可见的全局变量
overall_global = object()

# 全局常量
CONSTANT = 60 * 70
```

#### G.VAR.01 禁止在变量的生命周期内修改其类型【要求】

**【描述】**
在变量的生命周期内，如果变量被赋值为不同类型对象，可能会导致运行时错误，另外变量上下文语义的变化会导致代码复杂度提升，从而难以调试和维护，也不会有任何性能的提升。因此，给变量赋值时，值的类型应该和变量的类型匹配，禁止变量在其生命周期内的值类型发生变化。

**【修改建议】**
保证变量在生命周期内部不改变其类型。

**【正例】**
1：变量类型被改变
- 修复示例：
```python
variable: int = 1
variable = 2  # 符合
```

**【反例】**
1：变量类型被改变
- 错误示例：
```python
variable: str = 1  # 不符合
variable = b'hello world'
```

#### G.VAR.02 禁止使用global关键字声明不存在的外部变量【要求】

**【描述】**
使用`global`关键字声明不存在的外部变量，导致代码可读性差、难以维护，还可能会引发一些不可预知的错误。因此，禁止使用`global`关键字声明不存在的外部变量。

**【修改建议】**
1. 禁止使用global关键字声明不存在的外部变量。
2. 函数中修改全局变量时，需要使用`global`进行声明，对于仅需要读的场景，不需要使用`global`关键字。

**【正例】**
1：global声明不存在的外部变量
- 修复示例：函数中修改全局变量时，需要使用`global`进行声明
```python
_variable = 1

def test():
    global _variable  # 符合
    _variable = 2

test()
print(_variable)
```

**【反例】**
1：global声明不存在的外部变量
- 错误示例：外部作用域中没有全局变量`variable`，在`test`函数内使用`global`创建了全局变量`variable`，这是不好的实践。
```python
def test():
    global variable  # 不符合，不存在全局变量variable
    variable = 1

test()
print(variable)
```
- 错误示例：函数中仅读取全局变量时，不需要使用`global`进行声明。
```Python
_variable = 1

def test():
    global _variable  # 不符合，仅读取全局变量时，不需要使用global进行声明
    print(_variable)

test()
```

#### G.VAR.03 禁止覆盖外部作用域中的标识符【要求】

**【描述】**
禁止出现当前局部作用域遮盖更外层作用域中的标识符，给阅读者带来困扰，无法清晰知道在使用哪个变量。

**【修改建议】**
避免局部变量和全局变量重名，以及参数，导入对象和本模块内部对象重名等。

**【正例】**
1：局部变量和全局变量重名
- 修复示例：修改局部变量名称避免和外部变量重名
```python
_global = 1

def test():
    local_number = 2  # 符合
    if local_number == _global:
        raise MyException
```

**【反例】**
1：局部变量和全局变量重名
- 错误示例：函数内部变量和外部的变量重名
```python
_global = 1

def test():
    _global = 2  # 不符合, 更外层作用域（模块命名空间）中变量被遮盖
    ...
```

## 2.6 类与面向对象

#### G.CLS.01 如果子类和父类中都有__init__ 方法，则子类中的__init__ 方法必须正确调用其父类__init__ 方法【要求】

**【描述】**
如果子类和父类都有`__init__`初始化方法，子类其实是重写了父类的`__init__`方法，如果不显式调用父类的`__init__`方法，父类的`__init__`方法就不会被执行，导致子类实例访问父类`__init__`方法中初始化的变量时出现问题。
因此，如果子类和父类都有初始化方法，则子类必须在自己的初始化方法中调用父类的初始化方法。

**【修改建议】**
在子类中使用super.__init__方法来调用父类的初始化方法。

**【正例】**
单继承场景，子类调用父类初始化方法。
```python
class Base:
    def __init__(self):
        self.base_attr = 1

class Derived(Base):
    def __init__(self):
        super().__init__()
        self.derived_attr = 2

if __name__ == '__main__':
    derived_obj = Derived()
    print(derived_obj.base_attr)  # 1
```

**【反例】**
单继承场景，不调用父类初始化方法，导致父类初始化过程遗漏。
```python
class Base:
    def __init__(self):
        self.base_attr = 1

class Derived(Base):
    def __init__(self):
        self.derived_attr = 2

if __name__ == '__main__':
    derived_obj = Derived()
    print(derived_obj.base_attr)  # AttributeError: 'Derived' object has no attribute 'base_attr'
```

#### G.CLS.02 重写方法的方法签名应该和被重写的方法一致【建议】

**【描述】**
子类重写父类方法时，如果方法签名不一致，则会覆盖父类同名方法的实现。这种重写行为违反了里氏替换原则，使子类丢失了一部分父类功能。从而会导致程序出现意外的结果。

**【修改建议】**
子类重写父类方法时，方法签名保持一致，当方法签名不一致的情况下，选择放弃重写继承原方法，新的功能创建子类方法实现。

**【正例】**
1：类方法继承
- 修复示例：子类继承方法签名不改变
```python
class Base:
    def __init__(self):
        self.base_attr = 1

    @property
    def length(self):
        return self.base_attr

class Derived(Base):
    def __init__(self):
        self.derived_attr = 2

    # 符合
    @property
    def length(self):
        return self.derived_attr
```

**【反例】**
1：类方法继承
- 错误示例：子类继承方法从普通方法改为属性
```python
class Base:
    def __init__(self):
        self.base_attr = 1

    def length(self):
        return self.base_attr

class Derived(Base):
    def __init__(self):
        self.derived_attr = 2

    # 不符合，继承基类方法时更改了方法的性质
    @property
    def length(self):
        return self.base_attr
```

#### G.CLS.03 建议避免在继承内置类型的同时重写其魔法函数【建议】

**【描述】**
自定义类可以继承自Python的内置类型(如int, list, dict)。当自定义类继承自这些内置类型时，需要额外注意其魔法函数的完整性，因为这些内置类型的魔法函数之间通常是有关联的，修改其中一个通常意味着要联动修改另一个和它相关的魔法函数，否则会出现预期之外的执行结果。

**【正例】**
使用组合代替继承（推荐）
```python
class CustomList:
    def __init__(self, items=None):
        self._data = list(items) if items else []  # 组合内置的 list

    def append(self, item):
        self._data.append(item)

    def __len__(self):
        return len(self._data)

    def __getitem__(self, index):
        return self._data[index]

# 使用示例
cl = CustomList([1, 2, 3])
print(cl[0])  # 输出: 1
```

**【反例】**
单独重写 __add__ 导致不一致
```python
class BadList(list):
    def __add__(self, other):
        # 只重写 __add__，未考虑 __iadd__ 或 __radd__
        return BadList(super().__add__(other))

# 问题1：+= 操作（__iadd__）未被覆盖，行为不一致
bl = BadList([1, 2])
bl += [3]  # 调用 list.__iadd__，返回普通 list，而非 BadList
print(type(bl))  # 输出: <class 'list'>（预期应为 BadList）

# 问题2：反向加法（__radd__）未实现
try:
    result = [0] + BadList([1, 2])  # 报错：TypeError
except TypeError as e:
    print(e)
```

错误继承 dict 并破坏键查找
```python
class BadDict(dict):
    def __getitem__(self, key):
        # 重写 __getitem__ 但忽略 get() 或 pop() 等方法
        return super().__getitem__(key) * 2

bd = BadDict({"a": 1})
print(bd["a"])  # 输出: 2（符合预期）
print(bd.get("a"))  # 输出: 1（不符合预期，未联动修改）
```

#### G.CLS.04 建议在实现抽象类时使用abc模块【建议】

**【描述】**
面向对象程序设计有抽象类的概念，实例化抽象类会报错，且抽象类的子类如果不实现抽象类中定义的抽象方法时，子类也无法实例化。
这种抽象类经常被用于面向对象设计者表达自己的设计意图，并且要求后续的开发者严格按照自己的设计来泛化实现。
Python程序中设计抽象类时如果使用普通的类作为父类，那么将无法享受到抽象类带来的强约束收益，因此，在需要实现抽象类时正确地使用abc模块相关类型，保证抽象类的强约束功能，从而使抽象设计不被轻易破坏。

**【正例】**
正确使用 abc 模块
```python
from abc import ABC, abstractmethod

# 抽象类：定义必须实现的方法
class Animal(ABC):
    @abstractmethod
    def make_sound(self):
        """子类必须实现此方法"""
        pass

    @abstractmethod
    def move(self):
        """子类必须实现此方法"""
        pass

# 子类必须实现所有抽象方法
class Dog(Animal):
    def make_sound(self):
        return "Woof!"

    def move(self):
        return "Running on four legs"

# 正确实例化
dog = Dog()
print(dog.make_sound())  # 输出: Woof!

# 如果子类未实现所有抽象方法，会抛出 TypeError
class Cat(Animal):
    def make_sound(self):
        return "Meow!"

# 报错：TypeError: Can't instantiate abstract class Cat with abstract method move
# cat = Cat()  # 这行会报错
```

**【反例】**
普通基类（无约束）
```python
# 普通基类（无强制约束）
class Animal:
    def make_sound(self):
        """子类 '应该' 实现，但不会强制检查"""
        raise NotImplementedError("子类必须实现 make_sound()")

    def move(self):
        """子类 '应该' 实现，但不会强制检查"""
        raise NotImplementedError("子类必须实现 move()")

# 子类可以只实现部分方法，甚至不实现
class LazyDog(Animal):
    def make_sound(self):
        return "Woof!"

# 实例化时不会报错，但调用未实现的方法时会抛出异常
dog = LazyDog()
print(dog.make_sound())  # 输出: Woof!
# dog.move()  # 运行时抛出 NotImplementedError
```

#### G.CLS.05 子类调用父类初始化方法的方式，建议使用super类辅助【建议】

**【描述】**
Python中子类调用父类初始化方法一般有以下两种方式：

- 使用父类类名`ClassName.__init__(self)`的方式，这种写法比较清晰易懂，但是与父类类名绑定，而且在菱形继承场景下顶层父类初始化函数会被调用多次。
- 使用`super`类的方式调用父类初始化方法，这种写法不与父类类名绑定，且可以保证菱形继承场景下，创建一个子类对象仅调用顶层父类初始化函数一次。

因此，子类调用父类初始化方法的方式建议使用`super`类。

**【修改建议】**
子类调用父类初始化方法的方式建议使用`super`类辅助。

**【正例】**
1：菱形继承场景
- 修复示例：使用super代替类名调用
```python
class Ancestor:
    def __init__(self, **kwargs):
        print("ancestor initialize invoked")

class Base(Ancestor):
    def __init__(self, base_attr, **kwargs):
        super().__init__(**kwargs)  # 符合
        self.base_attr = base_attr

class BaseTwo(Ancestor):
    def __init__(self, base_two_attr, **kwargs):
        super().__init__(**kwargs)  # 符合
        self.base_two_attr = base_two_attr

class Derived(Base, BaseTwo):
    def __init__(self, base_attr, base_two_attr, derived_attr, **kwargs):
        super().__init__(base_attr=base_attr, base_two_attr=base_two_attr, **kwargs)  # 符合
        self.derived_attr = derived_attr

if __name__ == '__main__':
    derived_obj = Derived(base_attr=1, base_two_attr=2, derived_attr=3)  # ancestor initialize invoked
    print(derived_obj.base_attr) 
    print(derived_obj.base_two_attr) 
    print(derived_obj.derived_attr) 
```

**【反例】**
1：菱形继承场景
- 错误示例：如果直接使用类名调用`__init__`方法，将造成Ancestor类的初始化方法被调用两次
```python
class Ancestor:
    def __init__(self):
        print("ancestor initialize invoked")

class Base(Ancestor):
    def __init__(self, base_attr):
        Ancestor.__init__(self)  # 不符合，未使用super方式调用基类方法
        self.base_attr = base_attr

class BaseTwo(Ancestor):
    def __init__(self, base_two_attr):
        Ancestor.__init__(self)  # 不符合，未使用super方式调用基类方法
        self.base_two_attr = base_two_attr

class Derived(Base, BaseTwo):
    def __init__(self, base_attr, base_two_attr, derived_attr):
        Base.__init__(self, base_attr)
        BaseTwo.__init__(self, base_two_attr)
        self.derived_attr = derived_attr

if __name__ == '__main__':
    derived_obj = Derived(1, 2, 3)  # "ancestor initialize invoked" will print twice.
    print(derived_obj.base_attr)  # 1
    print(derived_obj.base_two_attr)  # 2
    print(derived_obj.derived_attr)  # 3
```

#### G.CLS.06 类的方法建议统一按照一种规则进行排列【建议】

**【描述】**
按照业界约定俗成的顺序来组织类的方法，否则会导致代码可读性差，代码组织结构混乱。

**【修改建议】**
建议类的多个方法按照如下的顺序组织：
1. `__new__`静态方法
2. `__init__`方法
3. `__post_init__`方法
4. 其它魔法函数
5. `@property`修饰的对象属性
6. `@staticmethod`修饰的静态方法
7. `@classmethod`修饰的类方法
8. 普通方法
9. 保护方法或私有方法

**【正例】**
1：staticmethod和classmethod方法的顺序
- 修复示例：staticmethod和classmethod定义在__init__方法之后，并且staticmethod在classmethod之前
```python
class A(object):
    def __init__(self):  #  符合
        self.name = 'huawei_rule'

    @staticmethod
    def sample_static_method():
        print('called')

    @classmethod
    def sample_cls_method(cls):
        cls.sample_static_method()
```

**【反例】**
1：staticmethod和classmethod方法的顺序
- 错误示例：staticmethod和classmethod定义在__init__方法之前
```python
class A(object):
    @classmethod
    def sample_cls_method(cls):
        cls.sample_static_method()

    @staticmethod
    def sample_static_method():
        print('called')

    def __init__(self):  #  不符合
        self.name = 'huawei_rule'
```

#### G.CLS.07 类的方法不需要访问实例时，建议定义为staticmethod或classmethod【建议】

**【描述】**
类的方法不需要访问实例时，使用普通的实例方法定义虽然可以实现功能，但会在使用时要求必须由类的实例调用此方法。这就造成使用过程中一次冗余的实例生成、回收过程，代码本身编写和阅读时也显得冗余。

**【修改建议】**
1. 在不需要访问实例，需要访问类属性或方法时，建议使用`@classmethod`将方法定义为类方法；
2. 在不需要访问实例也不需要访问类属性或方法时，建议使用`@staticmethod`将方法定义为静态方法。

**【正例】**
1：类的方法不需要访问实例
- 修复示例：类方法不需要访问类实例，使用classmethod或者staticmethod
```python
class MyClass:
    class_attr = "MyClass.class_attr"

    @classmethod
    def refresh_class_attr(cls, string_value: str):  # 符合
        cls.class_attr = string_value

    @staticmethod
    def add(a: int, b: int) -> int:  # 符合
        return a + b

if __name__ == '__main__':
    MyClass.refresh_class_attr("Refreshed MyClass.class_attr")
    print(MyClass.class_attr)  # "Refreshed MyClass.class_attr"
    print(MyClass.add(1, 2))  # 3
```

**【反例】**
1：类的方法不需要访问实例
- 错误示例：
```python
class MyClass:
    class_attr = "MyClass.class_attr"

    def refresh_class_attr(self, string_value: str):  # 不符合，在不需要访问实例，需要访问类属性或方法
        MyClass.class_attr = string_value

    def add(self, a: int, b: int) -> int:  # 不符合，不需要访问实例也不需要访问类属性或方法
        return a + b

if __name__ == '__main__':
    MyClass().refresh_class_attr("Refreshed MyClass.class_attr")
    print(MyClass.class_attr)  # "Refreshed MyClass.class_attr"
    print(MyClass().add(1, 2))  # 3
```

#### G.CLS.08 禁止在__init__ 方法外定义实例属性【建议】

**【描述】**
在其它实例方法中定义`__init__`不包含的新属性在功能上虽然没有问题，但会造成多个类实例属性的存在生命周期不一致，为后续跨方法访问埋下隐患。因此，应避免在`__init__`方法外定义类实例属性。

**【修改建议】**
1. 实例方法中使用的类实例属性，可以定义在`__init__`方法中，保证在访问时必然存在。
2. 也可以在`__init__`方法中调用的初始化功能的私有方法。

**【正例】**
1：在其它实例方法中定义__init__不包含的新属性
- 修复示例1：实例方法中使用的类实例属性，可以定义在`__init__`方法中，保证在访问时必然存在，不会出现`AttributeError`异常。
```python
class Coder:
    def __init__(self, key_board="no key_board", mouse="no mouse", headphone="no headphone"):
        self.key_board = key_board
        self.mouse = mouse
        self.headphone = headphone  # 符合

    def obtain_headphone(self, headphone):
        self.headphone = headphone

if __name__ == '__main__':
    coder = Coder(key_board="logitech key_board", mouse="logitech mouse")
    ...
    my_equipments = f'I have got {coder.key_board}, {coder.mouse} and {coder.headphone}.'   # I have got logitech key_board, logitech mouse and no headphone.
    print(my_equipments)
```
- 修复示例2：也可以在`__init__`方法中调用的初始化功能的私有方法。
如下案例，私有方法`_set_headphone 和_headphone_primary_equipment`在` __init__`方法中调用了，可以保证在访问时必然存在，不会出现`AttributeError`异常。
```python
class Coder:
    def __init__(self, key_board="no key_board", mouse="no mouse"):
        self._set_secondary_equipment()
        self._set_primary_equipment(key_board, mouse)  #  符合

    def _set_secondary_equipment(self):
        self.headphone = "no headphone"

    def _set_primary_equipment(self, key_board, mouse):
        self.key_board = key_board
        self.mouse = mouse

    def obtain_headphone(self, headphone):
        self.headphone = headphone
```

**【反例】**
1：在其它实例方法中定义__init__不包含的新属性
- 错误示例：headphone`是程序运行时通过调用实例方法`obtain_headphone`为`coder`对象添加的属性。在组织`my_equipments`字符串时，如果没有调用过`obtain_headphone`方法，则很容易出现`AttributeError`异常。
```python
class Coder:
    def __init__(self, key_board="no key_board", mouse="no mouse"):
        self.key_board = key_board
        self.mouse = mouse

    def obtain_headphone(self, headphone):
        self.headphone = headphone  # 不符合

if __name__ == '__main__':
    coder = Coder(key_board="logitech key_board", mouse="logitech mouse")
    my_equipments = f'I have got {coder.key_board}, {coder.mouse} and {coder.headphone}.'  # AttributeError: 'Coder' object has no attribute 'headphone'
    print(my_equipments)
```

#### G.CLS.09 重写类的魔法函数时必须返回其原型指定的类型【要求】

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__bool__`时与其原型返回类型bool不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数时`__bool__`返回bool类型。

**【正例】**
1：`__bool__`返回类型
- 修复示例： 重写`__bool__`应该返回一个bool类型，True or False
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __bool__(self):
        return True if self.objs_repo else False  # 符合
```

**【反例】**
1：`__bool__`返回类型
- 错误示例：  __bool__返回要求bool类型，此处返回int
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __bool__(self):
        return len(self.objs_repo)  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__bytes__`时与其原型返回类型bytes不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数时`__bytes__`返回bytes类型。

**【正例】**
1：`__bytes__`返回类型
- 修复示例：  __bytes__返回bytes类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __bytes__(self):
        return b'repostory'  # 符合
```

**【反例】**
1：`__bytes__`返回类型
- 错误示例：  __bytes__返回str类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __bytes__(self):
        return 'repostory'  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__format__`时与其原型返回类型str不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数`__format__`时返回str类型。

**【正例】**
1：`__format__`返回类型
- 修复示例： __format__返回str类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __format__(self):
        return 'repostory'  # 符合
```

**【反例】**
1：`__format__`返回类型
- 错误示例：  __format__返回int类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __format__(self):
        return len(self.objs_repo)  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法方法`__getnewargs__`时与其原型返回类型tuple不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法方法`__getnewargs__`时返回tuple类型。

**【正例】**
1：`__getnewargs__`返回类型
- 修复示例： __getnewargs__返回tuple类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __getnewargs__(self):
        return (1, 2)  # 符合
```

**【反例】**
1：`__getnewargs__`返回类型
- 错误示例：  __getnewargs__返回int类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __getnewargs__(self):
        return len(self.objs_repo)  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法方法`__getnewargs_ex__`时与其原型返回类型tuple((tuple, dict))不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法方法`__getnewargs_ex__`时返回tuple类型，并且元素是(tuple, dict)类型。

**【正例】**
1：`__getnewargs_ex__`返回类型
- 修复示例： __getnewargs_ex__返回tuple((tuple, dict))类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __getnewargs_ex__(self):
        return ((1,2),{1:2})  # 符合
```

**【反例】**
1：`__getnewargs_ex__`返回类型
- 错误示例：  __getnewargs_ex__返回tuple类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __getnewargs_ex__(self):
        return (1, 2)  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__hash__`时与其原型返回类型int不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数`__hash__`时返回int类型。

**【正例】**
1：`__hash__`返回类型
- 修复示例： __hash__返回int类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __hash__(self):
        return len(self.objs_repo)  # 符合
```

**【反例】**
1：`__hash__`返回类型
- 错误示例：  __hash__返回str类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __hash__(self):
        return 'repostory'  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__index__`时与其原型返回类型int不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数`__index__`时返回int类型。

**【正例】**
1：`__index__`返回类型
- 修复示例： __index__返回int类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __index__(self, i):
        return self.objs_repo.index(i)  # 符合
```

**【反例】**
1：`__index__`返回类型
- 错误示例：  __index__返回str类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __index__(self, i):
        return 'repostory'  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__iter__`时与其原型返回类型iterator不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数`__iter__`时返回iterator迭代器类型。

**【正例】**
1：`__iter__`返回类型
- 修复示例： __iter__应该返回一个iterator类型
```python
import six

class IteratorMetaclass(type):
    def __next__(cls):
        return 1

    def next(cls):
        return 2

@six.add_metaclass(IteratorMetaclass)
class IteratorClass(object):
    """Iterable through the metaclass."""

class FifthGoodIterator(object):
    """__iter__ returns a class which uses an iterator-metaclass."""
    def __iter__(self):
        return IteratorClass  # 符合
```

**【反例】**
1：`__iter__`返回类型
- 错误示例：  __iter__返回要求iterator类型，此处返回列表
```python
class FirstBadIterator(object):
    """ __iter__ returns a list """

    def __iter__(self):
        return []  #  不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__len__`时与其原型返回类型int不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数`__len__`时返回int类型。

**【正例】**
1：`__len__`返回类型
- 修复示例：__len__应该返回一个非负整数，取整
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __len__(self):
        return len(self.objs_repo) // 10  # 符合
```

**【反例】**
1：`__len__`返回类型
- 错误示例：   __len__应该返回一个非负整数，此处返回float
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __len__(self):
        return len(self.objs_repo) / 10  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__length_hint__`时与其原型返回类型非负整数不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数`__length_hint__`时返回非负整数。

**【正例】**
1：`__length_hint__`返回类型
- 修复示例： __length_hint__返回正整数类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __length_hint__(self):
        return len(self.objs_repo)  # 符合
```

**【反例】**
1：`__length_hint__`返回类型
- 错误示例：  __length_hint__返回字符串类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __length_hint__(self):
        return 'repostory'  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__repr__`时与其原型返回类型str不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数`__repr__`时返回str类型。

**【正例】**
1：`__repr__`返回类型
- 修复示例： __repr__返回str类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __repr__(self):
        return 'repostory'  # 符合
```

**【反例】**
1：`__repr__`返回类型
- 错误示例：  __repr__返回int类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __repr__(self):
        return len(self.objs_repo)  # 不符合
```

**【描述】**
由于和解释器的框架代码耦合，如果重写类的魔法函数`__str__`时与其原型返回类型str不一致，将在很多基本功能中出错（真值判断，比较等）。

**【修改建议】**
重写类的魔法函数`__str__`时返回str类型。

**【正例】**
1：`__str__`返回类型
- 修复示例： __str__返回str类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __str__(self):
        return 'repostory'  # 符合
```

**【反例】**
1：`__str__`返回类型
- 错误示例：  __str__返回int类型
```python
class Repostory:
    def __init__(self):
        self.objs_repo = list()

    def __str__(self):
        return len(self.objs_repo)  # 不符合
```

#### G.CLS.10 未实现的数值运算类型魔法函数必须返回NotImplemented而不是抛出NotImplementedError【要求】

**【描述】**
当魔法函数返回`NotImplemented`时，解释器将尝试使用其它关联方法（或其他后备情况，具体取决于运算符）完成功能。
因此，要求数值运算类型的魔法函数（如`__eq__()`，`__lt__()`，`__add__()`，`__rsub__()`等）在有定义却无具体实现时返回`NotImplemented`，而不是抛出`NotImplementedError`异常。

**【修改建议】**
数值运算类型魔法函数返回NotImplemented而不是抛出NotImplementedError。

**【正例】**
在`a == b`的比较中解释器会先调用`a.__eq__`，发现`a.__eq__`方法返回`NotImplemented`后，会调用`b.__eq__`方法来完成功能。
```python
class Entity:
    def __init__(self, eid=0):
        self.eid = eid

class EntityA(Entity):
    def __eq__(self, other):
        return NotImplemented

class EntityB(Entity):
    def __eq__(self, other):
        return self.eid == other.eid

if __name__ == '__main__':
    a = EntityA(eid=1)
    b = EntityB(eid=2)
    print(a == b)  # False
```

**【反例】**
在魔法函数中抛出NotImplementedError
```python
class Entity:
    def __init__(self, eid=0):
        self.eid = eid

class EntityA(Entity):
    def __eq__(self, other):
        raise NotImplementedError()

class EntityB(Entity):
    def __eq__(self, other):
        return self.eid == other.eid

if __name__ == '__main__':
    a = EntityA(eid=1)
    b = EntityB(eid=2)
    print(a == b)  # NotImplementedError
```

#### G.CLS.11 避免在类外或者子类中访问父类受保护的成员【建议】

**【描述】**
被`__`双下划线修饰为private类型，那么这就代表着设计者仅允许在本类中使用此属性，不希望外界访问。
被`_`单下划线修饰为protected类型，那么这就代表着设计者仅允许在本类或继承关系中使用，不希望这个属性被外界直接访问(这里的外界概念包含且不限于类方法之外访问，类方法之内跨实例直接访问)。

因此，考虑到不破坏封装性，不建议进行以下操作：
- 不建议在外界直接访问protected类实例属性；
- 不建议使用名字改写特性（name mangling）直接访问private类实例属性。

应该在封装设计的前提下，合理地提供方法访问被保护的类实例属性。

**【修改建议】**
可以通过以下方法访问被保护的类实例属性：
1. 在类中定义一个公有成员函数，该函数可以访问类的受保护的成员，以提供外部访问功能。
2. 通过 property 装饰器创建只读属性的形式提供外部访问功能。

**【正例】**
1：类外或者子类中访受保护的成员
- 修复示例1：protected类型的成员可以在继承关系中被继承，并以方法的形式提供外部访问功能
```python
class Entity:
    def __init__(self, eid: int = 0, race: str = "no name", age: int = 0):
        self.__eid = eid
        self._race = race
        self.age = age

class EntityA(Entity):
    def get_race(self):
        return self._race  

if __name__ == "__main__":
    obj_a = EntityA(eid=1, race="dog")
    print(obj_a.get_race())  # 符合
```
- 修复示例2：protected类型的成员可以在继承关系中被继承，并以属性的形式提供外部访问功能
```python
class Entity:
    def __init__(self, eid: int = 0, race: str = "no name", age: int = 0):
        self.__eid = eid
        self._race = race
        self.age = age

class EntityA(Entity):
    @property
    def race(self):
        return self._race 

if __name__ == "__main__":
    obj_a = EntityA(eid=1, race="dog")
    print(obj_a.race)  # 符合
```

**【反例】**
1：类外或者子类中访受保护的成员
- 错误示例：不建议通过直接访问、跨实例访问的形式访问类的protected类实例属性
```python
class Entity:
    def __init__(self, eid: int = 0, race: str = "no name", age: int = 0):
        self.__eid = eid
        self._race = race
        self.age = age

class EntityA(Entity):
    def copy_race(self, entity_obj: Entity):  
        self._race = entity_obj._race  # 不符合，跨实例访问类的protected类实例属性，W0212: Access to a protected member _race of a client class (protected-access)

    def get_race(self):
        return self._race

if __name__ == "__main__":
    obj_a = EntityA(eid=1, race="dog")
    obj_b = EntityA(eid=2, race="cat")
    obj_b.copy_race(obj_a)
    print(obj_b._race)  # 不符合，直接访问类的protected类实例属性，W0212: Access to a protected member _race of a client class (protected-access)
```
- 错误示例：Python的名字改写特性（name mangling）对private类型设计的类实例属性访问，同样是一种破坏封装的行为，不鼓励。
```python
class Entity:
    def __init__(self, eid: int = 0, race: str = "no name", age: int = 0):
        self.__eid = eid
        self._race = race
        self.age = age

if __name__ == "__main__":
    obj_a = Entity(eid=1, race="dog")
    print(obj_a._Entity__eid)  # 不符合
```

#### G.CLS.12 类实例较多时，推荐使用__slots__来加强管理类的成员属性【建议】

**【描述】**
类的__slots__用于显式地为对象绑定数据成员属性，并不针对每个实例自动生成__dict__和__weakref__。
__slots__可以是字符串、可迭代对象，或是以多个成员属性命名的字符串组成的序列，推荐做法可以是tuple或list等等。
通过使用__slots__可以减少类实例所占用的内存大小，但相对的需要注意：比如失去了__dict__和__weakref__属性的问题（如果确实需要也可以加回__slots__）。
因此，在类实例较多的时候（一般百万级别以上），可以考虑定义类的__slots__来节省内存。具体需要注意的问题可以参口Python官方文档中的__slots__章节。

**【正例】**
正确使用 __slots__
```python
class User:
    __slots__ = ("name", "age")  # 使用元组定义允许的属性

    def __init__(self, name, age):
        self.name = name
        self.age = age

# 创建实例
user = User("Alice", 30)
print(user.name)  # 输出: Alice

# 尝试动态添加属性（会报错）
try:
    user.email = "alice@example.com"  # AttributeError: 'User' object has no attribute 'email'
except AttributeError as e:
    print(e)
```
优点：
内存节省：实测对比（见下方反例），百万实例可节省 30%~50% 内存。
运行速度提升：属性访问比 __dict__ 更快（因无需哈希查找）。

**【反例】**
未使用 __slots__（默认 __dict__ 动态存储）
```python
class User:
    def __init__(self, name, age):
        self.name = name
        self.age = age

# 创建实例
user = User("Bob", 25)
print(user.name)  # 输出: Bob

# 动态添加属性（允许但内存开销大）
user.email = "bob@example.com"  # 不会报错

# 内存占用对比
import sys
def test_memory(cls):
    instances = [cls("Name", i) for i in range(1_000_000)]
    return sys.getsizeof(instances[0]) * 1_000_000

print(f"无 slots 内存占用（预估）: {test_memory(User):,} bytes")  # 约 224 MB
print(f"有 slots 内存占用（预估）: {test_memory(UserWithSlots):,} bytes")  # 约 64 MB
```
问题：
内存浪费：每个实例携带 __dict__，存储少量属性时冗余严重。
速度稍慢：属性访问需查 __dict__ 哈希表。

## 2.7 异常处理

#### G.ERR.01 try代码块内只包含可能抛出异常的代码段【建议】

**【描述】**
异常捕获语句，是将已知或未知的异常，使用固定的逻辑进行处理，从而提升代码的健壮性。

如果在`try`代码块中包含了过多的代码，在`except`代码块内很难对各种异常做出合适的处理逻辑。

**【修改建议】**
1. 只将可能引发异常的最小代码段放入`try`代码块内。
2. 一个`try`代码块只处理一段可能引发异常的代码。

**【正例】**
将读取文件与处理文件内容的异常处理分开，各代码段的职责独立且清晰
```python
try:
    #  符合
    with open(file_name) as fd:
        content = fd.read()
except FileNotFoundError as e:
    do_something(file_name, e)
except UnicodeDecodeError as e:
    do_otherthing(file_name, e)

try:
    #  符合
    handle_file_content(content)
except UserDefined.FileFormatError as e:
    do_something(e)
```

**【反例】**
放在`try`代码块中的代码段未保证逻辑的相对独立性
```python
try:
    a = 1  # 不符合，不会产生异常的语句，应该放到try前面
    b = get_input()  # 不符合，get_input和a / b属于不同的语义逻辑且会引发不同异常
    result = a / b
except UserDefined.InputInvalid as e:
    do_something(e)
except ZeroDivisionError as e:
    do_otherthing(e)
```

#### G.ERR.02 用异常来表示异常，而不是用返回值表示异常【建议】

**【描述】**
异常作为防御式编程的重要组成，常用来处理非正常的逻辑分支，如非法输入输出、逻辑冲突等。在函数中使用固定的错误返回值，能够实现与异常类似的效果。
在函数单一职责的理念下，常常会出现嵌套较深的函数调用关系。此时如果选择用返回值来表示异常，会产生多层逻辑判断，降低代码的可读性和可扩展性。

**【修改建议】**
捕获异常后要抛出异常,而不是用返回值表示异常。

**【正例】**
```python
def get_content(file_name):
    if file_not_exsits(file_name):
        raise UserDefined.FileNotFound(...)  # 此处抛出的异常统一在main函数中捕获
    ...

def handle_content(content):
    return do_something()

def analyze_data():
    ...
    content = get_content(file_name)
    data = handle_content(content)
    ...

def main():
    try:
        analyze_data()
    except UserDefined.RecoverableException as e:
        do_something(e)
    except UserDefined.UnRecoverableException as e:
        do_something(e)
```

**【反例】**
```python
def divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return None

result = divide(x, y)
if result is None:  # 使用None作为异常返回，result存在两种不同的含义，给调用者带来额外的判断开销
    print('Invalid inputs')
```

```python
def divide(a, b):
    try:
        return True, a / b
    except ZeroDivisionError:
        return False, None

success, result = divide(a, b)
if not success:  # 使用tuple作为返回值，产生额外的内存开销
    print('Invalid inputs')
```

#### G.ERR.03 异常的类型定义必须继承自Exception【要求】

**【描述】**
`BaseException`是所有异常的基类，`Exception`是所有不需要进程退出的异常基类，具体的继承关系如下：
```shell
- BaseException
  |- KeyboardInterrupt
  |- SystemExit
  |- GeneratorExit
  |- Exception
     |- (all other current built-in exceptions)
```
自定义的异常类型必须继承自`Exception`，按照`已知异常->Exception`的顺序捕获时，不需要关注对键盘中断、进程退出、生成器结束等异常的特殊处理。
禁止使用非异常类型作为`raise`对象，如`NotImplemented`、可迭代对象等。

**【修改建议】**
异常类必须继承自Exception。

**【正例】**
```python
class AuthenticationError(Exception):
    def __init__(self, message=None):
        super(AuthenticationError, self).__init__(message)
        self.http_code = 404

def handle_request(req):
    try:
        ...
    except AuthenticationError as e:
        return Response(e.http_code, e.message)
    except Exception as e:
        return Response(400, e.message)
```

**【反例】**
```python
class AuthenticationError(BaseException):
    def __init__(self, message=None):
        super(AuthenticationError, self).__init__(message)
        self.http_code = 404

def handle_request(req):
    try:
        ...
    # 对中断做例外处理，因为异常继承自BaseException，若不做例外处理，则会因为中断导致覆盖AuthenticationError，最终被BaseException捕获
    except (KeyboardInterrupt, SystemExit):
        raise
    except AuthenticationError as e:
        return Response(e.http_code, e.message)
    except BaseException as e:  # 不建议使用BaseException作为最终的异常捕获类型
        return Response(400, e.message)
```

#### G.ERR.04 对异常做类型转换时要保留原始异常的错误调用栈信息【建议】

**【描述】**
如果需要对异常类型进行转换，建议保留原始异常的错误调用栈信息。如果丢失了错误调用栈信息，会给问题定位、运维等带来不必要的麻烦。

**【修改建议】**
使用raise from语句来保留原始异常的错误调用栈信息。

**【正例】**
1：异常抛出
- 修复示例：使用raise from语句来保留原始异常的错误调用栈。
```python
try:
    with open(file_name) as fd:
        ...
except OSError as e:
    # 符合
    raise UserDefined.InvalidFile('Please check file name') from e
```

**【反例】**
1：异常抛出
- 错误示例：丢失了错误调用栈，无法判断具体异常是PermissionError还是FileNotFoundError。
```python
try:
    with open(file_name) as fd:
        ...
except OSError:
    # 不符合，抛出异常丢失了具体异常信息
    raise UserDefined.InvalidFile('Please check file name')
```

#### G.ERR.05 使用有明确业务属性的异常类型【要求】

**【描述】**
如果直接使用`except:`语句，实际捕获的异常是`BaseException`，常常与设计预期不一致，且该问题容易被代码维护人员忽视，会导致程序员无法获知具体的异常类型，从而使代码难以维护和理解。

**【修改建议】**
尽量使用具体的异常类型，少使用范围很大的异常类型。

**【正例】**
1：捕获异常
- 修复示例：捕获具体的异常类型,并将Exception放在最后捕获，用于处理未知异常。
```python
try:
    with open(file_name) as fd:
        ...
# 符合
except FileNotFoundError as e:
    ...
# 符合
except PermissionError as e:
    ...
# 符合
except Exception as e: 
    ...
```

**【反例】**
1：捕获异常
- 错误示例：捕获异常未指定异常类型
```python
try:
    ...
    exit(1)
except:  # 不符合，会将exit(1)抛出的SystemExit异常捕获
    ...
```

#### G.ERR.06 raise语句必须包含异常实例【要求】

**【描述】**
使用`raise`语句时，Python会查找被`except`语句捕获的最后一个异常，如果不存在对应的异常（即没有`except`语句），抛出的异常类型为`RuntimeError`，丢失了原始错误调用栈信息，从而会导致代码错误难以定位。

**【修改建议】**
raise语句抛出异常实例，或者在except语句范围内。

**【正例】**
1：捕获异常
- 修复示例：raise语句抛出异常实例。
```python
try:
    ...
except UserDefined.UnrecoverableException as e:
    do_something(e)
    raise  # 符合，重新抛出异常UserDefined.UnrecoverableException
```
- 修复示例：raise语句抛在except语句范围内。
```python
try:
    ...
except UserDefined.UnrecoverableException as e:
    do_something(e)
    raise e  # 符合，重新抛出异常UserDefined.UnrecoverableException
```

**【反例】**
1：捕获异常
- 错误示例：单使用raise抛出异常,后面不接异常类型，并且不在except语句范围内
```python
raise  # 不符合，会抛出RuntimeError
```

#### G.ERR.07 避免抑制或忽略异常【建议】

**【描述】**
避免抑制或忽略异常。

当一段代码可能发生异常时，需要明确对这些异常的处理策略，包括但不限于重置状态、填充默认值、重试、返回错误等。 

编码时应尽量避免捕获一个异常但什么都不做的情况，抑制或忽略异常很可能丢掉关键的错误和应对，对程序的稳定运行产生风险。

**【修改建议】**
捕获异常，并对异常做出相应的处理。

**【正例】**
1：捕获异常后pass
- 修复示例： 捕获异常，并对异常做出相应的处理

  ```python
  try:
      ...
  except CertainException as e:
      log_something(e)  # 符合：对异常做出相应的处理
      do_something(e)  # 符合：对异常做出相应的处理
  ```
2：捕获异常后continue
- 修复示例：捕获异常，并对异常做出相应的处理

  ```python
  try:
      ...
  except CertainException as e:
      log_something(e)  # 符合：对异常做出相应的处理
      do_something(e)  # 符合：对异常做出相应的处理
  ```
3：捕获异常后return
- 修复示例：捕获异常，并对异常做出相应的处理

  ```python
  try:
      ...
  except CertainException as e:
      log_something(e)  # 符合：对异常做出相应的处理
      do_something(e)  # 符合：对异常做出相应的处理
  ```

**【反例】**
1：捕获异常后pass
- 错误示例：没有对异常做出相应的处理

  ```python
  def get_input_integer():
      while True:
          try:
              i = input('Please enter an integer: ')
              check_integer(i)
          except ValueError:
              pass  # 不符合：这里看似合理，实际上在捕获异常后需要给用户足够的错误信息
      return i
  ```
2：捕获异常后continue
- 错误示例：没有对异常做出相应的处理

  ```python
  def get_input_integer():
      while True:
          try:
              i = input('Please enter an integer: ')
              check_integer(i)
          except ValueError:
              continue  # 不符合：这里看似合理，实际上在捕获异常后需要给用户足够的错误信息
      return i
  ```
3：捕获异常后return
- 错误示例：没有对异常做出相应的处理

  ```python
  def get_input_integer():
      while True:
          try:
              i = input('Please enter an integer: ')
              check_integer(i)
          except ValueError:
              return  # 不符合：这里看似合理，实际上在捕获异常后需要给用户足够的错误信息
      return i
  ```

#### G.ERR.08 禁止通过异常泄露敏感数据【要求】

**【描述】**
禁止通过异常泄露敏感数据。

如果在传递异常的时候未对其中的敏感信息进行过滤，会导致信息泄露，可能帮助攻击者尝试发起进一步的攻击。攻击者可以通过构造恶意的输入参数来发掘应用的内部结构和机制。
异常中的错误信息，以及异常本身的类型都可能泄露敏感数据。
当异常会被传递到信任边界以外时，必须同时对敏感的异常信息和敏感的异常类型进行过滤。
需要注意，在某些场景下，不进行异常处理，反而会泄漏敏感数据，必须慎重审视跨信任边界的交互。
敏感数据的具体范围取决于产品的应用场景，产品应根据风险进行分析和判断。典型的敏感数据包括认证凭据、个人数据和通信内容等。

例如，在对公网用户开放的web服务接口，返回的错误信息中禁止包含`ImportError`和`OSError`等潜在泄漏内部文件目录结构的内容。
提供身份认证的函数，当发生用户名或密码认证失败时，返回的异常类型禁止明确标明是用户名错误或是密码错误，调用者如果捕获异常并将异常类型记录到日志中，攻击者可能结合日志文本，通过暴力探测获取用户名清单。

**【修改建议】**
当异常会被传递到信任边界以外时，必须同时对敏感的异常信息和敏感的异常类型进行过滤。

**【正例】**
1：通过异常泄露敏感数据
- 修复示例：异常中没有敏感数据
```python
try:
    password = 'password@123'
    print(int(password))
# 异常中没有密码信息
except ValueError:
    print('Invalid value')  # 符合
except Exception:
    print('Invalid value')  # 符合
```

**【反例】**
1：通过异常泄露敏感数据
- 错误示例：通过异常泄露敏感数据
```python
try:
    password = 'password@123'
    print(int(password))
# 在异常中泄露了密码信息
except Exception as e:
    print(e)  # 不符合
```

#### G.ERR.09 在单个except代码块内，禁止重复捕获同类异常【要求】

**【描述】**
在异常捕获语句中，重复捕获同类异常不会直接产生运行问题，但这不是好的编码习惯，在较长的软件生命周期中，会带来可读性和可维护性问题。

**【修改建议】**
捕获异常不要同时捕获父类异常和子类异常，不要重复捕获同一个异常。

**【正例】**
1：同时捕获多个异常
- 修复示例：捕获异常属于不同异常类型
```python
try:
    with open(file_name) as fd:
        ...
except (FileNotFoundError, PermissionError):    # 符合
    ...
```

**【反例】**
1：同时捕获多个异常
- 错误示例：同时捕获父子异常类型
```python
try:
    with open(file_name) as fd:
        ...
except (FileNotFoundError, OSError):  # 不符合，FileNotFoundError继承自OSError，逻辑冗余
    ...
```

#### G.ERR.10 同时使用多个except语句时，要注意异常捕获的顺序【要求】

**【描述】**
对于同一个`try`语句，支持配对多个`except`语句，按照`except`语句的次序捕获对应的异常。
捕获异常A的语句应该放在其父类之前。如果先捕获异常A的父类，因为对应的异常已经被处理，则捕获异常A的语句不会被执行，即产生了永远不会被执行的代码块。

**【修改建议】**
注意异常捕获的顺序，先捕获子异常类型，再捕获父异常类型。

**【正例】**
先捕获子异常类型，再捕获父异常类型
```python
try:
    with open(file_name) as fd:
        ...
except (FileNotFoundError, PermissionError) as e:
    do_something(e)
except Exception as e:
    do_otherthing(e)
```

**【反例】**
先捕获父异常类型，再捕获子异常类型
```python
try:
    with open(file_name) as fd:
        ...
except OSError as e:
    do_something(e)
except FileNotFoundError as e:  # FileNotFoundError继承自OSError，该代码块永远不会被执行
    do_otherthing(e)
```

#### G.ERR.11 避免使用SystemExit和sys.exit()，主进程入口中例外【建议】

**【描述】**
执行`sys.exit()`与`raise SystemExit()`等价，会抛出`SystemExit`异常，这个异常应该一直向上抛出，直到进程退出。
在普通函数内调用`sys.exit()`会给调用者带来很多麻烦，应该避免这类设计。

**【修改建议】**
在__main__入口或者在入口调用的函数中使用sys.exit和SystemExit。

**【正例】**
1：捕获父子异常
- 修复示例：在__main__入口中调用sys.exit
```python
if __name__ == '__main__':
    if len(sys.argv) != 3:
        print('At least input 2 arguments')
        sys.exit(1)  # 符合，在主进程中，可以直接使用sys.exit退出
```
- 修复示例：在__main__入口调用的函数中调用sys.exit
```python
def run():
    if len(sys.argv) == 1:
        print("Usage: %s <filename> [options]" % sys.argv[0])
        sys.exit(1)   # 符合
    elif not sys.argv[1]:
        print("%s does not exist" % sys.argv[1])
        sys.exit(1)   # 符合
    else:
        sys.exit(sys.argv[1])   # 符合
        try:
            caller()
        except SystemExit as e:
            print(e)

if __name__ == '__main__':
    run()
```

**【反例】**
1：捕获父子异常
- 错误示例：在普通函数内调用`sys.exit()`和`raise SystemExit`
```python
def create_resource(resource_name):
    resource_instance = resource.create(resource_name)
    if resource_instance.error_info:
        sys.exit(ERROR_CODE)  # 不符合，不合理的设计，需要调用者做资源清理
    return resource_instance

def caller():
    try:
        resource_instance = create_resource(resource_name)
    except SystemExit as e:  # 不符合，这是不好的设计和实现，此处仅用来做资源清理的示例
        log_something(e)
        delete_resource(resource_name)
        raise e
```

#### G.ERR.12 合理地使用object.__exit__ 处理异常【建议】

**【描述】**
Python的对象支持定义`__enter__`与`__exit__`方法以实现上下文管理，`__exit__`定义的是对象退出时要执行的代码块。`__exit__`如果不能正确的返回值，会导致对象退出功能出现异常。

**【修改建议】**
在实现`__exit__`方法时，要明确对异常的处理方式：
1. 如果要屏蔽某个异常，必须返回`True`
2. 如果要某个异常保持外抛，返回`False`或`None`
3. 如果要抛出新的异常，执行`raise X()`

**【正例】**
1：实现`__exit__`方法
- 修复示例：在实现`__exit__`方法时，返回`True`
```python
import contextlib

class SuppressAllExceptions(contextlib.AbstractContextManager):
    """屏蔽所有异常"""

    def __exit__(self, exc_type, exc_value, traceback):
        return True  # 符合

with SuppressAllExceptions():
    raise IOError()  # 这里抛出的异常会被屏蔽
```

**【反例】**
1：实现`__exit__`方法
- 错误示例：在实现`__exit__`方法时，返回整数
```python
import contextlib

class NegativeExample(contextlib.AbstractContextManager):
    def __exit__(self, exc_type, exc_value, traceback):
        ...
        return 1  # 不符合，返回的类型不属于True/False/None
```

#### G.ERR.13 捕获异常后避免直接重新抛出【建议】

**【描述】**
`except`语句在捕获异常后，避免直接重新抛出，捕获并重新抛出异常与不写`except`语句没区别，这些无效的逻辑影响了代码的可读性。

**【修改建议】**
捕获异常后抛出新异常或者调用函数进行异常处理。

**【正例】**
1：抛出捕获异常
- 修复示例：同时使用多个`except`语句时，如果需要对某个异常子类做特殊处理，需要加必要的注释
```python
try:
    1 / 0
except ZeroDivisionError:
    # 符合，除0异常需要外抛，由调用者捕获并处理
    raise
except Exception as e:
    do_something(e)
```

**【反例】**
1：抛出捕获异常
- 错误示例：捕获异常后直接抛出
```python
try:
    do_something()
except SomeException:
    raise    # 不符合
except Exception as e:
    do_something(e)
```

#### G.ERR.14 不要使用return、break、continue或抛出异常使finally块非正常结束【要求】

**【描述】**
在finally代码块中，由于直接使用return语句，或者由于调用方法的异常未处理，会导致finally代码块无法正常结束。

非正常结束的finally代码块会影响try或catch代码块中异常的抛出，也可能会影响函数或方法的返回值。

**【修改建议】**
finnaly语句应该做try-except语句正常结束的代码总处理。

**【正例】**
1：finally里出现return语句
- 修复示例：正确处理try代码块中可能产生的异常，不要在finally代码块中出现return语句
```python
def control_statement_in_finally(param):
    ret = -1
    try:
        ret = 1 / param
    except ZeroDivisionError:
        do_something()
    finally:
        # 符合
        do_finally()
    return ret
```
2：finally语句非正常结束
- 修复示例：判断文件是否关闭，确保finally正常结束
```python
fp = None
try:
    fp = open('test_read.txt', encoding='utf8')
    print(fp.read())
except FileNotFoundError:
    print('文件不存在')
except UnicodeDecodeError:
    print('编码格式错误')
finally:
    if fp:   # 符合，关闭文件之前，增加判断，避免异常
        fp.close()
```

**【反例】**
1：finally里出现return语句
- 错误示例：finally里的return语句会导致param为0时也不会抛出ZeroDivisionError异常

```python

def control_statement_in_finally(param):

    ret = -1

    try:

        ret = 1 / param

    finally:

        # 不符合，finnaly出现return语句

        return ret  

```
2：finally语句非正常结束
- 错误示例：使用finally来确保文件被关闭，但文件不存在时使finally子句中的代码引发了异常，不能正常结束

```python

try:

    fp = open('test_read.txt', encoding='utf8')

    print(fp.read())

except FileNotFoundError:

    print('文件不存在')

except UnicodeDecodeError:

    print('编码格式错误')

finally:

    # 不符合，非正常结束

    fp.close()

Traceback (most recent call last):

 File "<pyshell#130>", line 9, in <module>

 fp.close()

NameError: name 'fp' is not defined

```

## 2.8 并行与并发

#### P.06 不要依赖于内置类型的原子性【建议】

**【描述】**
在Python中可以通过GIL(Global Interpreter Lock)保证在同一个时刻Python虚拟机中只能有一个线程在运行。
Python虚拟机可以保证只在字节码指令级别做线程切换，这也就代表着很多内置类型的操作是线程安全的。相反，某些看起来非常简练的操作实际上却无法保证原子性（如对象替换操作，使用重写后的魔法方法等），这些场景非常繁多且难以记忆。在并发场景中遇到不确定是否线程安全时，建议使用锁来保护临界区资源。
以下为线程安全的原子操作：
```Python
L.append(x)
L1.append(L2)
x = L[i]
x = L.pop()
L1[i:j] = L2
L.sort()
x = y
x.field = y
D[x] = y
D1.update(D2)
D.keys()
```
以下为非线程安全的操作，其中包含了一些替换操作，被替换的对象引用计数为0时，会调用__del__()方法，所以单行代码的操作并不是原子性的。
```Python
i = i + 1
L.append(L[-1])
L[i] = L[j]
D[x] = D[x] + 1
```

#### P.07 Python多线程适用于阻塞式IO场景，不适用于并行计算场景【建议】

**【描述】**
Python的标准实现是CPython。CPython执行Python代码分为2个步骤：首先，将文本源码解释编译为字节码，然后再用一个解释器去解释运行字节码。字节码解释器是有状态的，为了维护该状态的一致性，因此使用了GIL(Global Interpreter Lock)。GIL使得CPython在执行多线程代码的时候，同一时刻只有一个线程在运行，无法利用多CPU提高运算效率，但是这个特点也带来了一个好处：CPython运行多线程的时候，内部对象缺省就是线程安全的。这个特性被非常多的Python库开发者所依赖，直到CPython的开发者想要去除GIL的时候，发现已有大量的代码库严重依赖这个GIL带来的内部对象缺省就是线程安全的特性，变成了一个无法解决的问题。
虽然多线程在并行计算的场景下无法带来好处，但是在阻塞式IO场景下，却仍然可以起到提高效率的作用。这是因为阻塞式IO的场景下，线程在执行IO操作时并不需要占用CPU时间，此时阻塞IO的线程可以被挂起的同时继续执行IO操作，而让出CPU时间给其他线程执行非IO操作。这样一来，多线程并行IO操作就可以起到提高运行效率的作用。
综上，Python的标准实现CPython，适用于阻塞式IO的场景，但是由于GIL的存在，同一个时刻只能运行一个线程，无法充分利用多CPU提升运算效率，因此不适用于并行计算的场景。

**【正例】**
多线程优化阻塞式I/O
```python
import threading
import requests
import time

def fetch_url(url):
    response = requests.get(url)
    print(f"{url} 返回状态码: {response.status_code}")

# 要请求的URL列表
urls = [
    "https://www.example.com",
    "https://www.python.org",
    "https://www.github.com",
]

# 单线程（耗时约3秒）
start = time.time()
for url in urls:
    fetch_url(url)
print(f"单线程耗时: {time.time() - start:.2f}秒")

# 多线程（耗时约1秒）
start = time.time()
threads = []
for url in urls:
    thread = threading.Thread(target=fetch_url, args=(url,))
    thread.start()
    threads.append(thread)

for thread in threads:
    thread.join()
print(f"多线程耗时: {time.time() - start:.2f}秒")
```
输出结果：
```text
https://www.example.com 返回状态码: 200
https://www.python.org 返回状态码: 200
https://www.github.com 返回状态码: 200
单线程耗时: 3.12秒
多线程耗时: 1.05秒
```
优点：
显著缩短I/O等待时间：线程在等待网络响应时可切换执行其他任务。
适合高延迟操作：如爬虫、API调用等。

**【反例】**
多线程处理CPU密集型任务
```python
import threading
import time

def calculate(n):
    result = 0
    for i in range(n):
        result += i * i
    print(f"计算结果: {result}")

# 单线程（耗时约2秒）
start = time.time()
calculate(10_000_000)
calculate(10_000_000)
print(f"单线程耗时: {time.time() - start:.2f}秒")

# 多线程（耗时约4秒，更慢！）
start = time.time()
thread1 = threading.Thread(target=calculate, args=(10_000_000,))
thread2 = threading.Thread(target=calculate, args=(10_000_000,))
thread1.start()
thread2.start()
thread1.join()
thread2.join()
print(f"多线程耗时: {time.time() - start:.2f}秒")
```
输出结果：
```text
计算结果: 333333283333335000000
计算结果: 333333283333335000000
单线程耗时: 2.01秒
计算结果: 333333283333335000000
计算结果: 333333283333335000000
多线程耗时: 4.03秒
```

#### G.CNP.01 建议为communicate传入超时参数来防止子进程死锁或失去响应【建议】

**【描述】**
建议为communicate传入超时参数来防止子进程死锁或失去响应。

在使用subprocess模块来管理子进程时，给communicate方法传入timeout参数，以避免子进程死锁或失去响应。

**【修改建议】**
在使用subprocess模块来管理子进程时，给communicate方法传入timeout参数，以避免子进程死锁或失去响应。

**【正例】**
1：没有超时处理
- 修复示例1：传入timeout参数

 ```python
 import subprocess

 if __name__ == "__main__":
     proc = subprocess.Popen("ping 192.168.23.45 -t")
     try:
         outs, errs = proc.communicate(timeout=5)  # 符合
     except subprocess.TimeoutExpired:
         proc.kill()  # 子进程如果在超时时间内无响应，则将其终止
 ```

**【反例】**
1：没有超时处理
- 错误示例：

 ```python
 import subprocess

 if __name__ == "__main__":
     proc = subprocess.Popen("ping 192.168.23.45 -t")
     print(proc.communicate())  # 不符合，没有设置超时参数，如果子进程死锁，将导致程序阻塞
 ```

## 2.9 包与模块

#### P.08 使用package对module分层管理【建议】

**【描述】**
当多个Python源码文件分不同子目录存放时，应该合理设计目录层级及各目录名和文件名，用package形式管理各个目录下的模块。
基于高内聚原则设计包和模块，将相关功能的模块放到同一个包内，将同类功能的对象放到同一个模块内。包和子包的目录下必须包含__init__.py文件，以确保Python解释器能够正确地将该目录识别为包或子包。

#### P.09 使用__all__声明允许外部访问的变量、函数和类【建议】

**【描述】**
与Java等语言不同，Python不支持在模块内严格限制外部可访问的对象清单。Python社区约定，支持在模块内使用__all__声明公共接口，即允许外部访问的变量、函数和类。
作为模块的提供者，应该通过__all__声明公共接口，并保证在模块版本生命周期内的公共接口稳定和跨版本兼容。作用模块的使用者，避免使用未包含在__all__清单内的接口（内部接口），因为提供者不会承诺内部接口的稳定性，随着版本演进可能有不兼容的修改。


#### G.IMP.01 使用绝对路径导入模块【建议】

**【描述】**
使用正确的导入方式导入模块，可以保证代码可读性，否则可能会导致运行错误。

**【修改建议】**
1. 应该使用绝对路径导入（absolute imports），避免使用相对路径导入（relative imports），使用绝对路径可以清晰明确地知道所导入模块的所属包和完整路径，在出现导入错误时更容易定位，能够减少调整代码路径时的配套修改工作量。项目库内的代码，对项目库本身模块的导入，可以使用相对路径。
2. 如果代码的路径较深（例如导入代码的语句需要换行时），可以使用相对路径导入。
3. 禁止对外部库（包括系统库、三方库和二方库）使用相对路径导入。
4. 禁止对同一个包的导入，同时使用绝对路径和相对路径。

**【正例】**
1：使用绝对和相对导入模块
- 修复示例：按正确顺序导入模块
```python
from third_lib import module_a  # 三方库使用绝对路径
from huawei_sdk import module_b  # 二方库使用绝对路径
from .module_c.module_cc import ClassD  # 本项目库可以使用相对路径
```

**【反例】**
1：使用绝对和相对导入模块
- 错误示例：在同一个文件内，对`mypkg`同时使用绝对路径和相对路径导入，不利于代码维护
```python
# mypkg/mymodule.py
from . import module_a
from mypkg.module_b import SomeClass   # 不符合
```
- 错误示例：在不同文件内，对`mypkg`同时使用绝对路径和相对路径导入，不利于代码维护
```python
# mypkg/module_a.py
from mypkg.module_b import SomeClass
```
- 错误示例：同时需要具备可执行和可导入的文件内，使用相对路径导入，会发生导入错误
```python
# test_relative_import/model_convert.py
def str2int(_in):
    if not isinstance(_in, str):
        raise UserDefined.InvalidInput()
    return int(_in)
```

#### G.IMP.02 使用 from ... import ... 语句的注意事项【建议】

**【描述】**
禁止使用`from ... import *`，该方法会导入模块内所有非`_`前缀的对象，存在以下缺点：

1. 如果多个模块存在同名对象，后导入的对象会覆盖先导入的同名对象，开发者无法快速识别该覆盖行为；

2. 无法明确各对象的所属模块，给代码的功能调测、长期维护等带来额外的开销。

测试代码使用`from ... import *`，同样存在上述缺点。虽然测试代码不会在生产环境运行，但会给开发调试带来不必要的麻烦，建议避免使用该方式导入。

**【修改建议】**
使用`from ... import ...`方式导入多个模块时要避免导入重名对象，禁止使用`from ... import *`方式导入模块所有对象。

**【正例】**
1：导入模块成员
- 修复示例：常见的导入方式，两种导入方式按需混用

```python

import os

import sys

from sqlalchemy import create_engine

```
- 修复示例：对于某些导入耗时较高的模块，可以使用示例方式控制使用的对象清单，同时规避易混淆的缺点

```python

from os import path as os_path

from sys import path as sys_path

```

**【反例】**
1：导入模块成员
- 错误示例：使用*号导入模块成员

```python

from os import *

from sys import *  # 不符合，os模块的path被sys模块的path覆盖

```

#### G.IMP.03 避免使用__import__ 函数【建议】

**【描述】**
建议使用`importlib.import_module`函数替代`__builtins.__import__`。
在`importlib`模块中，提供了比内置函数`__import__`更为丰富的接口，不需要关注导入细节，使用更为简单。

**【修改建议】**
使用`importlib.import_module`函数来动态导入模块。

**【正例】**
1：动态导入模块
- 修复示例：使用importlib动态导入模块
```python
import importlib

# 以下用法为建议用法
os_path_recommend = importlib.import_module('os.path')
# <module 'posixpath' from '.../pythonX/posixpath.py'>

```

**【反例】**
1：动态导入模块
- 错误示例：使用__import__动态导入模块
```python
os_path_negative = __import__('os.path')
# <module 'os' from '.../pythonX/os.py'>
```

## 2.10 标准库

#### P.10 注意根据场景选用copy或deepcopy完成浅拷贝或深拷贝

**【描述】**
在python中，对象赋值实际上是对象的引用。当创建一个对象，然后把它赋给另一个变量的时候，python并没有拷贝这个对象，而是拷贝了这个对象的引用。如果需要拷贝对象，需要使用标准库中的copy模块。copy模块提供copy和deepcopy两个函数：
copy浅拷贝：拷贝一个对象，但是对象的属性还是引用原来的。对于可变类型，比如列表和字典，只是复制其引用。基于引用所作的改变会影响到被引用对象。
deepcopy深拷贝：创建一个新的容器对象，包含原有对象元素（引用）全新拷贝的引用、外围和内部元素都拷贝对象本身，而不是引用。
注意对于数字、字符串和其他原子类型对象等，没有被拷贝的说法。如果对其重新赋值，也只是新创建一个对象替换掉旧的而已。
copy.deepcopy的执行效率低于copy.copy。要根据场景选用合适的拷贝函数，不能全部使用深拷贝。

**【正例】**
正确选择拷贝方式
场景1：浅拷贝适用于无嵌套可变对象
```python
import copy

# 原始对象（无嵌套可变结构）
original_list = [1, 2, 3]
shallow_copied = copy.copy(original_list)

# 修改浅拷贝对象的外层
shallow_copied.append(4)
print(original_list)  # 输出: [1, 2, 3]（原对象未受影响）
print(shallow_copied) # 输出: [1, 2, 3, 4]
```

场景2：深拷贝适用于嵌套可变对象
```python
# 原始对象（嵌套可变结构）
original_dict = {"a": [1, 2], "b": {"c": 3}}
deep_copied = copy.deepcopy(original_dict)

# 修改深拷贝对象的嵌套数据
deep_copied["a"].append(99)
deep_copied["b"]["c"] = 100
print(original_dict)  # 输出: {'a': [1, 2], 'b': {'c': 3}}（原对象完全不受影响）
print(deep_copied)    # 输出: {'a': [1, 2, 99], 'b': {'c': 100}}
```

**【反例】**
错误选择拷贝方式
反例1：浅拷贝误用于嵌套对象
```python
original = [[1, 2], [3, 4]]
shallow_copied = copy.copy(original)

# 修改浅拷贝对象的嵌套列表
shallow_copied[0].append(99)
print(original)       # 输出: [[1, 2, 99], [3, 4]]（原对象被意外修改！）
print(shallow_copied) # 输出: [[1, 2, 99], [3, 4]]
```

反例2：无脑使用深拷贝（性能浪费）
```python
# 不需要深拷贝的简单对象
simple_list = [1, 2, 3]
unnecessary_deepcopy = copy.deepcopy(simple_list)  # 浪费性能！

# 原子类型（深拷贝无意义）
a = "hello"
b = copy.deepcopy(a)  # 完全等价于 b = a
```

#### G.PSL.01 避免使用已经被标记为弃用并有明确替代的方法【建议】

**【描述】**
当代码运行出现`DeprecationWarning`，明确指出某些模块、类或函数计划废弃，并给出了新的替代方案时，必须按照其提示的方法、版本正确地使用新方案替代计划废弃的老方案。

可以使用下面的方式，兼容在不同版本的CPython中模块命名发生改变的情况
```python
try:
    import configparser
except ImportError:
    import ConfigParser as configparser
```

**【修改建议】**
关注python版本变化导致某些模块过期或删除的问题，可以使用异常捕获的方式来兼容不同的python版本模块过期的问题。

**【正例】**
1：过期模块
- 修复示例：使用新模块代替过期模块
```python
import argparse # 符合
import xml.etree.ElementTree # 符合
import tkinter.ttk # 符合
```

2：过期方法
- 修复示例：使用新方法代替过时方法
```python
import logging

log = logging.getLogger()
logging.warning("this is test")   # 符合
log.warning("this is test")   # 符合
```

3：过期类
- 修复示例：使用collections.abc代替collections
```python
from collections.abc import Iterable   # 符合
from collections.abc import Collection   # 符合
```

**【反例】**
1：过期模块
- 错误示例：使用过期模块
```python
import optparse  # 不符合
import xml.etree.cElementTree   # 不符合
import tkinter.tix   # 不符合
```

2：过期方法
- 错误示例：使用过期方法
```python
import logging

log = logging.getLogger()
logging.warn("this is test")   # 不符合，方法已过时
log.warn("this is test")   # 不符合，方法已过时
```

3：过期类
- 错误示例：使用collections过期模块
```python
from collections import Iterable   # 不符合
from collections import Collection  # 不符合
```

#### G.PSL.02 在datetime的使用过程中注意时区的影响，时区敏感的场景建议显式指定时区【建议】

**【描述】**
`datetime`标准库在未指定`tz`可选参数时，会按照操作系统设置的时区显示时间。未显式指定时区的软件在跨时区使用时，会因为不同的系统时区设置导致预期外的问题。在涉及时间比较和时间差计算等场景，在夏令时切换时，系统时区的时间会发生跳变，使用系统时区的时间可能会导致预期外的问题。

**【修改建议】**
使用`datetime`标准库时，显式指定`tz`可选参数为希望使用的时区。使用`UTC`时间时建议直接使用`datetime.now(tz=timezone.utc)`方式。

**【正例】**
1：datetime的使用
- 修复示例：使用带时区的时间
```python
from datetime import datetime, timezone

def main():
    print(datetime.now(tz=timezone.utc))  # 2021-04-02 15:04:31.759787+00:00，推荐该用法，包含明确的时区信息
    print(datetime.now(tz=timezone.utc).tzname())  # UTC
    print(datetime.utcnow())  # 2021-04-02 15:04:31.759787

if __name__ == '__main__':
    main()
```

**【反例】**
1：datetime的使用
- 错误示例：直接使用本地时间
```python
from datetime import datetime

def main():
    print(datetime.now())  # 2021-04-02 15:04:31.759787 比UTC时间快8小时
    print(datetime.now().tzname())  # None

if __name__ == '__main__':
    main()
```

#### G.PSL.03 修改sys.path时注意避免模块重名问题【建议】

**【描述】**
`sys.path`是Python在执行`import`语句时搜索模块使用的路径列表，由当前目录、系统环境变量、库目录、`.pth`文件配置组合拼装而成，直接修改之后将作用于当次Python进程运行生命周期内所有`import`语句。
原则上`sys.path`只应该根据用户的系统配置来生成，默认的`sys.path`应该就可以支持模块的搜索过程，不应该在代码里面直接修改。如果确实需要修改，则需要注意尽量不要影响其它模块搜索`sys.path`的顺序，否则可能导致某些`import`语句因为搜索到了错误的模块，导入不了相应的符号而出现`ImportError`异常。

**【修改建议】**
用`sys.path.append`代替`sys.path.insert`来避免模块重名问题。

**【正例】**
1：修改`sys.path`
- 修复示例：使用`append`、`extend`等方法加在`sys.path`最后修改`sys.path`，保证不影响其他标准库、三方包模块加载
```python
import sys
sys.path.append("./local_packages")  # 符合
```

**【反例】**
1：修改`sys.path`
- 错误示例：使用sys.path.insert修改`sys.path`
```python
import sys
sys.path.insert(0, "./local_packages")  # 不符合
```

#### G.PSL.04 建议用functools.wraps定义函数装饰器【建议】

**【描述】**
一般的装饰器写法在功能上虽然没有问题，但是会导致被装饰函数对象的内部属性发生变化，造成了后续使用上的不便。
因此，建议在装饰器的书写过程中，使用`functools.wraps`的写法定义函数装饰器，避免被装饰函数内部属性被破坏。

**【修改建议】**
用functools.wraps定义函数装饰器。

**【正例】**
1：使用函数装饰器
- 修复示例：使用functools.wraps定义函数装饰器
```python
from functools import wraps

def my_decorator(func):
    @wraps(func)
    def wrapper(*args, **kwargs):    # 符合
        print("call decorated function")
        return func(*args, **kwargs)

    return wrapper

@my_decorator
def example():
    """this is example docstring"""
    print("call example function")

example()
print(example.__name__)  # example
print(example.__doc__)  # this is example docstring
```

**【反例】**
1：使用函数装饰器
- 错误示例：如下一般的装饰器写法将会改写被装饰函数的部分属性，导致`__name__`，`__doc__`等内部属性产生混乱
```python
def my_decorator(func):
    def wrapper(*args, **kwargs):      # 不符合
        print("call decorated function")
        return func(*args, **kwargs)

    return wrapper

@my_decorator
def example():
    """this is example docstring"""
    print("call example function")

example()
print(example.__name__)  # wrapper
print(example.__doc__)  # None
```

## 2.11 代码工程

#### P.11 建议尽量使用标准库中的功能来替代直接调用操作系统的系统命令【建议】

**【描述】**
python有很丰富的库，比如os提供了很多常用的与操作系统相关的命令。为了让代码更易读也更稳定，建议在做相关的操作时尽量使用标准库中的功能来替代操作系统的系统命令。

**【正例】**
```Python
import os

if __name__ == "__main__":
    print(os.remove("/tmp/abd"))
```

**【反例】**
```Python
import os

if __name__ == "__main__":
    print(os.system("rm /tmp/abd"))
```

#### G.PRJ.01 建议为启动文件添加启动文件头【建议】

**【描述】**
类Unix操作系统上使用启动头`#!/usr/bin/python3.7`以明确指定运行此文件的解释器版本，推荐采用这种方式指定。这样有助于正确指定执行python文件的解释器，防止使用非预期版本的解释器执行文件。当解释器版本不做要求时，也可以使用`#!/usr/bin/env python`声明，选择系统的PATH变量中指定的第一个Python解释器来执行Python代码。启动头的位置应该放在文件编码声明之前。
如果一个计划中类Unix操作系统运行的代码项目有执行入口文件，那么建议为这个入口文件添加启动文件头。如果项目只是子项目无执行入口文件，那么不需要添加。不推荐将所有文件都添加气启动头，虽然这并没有额外的功能问题。


#### G.PRJ.02 建议为启动文件设置执行入口【建议】

**【描述】**
"__main__"是顶层代码执行的作用域的名称。模块的__name__在通过标准输入，脚本文件或是交互式命令读入的时候会等于"__main__"。模块可以通过检查自己的__name__来得知是否运行在main作用域中，这使得模块可以在作为脚本或是通过python -m运行时条件性地执行一些代码，而在被import时不会执行。因此，建议在代码工程启动文件中设置执行入口`(if __name__ == "__main__")`。在python多进程程序中，用于启动子进程的代码文件则必须使用`(if __name__ == "__main__")`确定是顶层代码作用域之后才能正常启动子进程。

**【正例】**
```python
import os
from multiprocessing import Process

def child_process(name):
    print(f'this is child process({name})({os.getpid()})')

if __name__ == "__main__":
    p = Process(target=child_process, args=('child',))
    p.start()
    p.join()
```

**【反例】**
```python
import os
from multiprocessing import Process

def child_process(name):
    print(f'this is child process({name})({os.getpid()})')

p = Process(target=child_process, args=('child',))
p.start()
p.join()
```

#### G.PRJ.03 产品代码不要包含任何调试入口点【要求】

**【描述】**
产品代码不要包含任何调试入口点。

出于调试或测试目的，开发者经常在代码中添加特定的调试或测试代码，这些代码并没有打算与应用一起交付或部署。当这类的调试或测试代码不小心被留在了应用中，这个应用对某些特殊交互就是开放的。这些后门入口点可能会导致安全风险。因此，开发者在交付前必须删除所有调试相关的代码。

**【修改建议】**
代码在交付前务必删除所有调试相关的代码。

**【正例】**
1：代码中引入pdb模块
- 修复示例：删除所有调试相关的代码
```python
if not flag:
    ...  # 符合
print('.....')
```

**【反例】**
1：代码中引入pdb模块
- 错误示例：代码包含pdb模块
```python
if not flag:
    import pdb
    pdb.set_trace()  # 不符合
print('.....')
```

#### G.PRJ.04 建议同一项目内的编码方式保持一致，推荐使用UTF-8【建议】

**【描述】**
Python3默认使用UTF-8编码，使用其它的编码（如`latin-1`，`gbk`等等）可能在使用默认解码的程序解码时出现解码失败。
建议同一项目内的编码方式保持一致。推荐使用默认的UTF-8，如果使用UTF-8编码可以省略不写编码方式。

**【修改建议】**
文件编码统一使用utf-8格式编码，或者文件开头使用# coding: utf-8进行编码声明。

**【正例】**
1：编码申明
- 修复示例：使用utf-8编码申明
```python
#!/usr/local/bin/python
# coding: utf-8
import os
import sys
...
```
- 修复示例：默认不写编码方式
```python
#!/usr/bin/python
import os
import sys
...
```

**【反例】**
1：编码申明
- 错误示例：`# latin-1`编码格式错误
```python
#!/usr/local/bin/python
# latin-1    # 不符合
import os
import sys
...
```
- 错误示例：编码申明不在第1、第2行
```python
#!/usr/local/bin/python
#
# -*- coding: latin-1 -*-       # 不符合
import os
import sys
...
```
- 错误示例：不支持的编码方式
```python
#!/usr/local/bin/python
# -*- coding: utf-42 -*-         # 不符合
import os
import sys
...
```

#### G.PRJ.05 不用的代码段直接删除，不要注释掉【要求】

**【描述】**
基于python语言运行时编译的特殊性，如果在提供代码的时候提供的是py文件，该文件中包含被注释掉的代码，当企图恢复使用这段代码时，极有可能引入易被忽略的缺陷；尤其是某些接口函数，
如果不在代码中进行彻底删除，某些本应被屏蔽的功能可能在不知情的情况下就被启用了。另外，同样禁止以False为条件语句或者其他任何形式使之成为无法执行到的无效代码。

**【修改建议】**
对不使用的旧代码应该及时删除，以免暴露程序接口，造成不安全的因素。

**【正例】**
1：被注释的代码
- 修复示例：删除注释的代码
```python
 if __name__ == "__main__":
     if sys.argv[1].startswith('--'):
         option = sys.argv[1][2:]
         if option == "load":
             # 安装应用
             LoadCmd(option, sys.argv[2:3][0])
         elif option == "unload":
             # 卸载应用
             UnloadCmd(sys.argv[2:3][0])
         elif option == "unloadproc":
             # 卸载流程
             UnloadProcessCmd(sys.argv[2:3][0])
         else:
             Loginfo("Command {} is unknown".format(sys.argv[1]))
```

**【反例】**
1：被注释的代码
- 错误示例：程序中的两个屏蔽的接口，容易造成不安全的因素，注释及被屏蔽的代码段应该直接删除
```python
if __name__ == "__main__":
    if sys.argv[1].startswith('--'):
        option = sys.argv[1][2:]
        if option == "load":
            # 安装应用
            LoadCmd(option, sys.argv[2:3][0])
        elif option == "unload":
            # 卸载应用
            UnloadCmd(sys.argv[2:3][0])
        elif option == "unloadproc":
            # 卸载流程
            UnloadProcessCmd(sys.argv[2:3][0])
        # elif option == 'active':  不符合，被注释的代码
        #   ActiveCmd(sys.argv[2:3][0])
        # elif option == 'inactive':
        #   InActiveCmd(sys.argv[2:3][0])
        else:
            Loginfo("Command {} is unknown".format(sys.argv[1]))
```

#### G.PRJ.06 正式发布的代码及注释内容不应包含开发者个人信息【要求】

**【描述】**
发布的代码及注释内容不应包含个人敏感信息，如：身份证号码。

由于从应用程序中提取字符串很容易，因此敏感信息不应硬编码，否则很容易落入攻击者手中。对于分布式的应用程序尤其如此。

**【修改建议】**
删除身份证号码等敏感信息。应存储在代码外部的受强保护的加密配置文件或数据库中。

**【正例】**
1：代码中包含个人信息
- 修复示例：代码中没有个人信息
```python
# 符合: 代码中没有个人信息
line_no = 1
```

**【反例】**
1：代码中包含个人信息
- 错误示例：代码中包含个人信息
```python
# 不符合: 代码中包含了个人工号信息
employee_no = 'a00123456'
```

#### G.PRJ.07 禁止代码中包含公网地址【要求】

**【描述】**
IP地址、密码硬编码。

代码及注释内容不应包含敏感信息。敏感信息检查分类包括：IP地址、密码。

**【修改建议】**
删除IP地址、密码等敏感信息。

**【正例】**
```Python
删除IP地址、密码等敏感信息
```

**【反例】**
```python
def badTest():
    # POTENTIAL FLAW: Sensitive information is hard coded in the program
    pwd = 'xxx'
```

## 2.12 文件

#### P.12 使用open打开文件时应注意使用正确的模式和编码【要求】

**【描述】**
使用open打开文件时，不同的mode参数和encoding参数会对文件打开的方式造成影响，mode可选参数含义列表：
| 字符  |含义   |
|---|---|
|  'r' | 读取（默认）  |
|  'w' | 写入，如果文件已存在会在打开时清空文件  |
|  'x' | 独占式创建，如果文件已存在会失败，打开后可以写入不可以读取  |
|  'a' | 从文件结尾开始续写  |
|  'b' | 二进制模式打开  |
|  't' | 文本模式打开（默认）  |
|  '+' | 更新（可读可写）  |

模式可以进行合理的组合使用。比如'rb'、'wb'
encoding可选参数需要指定合法的编码名称字符串，如utf-8,gb2312等。选择错误的解码方式会导致程序出现解码异常
在使用open打开文件时，应选择合理的mode和encoding组合，防止出现文件意外清空，解码失败等问题

**【正例】**
```Python
def daily_write_down_content(content: str):
    with open('weekly_notebook.txt', 'a', encoding='utf-8') as f:
        f.write(content)
```

**【反例】**
```python
## 错误使用'w'导致每次都清空了之前的内容
def daily_write_down_content(content: str):
    with open('weekly_notebook.txt', 'w', encoding='utf-8') as f:
        f.write(content)
```

#### G.FIO.01 在多用户系统中创建文件时应根据需要指定合适的权限【要求】

**【描述】**
在多用户系统中创建文件时应根据需要指定合适的权限。

多用户系统中的文件通常归属于一个特定的用户。文件的主人能够指定系统中哪些其他用户能够访问该文件的内容。这些文件系统使用权限和许可模型来保护文件访问。当一个文件被创建时，文件访问许可规定了哪些用户可以访问或者操作这个文件。当一个程序在创建文件时没有对文件的访问许可做足够的限制，攻击者可能在程序修改此文件的访问权限之前对其进行读取或者修改。另外在跨环境场景也有类似问题，需要在创建文件时指定合适的权限。

**【修改建议】**
使用os.open函数，并指定第三个参数为0o755或更低级别。建议按照文件使用场景严格限制文件访问许可，阻止未授权的访问。

**【正例】**
1：创建文件时没有指定权限
- 修复示例：创建文件时指定了合适的权限

```python
import os
import stat

flags = os.O_WRONLY | os.O_CREAT | os.O_EXCL  # 注意根据具体业务的需要设置文件读写方式
mode = stat.S_IWUSR | stat.S_IRUSR  # 注意根据具体业务的需要设置文件权限
with os.fdopen(os.open('testfile.txt', flags, mode), 'w') as fout:  # 符合：创建文件时在os.open的第三个参数指定了合适的权限
    fout.write('secrets!')
```

**【反例】**
1：创建文件时没有指定权限
- 错误示例：创建文件时没有指定权限

```python
with open('testfile.txt', 'w') as fout:  # 不符合：创建文件时没有指定权限
    fout.write('hi, 2012')
```

#### G.FIO.02 校验文件路径之前应该先对其进行规范化处理【要求】

**【描述】**
路径遍历，校验文件路径之前应该先对其进行规范化处理。

绝对路径或者相对路径中可能会包含如符号（软）链接（symbolic [soft] links）、硬链接（hard links）、快捷方式（shortcuts）、影子文件（shadows）、别名（aliases）和连接文件（junctions）等形式，在进行文件验证操作之前必须完整解析这些文件链接。路径中也可能会包含如下所示的文件名，使得验证变得困难：
1. "." 指当前目录。
2. 在一个目录内，".." 指该目录的上一级目录。

除此之外，还有与特定操作系统和特定文件系统相关的命名约定，也会使验证变得困难。
同一个目录或者文件，可以通过多种路径名来引用它，所以在文件路径校验前必须使用os.path.realpath方法对文件路径进行规范化处理，可以使文件路径校验较为容易。
当试图限制用户只能访问某个特定目录中的文件时，或者当基于文件名或者路径名来做安全决策时，校验是必须的。攻击者可能会利用目录遍历（directory traversal）或者等价路径（path equivalence）漏洞的方式来绕过这些限制。
目录遍历漏洞使得攻击者能够转移到一个特定目录进行I/O操作，等价路径漏洞使得攻击者可以使用与某个资源名不同但是等价的名称来绕过安全检查。
在程序获取一个文件标准路径与打开这个文件之间，会有一个固有的时间竞争窗口。在对规范化的文件路径进行校验时，文件系统可能被修改，规范化的路径名可能不再指向原始的有效文件。值得庆幸的是，可以使用规范化的路径名来判断引用的文件名是否在安全目录中，来消除条件竞争。如果引用的文件是在一个安全目录之中，很明显攻击者无法篡改文件，也无法利用条件竞争。

**【修改建议】**
使用os.path.realpath方法，它能在所有的平台上对所有别名、快捷方式以及符号链接进行一致地解析。特殊的文件名，比如..会被移除，这样输入在验证之前会被简化成其规范形式。当使用规范化的文件路径来做校验时，攻击者将无法使用../序列来跳出特定目录，同时为了防止软链接攻击，有必要对规范化之后的路径进行预期判断，以防止最终操作的路径为攻击者意图访问的路径。

**【正例】**
1：未对文件路径进行规范化处理
- 修复示例：对文件路径进行校验
```python
import os

def path_verify(path, safe_start):
    # 校验函数里是对参数进行realpath方法生成真实路径，并对生成的路径进行预期校验，预期校验是根据业务的角度去校验的，常见的预期校验方法如：startswith、正则等。
    # 注：os.path.exists不属于预期校验
    real_path = os.path.realpath(path)  # 清理告警第一步：用realpath方法
    if real_path.startswith(safe_start):  # 清理告警第二步：预期校验
        return real_path

path = input()  # 污染源，例如input、sys.argv、os.environ 等
safe_start = "/usr/test"
try:
    # 对文件路径进行校验
    verified_path = path_verify(path, safe_start)  # 污染源数据经过特定函数名的校验函数，从而从不可信数据变为可信数据
    if verified_path:
        os.removedirs(verified_path)  # 符合
except Exception as ex:
    print(ex)
```

**【反例】**
1：未对文件路径进行规范化处理
- 错误示例：
```python
import os

path = input()
try:
    # 未对文件路径进行规范化处理
    os.removedirs(os.path.abspath(path))  # 不符合
except Exception as ex:
    print(ex)
```

#### G.FIO.03 禁止使用tempfile.mktemp创建临时文件【要求】

**【描述】**
禁止使用tempfile.mktemp创建临时文件。

mktemp 函数返回的临时文件名可能存在重名（与时间强相关）产生未知风险。禁止使用已知有风险的`tempfile.mktemp`函数创建临时文件。要求使用安全的方法创建临时文件，包括但不限于`tempfile`模块的`mkstemp`, `mkdtemp`, `NamedTemporaryFile`函数。os.tempnam和os.tmpnam也存在同样的风险。

**【修改建议】**
可以使用替代函数NamedTemporaryFile() 、mkstemp() 和 mkdtemp() ，这些函数调用的同时立即创建临时文件，避免攻击者利用时间差进行符号链接攻击。

**【正例】**
1：使用tempfile.mktemp创建临时文件
- 修复示例：使用安全的函数创建临时文件

```python
import os
import shutil
import tempfile

tmp_file_one = tempfile.mkstemp()  # 符合：(3, '/tmp/tmpyo8ddjhq') 创建临时文件
tmp_file_two = tempfile.mkdtemp()  # 符合：/tmp/tmpf_od5le5 创建临时目录
tmp_file_three = tempfile.NamedTemporaryFile(delete=False)  # 符合：<tempfile._TemporaryFileWrapper object at 0x000001E3D182BE88>

if os.path.isfile(tmp_file_one[1]):
    os.close((tmp_file_one[0]))
    os.remove(tmp_file_one[1])

if os.path.isfile(tmp_file_three.name):
    tmp_file_three.close()
    os.remove(tmp_file_three.name)

if os.path.isdir(tmp_file_two):
    os.mkdir(os.path.join(tmp_file_two, '1.txt'))
    shutil.rmtree(tmp_file_two)
```

**【反例】**
1：使用tempfile.mktemp创建临时文件
- 错误示例：使用tempfile.mktemp创建临时文件

```python
import tempfile

filename = tempfile.mktemp()  # 不符合：生成的文件名与时间强相关，有可能引起重名风险
with open(filename, "w+") as tmp_file:
    ...
```

#### G.FIO.04 临时文件使用完毕应及时删除【要求】

**【描述】**
临时文件使用完毕应及时删除。

在全局可写的目录中创建临时文件，例如，POSIX系统下的/tmp与/var/tmp目录，Windows系统下的C:\TEMP目录。这类目录中的文件可能会被定期清理，例如，每天晚上或者重启时。然而，如果文件未被安全地创建或者用完后还是可访问的，具备本地文件系统访问权限的攻击者便可以利用共享目录中的文件进行恶意操作。删除已经不再需要的临时文件有助于对文件名和其他资源（如二级存储）进行回收利用。每一个程序在正常运行过程中都有责任确保删除已使用完毕的临时文件。

**【修改建议】**
临时文件使用完毕后使用os.remove或os.unlink删除

**【正例】**
1：临时文件使用完毕未及时删除
- 修复示例1：使用os.remove或os.unlink函数删除
```python
import os

diy_file = "diyData.txt"
content = "Data"
try:
   file_handle = open(diy_file, os.O_WRONLY, int("0600", 8))
   try:
       file_handle.write(content)
   except Exception as e:
       doing_something()
   finally:
       file_handle.close()
except Exception as ex:
   print(ex)

# 建议使用with语句实现上述功能
# 结束时，显式的删除它
if os.path.isfile(diy_file):
    os.remove(diy_file)  # 符合
```

- 修复示例2：这个示例创建临时文件时用到了NamedTemporaryFile ()方法，该方法会新建一个随机的文件名。文件使用try-finally构造块，在finally处手动关闭文件。而不管是否有异常发生，由于在打开文件时用到了delete选项，使得文件在关闭后会被自动删除。
```python
import tempfile

tmp_file_handle = tempfile.NamedTemporaryFile(delete=True)  # 符合
print(tmp_file_handle.name)
try:
   tmp_file_handle.file.write(b"abc")
except Exception as e:
   doing_something()
finally:
   tmp_file_handle.close()
```

**【反例】**
1：临时文件使用完毕未及时删除
- 错误示例：
```python
import os
import tempfile

fd, path = tempfile.mkstemp()  # 不符合
try:
    with os.fdopen(fd, "w") as f:
        f.write('Hello, world!')
except Exception as e:
    doing_something()
```

#### G.FIO.05 构造文件路径时应屏蔽操作系统的差异，建议使用库函数辅助构造【建议】

**【描述】**
不同的操作系统使用不同的字符作为路径分隔符。例如，Windows系统使用`\\`，而UNIX系统使用`/`。 
当应用程序必须在不同的平台上运行时，使用硬编码的路径分隔符可能会导致应用程序逻辑执行不正确。

**【修改建议】**
使用`os`，`pathlib`库来操作路径。

**【正例】**
1：路径操作
- 修复示例：使用`os`库辅助构造，路径格式和操作系统无关
```python
import os

file_name = 'tmp.txt'

file_path2 = os.getcwd() + os.sep + file_name  # 符合，/mnt/d/code/test/tmp.txt
file_path3 = os.path.join(os.getcwd(), file_name)  # 符合，/mnt/d/code/test/tmp.txt
```

**【反例】**
1：路径操作
- 错误示例：使用带有操作系统特有的路径格式
```python
import os

file_name = 'tmp.txt'
file_path1 = os.getcwd() + '\\\\' + file_name  # 不符合，该路径在Linux操作系统无法使用: /mnt/d/code/test\\tmp.txt
```

#### G.FIO.06 解压文件必须进行安全检查【要求】

**【描述】**
解压文件必须进行安全检查。

攻击者有可能上传一个很小的zip文件，但是完全解压缩之后达到几百万GB甚至更多，消耗完磁盘空间导致系统或你的程序无法正常运行。因此在解压缩文件时须要限制所使用的磁盘空间。

**【修改建议】**
禁止直接一次性递归解压压缩包全部内容，在解压前最少进行以下几点基础安全检查：
1. 文件个数是否超出业务预期个数；
2. 文件大小是否超出业务预期大小；
3. 文件大小是否超出目标目录所在磁盘空间。

建议根据需要，依赖其它工程手段加强防范，这些工程手段包括并不限于：
1. 为解压文件单独分区，限定大小；
2. 对压缩包做健康检查，包括其中内容是否符合业务预期；
3. 对CPU和内存的使用量进行限定，防止大量压缩包中海量小文件等攻击手段。（需结合程序实际运行情况估计，慎用）

以上几点建议**非强制执行**，正例中展示的是常用的校验方法，不能规避所有问题。

**【正例】**
1：未进行安全检查
- 修复示例：解压前最少进行以下几点基础安全检查
```python
import os
import zipfile
import psutil

class MyZip:  # 符合
    # 限制解压后大小不能超过1M，文件个数不能超过10个
    MAX_SIZE = 1 * 1024 * 1024
    MAX_FILE_CNT = 10

    @staticmethod
    def unzip(path, zip_file):
        file_path = path + os.sep + zip_file
        dest_dir = path

        with zipfile.ZipFile(file_path, 'r') as src_file:
            # 检查点1：检查文件个数，文件个数大于预期值时上报异常退出
            file_count = len(src_file.infolist())
            if file_count >= MyZip.MAX_FILE_CNT:
                raise IOError(f'zipfile({zip_file}) contains {file_count} files exceed max file count')

            # 检查点2：检查第一层解压文件总大小，总大小超过设定的上限值
            total_size = sum(info.file_size for info in src_file.infolist())
            if total_size >= MyZip.MAX_SIZE:
                raise IOError(f'zipfile({zip_file}) size({total_size}) exceed max limit')

            # 检查点3：检查第一层解压文件总大小，总大小超过磁盘剩余空间
            dest_dir_partition = '/'  # 解压目录所在分区
            if total_size >= psutil.disk_usage(dest_dir_partition).free:
                raise IOError(f'zipfile({zip_file}) size({total_size}) exceed remain target disk space')

            # 所有检查通过之后，解压所有文件
            src_file.extractall(dest_dir)
```

**【反例】**
1：未进行安全检查
- 错误示例：
```python
import zipfile
import os

def unzip(path, zip_file):  # 不符合，没有进行安全检查
    file_path = path + os.sep + zip_file
    dest_dir = path
    src_file = zipfile.ZipFile(file_path, 'r')
    src_file.extractall(dest_dir)
```

## 2.13 序列化

#### G.SER.01 禁止使用pickle.load、_pickle.load和shelve模块加载外部数据【要求】

**【描述】**
禁止使用pickle.load、_pickle.load和shelve模块加载外部数据。

模块 `pickle` 实现了对一个 Python 对象结构的二进制序列化和反序列化。 *"pickling"* 是将 Python 对象及其所拥有的层次结构转化为一个字节流的过程，而 *"unpickling"* 是相反的操作，会将（来自一个 `binary file` 或者 `bytes-like object` 的）字节流转化回一个对象层次结构。
`pickle`模块存在安全风险，攻击者通过构造恶意数据，在`pickle`模块反序列化时触发任意代码执行。因此禁止对外部数据和可能被篡改过的数据进行反序列化。
`_pickle`模块是用C语言实现的序列化模块，同样存在安全风险。当`_pickle`模块存在时，`pickle`模块会优先使用`_pickle`模块进行序列化和反序列化；反之`pickle`模块会使用python语言实现的序列化模块。
`shelve`模块使用`pickle`模块实现反序列化数据，数据保存在`shelve`模块Shelf类的实例中。因此使用`shelve`模块加载外部数据也是不安全的。

**【修改建议】**
使用 `hmac` 对序列化数据进行签名，确保数据没有被篡改。

**【正例】**
1：使用pickle加载外部数据
- 修复示例：使用json加载外部数据
```python
import json

with open('data.json', 'r') as f:
    # 使用json.loads加载外部数据
    data = json.loads(f.read())  # 符合
```

**【反例】**
1：使用pickle加载外部数据
- 修复示例：使用pickle加载外部数据
```python
import pickle

with open('data.pkl', 'rb') as f:
    # 使用pickle.loads加载外部数据
    data = pickle.loads(f.read())  # 不符合
```

#### G.SER.02 禁止序列化未加密的敏感数据【要求】

**【描述】**
禁止序列化未加密的敏感数据。

虽然序列化可以将对象的状态保存为一个字节序列，之后通过反序列化该字节序列又能重新构造出原来的对象，但是它并没有提供一种机制来保证序列化数据的安全性。可访问序列化数据的攻击者可以借此获取敏感信息并确定对象的实现细节。敏感数据序列化之后是是对外暴露着的，因此序列化信息中不应该包括：密钥、数字证书、以及那些在序列化时引用敏感数据的类。此条规则的意义在于防止敏感数据被无意识的序列化导致敏感信息泄露。

**【修改建议】**
在将某个包含敏感数据的类序列化时，程序必须确保敏感数据不被序列化。这包括阻止包含敏感信息的数据成员被序列化，以及不可序列化或者敏感对象的引用被序列化。

**【正例】**
1：序列化未加密含敏感信息
- 修复示例：序列化之前删除敏感数据
```python
import pickle

class Password:
    def __init__(self, password, id):
        self.password = password
        self.id = id

    def __getstate__(self):
        state = dict(self.__dict__)
        del state['password']  # 符合
        return state

dump_str = pickle.dumps(Password(12, 3))
```

**【反例】**
1：序列化未加密含敏感信息
- 错误示例：
```python
import pickle

class Password:
    def __init__(self, password, id):
        self.password = password
        self.id = id

    def __getstate__(self):
        state = dict(self.__dict__)
        return state

dump_str = pickle.dumps(Password(12, 3))  # 不符合
```

#### G.SER.03 禁止使用yaml模块的load函数【要求】

**【描述】**
禁止使用yaml模块的load函数。

yaml模块在数据序列化和配置文件中使用比较广泛，其在解析数据的时候遇到特定格式的数据类型会自动转换为Python的对象，比如会将时间类型的数据自动转化Python时间对象。这个特点让攻击者有机可乘。

**【修改建议】**
下载PyYAML模块的最新版本，并使用其提供的安全函数：

- yaml.load(data, Loader=SafeLoader)
- yaml.load_all(data, Loader=SafeLoader)
- yaml.safe_load(data)
- yaml.safe_load_all(data)

**【正例】**
1：使用yaml.load加载外部数据
- 修复示例：使用安全的函数加载外部数据
```python
import yaml

poc = "!!python/object/apply:subprocess.check_output [[\\"calc.exe\\"]]"
# 符合：等价于 yaml.load(poc, Loader=yaml.SafeLoader)
yaml.safe_load(poc)
```

**【反例】**
1：使用yaml.load加载外部数据
- 错误示例1：使用yaml.load加载外部数据
```python
# PyYAML<5.1 版本成功启动计算器
import yaml

poc = "!!python/object/apply:subprocess.check_output [[\\"calc.exe\\"]]"
# 不符合：等价于 yaml.load(poc, Loader=yaml.Loader)
yaml.load(poc)
```
- 错误示例2：使用yaml.load加载外部数据
```python
# PyYAML<5.4 版本成功启动计算器
import yaml

poc = """!!python/object/new:tuple 
        - !!python/object/new:map 
        - !!python/name:eval
        - [ "__import__('os').system('calc.exe')" ]"""
# 不符合：等价于 yaml.load(poc, Loader=yaml.Loader)
yaml.load(poc)
```

#### G.SER.04 禁止使用jsonpickle模块的encode/decode或dumps/loads函数【要求】

**【描述】**
禁止使用jsonpickle模块的encode/decode或dumps/loads函数。

jsonpickle模块支持将任意对象转化为json。
使用jsonpickle模块加载来源不可信的JSON字符串存在潜在的安全风险。 jsonpickle模块不会对输入进行校验，这导致攻击者可构造恶意输入获取执行权限。

**【修改建议】**
使用其它安全的序列化模块，否则就要进行严格的白名单、黑名单过滤。

**【正例】**
1：代码中使用了jsonpickle模块
- 修复示例：使用json模块
```python
import json

poc = '{"py/reduce": [{"py/type": "subprocess.Popen"}, {"py/tuple": [{"py/tuple": ["cmd.exe", "/c", "calc.exe"]}]}]}'
json.decode(poc)  # 符合
```

**【反例】**
1：代码中使用了jsonpickle模块
- 错误示例：
```python
import jsonpickle

poc = '{"py/reduce": [{"py/type": "subprocess.Popen"}, {"py/tuple": [{"py/tuple": ["cmd.exe", "/c", "calc.exe"]}]}]}'
# 成功启动计算器
jsonpickle.decode(poc)  # 不符合
```

#### G.SER.05 在序列化操作时建议使用较为安全的json模块【建议】

**【描述】**
JSON是一种轻量级的数据交换格式。Python3提供了json模块对JSON数据进行序列化，dump/dumps用来序列化，load/loads用来反序列化。当处理外部数据序列化的需求时，推荐使用较为安全的json模块，并且json模块支持跨平台跨语言操作。

**【正例】**
```python
import json

d = dict(name='Bob', age=20, score=88)
json_str = json.dumps(d)
print(json_str)
```

对于类的实例对象，使用json序列化需要提供专门的转换函数
```python
import json

class Student(object):
    def __init__(self, name, age, score):
        self.name = name
        self.age = age
        self.score = score

s = Student('Bob', 20, 88)
print(json.dumps(s, default=lambda obj: obj.__dict__))
```

## 2.14 外部数据校验

#### P.13 检验跨信任边界传递的外部数据【要求】

**【描述】**
程序可能会接收来自用户、网络连接或其他来源的外部数据，并将这些数据跨信任边界传递到目标系统（如浏览器、数据库等）。由于目标系统可能无法区分处理畸形的外部数据，未经校验的外部数据可能会引起某种注入攻击，对系统造成严重影响，因此，必须对外部数据进行校验，且数据校验必须在信任边界以内进行（如对于web应用，需要在服务端做校验）
外部数据的范围包括但不限于：网络、用户输入（包括命令行、界面）、命令行、文件（包括程序的配置文件）、环境变量、进程间通信（包括管道、消息、共享内存、socket等、RPC）、跨信任域方法参数（对于API）等。

对于外部数据的具体校验，要结合实际的业务场景要采用与之相对的校验方式来消除安全隐患，对于缺少校验规则的场景，可结合其他的措施进行防护，保证不会存在安全隐患

对外部数据的校验包括但不局限于：
- 校验API接口参数合法性
- 校验数据长度
- 校验数据范围
- 校验数据类型和格式
- 校验集合大小
- 校验外部数据是否只包含可接受的字符（白名单校验，尤其需要注意一些特殊情况下的特殊字符）

**【正例】**
白名单校验
```python
def whitelist_verify(input_str):
    if not re.match("^[0-9A-Za-z_]+$", input_str):
        return remove_illegal_char(input_str)
    return input_str
```

#### G.EDV.01 禁止使用eval和exec函数执行不可信代码【要求】

**【描述】**
使用eval和exec函数执行不可信代码。

* eval函数的定义为`eval(expression[, globals[, locals]])` ,它将字符串expression当成有效 Python 表达式来求值，并返回计算结果。 
* exec函数的定义为`exec(object[, globals[, locals]])` ,它可以接受大量Python代码块。 

如果eval和exec使用了外部输入的字符串，且外部输入的字符串中存在恶意的代码，将造成由于代码注入导致的安全问题。
例如：下例中系统命令ls将被执行，同样的问题在调用exec时也是存在。

```python
please input string: __import__('os').system('ls -l')

eval(input('please input string: '))
```

要严格校验输入的字符串表达式的合法性。如果校验缺失，用户可以访问代码名称空间的变量，会引起信息泄露。
另外注意，eval函数还可以使用\_\_import__导入任意模块。

**【修改建议】**
使用白名单对传入eval、exec等函数的不可信参数进行校验。

**【正例】**
1：外部输入的数据作为参数传入可执行代码的函数（eval、exec等），且参数未经校验
- 修复示例：对外部数据进行校验
```python
def string_verify(input_str):
    # 检查输入字符串的长度
    if not input_str or len(input_str) > 20:
        raise ValueError("输入字符串无效")
    # 删除或转义输入字符串中的特殊字符
    verified_str = input_str.replace("'", "").replace('"', "").replace("\\\\", "")
    return verified_str

code = input("请输入代码：")
# 校验外部数据
verified_code = string_verify(code)
eval(verified_code)  # 符合
```

**【反例】**
1：外部输入的数据作为参数传入可执行代码的函数（eval、exec等），且参数未经校验
- 错误示例：
```python
code = input("请输入代码：")
# 直接使用外部数据执行eval函数
eval(code)  # 不符合
```

#### G.EDV.02 禁止使用OS命令解析器或"危险函数"调用系统命令【要求】

**【描述】**
禁止使用OS命令解析器或"危险函数"调用系统命令。

使用未经校验的不可信输入作为系统命令的参数或命令的一部分，可能导致命令注入漏洞。对于命令注入漏洞，命令将会以与Python应用程序相同的特权级别执行，它向攻击者提供了类似系统shell的功能。在Python中，os.system 或 os.popen 经常被用来调用一个新的进程，如果被执行的命令来自于外部输入，则可能会产生命令和参数注入。
执行命令的时候，必须注意以下几点：
1. 命令执行的字符串不要去拼接输入的参数，如果必须拼接时，要对输入参数进行白名单过滤
2. 对传入的参数要做类型校验，例如：整数数据，可以对数据进行整数强制转换
3. 对于要求限定格式化字符串类型的业务场景，要保证占位符的正确性。例如：int类型参数的拼接，使用`{:d}`，不能用`{:s}`

**【修改建议】**
使用白名单对os.system等命令执行函数的不可信参数进行校验，建议减少在python代码中调用命令执行函数，使用python提供的安全API替代shell命令操作。

**【正例】**
1：使用os.system执行外部命令
- 修复示例1：使用系统函数
```python
import os
import sys

try:
   # 使用os.listdir来列举目录下的内容
   print(os.listdir(sys.argv[1]))  # 符合
except Exception as ex:
   print(ex)
```

- 修复示例2：对外部数据进行校验
```python
import os
import re
import sys

def args_verify(args_list):
    # 校验数据长度
    if len(args_list) > 20:
        print('Parameter length error.')
        sys.exit()
    # 校验数据内容
    if re.match(r"^[.0-9A-Za-z@]+$", args_list[1]):
        return args_list[1]

try:
    # 校验外部数据
    verified_arg = args_verify(sys.argv)
    if verified_arg:
        print(os.system("ls " + verified_arg))  # 符合
except Exception as ex:
    print('exception:', ex)
```

**【反例】**
1：使用os.system执行外部命令
- 错误示例：使用os.system直接执行外部命令
```python
import os
import sys

try:
    # 使用os.system直接执行外部命令
    print(os.system("ls " + sys.argv[1]))  # 不符合
except Exception as ex:
    print('exception:', ex)
```

#### G.EDV.03 避免在命令解析器中使用通配符【要求】

**【描述】**
避免在命令解析器中使用通配符。

通配符是一种特殊符号，主要有星号（*）和问号（？），用来模糊匹配字符串（比如文件名，参数名），Linux系统中许多命令接受通配符，如果攻击者将软链接或者一些特性文件置于给定的路径位置，则可能造成严重后果。

**【修改建议】**
函数'chown','chmod'，'subprocess'等操作文件访问许可的函数或执行子进程的函数参数中不要使用包含有‘*’通配符

**【正例】**
1：执行子进程的函数参数中包含"*"通配符
- 修复示例：执行子进程的函数参数中不要包含"*"通配符
```python
import subprocess
import os

file_path = 'test.txt'
subprocess.Popen(['/bin/chmod', '640', file_path], shell=False)  # 符合
subprocess.Popen(['/bin/chown', 'user:user', file_path], shell=False)  # 符合
os.chown(file_path, uid, gid, follow_symlinks=False)  # 符合，禁止对软链接对应的目标文件操作
```

**【反例】**
1：执行子进程的函数参数中包含"*"通配符
- 错误示例：
```python
import subprocess
import os

os.system('/bin/chmod 640 *')  # 不符合
subprocess.Popen('/bin/chown user:user *', shell=True)  # 不符合
```

#### G.EDV.04 禁止使用subprocess模块中的shell=True选项【要求】

**【描述】**
禁止使用subprocess模块中的shell=True选项。

subprocess模块帮助开发者执行外部命令和程序，为开发者带来便利的同时也带来了风险，该模块下多个接口（如call、check_call、Popen、check_output等）都可以传递shell参数。 
shell=True这个参数的功能是Python解释器先运行一个shell环境，再用这个shell来执行Popen函数的第一个命令行字符串参数。 
推荐调用子进程的方式是使用run()函数，对于其他需要使用到更高阶的用法的可以使用底层Popen()接口，需要注意的一点是使用Popen方式时，当stdout=PIPE或者stderr=PIPE时有可能会造成阻塞，除非调用Popen.communicate()才能解决。

**【修改建议】**
安全的做法是将shell参数置为False，前面的参数转成list列表，这样传入的参数里即使有注入指令也不会被解析执行。切记第1个参数中的list列表的第一个元素不允许是“bash”、“cmd”、“/bin/sh”，第二个元素不允许是“-c”；只有满足了这两个前提条件，参数shell=False的情况才是安全的。

**【正例】**
1：在subprocess模块中开启shell=True
- 修复示例：设置shell=False
```python
import subprocess

# 符合：设置shell=False
subprocess.check_call(['/bin/ls', '-l'], shell=False)
```

**【反例】**
1：在subprocess模块中开启shell=True
- 错误示例：在subprocess模块中开启shell=True
```python
import subprocess

# 不符合：开启shell=True
subprocess.check_call('/bin/ls -l', shell=True)
subprocess.Popen('/bin/ls *', shell=True)
subprocess.Popen('/bin/ls %s' % ('something',), shell=True)
subprocess.Popen('/bin/ls *', shell=True)
subprocess.Popen('/bin/ls %s' % ('something',), shell=True)
subprocess.Popen('/bin/ls {}'.format('something'), shell=True)
```

#### G.EDV.05 调用外部可执行程序时建议使用绝对路径【建议】

**【描述】**
调用外部可执行程序时建议使用绝对路径。

在POSIX环境中，调用可执行程序依赖于PATH环境变量，如果攻击者能够调整PATH变量的内容或操纵文件系统，则用户可能会调用到虚假的可执行文件。该可执行文件将以创建Python进程的用户权限（可能是ROOT用户）来调用。因此建议以绝对路径调用可执行程序。

**【修改建议】**
以绝对路径调用可执行程序。

**【正例】**
1：未使用绝对路径调用可执行程序
- 修复示例：以绝对路径调用可执行程序
```python
import subprocess

subprocess.run(['/usr/bin/gcc', '--version'], shell=False)  # 符合，以绝对路径调用可执行程序
```

**【反例】**
1：未使用绝对路径调用可执行程序
- 错误示例：
```python
import subprocess

subprocess.run(['gcc', '--version'], shell=False)  # 不符合，未使用绝对路径调用可执行程序
```

#### G.EDV.06 禁止直接使用外部数据来拼接SQL语句【要求】

**【描述】**
禁止直接使用外部数据来拼接SQL语句。

SQL注入是指使用外部数据构造的SQL语句所代表的数据库操作与预期不符，这样可能会导致信息泄露或者数据被篡改。

**【修改建议】**
SQL注入产生的根本原因是使用外部数据直接拼接SQL语句，防护措施主要有以下三类：
1. 使用参数化查询：最有效的防护手段;
2. 对外部数据进行白名单校验;
3. 对外部数据中的与SQL注入相关的特殊字符进行转义：适用于必须通过字符串拼接构造SQL语句的场景，转义仅对由引号限制的字段有效。

**【正例】**
1：直接使用外部数据拼接SQL语句
- 修复示例：对外部数据进行校验
对于字符型的字段进行处理时，要对输入做转义，将单引号替换为两个单引号。
```python
import sqlite3
import sys

def string_verify(input_str):
    # Replace single quotes with two single quotes
    verified_str = input_str.replace("'", "''")
    return verified_str

def bad():
    conn = sqlite3.connect("e:/test_sqlite3.db")
    con_cursor = conn.cursor()

    username = sys.argv[0]
    # 校验外部数据
    verified_username = string_verify(username)
    cmd = "select * from COMPANY where NAME = '{:s}'".format(verified_username)
    con_cursor.execute(cmd)  # 符合

    conn.commit()
    conn.close()
```

**【反例】**
1：直接使用外部数据拼接SQL语句
- 错误示例：直接使用外部数据拼接SQL语句
```python
import sqlite3
import sys

def bad():
    conn = sqlite3.connect("e:/test_sqlite3.db")
    con_cursor = conn.cursor()

    # SOURCE：从 system 中读取数据
    username = sys.argv[0]
    # 直接使用外部数据拼接SQL语句
    cmd = "select * from COMPANY where NAME = '{:s}'".format(username)
    # SINK: 数据直接连接到execute()中使用的SQL语句中，可能会导致SQL注入
    con_cursor.execute(cmd)  # 不符合

    conn.commit()
    conn.close()
```

#### G.EDV.07 不受信任的外部数据禁止使用.format()进行格式化【要求】

**【描述】**
不受信任的外部数据禁止使用.format()进行格式化。

Python 2.6版本引入str.format字符串格式化方法，支持通过string类的format函数处理复杂变量替换以及值的格式化。如果格式化字符串可控，可能导致系统中的敏感信息泄露。

**【修改建议】**
禁止使用.format()对不受信任的外部数据进行格式化，若不可避免，则需通过白名单方式对外部数据进行校验或净化。

**【正例】**
1： 直接对外部数据进行格式化
- 修复示例：格式化前校验外部数据
```python
import re

class User:
    def __init__(self, name, password):
        self.name = name
        self.password = password

def args_verify(input_str):
    # 白名单检验：根据具体场景定制合法输入正则表达式
    safe_pattern = re.compile(r'^[0-9a-zA-z]{6}')
    if safe_pattern.search(input_str):
        return True
    return False

def string_verify(input_str):
    # 黑名单校验：过滤存在风险的字符
    risk_pattern = re.compile(r'[\{\}\._"\'\[\]]')
    if risk_pattern.search(input_str):
        return False
    return True

name = input('Please input name: ')
password = input('Please input password: ')
# 校验外部数据
if args_verify(name) and args_verify(password):
    user = User(name, password)
    data_format = input('Please input data format: ')
    # 校验外部数据
    if string_verify(data_format):
        print(data_format.format(u=user))  # 符合
```

**【反例】**
1： 直接对外部数据进行格式化
- 错误示例：
```python
class User:
    def __init__(self, name, password):
        self.name = name
        self.password = password

name = input('Please input name: ')
password = input('Please input password: ')
data_format = input('Please input data format: ')
user = User(name, password)
# 直接对外部数据进行格式化
print(data_format.format(u=user))  # 不符合
```

#### G.EDV.08 防止正则表达式引起的ReDos攻击【要求】

**【描述】**
防止正则表达式引起的ReDos攻击。

Python语言的正则引擎本质上是非确定型有穷自动机（NFA），通过回溯机制尝试正则表达式的所有可能执行路径。NFA引擎功能强大，但回溯机制存在效率问题，在最坏的情况下，正则表达式的回溯路径在输入的大小上呈指数级增长。若直接使用外部输入数据进行正则匹配，攻击者可通过构造特殊的正则表达式或目标字符串触发"回溯陷阱"，造成拒绝服务，这种攻击方式称为正则表达式拒绝服务（ReDoS）。

**【修改建议】**
禁止直接使用外部数据作为正则匹配的表达式或目标字符串，若不可避免，则必须使用白名单或黑名单对外部数据进行校验和净化；此外，应检视程序内的正则表达式，避免使用存在风险的表达式结构，包括但不限于：
```
(a+)+b([a-zA-Z]+)*(a|aa)+(a|a?)+(.*a){x} for x > 10(a[ab]*)+...(a+)+b
([a-zA-Z]+)*
(a|aa)+
(a|a?)+
(.*a){x} for x > 10
(a[ab]*)+
...
```

**【正例】**
1：可能引起redos攻击的正则表达式
- 修复示例：安全的正则表达式
```python
import re

# 符合：安全的正则表达式
pattern1 = re.compile(r'^(\d+)$')
pattern2 = re.compile(r'^(\d*)$')
```

**【反例】**
1：可能引起redos攻击的正则表达式
- 错误示例：可能引起redos攻击的正则表达式
```python
import re

# 不符合：具有自我重复的重复性分组的正则表达式
pattern1 = re.compile(r'^(\d+)+$')
pattern2 = re.compile(r'^(\d*)*$')
pattern3 = re.compile(r'^(\d+)*$')
pattern4 = re.compile(r'^(\d+|\s+)*$')

# 不符合：包含替换的重复性分组的正则表达式
pattern5 = re.compile(r'^(\d|\d|\d)+$')
pattern6 = re.compile(r'^(\d|\d?)+$')
```

#### G.EDV.09 禁止直接使用外部数据来拼接XML【要求】

**【描述】**
禁止直接使用外部数据来拼接XML。

若写入XML文档的数据可控，则攻击者可通过构造特殊输入对XML文档内容进行篡改，例如插入意外的标签、引起XML解析器异常等。一个典型的攻击场景是，攻击者可以通过控制XML文档修改电子商务中的认证凭据，或修改商品的价格，对商家造成经济损失。

**【修改建议】**
禁止直接使用外部数据拼接XML，若无法避免，则需对外部数据进行严格校验和净化；此外，建议使用defusedxml模块处理XML数据，详情可参考defusedxml官方文档。

**【正例】**
1：直接使用外部数据拼接XML
- 修复示例1：白名单方式校验示例一（使用正则表达式）
```python
import xml.etree.ElementTree as ET
import re

def my_clean(input_str):
    # 白名单校验：使用正则表达式
    compile_pattern = re.compile('^\d+$')
    if compile_pattern.match(input_str):
        return input_str
    return '0'

root = ET.Element("root")
child = ET.Element("child")
amount = input()
# 校验外部数据
verified_amount = my_clean(amount)
child.text = '<order>' \
             '<item>laptop</item>' \
             '<price>2800.00</price>' \
             '<amount>' + verified_amount + '</amount>' \
             '</order>'
root.append(child)  # 符合
```

- 修复示例2：白名单方式校验示例二（使用字符串方法isdigit()判断字符串中是否只包含数字字符）
```python
import xml.etree.ElementTree as ET

def my_clean(input_str):
    # 白名单校验：判断字符串中是否只包含数字字符
    if input_str.isdigit():
        return input_str
    return '0'

root = ET.Element("root")
child = ET.Element("child")
amount = input()
# 校验外部数据
verified_amount = my_clean(amount)
child.text = '<order>' \
             '<item>laptop</item>' \
             '<price>2800.00</price>' \
             '<amount>' + verified_amount + '</amount>' \
             '</order>'
root.append(child)  # 符合
```

- 修复示例3：黑名单方式校验
```python
import xml.etree.ElementTree as ET
import re

def my_clean(input_str):
    # 黑名单校验：使用正则表达式
    compile_pattern = re.compile('[<>"\'＆]+')
    if compile_pattern.search(input_str):
        return '0'
    return input_str

root = ET.Element("root")
child = ET.Element("child")
amount = input()
# 校验外部数据
verified_amount = my_clean(amount)
child.text = '<order>' \
             '<item>laptop</item>' \
             '<price>2800.00</price>' \
             '<amount>' + verified_amount + '</amount>' \
             '</order>'
root.append(child)  # 符合
```

**【反例】**
1：直接使用外部数据拼接XML
- 错误示例：以下XML文档定义了电子商城中笔记本电脑的价格，同时接受外部数据修改笔记本电脑的数量
```python
import xml.etree.ElementTree as ET

root = ET.Element("root")
child = ET.Element("child")
amount = input()
# 直接使用外部数据拼接XML
child.text = '<order>' \
             '<item>laptop</item>' \
             '<price>2800.00</price>' \
             '<amount>' + amount + '</amount>' \
             '</order>'
root.append(child)  # 不符合
```

#### G.EDV.10 禁止在处理XML数据时解析不可信的实体【要求】

**【描述】**
禁止在处理XML数据时解析不可信的外部实体。

XML实体包括内部实体和外部实体。外部实体格式： `<!ENTITY 实体名 SYSTEM "URI"\>` 或者 `<!ENTITY 实体名 PUBLIC "public_ID" "URI"\>`。
XXE（XML External Entity）漏洞全称为XML外部实体漏洞，XML文档中可能包含带有URI的外部实体，解析该文档时可通过URI访问其指向的内容，若XML文档中的URI可控，则攻击者可以修改URI指向特定的恶意文件，执行拒绝服务攻击，或未经授权访问系统文件。

XML内部实体格式： `<!ENTITY 实体名 "实体的值"\>` 。XEE（XML Entity Expansion）漏洞全称为XML实体扩展漏洞，又称十亿狂笑（Billion Laughs）或XML炸弹（XML Bomb），若在处理XML数据时允许使用DTD功能定义XML文档结构，且构造该文档结构的数据可控，则攻击者可在XML文档中构造存在大量嵌套或递归结构的实体，导致解析该文档时数据爆炸性增长，从而造成拒绝服务。因此，在处理XML数据时必须关闭外部实体解析开关，若无法避免解析外部实体，则需对外部实体进行严格校验和净化；此外，建议使用defusedxml模块处理XML数据，详情可参考defusedxml官方文档。

**【修改建议】**
在处理XML数据时必须关闭外部实体解析开关，若无法避免解析外部实体，则需对外部实体进行严格校验和净化；此外，建议使用defusedxml模块处理XML数据，详情可参考defusedxml官方文档。

**【正例】**
1：XML外部实体漏洞
- 修复示例：设置resolve_entities=False
将resolve_entities参数设置为False：
```python
from lxml import etree

xml_str = ''
with open('xml_file.xml', 'r') as fp:    
    xml_str = fp.read()

parserSafe = etree.XMLParser(resolve_entities=False)  # 符合：将resolve_entities参数设置为False
root = etree.XML(xml_str.encode('utf-8'), parser=parserSafe)
_config = list()
for GuestOSType_node in root.getchildren():    
    one_guestos = {}    
    for item in GuestOSType_node.items():        
        one_guestos["@" + item[0]] = item[1]    
    for node in GuestOSType_node.getchildren():        
        one_guestos[node.tag] = node.text    
    _config.append(one_guestos)
print(_config)
```

2：XML实体扩展漏洞
- 修复示例：使用defusedxml模块
使用defusedxml模块：
```python
import defusedxml.minidom as dom

xml_path = input()
result = dom.parse(xml_path)  # 符合：使用defusedxml模块
print(result)
```

**【反例】**
1：XML外部实体漏洞
- 错误示例：存在XML外部实体漏洞
假设存在用户可配置的XML文件（xml_file.xml）如下：
```xml
<OSCONFIG version="v001">	
    <GuestOSType id="1" name="CentOS 7.4" OSType="linux" OSbit="64">		
        <MaxCPU>96</MaxCPU>		
        <MaxMemory>128</MaxMemory>	
    </GuestOSType>
</OSCONFIG>
```
2：XML实体扩展漏洞
- 错误示例：存在XML实体扩展漏洞
```python
import xml.dom.minidom as dom

xml_path = input()
result = dom.parse(xml_path)  # 不符合：存在XML实体扩展漏洞
print(result)
```

## 2.15 日志

#### G.LOG.01 logging模块应尽量使用懒插值的能力记录日志【建议】

**【描述】**
logging模块应尽量使用懒插值的能力记录日志。

logging模块具有懒插值特性：当采用`logging.<logging method>(format_string, format_args)`形式，logger将对日志消息中的参数字符串进行延迟插值。建议日志打印尽量采用该方式。

**【修改建议】**
logging模块具有懒插值特性：当采用`logging.<logging method>(format_string, format_args)`形式，logger将对日志消息中的参数字符串进行延迟插值。建议日志打印尽量采用该方式。

**【正例】**
1：使用%拼接
- 修复示例：
```python
import logging

error_details = "it is really a big bug."
error_details_ext = "Yes, really big."
logging.error("Here catch some errors, detail is:%s more:%s", error_details, error_details_ext)  # 符合
```
2：使用format拼接
- 修复示例：
```python
import logging

error_details = "it is really a big bug."
error_details_ext = "Yes, really big."
logging.error("Here catch some errors, detail is:%s more:%s", error_details, error_details_ext)  # 符合
```
3：f-string格式化
- 修复示例：
```python
import logging

error_details = "it is really a big bug."
error_details_ext = "Yes, really big."
logging.error("Here catch some errors, detail is:%s more:%s", error_details, error_details_ext)  # 符合
```

**【反例】**
1：使用%拼接
- 错误示例：
```python
import logging

error_details = "it is really a big bug"
logging.error("Here catch some errors, detail is:%s" % error_details)  # 不符合
```
2：使用format拼接
- 错误示例：
```python
import logging

error_details = "it is really a big bug"
logging.error("Here catch some errors, detail is:{}".format(error_details))  # 不符合
```
3：f-string格式化
- 错误示例：
```python
import logging

error_details = "it is really a big bug"
logging.error(f"Here catch some errors, detail is:{error_details}")  # 不符合
```

#### G.LOG.02 使用日志记录工具实现日志功能【建议】

**【描述】**
使用日志记录工具实现日志功能。

使用标准输出（print）或标准输出（sys.stdout.write），会导致难以监控程序运行状况。

**【修改建议】**
建议采用专门的日志记录工具或模块（如：logging）。

**【正例】**
1：使用print打印到控制台
- 修复示例：采用正确的级别及形式记录日志

  ```python
  import logging
  import threading
  import time

  logging.basicConfig(level=logging.NOTSET)  # 指定日志文件路径等

  class MyThread(threading.Thread):
      def __init__(self, thread_id, name, counter):
          threading.Thread.__init__(self)
          self.thread_id = thread_id
          self.name = name
          self.counter = counter

      def run(self):
          logging.info("Starting: %s", self.name)  # 符合：采用正确的级别及形式记录日志
          process_something(self.name, self.counter)
          logging.info("Exiting:%s", self.name)  # 符合：采用正确的级别及形式记录日志

  def process_something(thread_name, counter):
      while counter:
          logging.debug("%s: %s", thread_name, time.ctime(time.time()))  # 符合：采用正确的级别及形式记录日志
          counter -= 1
  ```
2：使用sys.stdout.write打印到控制台
- 修复示例：采用正确的级别及形式记录日志

  ```python
  import logging
  import threading
  import time

  logging.basicConfig(level=logging.NOTSET)  # 指定日志文件路径等

  class MyThread(threading.Thread):
      def __init__(self, thread_id, name, counter):
          threading.Thread.__init__(self)
          self.thread_id = thread_id
          self.name = name
          self.counter = counter

      def run(self):
          logging.info("Starting: %s", self.name)  # 符合：采用正确的级别及形式记录日志
          process_something(self.name, self.counter)
          logging.info("Exiting:%s", self.name)  # 符合：采用正确的级别及形式记录日志

  def process_something(thread_name, counter):
      while counter:
          logging.debug("%s: %s", thread_name, time.ctime(time.time()))  # 符合：采用正确的级别及形式记录日志
          counter -= 1
  ```

**【反例】**
1：使用print打印到控制台
- 错误示例：使用print打印到控制台

  ```python
  import threading

  class MyThread(threading.Thread):
      def __init__(self, thread_id, name, counter):
          threading.Thread.__init__(self)
          self.thread_id = thread_id
          self.name = name
          self.counter = counter

      def run(self):
          print("Starting " + self.name)  # 不符合：使用print打印到控制台
          process_something(self.name, self.counter, 5)
          print("Exiting " + self.name)  # 不符合：使用print打印到控制台
  ```
2：使用sys.stdout.write打印到控制台
- 错误示例：使用sys.stdout.write打印到控制台

  ```python
  import sys
  import threading

  class MyThread(threading.Thread):
      def __init__(self, thread_id, name, counter):
          threading.Thread.__init__(self)
          self.thread_id = thread_id
          self.name = name
          self.counter = counter

      def run(self):
          sys.stdout.write("Starting " + self.name)
          process_something(self.name, self.counter, 5)
          sys.stdout.write("Exiting " + self.name)  # 不符合：使用sys.stdout.write打印到控制台
  ```

#### G.LOG.03 禁止直接使用外部数据记录日志【要求】

**【描述】**
禁止直接使用外部数据记录日志。

直接将外部数据记录到日志中，可能存在以下风险：
- 日志注入：恶意用户可利用回车、换行等字符注入一条完整的日志； 
- 敏感信息泄露：当用户输入敏感信息时，直接记录到日志中可能会导致敏感信息泄露；
- 垃圾日志或日志覆盖：当用户输入的是很长的字符串，直接记录到日志中可能会导致产生大量垃圾日志；当日志被循环覆盖时，这样还可能会导致有效日志被恶意覆盖。

所以外部数据应尽量避免直接记录到日志中，如果必须要记录到日志中，要进行必要的校验及过滤处理，对于较长字符串可以截断。对于记录到日志中的数据含有敏感数据时，对于秘钥、口令类的敏感信息，参考\[G.LOG.04 禁止在日志中记录口令、密钥等敏感信息\]将这些敏感信息替换为固定长度的*，对于其他类的敏感信息（如手机号、邮箱等），可进行匿名化处理。

**【修改建议】**
外部数据应尽量避免直接记录到日志中，如果必须要记录到日志中，要进行必要的校验及过滤处理，对于较长字符串可以截断。

**【正例】**
```python
def replaceCRLF(message):
    if message:
        return message.replace('\n', '_').replace('\r', '_');
    else:
        ...
```

**【反例】**
```python
json_data = get_request_body_data(request)
if not validate_request_data(data):
    logger.error("Request data validate fail! Request Data :  " + json_data)
```

## 2.16 性能与资源管理

#### P.14 在try代码块内如果修改了资源，需要在except子句内将对应的资源还原【建议】

**【描述】**
在使用try/except结构对一段有原子性数据操作的代码做保护时，如果出现异常，应即使将对应的资源还原。这个原则不局限于数据库业务处理。

**【正例】**
异常时正确还原资源
场景1：文件操作异常时关闭文件
```python
file = None
try:
    file = open("data.txt", "w")
    file.write("Hello, World!")  # 模拟写入时出错
    raise ValueError("模拟写入错误")
except ValueError as e:
    print(f"捕获异常: {e}")
    if file:  # 检查文件是否已打开
        file.close()  # 确保文件句柄被释放
        print("已关闭文件")
finally:
    if file:  # 最终检查（防止未捕获的异常）
        file.close()
```

场景2：数据库事务回滚
```python
import sqlite3

conn = sqlite3.connect(":memory:")
cursor = conn.cursor()
cursor.execute("CREATE TABLE users (id INTEGER, name TEXT)")

try:
    cursor.execute("INSERT INTO users VALUES (1, 'Alice')")
    cursor.execute("INSERT INTO users VALUES (2, 'Bob')")
    raise RuntimeError("模拟数据库错误")  # 触发异常
    conn.commit()  # 正常情况下提交
except Exception as e:
    print(f"数据库操作失败: {e}")
    conn.rollback()  # 异常时回滚
finally:
    conn.close()
```

**【反例】**
未处理异常导致资源泄漏
反例1：文件未关闭
```python
try:
    file = open("data.txt", "w")
    file.write("Hello, World!")
    raise ValueError("模拟错误")
except ValueError as e:
    print(f"捕获异常: {e}")
    # 忘记关闭文件！导致文件句柄泄漏
```
问题：文件句柄未被释放，可能导致系统资源耗尽。

反例2：数据库未回滚
```python
conn = sqlite3.connect(":memory:")
cursor = conn.cursor()
cursor.execute("CREATE TABLE users (id INTEGER, name TEXT)")

try:
    cursor.execute("INSERT INTO users VALUES (1, 'Alice')")
    raise RuntimeError("模拟错误")
    conn.commit()
except Exception as e:
    print(f"错误: {e}")
    # 忘记 conn.rollback()！数据库处于未提交状态
finally:
    conn.close()
```
问题：事务未提交也未回滚，可能导致锁表或数据不一致。

#### P.15 合并大量字符串时建议根据需求选择合适的方式【建议】

**【描述】**
在字符串合并的场景，由于字符串是不可变的，因此如果使用+或+=会产生不必要的临时对象，导致需要额外的运行时间。所以应该根据具体的数量、内存使用和执行时间选取合适的字符串合并方式。
在大量字符串合并且对性能敏感的场景：
- 追求时间：优先选择`list.append + str.join(Iterable)`
- 追求内存使用少：优先使用`+, +=`的方式

少量字符串合并或性能不敏感的场景以可读性优先

**【正例】**
高效字符串合并
场景1：大量合并（时间优先）
```python
# 正确做法：使用 list.append + join（高效）
parts = []
for i in range(10_000):
    parts.append(f"data_{i}")  # 避免临时字符串
result = "".join(parts)        # 一次性合并
```
性能对比（10万次合并）：
```python
import time

# 方法1: += （慢）
start = time.time()
s = ""
for i in range(100_000):
    s += f"word_{i}"
print(f"+= 耗时: {time.time() - start:.4f}秒")

# 方法2: list.append + join （快）
start = time.time()
parts = []
for i in range(100_000):
    parts.append(f"word_{i}")
s = "".join(parts)
print(f"join 耗时: {time.time() - start:.4f}秒")
```
输出：
```text
+= 耗时: 0.1023秒
join 耗时: 0.0287秒  # 快3倍以上！
```
场景2：少量合并（内存优先）
```python
# 少量操作时，直接用 += （代码简洁）
name = "Alice"
greeting = "Hello, " + name + "!"  # 可接受
```

#### P.16 在内存敏感的场景下建议使用生成器代替一次性生成数据的容器【建议】

**【描述】**
推导式会一次性构造一个对象仓库并以聚合的关系长期持有其中的对象。生成器则会在外部调用时生成并返回一个对象，可以不持有生成的对象。因此，在内存敏感，且不需要长期大量持有对象的场景下，可以考虑选用生成器代替推导式。

**【正例】**
生成器节省内存
场景：读取大文件并逐行处理
```python
# 使用生成器函数（惰性读取）
def read_large_file(file_path):
    with open(file_path, "r") as file:
        for line in file:
            yield line.strip()  # 逐行生成，不一次性加载

# 处理文件（内存占用恒定）
for line in read_large_file("huge_log.txt"):
    process(line)  # 假设 process() 是处理函数
```
生成器表达式（更简洁）
```python
# 生成器表达式替代列表推导式
numbers = (x * 2 for x in range(1_000_000))  # 不立即计算
for num in numbers:
    print(num)  # 用时才生成
```
内存对比（通过 sys.getsizeof 验证）：
```python
import sys

# 列表推导式（占用内存）
list_data = [x for x in range(1_000_000)]
print(f"列表推导式内存: {sys.getsizeof(list_data):,} bytes")  # 约 8 MB

# 生成器表达式（几乎不占内存）
gen_data = (x for x in range(1_000_000))
print(f"生成器内存: {sys.getsizeof(gen_data):,} bytes")  # 约 128 bytes
```

#### G.PRM.01 在list成员个数可以预知的情况下，创建list时建议预留容纳所有成员的空间【建议】

**【描述】**
与java, C++等语言的list一样，python语言的list在append()成员时，如果没有多余的空间容纳新的成员，就会分配一块更大的内存，并将原来内存里的成员拷贝到新的内存上，并将最新append()的成员也拷贝到此新内存空间中，然后释放老的内存空间。如果append()调用次数很大，则如上过程会频繁发生，因而会造成灾难性性能下降。因此，建议在list成员个数较大的场景下使用固定大小创建并初始化list。个数的大小根据具体业务需要决定。

**【正例】**
```python
from timeit import Timer

def test_performance():
    members = [None] * 1000000
    for i in range(1, 1000000):
        members[i] = i

print("append:", Timer("test_performance()", "from __main__ import test_performance").timeit(1000)) # append: 48.7
```

**【反例】**
```python
from timeit import Timer

def test_performance():
    members = []
    for i in range(1, 1000000):
        members.append(i)

print("append:", Timer("test_performance()", "from __main__ import test_performance").timeit(1000)) # append: 74.707
```

#### G.PRM.02 在成员个数及内容皆不变的场景下建议使用tuple代替list【建议】

**【描述】**
list与tuple性能对比：
1. list是动态序列，而tuple是静态序列（其成员个数以及内容皆不可变），list需要更多的内存来跟踪其成员的状态
2. list的初始化过程比tuple更耗时
在list和tuple之间进行选取时可以权衡一下业务需要和性能要求，如果成员个数以及内容皆不变则优先考虑使用tuple。

**【正例】**
```python
# 在constant.py无需改变的固定常量采用元组的形式
LANGUAGE_TUPLE = ('en', 'en_US', 'ar', 'ar_AE', 'zh_CN')
```

**【反例】**
```python
# 在constant.py无需改变的固定常量采用列表的形式
LANGUAGE_TUPLE = ['en', 'en_US', 'ar', 'ar_AE', 'zh_CN']
```

#### G.PRM.03 资源的申请和释放需要成对使用，包括正常和异常场景【建议】

**【描述】**
使用open函数打开文件后，需要调用close关闭文件句柄。

**【修改建议】**
使用open后需要关闭文件句柄

**【正例】**
1：socket对象使用结束后未关闭
- 修复示例1：在同一个函数中显示关闭使用结束后的socket
```python
import socket

def good_case():
    s = None
    try:
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)  # 定义socket类型，网络通信，TCP
        s.connect((HOST, PORT))  # 要连接的IP与端口
        ...
    except IOError as e:
        logger.error(e)  

    if s:
        s.close()  # 符合，显式关闭socket
```

- 修复示例2：推荐使用with/as语句
```python
import socket

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:  # 符合
    s.connect((HOST, PORT))  # 要连接的IP与端口
    ...
```

- 修复示例3：异常场景建议在try/except/finally结构的finally代码块中关闭资源
```python
def good_case():
    s = None
    try:
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)  # 定义socket类型，网络通信，TCP
        s.connect((HOST, PORT))  # 要连接的IP与端口
        ...
    except IOError as e:
        logger.error(e)  
    finally:
        if s:
            s.close()  # 符合
```

**【反例】**
1：socket对象使用结束后未关闭
- 错误示例：在函数中打开socket，使用结束后未关闭
```python
import socket

def bad_case():
    try:
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)  # 不符合
        s.connect((HOST, PORT))  # 要连接的IP与端口
    except IOError as e:
        logger.error(e)   
```

## 2.17 代码测试

#### G.TES.01 禁止在生产版本的业务代码中使用assert【要求】

**【描述】**
禁止在生产版本的业务代码中使用assert。

在编译时编译优化参数如果大于等于1，编译器就会删除`assert`语句。 如果在业务代码中使用了`assert`语句做了一些特殊的业务匹配，同时使用了编译优化，则可能会出现不可预期的结果。
所以`assert`语句通常只在测试代码中使用，禁止在生产版本的业务代码中使用`assert`，具体的关于`assert`的信息可以查看官方介绍。

**【修改建议】**
正式发布代码中应删除assert语句。

**【正例】**
1：在业务代码中使用assert
- 修复示例：不使用assert
```python
import sys

class NotSupportedError(Exception):
    def __str__(self):
        return "Code is Linux only"

def check_system():
    if "linux" in sys.platform:
        return
    raise NotSupportedError()

check_system()  # 符合：不使用assert
```

**【反例】**
1：在业务代码中使用assert
- 错误示例：使用了assert
```python
import sys

def check_system():
    assert ("linux" in sys.platform), "Code is Linux only"  # 不符合：使用了assert

check_system()
```

#### G.TES.02 使用对应的方法做值断言【建议】

**【描述】**
对于不同的值做断言，Python单元测试模块unittest中的测试用例类TestCase提供了各种不同的方法，建议使用对应的方法做值断言。

**【修改建议】**
写测试用例时使用unittest模块中对应的方法做值断言。

**【正例】**
1：检查布尔值
- 修复示例：使用assertTrue/False来检查布尔值
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_bool_values(self):
        true, false = True, False
        self.assertTrue(true)   # 符合
        self.assertFalse(false)  # 符合
```
2：检查None或非None的值
- 修复示例：使用assertIs(Not)None来检查None或非None的值
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_is_none_and_not_none(self):
        none, not_none = None, ""
        self.assertIsNone(none)     # 符合
        self.assertIsNotNone(not_none)     # 符合
```
3：检查对象相等性
- 修复示例：建议使用assert(Not)Equal来检查对象相等性
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_is_equals_and_not_equals(self):
        value_one, value_two, value_three = 1, 2, 1
        self.assertEqual(value_one, value_three)    # 符合
        self.assertNotEqual(value_two, value_three)    # 符合
```
4：检查对象大小
- 修复示例：建议使用assert(Greater|Less|Equal)来检查比较对象大小
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_comparison(self):
        value_one, value_two, value_three, value_four = 1, 2, 1, 4
        self.assertGreater(value_two, value_one)   # 符合
        self.assertEqual(value_one, value_three)   # 符合
        self.assertLess(value_one, value_four)   # 符合
```
5：检查对象是否为特定类型的实例
- 修复示例：建议使用assert(Not)IsInstance来检查对象是否为特定类型的实例
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_is_instance_or_not_is_instance(self):
        value = 1
        self.assertIsInstance(value, int)   # 符合
        self.assertNotIsInstance(value, str)   # 符合
```
6：检查对象是否在对应的可迭代对象中
- 修复示例：建议使用assertI(Not)In来检查对象是否在对应的可迭代对象中
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_is_in_collection(self):
        value, values = 1, [1, 2, 3, 4]
        self.assertIn(value, values)   # 符合
        self.assertNotIn(5, values)   # 符合
```

**【反例】**
1：检查布尔值
- 错误示例：使用assertEqual来检查布尔值
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_bool_values(self):
        true, false = True, False
        self.assertEqual(true, True)   # 不符合
        self.assertEqual(false, False)   # 不符合
```
2：检查None或非None的值
- 错误示例：使用assertTrue来检查None或非None的值
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_is_none_and_not_none(self):
        none, not_none = None, ""
        self.assertTrue(none is None)       # 不符合
        self.assertTrue(not_none is not None)     # 不符合
```
3：检查对象相等性
- 错误示例：使用assertTrue/assertFalse来检查对象相等性
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_is_equals_and_not_equals(self):
        value_one, value_two, value_three = 1, 2, 1
        self.assertTrue(value_one == value_three)       # 不符合
        self.assertFalse(value_two == value_three)       # 不符合
```
4：检查对象大小
- 错误示例：使用assertTrue来检查比较对象大小
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_comparison(self):
        value_one, value_two, value_three, value_four = 1, 2, 1, 4
        self.assertTrue(value_two > value_one)       # 不符合
        self.assertTrue(value_one == value_three)       # 不符合
        self.assertTrue(value_one < value_four)       # 不符合
```
5：检查对象是否为特定类型的实例
- 错误示例：使用assertTrue/assertFalse来检查对象是否为特定类型的实例
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_is_instance_or_not_is_instance(self):
        value = 1
        self.assertTrue(isinstance(value, int))       # 不符合
        self.assertFalse(isinstance(value, str))       # 不符合
```
6：检查对象是否在对应的可迭代对象中
- 错误示例：使用assertTrue来检查对象是否在对应的可迭代对象中
```python
import unittest

class TestCaseDemo(unittest.TestCase):
    def test_object_is_in_collection(self):
        value, values = 1, [1, 2, 3, 4]
        self.assertTrue(value in values)      # 不符合
        self.assertTrue(5 not in values)      # 不符合
```

## 2.18 数据安全处理

#### G.DSP.01 将敏感对象发送出信任区域前进行签名并加密【要求】

**【描述】**
将敏感对象发送出信任区域前进行签名并加密。

敏感数据传输过程中存在被窃取和恶意篡改的可能。使用安全的加密算法加密传输对象可以保护数据，防止对象被非法篡改，保持其完整性。在以下场景中，需要对对象加密和数字签名来保证数据安全:
1. 序列化或传输敏感数据；
2. 没有使用类似于SSL传输通道；
3. 敏感数据需要长久保存（比如在硬盘驱动器上）。

**【修改建议】**
敏感信息跨信任域传递时要进行签名并加密。

**【正例】**
1：敏感信息跨信任域传递时未进行签名并加密
- 修复示例：加密，以SHA256算法为例
```python
import crypt

sensitive_data = "********"
file_path = 'xxxx'
sensitive_data = crypt.crypt(sensitive_data, crypt.METHOD_SHA256)  # 符合，加密，以SHA256算法为例
with open(file_path, 'w') as file:
    file.write(sensitive_data)
```

**【反例】**
1：敏感信息跨信任域传递时未进行签名并加密
- 错误示例：
```python
sensitive_data = "********"
file_path = 'xxxx'

with open(file_path, 'w') as file:
    file.write(sensitive_data)  # 不符合
```

#### G.DSP.02 安全场景下必须使用密码学意义上的安全随机数【要求】

**【描述】**
安全场景下必须使用密码学意义上的安全随机数。

Python的random模块实现了基于各种分布的伪随机数生成器。产生的随机数可以是均匀分布、高斯分布、对数正态分布、负指数分布以及alpha、beta分布，但是这些随机数都是伪随机数，禁止应用于安全加密目的的应用中。出于安全加密目的的应用中禁止使用random模块生成的伪随机数，必须使用安全随机数。

**【修改建议】**
出于安全加密目的的应用中禁止使用random模块生成的伪随机数，必须使用安全随机数。

**【正例】**
1：使用random模块生成伪随机数
- 修复示例：Python3.6以上版本的os.urandom方法以阻塞模式从系统指定的随机源获取随机字节，因此使用os.urandom方法生成随机数是安全的：
```python
import os
import platform

# 长度请参见密码算法规范，不同场景要求长度不一样
rand_length = 16

# 符合：Python3.6以上版本使用os.urandom生成随机数
_rand_lst = list(os.urandom(rand_length))
print(_rand_lst)
_rand_bytes = os.urandom(rand_length)
print(_rand_bytes)
```
- 修复示例：推荐使用secrets模块生成随机数
```python
import secrets

# 符合：使用secrets模块生成随机数
number = secrets.randbelow(10)
print("Secure random number is ", number)
# Secure random number is 0
secrets_generator = secrets.SystemRandom()
random_number = secrets_generator.randint(0, 50)
print("Secure random number is ", random_number)
# Secure random number is 26

# 指定范围并设置步长
random_number = secrets_generator.randrange(5, 50, 5)
print("Secure random number within range is ", random_number)
# Secure random number within range is 15

# 从指定的数据集中选择
number_list = [6, 12, 18, 24, 30, 36, 42, 48, 54, 60]
secure_choice = secrets_generator.choice(number_list)
print("Secure random choice using secrets is ", secure_choice)
# Secure random choice using secrets is 30
secure_sample = secrets_generator.sample(number_list, 3)
print("Secure random sample using secrets is ", secure_sample)
# Secure random sample using secrets is [54, 6, 42]

# 随机安全浮点数
secure_float = secrets_generator.uniform(2.5, 25.5)
print("Secure random float number using secrets is ", secure_float)
# Secure random float number using secrets is 9.445927455984885
```

**【反例】**
1：使用random模块生成伪随机数
- 错误示例：使用random模块生成伪随机数
```python
import random

# 不符合：使用random模块生成伪随机数
sr = random.randint(0, 100)
```

#### G.DSP.03 必须使用ssl.SSLSocket代替socket.Socket来进行安全数据交互【要求】

**【描述】**
禁止使用socket.Socket传输敏感数据。

必须使用ssl.SSLSocket代替socket.Socket来进行安全数据交互。

Python提供的socket.Socket类可用于创建套接字，传输敏感数据时必须使用ssl.SSLSocket类创建安全套接字，该类提供了SSL/TSL等安全传输协议来确保传输通道不受攻击者的监听或恶意篡改。

SSLSocket类提供的主要保护包括：
1. 完整性保护：SSL防止消息被主动窃取者篡改。
2. 认证：在大多数模式下，SSL都对对端进行认证。服务器通常都被认证，如果服务器要求，客户端也可以被认证。
3. 保密性：在大多数模式下，SSL对客户端和服务器之间传输的数据进行加密。这样保护了数据的隐私性，被动窃听器不能监听诸如财务或者个人信息等敏感信息。

**【修改建议】**
使用SSL/TLS安全协议保护传输的报文。

**【正例】**
1：服务端
- 修复示例：使用ssl.SSLSocket进行安全数据交互

```python
import socket
import time
import ssl

# 使用ssl.SSLSocket
context = ssl.SSLContext(ssl.PROTOCOL_TLSv1_2)
context.load_cert_chain(certfile="zxcert.pem", keyfile="zxkey.pem")

bindsocket = socket.socket()
print("socket create success")
bindsocket.bind(('127.0.0.1', 10023))
print("socket bind success")
bindsocket.listen(5)
print("socket listen success")

def do_something(connstream, data):
    print("data length:", len(data))
    return True

def deal_with_client(connstream):
    t_recv = 0
    t_send = 0
    n = 0
    t1 = time.perf_counter()
    data = connstream.recv(1024)
    t2 = time.perf_counter()
    print("receive time:", t2 - t1)
    # empty data means the client is finished with us
    while data:
        if not do_something(connstream, data):
            # we'll assume do_something returns False
            # when we're finished with client
            break
        n = n + 1
        t1 = time.perf_counter()
        connstream.send(b'b' * 1024)  # 符合
        t2 = time.perf_counter()
        t_send += t2 - t1
        print("send time:", t2 - t1)
        t1 = time.perf_counter()
        data = connstream.recv(1024)  # 符合
        t2 = time.perf_counter()
        t_recv += t2 - t1
        print("receive time:", t2 - t1)
    print("avg send time:", t_send / n, "avg receive time:", t_recv / n)

# finished with client
while True:
    newsocket, fromaddr = bindsocket.accept()
    print("socket accept one client")
    connstream = context.wrap_socket(newsocket, server_side=True)
    try:
        deal_with_client(connstream)
    finally:
        connstream.shutdown(socket.SHUT_RDWR)
        connstream.close()
```
2：客户端
- 修复示例：使用ssl.SSLSocket进行安全数据交互

```python
import pprint
import socket
import time
import ssl

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
print("socket create success")
# require a certificate from the server
# 使用ssl.SSLSocket
ssl_sock = ssl.wrap_socket(s,
                           ca_certs="zxcert.pem",
                           cert_reqs=ssl.CERT_REQUIRED)
ssl_sock.connect(('127.0.0.1', 10023))
print("socket connect success")
pprint.pprint(ssl_sock.getpeercert())
# note that closing the SSLSocket will also close the underlying socket
n = 0
t_send = 0
t_recv = 0
while n < 10:
    n = n + 1
    t1 = time.perf_counter()
    ssl_sock.send(b'a' * 100)  # 符合
    t2 = time.perf_counter()
    t_send += t2 - t1
    print("send time:", t2 - t1)
    t1 = time.perf_counter()
    data = ssl_sock.recv(1024)
    t2 = time.perf_counter()
    t_recv += t2 - t1
    print("receive time:", t2 - t1)
print("avg send time:", t_send / n, "avg receive time:", t_recv / n)
ssl_sock.close()
```

**【反例】**
1：服务端
- 错误示例：使用socket.Socket进行数据交互

```python
import socket

# Symbolic name meaning all available interfaces
HOST = ''
# Arbitrary non-privileged port
PORT = 50007
# 使用socket.Socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.bind((HOST, PORT))
s.listen(1)
conn, addr = s.accept()
print('Connected by', addr)
while True:
    data = conn.recv(1024)  # 不符合
    if not data:
        break
    conn.sendall(data)  # 不符合
conn.close()
```
2：客户端
- 错误示例：使用socket.Socket进行数据交互

```python
import socket

# The remote host
HOST = ''
# The same port as used by the server
PORT = 50007
# 使用socket.Socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.connect((HOST, PORT))
s.sendall(b'Hello, world')  # 不符合
data = s.recv(1024)
s.close()
print('Received', repr(data))
```

#### G.DSP.04 禁止在用户界面、日志中暴露不必要信息【要求】

**【描述】**
如果攻击者获取了系统所涉及的操作系统、中间件、应用程序、实现细节、密钥、个人隐私信息等，则会根据这些信息进行有针对性的漏洞分析或直接窃取有效价值信息
因此，要避免将系统信息暴露出来，具体而言：
- 禁止在未经认证的用户界面明文显示软件信息
- 禁止在用户界面、日志中明文显示或打印会话标识、敏感个人信息等
- 禁止在用户界面、日志中明文或密文显示或打印认证凭据。若因为特殊原因需要显示或记录的，可用固定长度的星号(*)代替

**用户界面认证前禁止显示或打印的信息包括：产品安装和使用的软件和冷热补丁名称和版本号、软件版本号、操作系统及版本号、单板名称、内存地址、内存布局、处理器类型、二进制文件名、设备架构、进程名称、文件结构、服务器物理绝对路径、设备文件结构、函数调用痕迹、主机列表、SQL语句、数据库名/表名、堆栈、SAL指令、会话标识、认证凭据、敏感个人信息数据**

用户界面认证后可以根据业务必须的信息按照最小化原则显示：产品安装和使用的软件和冷热补丁名称和版本号、软件版本号、操作系统及版本号、单板名称、内存地址、内存布局、处理器类型、二进制文件名、设备架构、进程名称、文件结构、服务器物理绝对路径、设备文件结构、函数调用痕迹、主机列表、SQL语句、数据库名/表名、堆栈、SAL指令， **禁止显示或打印会话标识、认证凭据、敏感个人信息数据**

后台日志中可以根据问题定位等业务必须场景，按照最小化原则显示或打印：产品安装和使用的软件和冷热补丁名称和版本号、软件版本号、操作系统及版本号、单板名称、内存地址、内存布局、处理器类型、二进制文件名、设备架构、进程名称、文件结构、服务器物理绝对路径、设备文件结构、函数调用痕迹、主机列表、SQL语句、数据库名/表名、堆栈、SAL指令， **禁止显示或打印会话标识、认证凭据、敏感个人信息数据**

**【正例】**
```python
# Python调用Python，可以使用import和函数调用的方式传递敏感信息
from demo import send_requests

results = send_requests(url, headers={"x-auth-token": "xxx"})
```

Bash调用Python，可以使用标准输入或环境变量的方式传递敏感信息。
注意，使用标准输入方式时，攻击者可以通过读取进程句柄获取对应数据（如linux环境使用`cat /proc/{pid}/fd/0`命令），需要结合用户权限进行访问控制。
```python
#!/bin/bash
python ./get_env.py <<< "xxx"

#!/usr/bin/env python
import sys

if __name__ == '__main__':
    password = sys.stdin.read()
```

使用环境变量方式时，攻击者可以通过读取进程环境变量获取对应数据（如linux环境使用`cat /proc/{pid}/environ`命令），需要结合用户权限进行访问控制。
```python
#!/bin/bash
env password=xxx python ./get_env.py

#!/usr/bin/env python
import os

if __name__ == '__main__':
    if 'password' in os.environ:
        password = os.environ['password']
        del os.environ['password']
```

Python调用Bash，可以使用环境变量的方式传递敏感信息
使用环境变量方式时，攻击者可以通过读取进程环境变量获取对应数据（如linux环境使用`cat /proc/{pid}/environ`命令），需要结合用户权限进行访问控制。
```python
#!/usr/bin/env python
import os

def change_password(password):
    os.putenv("PASSWORD", password)
    execute_command("change_password.sh")
    os.unsetenv("PASSWORD")

#!/bin/bash
password=${PASSWORD}
```

**【反例】**
```python
# 在日志中打印敏感信息
import logging

...
logging.info("Login success, user is:%s, password is:%s", user_name, encrypt(password))
```