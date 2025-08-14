- [1.代码风格](#1代码风格)
  - [1.1 命名](#11-命名)
      - [G.NAM.01 标识符应由不超过64字符的字母、数字和下划线组成【建议】](#gnam01-标识符应由不超过64字符的字母数字和下划线组成建议)
      - [G.NAM.02 包名中的字母应小写，包名以点号分隔层级【建议】](#gnam02-包名中的字母应小写包名以点号分隔层级建议)
      - [G.NAM.03 类、枚举和接口名应采用大驼峰命名【建议】](#gnam03-类枚举和接口名应采用大驼峰命名建议)
      - [G.NAM.04 方法名应采用小驼峰命名【建议】](#gnam04-方法名应采用小驼峰命名建议)
      - [G.NAM.05 常量名采用全大写单词，单词间以下划线分隔【建议】](#gnam05-常量名采用全大写单词单词间以下划线分隔建议)
      - [G.NAM.06 变量采用小驼峰命名【建议】](#gnam06-变量采用小驼峰命名建议)
      - [G.NAM.07 避免使用具有否定含义布尔变量名【建议】](#gnam07-避免使用具有否定含义布尔变量名建议)
      - [G.NAM.08 布尔变量建议以表达是非意义的动词开头【建议】](#gnam08-布尔变量建议以表达是非意义的动词开头建议)
  - [1.2 注释](#12-注释)
      - [G.CMT.01 public或protected修饰的元素应添加Javadoc注释【建议】](#gcmt01-public或protected修饰的元素应添加javadoc注释建议)
      - [G.CMT.02 顶层public类的Javadoc应该包含功能说明和创建日期/版本信息【建议】](#gcmt02-顶层public类的javadoc应该包含功能说明和创建日期版本信息建议)
      - [G.CMT.03 方法的Javadoc中应该包含功能说明，根据实际需要按顺序使用@param、@return、@throws标签对参数、返回值、异常进行注释【建议】](#gcmt03-方法的javadoc中应该包含功能说明根据实际需要按顺序使用paramreturnthrows标签对参数返回值异常进行注释建议)
      - [G.CMT.04 不写空有格式的方法头注释【建议】](#gcmt04-不写空有格式的方法头注释建议)
      - [G.CMT.05 文件头注释应该包含版权许可信息【建议】](#gcmt05-文件头注释应该包含版权许可信息建议)
      - [G.CMT.06 注释与代码之间应该有空行或空格，注释符与注释内容之间应该有空格【建议】](#gcmt06-注释与代码之间应该有空行或空格注释符与注释内容之间应该有空格建议)
      - [G.CMT.07 正式交付给客户的代码不应包含TODO/FIXME注释【建议】](#gcmt07-正式交付给客户的代码不应包含todofixme注释建议)
  - [1.3 格式](#13-格式)
      - [G.FMT.01 源文件编码格式（包括注释）应该是UTF-8【建议】](#gfmt01-源文件编码格式包括注释应该是utf-8建议)
      - [G.FMT.02 一个源文件按顺序包含版权、package、import、顶层类，且用空行分隔【建议】](#gfmt02-一个源文件按顺序包含版权packageimport顶层类且用空行分隔建议)
      - [G.FMT.03 import包应该按照先安卓、华为公司、其他商业组织、其他开源第三方、net/org开源组织、最后java的分类顺序出现，并用一个空行分组【建议】](#gfmt03-import包应该按照先安卓华为公司其他商业组织其他开源第三方netorg开源组织最后java的分类顺序出现并用一个空行分组建议)
      - [G.FMT.04 一个类或接口的声明部分应该按照类变量、静态初始化块、实例变量、实例初始化块、构造器、方法的顺序出现，且用空行分隔【建议】](#gfmt04-一个类或接口的声明部分应该按照类变量静态初始化块实例变量实例初始化块构造器方法的顺序出现且用空行分隔建议)
      - [G.FMT.05 在条件语句和循环块中应该使用大括号【建议】](#gfmt05-在条件语句和循环块中应该使用大括号建议)
      - [G.FMT.06 对于非空块状结构，左大括号应该放在行尾，右大括号应该另起一行【建议】](#gfmt06-对于非空块状结构左大括号应该放在行尾右大括号应该另起一行建议)
      - [G.FMT.07 应该避免空块，必须使用空块时，应采用统一的大括号换行风格【建议】](#gfmt07-应该避免空块必须使用空块时应采用统一的大括号换行风格建议)
      - [G.FMT.08 使用空格进行缩进，每次缩进4个空格【建议】](#gfmt08-使用空格进行缩进每次缩进4个空格建议)
      - [G.FMT.09 每行不超过一个语句【建议】](#gfmt09-每行不超过一个语句建议)
      - [G.FMT.10 行宽不超过120个窄字符【建议】](#gfmt10-行宽不超过120个窄字符建议)
      - [G.FMT.11 建议换行起点在操作符之前【建议】](#gfmt11-建议换行起点在操作符之前建议)
      - [G.FMT.12 减少不必要的空行，保持代码紧凑【建议】](#gfmt12-减少不必要的空行保持代码紧凑建议)
      - [G.FMT.13 用空格突出关键字和重要信息【建议】](#gfmt13-用空格突出关键字和重要信息建议)
      - [G.FMT.14 不应插入多余空格使代码垂直对齐【建议】](#gfmt14-不应插入多余空格使代码垂直对齐建议)
      - [G.FMT.15 枚举常量间用逗号隔开，换行可选【建议】](#gfmt15-枚举常量间用逗号隔开换行可选建议)
      - [G.FMT.16 case语句块结束时如果不加break，需要有注释说明（fall-through）【建议】](#gfmt16-case语句块结束时如果不加break需要有注释说明fall-through建议)
      - [G.FMT.17 应用于类、方法、类属性的每个注解独占一行【建议】](#gfmt17-应用于类方法类属性的每个注解独占一行建议)
      - [G.FMT.18 块注释的缩进级别应与上下文代码相同【建议】](#gfmt18-块注释的缩进级别应与上下文代码相同建议)
      - [G.FMT.19 类和成员修饰符（如果存在）按Java语言规范建议的顺序显示【建议】](#gfmt19-类和成员修饰符如果存在按java语言规范建议的顺序显示建议)
      - [G.FMT.20 数字字面量应该设置合适的后缀，long类型应该使用L作为后缀【建议】](#gfmt20-数字字面量应该设置合适的后缀long类型应该使用l作为后缀建议)
- [2. 编程实践](#2-编程实践)
  - [2.1 声明和初始化](#21-声明和初始化)
      - [G.DCL.01 每行声明一个变量【要求】](#gdcl01-每行声明一个变量要求)
      - [G.DCL.02 局部变量被声明在接近它们首次使用的行【建议】](#gdcl02-局部变量被声明在接近它们首次使用的行建议)
      - [G.DCL.03 禁止C风格的数组声明【要求】](#gdcl03-禁止c风格的数组声明要求)
      - [G.DCL.04 避免枚举常量序号的产生依赖于ordinal()方法【建议】](#gdcl04-避免枚举常量序号的产生依赖于ordinal方法建议)
      - [G.DCL.05 禁止将mutable对象定义为常量【要求】](#gdcl05-禁止将mutable对象定义为常量要求)
      - [G.DCL.06 应该优先使用枚举类型管理用于表示业务状态或类型的常量【建议】](#gdcl06-应该优先使用枚举类型管理用于表示业务状态或类型的常量建议)
  - [2.2 数据类型](#22-数据类型)
      - [G.TYP.01 进行数值运算时，避免整数溢出【建议】](#gtyp01-进行数值运算时避免整数溢出建议)
      - [G.TYP.02 确保除法运算和模运算中的除数不为0【要求】](#gtyp02-确保除法运算和模运算中的除数不为0要求)
      - [G.TYP.03 禁止使用浮点数作为循环计数器【要求】](#gtyp03-禁止使用浮点数作为循环计数器要求)
      - [G.TYP.04 需要精确计算时使用BigDecimal，不要使用float和double【要求】](#gtyp04-需要精确计算时使用bigdecimal不要使用float和double要求)
      - [G.TYP.05 浮点型数据判断相等不要直接使用==，浮点型包装类型不要用equals()或者flt.compareTo(another)==0作相等的比较【要求】](#gtyp05-浮点型数据判断相等不要直接使用浮点型包装类型不要用equals或者fltcomparetoanother0作相等的比较要求)
      - [G.TYP.06 禁止尝试与NaN进行比较运算，相等操作使用Double或Float的isNaN()方法【要求】](#gtyp06-禁止尝试与nan进行比较运算相等操作使用double或float的isnan方法要求)
      - [G.TYP.07 不要在代码中硬编码用于表示换行、文件路径分隔的字符--不要在代码中硬编码用于表示换行字符【建议】](#gtyp07-不要在代码中硬编码用于表示换行文件路径分隔的字符--不要在代码中硬编码用于表示换行字符建议)
      - [G.TYP.08 字符串大小写转换、数字格式化为西方数字时，必须加上Locale.ROOT或Locale.ENGLISH【要求】](#gtyp08-字符串大小写转换数字格式化为西方数字时必须加上localeroot或localeenglish要求)
      - [G.TYP.09 字符与字节的互相转换操作，要指明正确的编码方式【要求】](#gtyp09-字符与字节的互相转换操作要指明正确的编码方式要求)
      - [G.TYP.10 内存中的敏感信息使用完毕后立即清0【建议】](#gtyp10-内存中的敏感信息使用完毕后立即清0建议)
      - [G.TYP.11 基本类型优于包装类型，注意合理使用包装类型【建议】](#gtyp11-基本类型优于包装类型注意合理使用包装类型建议)
      - [G.TYP.12 明确地进行类型转换，避免依赖隐式类型转换【建议】](#gtyp12-明确地进行类型转换避免依赖隐式类型转换建议)
      - [G.TYP.13 在引用类型向下转换前用instanceof进行判断【建议】](#gtyp13-在引用类型向下转换前用instanceof进行判断建议)
  - [2.3 表达式](#23-表达式)
      - [G.EXP.01 不要在单个表达式中对相同的变量赋值超过一次【要求】](#gexp01-不要在单个表达式中对相同的变量赋值超过一次要求)
      - [G.EXP.02 用括号明确表达式的操作顺序，避免过分依赖默认优先级【建议】](#gexp02-用括号明确表达式的操作顺序避免过分依赖默认优先级建议)
      - [G.EXP.03 条件表达式?:的第2和第3个操作数应使用相同的类型【建议】](#gexp03-条件表达式的第2和第3个操作数应使用相同的类型建议)
      - [G.EXP.04 表达式的比较，应该遵循左侧倾向于变化、右侧倾向于不变的原则--表达式比较左变右不变【建议】](#gexp04-表达式的比较应该遵循左侧倾向于变化右侧倾向于不变的原则--表达式比较左变右不变建议)
      - [G.EXP.05 禁止直接使用可能为null的对象，防止出现空指针引用【要求】](#gexp05-禁止直接使用可能为null的对象防止出现空指针引用要求)
      - [G.EXP.06 代码中不应使用断言（assert）【建议】](#gexp06-代码中不应使用断言assert建议)
  - [2.4 控制语句](#24-控制语句)
      - [G.CTL.01 不要在控制性条件表达式中执行赋值操作或执行复杂的条件判断【要求】](#gctl01-不要在控制性条件表达式中执行赋值操作或执行复杂的条件判断要求)
      - [G.CTL.02 含else if分支的条件判断应在最后加一个else分支【建议】](#gctl02-含else-if分支的条件判断应在最后加一个else分支建议)
      - [G.CTL.03 switch语句要有default分支【要求】](#gctl03-switch语句要有default分支要求)
      - [G.CTL.04 循环必须保证可正确终止【要求】](#gctl04-循环必须保证可正确终止要求)
      - [G.CTL.05 避免在循环体中修改循环控制变量【建议】](#gctl05-避免在循环体中修改循环控制变量建议)
      - [G.CTL.06 禁止switch语句中直接嵌套switch【要求】](#gctl06-禁止switch语句中直接嵌套switch要求)
      - [G.CTL.07 避免在条件/循环控制语句中包含过多的条件【建议】](#gctl07-避免在条件循环控制语句中包含过多的条件建议)
  - [2.5 方法](#25-方法)
      - [G.MET.01 方法要简短--方法的参数不应超过5个【建议】](#gmet01-方法要简短--方法的参数不应超过5个建议)
      - [G.MET.02 不要使用已标注为@Deprecated的方法、类、类的属性等【要求】](#gmet02-不要使用已标注为deprecated的方法类类的属性等要求)
      - [G.MET.03 不应把方法的参数当做临时变量【建议】](#gmet03-不应把方法的参数当做临时变量建议)
      - [G.MET.04 谨慎使用可变数量参数【建议】](#gmet04-谨慎使用可变数量参数建议)
      - [G.MET.05 对于返回数组或者容器的方法，应返回长度为0的数组或者容器，代替返回null【建议】](#gmet05-对于返回数组或者容器的方法应返回长度为0的数组或者容器代替返回null建议)
      - [G.MET.06 使用Optional代替null作为返回值或者可能的缺失值；禁止对Optional对象赋值为null【建议】](#gmet06-使用optional代替null作为返回值或者可能的缺失值禁止对optional对象赋值为null建议)
      - [G.MET.07 不要忽略方法的返回值【建议】](#gmet07-不要忽略方法的返回值建议)
  - [2.6 类与接口](#26-类与接口)
      - [G.OBJ.01 应避免定义public且非final的类属性【建议】](#gobj01-应避免定义public且非final的类属性建议)
      - [G.OBJ.02 不要在父类的构造方法中调用可能被子类覆写的方法【要求】](#gobj02-不要在父类的构造方法中调用可能被子类覆写的方法要求)
      - [G.OBJ.03 构造方法如果有多个，尽量重用【建议】](#gobj03-构造方法如果有多个尽量重用建议)
      - [G.OBJ.04 避免在无关的变量或无关的概念之间重用名字，避免隐藏（hide）、遮蔽（shadow）和遮掩（obscure）【要求】](#gobj04-避免在无关的变量或无关的概念之间重用名字避免隐藏hide遮蔽shadow和遮掩obscure要求)
      - [G.OBJ.05 避免基本类型与其包装类型的同名重载方法【建议】](#gobj05-避免基本类型与其包装类型的同名重载方法建议)
      - [G.OBJ.06 覆写equals方法时，要同时覆写hashCode方法【要求】](#gobj06-覆写equals方法时要同时覆写hashcode方法要求)
      - [G.OBJ.07 子类覆写父类方法或实现接口时必须加上@Override注解【要求】](#gobj07-子类覆写父类方法或实现接口时必须加上override注解要求)
      - [G.OBJ.08 正确实现单例模式【建议】](#gobj08-正确实现单例模式建议)
      - [G.OBJ.09 使用类名调用静态方法，而不要使用实例或表达式来调用【要求】](#gobj09-使用类名调用静态方法而不要使用实例或表达式来调用要求)
      - [G.OBJ.10 接口定义中去掉多余的修饰词【建议】](#gobj10-接口定义中去掉多余的修饰词建议)
      - [G.OBJ.11 可以在接口中加上静态方法表示相关的工厂或助手方法【建议】](#gobj11-可以在接口中加上静态方法表示相关的工厂或助手方法建议)
  - [2.7 异常处理](#27-异常处理)
      - [G.ERR.01 不要通过一个空的catch块忽略异常【要求】](#gerr01-不要通过一个空的catch块忽略异常要求)
      - [G.ERR.02 不要直接捕获异常的基类Throwable、Exception、RuntimeException【建议】](#gerr02-不要直接捕获异常的基类throwableexceptionruntimeexception建议)
      - [G.ERR.03 不要直接捕获可通过预检查进行处理的RuntimeException，如NullPointerException、IndexOutOfBoundsException等【建议】](#gerr03-不要直接捕获可通过预检查进行处理的runtimeexception如nullpointerexceptionindexoutofboundsexception等建议)
      - [G.ERR.04 防止通过异常泄露敏感信息【要求】](#gerr04-防止通过异常泄露敏感信息要求)
      - [G.ERR.05 方法抛出的异常，应该与本身的抽象层次相对应【要求】](#gerr05-方法抛出的异常应该与本身的抽象层次相对应要求)
      - [G.ERR.06 在catch块中抛出新异常时，避免丢失原始异常信息【建议】](#gerr06-在catch块中抛出新异常时避免丢失原始异常信息建议)
      - [G.ERR.07 一个方法不应抛出超过5个异常，并在Javadoc的@throws标签中记录每个抛出的异常及其条件【建议】](#gerr07-一个方法不应抛出超过5个异常并在javadoc的throws标签中记录每个抛出的异常及其条件建议)
      - [G.ERR.08 不要使用return、break、continue或抛出异常使finally块非正常结束【要求】](#gerr08-不要使用returnbreakcontinue或抛出异常使finally块非正常结束要求)
      - [G.ERR.09 不要调用System.exit()终止JVM【建议】](#gerr09-不要调用systemexit终止jvm建议)
      - [G.ERR.10 尽量消除非受检的异常，不应该在整个类上使用SuppressWarning【建议】](#gerr10-尽量消除非受检的异常不应该在整个类上使用suppresswarning建议)
      - [G.ERR.11 对于GeneralSecurityException及其子类异常应记录日志【建议】](#gerr11-对于generalsecurityexception及其子类异常应记录日志建议)
  - [2.8 并发与多线程](#28-并发与多线程)
      - [P.03 使用相同的顺序请求和释放锁来避免死锁【要求】](#p03-使用相同的顺序请求和释放锁来避免死锁要求)
      - [G.CON.01 对共享变量做同步访问控制时需避开同步陷阱【要求】](#gcon01-对共享变量做同步访问控制时需避开同步陷阱要求)
      - [G.CON.02 在异常条件下，保证释放已持有的锁【要求】](#gcon02-在异常条件下保证释放已持有的锁要求)
      - [G.CON.03 避免在持有锁时执行耗时或阻塞性的操作【建议】](#gcon03-避免在持有锁时执行耗时或阻塞性的操作建议)
      - [G.CON.04 避免使用不正确形式的双重检查锁【要求】](#gcon04-避免使用不正确形式的双重检查锁要求)
      - [G.CON.05 禁止使用非线程安全的方法来覆写线程安全的方法【要求】](#gcon05-禁止使用非线程安全的方法来覆写线程安全的方法要求)
      - [G.CON.06 使用新并发工具代替wait()和notify()【要求】](#gcon06-使用新并发工具代替wait和notify要求)
      - [G.CON.07 创建新线程时必须指定线程名【要求】](#gcon07-创建新线程时必须指定线程名要求)
      - [G.CON.08 使用Thread对象的setUncaughtExceptionHandler方法注册未捕获异常处理者【要求】](#gcon08-使用thread对象的setuncaughtexceptionhandler方法注册未捕获异常处理者要求)
      - [G.CON.09 不要依赖线程调度器、线程优先级和yield()方法【要求】](#gcon09-不要依赖线程调度器线程优先级和yield方法要求)
      - [G.CON.10 线程中断由业务代码来协作完成，慎用Thread.interrupt方法【建议】](#gcon10-线程中断由业务代码来协作完成慎用threadinterrupt方法建议)
      - [G.CON.11 禁止使用Thread.stop()来终止线程【要求】](#gcon11-禁止使用threadstop来终止线程要求)
      - [G.CON.12 避免不加控制地创建新线程，应该使用线程池来管控资源【建议】](#gcon12-避免不加控制地创建新线程应该使用线程池来管控资源建议)
      - [G.CON.13 线程池中的任务结束后必须清理其自定义的ThreadLocal变量【要求】](#gcon13-线程池中的任务结束后必须清理其自定义的threadlocal变量要求)
  - [2.9 泛型和集合](#29-泛型和集合)
      - [G.COL.01 方法的设计可以优先考虑泛型【建议】](#gcol01-方法的设计可以优先考虑泛型建议)
      - [G.COL.02 优先使用泛型集合，而不是数组【建议】](#gcol02-优先使用泛型集合而不是数组建议)
      - [G.COL.03 声明一个泛型类通过限定符限制可用的泛型类型【建议】](#gcol03-声明一个泛型类通过限定符限制可用的泛型类型建议)
      - [G.COL.04 不要在foreach循环中通过remove()/add()方法更改集合【要求】](#gcol04-不要在foreach循环中通过removeadd方法更改集合要求)
  - [2.10 输入和输出](#210-输入和输出)
      - [G.FIO.01 使用外部数据构造的文件路径前必须进行校验，校验前必须对文件路径进行规范化处理【要求】](#gfio01-使用外部数据构造的文件路径前必须进行校验校验前必须对文件路径进行规范化处理要求)
      - [G.FIO.02 从ZipInputStream中解压文件必须进行安全检查【要求】](#gfio02-从zipinputstream中解压文件必须进行安全检查要求)
      - [G.FIO.03 对于从流中读取一个字符或字节的方法，使用int类型的返回值【要求】](#gfio03-对于从流中读取一个字符或字节的方法使用int类型的返回值要求)
      - [G.FIO.04 防止外部进程阻塞在输入输出流上【要求】](#gfio04-防止外部进程阻塞在输入输出流上要求)
      - [G.FIO.05 临时文件使用完毕必须及时删除【要求】](#gfio05-临时文件使用完毕必须及时删除要求)
  - [2.11 序列化](#211-序列化)
      - [G.SER.01 尽量避免实现Serializable接口【建议】](#gser01-尽量避免实现serializable接口建议)
      - [G.SER.02 实现Serializable接口的可序列化类应该显式声明serialVersionUID【建议】](#gser02-实现serializable接口的可序列化类应该显式声明serialversionuid建议)
      - [G.SER.03 序列化对象中的HashMap，HashSet或HashTable等集合禁止包含对象自身的引用【要求】](#gser03-序列化对象中的hashmaphashset或hashtable等集合禁止包含对象自身的引用要求)
      - [G.SER.04 禁止直接序列化指向系统资源的信息【要求】](#gser04-禁止直接序列化指向系统资源的信息要求)
      - [G.SER.05 禁止序列化非静态的内部类【要求】](#gser05-禁止序列化非静态的内部类要求)
      - [G.SER.06 序列化操作要防止敏感信息泄露【要求】](#gser06-序列化操作要防止敏感信息泄露要求)
      - [G.SER.07 防止反序列化被利用来绕过构造方法中的安全操作【要求】](#gser07-防止反序列化被利用来绕过构造方法中的安全操作要求)
      - [G.SER.08 禁止直接将外部数据进行反序列化【要求】](#gser08-禁止直接将外部数据进行反序列化要求)
  - [2.12 外部数据校验](#212-外部数据校验)
      - [P.05 外部数据使用前必须进行合法性校验【要求】](#p05-外部数据使用前必须进行合法性校验要求)
      - [G.EDV.01 禁止直接使用外部数据来拼接SQL语句【要求】](#gedv01-禁止直接使用外部数据来拼接sql语句要求)
      - [G.EDV.02 禁止直接使用外部数据构造格式化字符串【要求】](#gedv02-禁止直接使用外部数据构造格式化字符串要求)
      - [G.EDV.03 禁止直接向Runtime.exec()方法或java.lang.ProcessBuilder类传递外部数据【要求】](#gedv03-禁止直接向runtimeexec方法或javalangprocessbuilder类传递外部数据要求)
      - [G.EDV.04 禁止直接使用外部数据来拼接XML【要求】](#gedv04-禁止直接使用外部数据来拼接xml要求)
      - [G.EDV.05 防止解析来自外部的XML导致的外部实体（XML External Entity）攻击【要求】](#gedv05-防止解析来自外部的xml导致的外部实体xml-external-entity攻击要求)
      - [G.EDV.06 防止解析来自外部的XML导致的内部实体扩展（XML Entity Expansion）攻击【要求】](#gedv06-防止解析来自外部的xml导致的内部实体扩展xml-entity-expansion攻击要求)
      - [G.EDV.07 禁止使用不安全的XSLT转换XML文件【要求】](#gedv07-禁止使用不安全的xslt转换xml文件要求)
      - [G.EDV.08 正则表达式要尽量简单，防止ReDos攻击【要求】](#gedv08-正则表达式要尽量简单防止redos攻击要求)
      - [G.EDV.09 禁止直接使用外部数据作为反射操作中的类名/方法名【要求】](#gedv09-禁止直接使用外部数据作为反射操作中的类名方法名要求)
  - [2.13 日志](#213-日志)
      - [G.LOG.01 记录日志应该使用Facade模式的日志框架【要求】](#glog01-记录日志应该使用facade模式的日志框架要求)
      - [G.LOG.02 日志工具Logger类的实例必须声明为private static final或者private final【要求】](#glog02-日志工具logger类的实例必须声明为private-static-final或者private-final要求)
      - [G.LOG.03 日志必须分等级【要求】](#glog03-日志必须分等级要求)
      - [G.LOG.04 非仅限于中文区销售产品禁止用中文打印日志【要求】](#glog04-非仅限于中文区销售产品禁止用中文打印日志要求)
      - [G.LOG.05 禁止直接使用外部数据记录日志【要求】](#glog05-禁止直接使用外部数据记录日志要求)
  - [2.14 性能和资源管理](#214-性能和资源管理)
      - [G.PRM.01 将集合转为数组时使用Collection.toArray(T\[\])方法；Java 11后使用Collection.toArray(IntFunction\<T\[\]\>)【要求】](#gprm01-将集合转为数组时使用collectiontoarrayt方法java-11后使用collectiontoarrayintfunctiont要求)
      - [G.PRM.02 使用System.arraycopy()或Arrays.copyOf()进行数组复制【建议】](#gprm02-使用systemarraycopy或arrayscopyof进行数组复制建议)
      - [G.PRM.03 初始化集合时，如果可预估元素数量，应该指定初始化大小【建议】](#gprm03-初始化集合时如果可预估元素数量应该指定初始化大小建议)
      - [G.PRM.04 不要对正则表达式进行频繁重复预编译【要求】](#gprm04-不要对正则表达式进行频繁重复预编译要求)
      - [G.PRM.05 禁止创建不必要的对象【要求】](#gprm05-禁止创建不必要的对象要求)
      - [G.PRM.06 将对象存入HashSet，或作为Key存入HashMap(或HashTable)后，必须确保该对象的HashCode值不变【要求】](#gprm06-将对象存入hashset或作为key存入hashmap或hashtable后必须确保该对象的hashcode值不变要求)
      - [G.PRM.07 进行IO类操作时，必须在try-with-resource或finally里关闭资源【要求】](#gprm07-进行io类操作时必须在try-with-resource或finally里关闭资源要求)
      - [G.PRM.08 禁止使用主动GC（除非在密码、RMI等方面），尤其是在频繁/周期性的逻辑中【要求】](#gprm08-禁止使用主动gc除非在密码rmi等方面尤其是在频繁周期性的逻辑中要求)
      - [G.PRM.09 禁止使用Finalizer机制【要求】](#gprm09-禁止使用finalizer机制要求)
      - [G.PRM.10 不要创建临时变量作为return语句的返回值【建议】](#gprm10-不要创建临时变量作为return语句的返回值建议)
  - [2.15 平台安全](#215-平台安全)
      - [G.SEC.01 进行安全检查的方法必须声明为private或final【要求】](#gsec01-进行安全检查的方法必须声明为private或final要求)
      - [G.SEC.02 自定义类加载器覆写getPermission()时，必须先调用父类的getPermission()方法【要求】](#gsec02-自定义类加载器覆写getpermission时必须先调用父类的getpermission方法要求)
      - [G.SEC.03 加载外部JAR文件时,不要依赖URLClassLoader和java.util.jar提供的默认自动签名检查机制【要求】](#gsec03-加载外部jar文件时不要依赖urlclassloader和javautiljar提供的默认自动签名检查机制要求)
      - [G.SEC.04 使用安全管理器来保护敏感操作【建议】](#gsec04-使用安全管理器来保护敏感操作建议)
  - [2.16 其他](#216-其他)
      - [G.OTH.01 安全场景下必须使用密码学意义上的安全随机数【要求】](#goth01-安全场景下必须使用密码学意义上的安全随机数要求)
      - [G.OTH.02 必须使用SSLSocket代替Socket来进行安全数据交互【要求】](#goth02-必须使用sslsocket代替socket来进行安全数据交互要求)
      - [G.OTH.03 不用的代码段包括import，直接删除，不要注释掉【要求】](#goth03-不用的代码段包括import直接删除不要注释掉要求)
      - [G.OTH.04 禁止代码中包含公网地址【要求】](#goth04-禁止代码中包含公网地址要求)
      - [G.OTH.05 删除无效或永不执行的代码【要求】](#goth05-删除无效或永不执行的代码要求)
      - [G.OTH.06 禁止在用户界面、日志中暴露不必要信息【要求】](#goth06-禁止在用户界面日志中暴露不必要信息要求)
      - [G.OTH.07 安全随机数生成器尽量复用【建议】](#goth07-安全随机数生成器尽量复用建议)

# 1.代码风格

代码风格一般包含标识符的命名风格、排版与格式风格，注释风格。一致的编码习惯与风格，会使代码更容易阅读、理解更容易维护。统一的代码风格也是一致性原则最直观的体现。

## 1.1 命名

#### G.NAM.01 标识符应由不超过64字符的字母、数字和下划线组成【建议】

**【描述】**
变量名应该只以字母数字下划线组成，且长度在[2,maxLength]之间。maxLength的默认值是64，可动态配置（上限是64）。

**【修改建议】**
删除变量名称中的不合规字符或缩短变量名长度。

**【正例】**
场景1：标识符里包含了除字母、数字和下划线之外的其他字符
- 修复示例：
  ```java
  int num; // 【GOOD】去掉标识符里面的$符号
  ```

**【反例】**
场景1：标识符里包含了除字母、数字和下划线之外的其他字符
- 错误示例：
  ```java
  int num$;  // 【POTENTIAL FLAW】标识符里面含有$符号
  ```

#### G.NAM.02 包名中的字母应小写，包名以点号分隔层级【建议】

**【描述】**
包名仅能使用小写字母、数字、下划线，下划线只能在一些特殊情况中使用。比如包名以数字开头或是java中的保留关键字时，如`int__.example`, `com.example.__123name`。一层包路径可以是多个单词（不带下划线）的简单连接。
所有的源文件均要设置一个具体的package。

**【正例】**
  ```java
  package com.opengauss.jdbc;
  package xxx.yyy.v2;
  ```

#### G.NAM.03 类、枚举和接口名应采用大驼峰命名【建议】

**【描述】**
类名、接口名通常是名词或名词短语，接口名还可以是形容词或形容词短语，都应采用**大驼峰命名**，例如：ArrayList（类）、Collection（接口）、Comparable（接口）等。

**【修改建议】**
类、枚举和接口名应采用大驼峰命名。

**【正例】**
场景1：类名没有使用大驼峰命名
- 修复示例：
  ```java
  class MarcoPolo { // 【GOOD】类名要采用大驼峰命名
      ...  
  }
  ```
场景2：枚举类名没有使用大驼峰命名
- 修复示例：
  ```java
  enum ComparisonResult { // 【GOOD】枚举类名要采用大驼峰命名
      ...  
  }
  ```
场景3：接口名没有使用大驼峰命名
- 修复示例：
  ```java
  interface ParameterSetNameInterface { // 【GOOD】接口名要采用大驼峰命名
      ...  
  }
  ```

**【反例】**
场景1：类名没有使用大驼峰命名
- 错误示例：
  ```java
  class marcoPolo { // 【POTENTIAL FLAW】类名采用了小驼峰命名
      ...  
  }
  ```
场景2：枚举类名没有使用大驼峰命名
- 错误示例：
  ```java
  enum  comparisonResult { // 【POTENTIAL FLAW】枚举类名采用了小驼峰命名
      ...  
  }
  ```
场景3：接口名没有使用大驼峰命名
- 错误示例：
  ```java
  interface parameterSetNameInterface { // 【POTENTIAL FLAW】接口名采用了小驼峰命名
      ...  
  }
  ```

#### G.NAM.04 方法名应采用小驼峰命名【建议】

**【描述】**
方法名通常是动词或动词短语，采用**小驼峰命名**。

**【修改建议】**
方法名采用小驼峰命名。

**【正例】**
场景1
- 修复示例
  ```java
  public boolean isFinished() // 【GOOD】Finished()--> isFinished()

  public void draw() // 【GOOD】DRAW()-->draw()

  public void addKeyListener(Listener) // 【GOOD】KeyListener(Listener)-->addKeyListener(Listener)
  ```

**【反例】**
场景1
- 错误示例
  ```java
  public boolean Finished() // 【POTENTIAL FLAW】大驼峰命名。

  public void DRAW() // 【POTENTIAL FLAW】

  public void KeyListener(Listener) // 【POTENTIAL FLAW】

  ```

#### G.NAM.05 常量名采用全大写单词，单词间以下划线分隔【建议】

**【描述】**
java规范中的常量是指不可被修改静态的field和枚举常量。“不可被修改”需要同时满足以下两个条件：

- field的值/对象不可被修改为其他的值/对象；
- field为对象类型时，对象在初始化完成后其属性不能被修改。

常量定义的一般格式为：`[访问修饰符] static final 类型 常量名 = 常量值;`。

常量命名应该由**全大写单词与下划线**组成，单词间用下划线分隔，如CONSTANT_CASE。常量命名要尽量表达完整的语义。

不要使用魔鬼数字（难以理解的数字或字符串)，用有意义的常量代替。SQL或日志的字符串，不应视为魔鬼数字，不需定义为字符串常量；

**【修改建议】**
对于常量，应该采用全大写单词与下划线进行命名。

对于魔鬼数字，可采用如下方法进行优化：
- 如果有现成的API，不要定义数字，比如判断集合内元素是否为空时，不应该使用size() == 0，应使用isEmpty()方法；比如时间的比较判断，用java.time中的API；
- 有命名模式的可以用枚举类型。

**【正例】**
场景1
- 修复示例
  ```java
  static final int MAX_USER_NUM = 200; // 【GOOD】MAXUSERNUM-->MAX_USER_NUM  ，并用final修饰。

  static final String APPLICATION_NAME = "Launcher"; // 【GOOD】sL-->APPLICATION_NAME ，并用final修饰。

  static final int MAX_FILE_NUM = 5; // 【GOOD】
  ```

**【反例】**
场景1
- 错误示例
  ```java
  static final int MAXUSERNUM = 200; // 【POTENTIAL FLAW】单词间应该以下划线分隔

  static final String ApplicationName = "Launcher"; // 【POTENTIAL FLAW】常量名应该采用全大写单词，单词间以下划线分隔

  static final int NUM_FIVE = 5; // 【POTENTIAL FLAW】

  static final int NUM_5 = 5; // 【POTENTIAL FLAW】
  ```

#### G.NAM.06 变量采用小驼峰命名【建议】

**【描述】**
变量的名字通常是名词或名词短语，应采用**小驼峰命名**。

即使局部变量是final或不可改变（immutable）的，也不应该把它视为常量，应采用小驼峰命名。

**【修改建议】**
变量名采用小驼峰命名。

**【正例】**
场景1：成员变量命名
- 修复示例
  ```java
  String customerName; // 【GOOD】customername-->customerName小驼峰命名
  ```
场景2：方法中final修饰的临时变量命名
- 修复示例
  ```java
  void doSomething() {
      final String port = "9090";
      ...
  }
  ```

**【反例】**
场景1：成员变量命名
- 错误示例
  ```java
  String customername; // 【POTENTIAL FLAW】变量未使用小驼峰命名
  ```
场景2：方法中final修饰的临时变量命名
- 错误示例
  ```java
  void doSomething() {
      final String PORT = "9090";
      ...
  }
  ```

#### G.NAM.07 避免使用具有否定含义布尔变量名【建议】

**【描述】**
布尔型变量使用否定含义的变量名，会增加代码理解的难度，尤其是再对该变量进行逻辑非运算，如`!isNotError`。

**【修改建议】**
修改变量名，去除否定含义的单词。

**【正例】**
场景1：boolean型变量名中不能含有no或者not
- 修复示例：
  ```java
  boolean isError; // 【GOOD】去掉标识符里面的no
  ```

**【反例】**
场景1：boolean型变量名中不能含有no或者not
- 错误示例：
  ```java
  boolean isNoError; // 【POTENTIAL FLAW】标识符里含有no
  ```

#### G.NAM.08 布尔变量建议以表达是非意义的动词开头【建议】

**【描述】**
布尔变量建议以表达是非意义的动词开头，如`is`、`has`、`can`、`should`等。

**【正例】**
  ```java
  class Sample {
    private boolean hasLicense;
    ...
    public void doSomething() {
        boolean canDelete;
        boolean shouldAbort;
        ...
    }
  }
  ```

## 1.2 注释

尽量通过清晰的软件架构、良好的标识符命名来提高代码的可读性；在需要的时候，才辅以注释说明。
对晦涩难懂的代码、命名，应该进行重构而不是添加注释
注释要从读者的角度出发，按需注释，内容要简洁明了，无歧义，信息全面且不冗余，不要简单地复制接口或方法的名字
修改代码的同时也要保证其注释的一致性
使用通顺的英文进行注释

#### G.CMT.01 public或protected修饰的元素应添加Javadoc注释【建议】

**【描述】**
最低限度要为每个public或protected修饰的类、接口、枚举、类方法和类属性添加注释，这些注释的格式应该采用Javadoc注释格式（即使用`/** */`进行注释），除此之外按需添加Javadoc注释。实现接口方法时，其Javadoc允许使用{@inheritDoc}。

**【修改建议】**
为public或protected修饰的元素应添加Javadoc注释。

**【正例】**
场景1：
- 修复示例：

```java
// 【GOOD】public或protected修饰的元素应添加Javadoc注释
/**
 * doSomething方法的功能说明
 *
 * @param data xxx（data的具体含义）
 * @return List  返回结果集合，集合不会为null
 * @throws IOException 当出现xx时，会抛出IOException 
 */
public static List<String> doSomething(int data) throws IOException {
    ...
}
```

**【反例】**
场景1：
- 错误示例：

```java
// 【POTENTIAL FLAW】未添加注释
public static List<String> doSomething(int data) throws IOException {
    ...
}
 ```

#### G.CMT.02 顶层public类的Javadoc应该包含功能说明和创建日期/版本信息【建议】

**【描述】**
顶层public类的Javadoc中应该有功能说明、`@since`信息。日期格式为Java 8 time包中的`ISO_DATE`，例如“2011-12-03”或者“2011-12-03+01:00”。

编写文件头或顶层类头注释应注意：

- 禁止空有格式，无内容。
- 业界Java源码中一般没有History信息，History在配置库里面可以查询，不建议在Java源码的注释中包含History。
- 顶层public类头中创建日期的`@since`标签中的年份应该与版权中的起始年份相同。

**【修改建议】**
在Javadoc中添加功能说明、添加@since注解，并在后面添加时间，例如：@since 2023-08-29

**【正例】**
场景1：
- 修复示例：

```java
// 【GOOD】添加了顶层class的注释
/**
 * TopClassComment的功能说明
 *
 * @since 2020/5/26
 */
 public enum TopClassComment {
     ...
 }
```

**【反例】**
场景1：
- 错误示例：注释中无功能说明、`@since`信息

  ```java
  // 【POTENTIAL FLAW】注释中无功能说明、`@since`信息
  public enum TopClassComment {
      ...
  }
  ```

#### G.CMT.03 方法的Javadoc中应该包含功能说明，根据实际需要按顺序使用@param、@return、@throws标签对参数、返回值、异常进行注释【建议】

**【描述】**
书写方法的Javadoc时，推荐用Java 8新增的@implSpec，@apiNote和@implNote对注释内容进行分类描述（不强制要求对存量代码进行修改）。各标签的排列顺序如下：

* 功能描述，说明API的原理、意图、契约（前置与后置条件）等。功能描述与后面的各种标签之间需要空1行。
* @implSpec：特定于API实现的规格说明，让实现者决定是否覆盖。
* @apiNote：说明API的注意事项，包括是否允许null、是否线程安全、算法复杂度、输入输出范围、非受检异常等。
* @implNote：特定于API实现的备注，让实现者参考。
* @param：注释方法的参数。
* @return：注释方法的返回值。
* @throws：注释方法抛出的所有类型的异常，包括受检异常和运行时异常。将运行时异常文档化，可有效描述方法被成功执行的前提条件。
* @Deprecated：如果方法被废弃，添加该标签。

上述标签中，除了@Deprecated，不允许空的描述出现。某标签中的内容需多行显示时，新行内容应从@位置缩进4个空格来对齐。

@implSpec|@apiNote|@implNote与@param|@return|@throws这两组标签之间需要空1行。

**【修改建议】**
增加功能说明和相应标签。

**【正例】**
```java
/**
 * doSomething的功能说明
 *
 * @param str xxx
 * @return String xxx
 * @throws IOException xxx
 */
public String doSomething(String str) throws IOException {
    // doSomeThing function body
}

 /**
 * doSomething的功能说明
 *
 * @implSpec xxx
 * @apiNote xxx
 * @implNote xxx
 *
 * @param str xxx
 * @return String xxx
 * @throws IOException xxx
 */
public String doSomething(String str) throws IOException {
    // doSomeThing function body
}
```

**【反例】**
```java
protected abstract class Sample {
/**
 * doSomething的功能说明
 * @return String xxx
 */
public String doSomething(String str) throws IOException {
    // doSomeThing function body
}
```

#### G.CMT.04 不写空有格式的方法头注释【建议】

**【描述】**
对于不需要添加注释的方法无需添加空有格式的注释，这样代码更整洁。

**【修改建议】**
注释中对方法的描述信息不能为空，且应该使用@param、@return、@throws注解分别对方法的参数、返回值、抛出的异常信息做描述。

对于不需要添加注释的方法，将空有格式的javadoc注释删除。

**【正例】**
场景1：注释不够完整
- 修复示例：

```java
// 【符合】注释信息完整

    /**
     * doSomething describe message
     *
     * @param str xxxx
     * @return List<String>  xxxx
     * @throws IOException xxxxx
     */
    private List<String> doSomething(String str) throws IOException {
        ...
    }
```

**【反例】**
场景1：注释不够完整
- 错误示例：

  ```java
  // 【不符合】注释不够完整  
  /**
   *
   * @param str
   * @return
   * @throws IOException
   */
  public List<String> doSomething(String str) throws IOException {
      ...
  }
  ```

#### G.CMT.05 文件头注释应该包含版权许可信息【建议】

**【描述】**
文件头注释应该放在package和import之前，应该包含版权许可信息，如果需要在文件头注释中增加其他内容，可以在后面以相同格式补充。版权许可不应该使用Javadoc样式或单行样式的注释，应该从文件顶头开始。如果包含“关键资产说明”类注释，则应紧随其后。

版权许可内容及格式必须如下：

中文版：

```java
/* * 版权所有 (c) 华为技术有限公司 2012-2020 */
```

英文版：

```java
/* * Copyright (c) Huawei Technologies Co., Ltd. 2012-2020. All rights reserved. */
```

关于版本说明，应注意：

- 2012-2020 根据实际需要可以修改。
  2012 是文件首次创建年份，而 2020 是最后文件修改年份。二者可以一样，如 "2020-2020"。
  对文件有重大修改时，必须更新后面年份，如特性扩展，重大重构等。
- 版权说明可以使用华为子公司。
  如：版权所有 (c) 海思半导体 2012-2020
  或英文：Copyright (c) Hisilicon Technologies Co., Ltd. 2012-2020. All rights reserved.

**【修改建议】**
为.java文件添加文件头注释，文件头注释中添加版权许可信息，版权许可信息中的时间信息要与实际情况保持一致。

**【正例】**
场景1：无文件头注释
- 修复示例：

  ```java
  /*
   * Copyright (c) Huawei Technologies Co., Ltd. 2022-2022. All rights reserved.
   */

  package com.xxx;

  public class FileHeaderComment {
      public void method() {
      }
  }
  ```

**【反例】**
场景1：无文件头注释
- 错误示例：

  ```java
  // 【不符合】无文件头注释
  package com.xxx;

  public class FileHeaderComment {
      public void method() {
      }
  }
  ```

#### G.CMT.06 注释与代码之间应该有空行或空格，注释符与注释内容之间应该有空格【建议】

**【描述】**
注释与代码之间、注释符与注释信息之间应该合理通过空行、空格进行分隔，这样可保持代码格式更加清晰。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：在方法内部（语句级），注释与上面的代码之间未加空行。对于本范围内的最开始位置（即大括号中的第一行）的注释，注释前不需要空行。
- 修复示例：在方法内部（语句级），注释与上面的代码之间可以考虑加一个空行，以便更加清晰。对于本范围内的最开始位置的注释，注释前不需要空行。

  ```java
  public interface Example {
      /**
       * 成员变量注释 
       */      
      String SOME_FIELD = ...;

      /**
       * 成员变量注释
       */
      String OTHER_FIELD = ...;

      default int bar() throws ProblemException {
          // 变量注释          
          var aVar = ...;

          // 方法注释
          doSomething();
      }
  }
  ```
场景2：代码右边的注释，与代码之间，至少留1空格
- 修复示例：代码右边的注释，与代码之间，至少留1空格。

  ```java
  int foo = 100; // 变量注释
  int bar = 200; // 变量注释
  ```

**【反例】**
场景1：在方法内部（语句级），注释与上面的代码之间未加空行。对于本范围内的最开始位置（即大括号中的第一行）的注释，注释前不需要空行。
- 错误示例：

  ```java
  // 【不符合】在方法内部（语句级），注释与上面的代码之间可以应加一个空行，以便更加清晰
  public interface Example {
      /**
       * 成员变量注释 
       */
      String SOME_FIELD = ...;
      /**
       * 成员变量注释
       */
      String OTHER_FIELD = ...;
      default int bar() throws ProblemException {
          // 变量注释 
          var aVar = ...;
          // 方法注释
          doSomething();
      }
  }
  ```
场景2：代码右边的注释，与代码之间，至少留1空格
- 错误示例：

  ```java
  int foo = 100;//变量注释
  int bar = 200;//变量注释
  ```

#### G.CMT.07 正式交付给客户的代码不应包含TODO/FIXME注释【建议】

**【描述】**
TODO注释一般用来描述已知待改进、待补充的修改点。FIXME注释一般用来描述已知缺陷。在版本开发阶段可以使用这两类标签标注一些待处理的问题。

对于版本交付的代码中不应存在这两类标签，否则可能会被误解为代码中存在未实现的功能或已知的缺陷。

**【修改建议】**
正式交付的代码中，排查所有的TODO、FIXME注释，保证功能是完整的，已知缺陷都已经被修复，并将所有的TODO、FIXME注释删除。

**【正例】**
场景1：交付时文件中包含TODO/FIXME注释
- 修复示例：删除TODO、FIXME注释

  ```java
  public boolean doSomething(String data) {
      ...      
      return true;
  }
  ```

**【反例】**
场景1：交付时文件中包含TODO/FIXME注释
- 错误示例：

  ```java
  // 【不符合】交付时文件中包含TODO/FIXME注释
  // TODO(<author-name>): 补充XX处理
  public boolean doSomething(String data) {
      ...

      // FIXME: 存在XX缺陷，需添加xxx实现代码
      ...
      return true;
  }
  ```
## 1.3 格式

#### G.FMT.01 源文件编码格式（包括注释）应该是UTF-8【建议】

**【描述】**
对于源文件，应统一采用UTF-8进行编码。另外，对于资源文件（如xml, yml, properties等配置文件）等也应该采用utf-8编码

#### G.FMT.02 一个源文件按顺序包含版权、package、import、顶层类，且用空行分隔【建议】

**【描述】**
一个源文件中应按顺序包含以下信息：

1. 许可证或版权信息；
2. package语句，且语句内不换行；
3. import语句，且语句内不换行，不能用通配符*；
4. 顶级类（只有一个），所在.java源文件与它同名。

以上每个部分之间用一个空行隔开。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：版权、package、import、顶层类按推荐顺序排列
- 修复示例：版权、package、import、顶层类之间使用一个空行分隔

```java
/**
 * Copyright (c) Huawei Technologies Co., Ltd. 2012-2019. All rights reserved.
 */

package com.puppycrawl.tools.checkstyle;

import java.util.List;

/**
 * JavaComponentOrder介绍
 *
 * @since 2023-08-29
 */
public class JavaComponentOrder {
}
```

**【反例】**
场景1：版权、package、import、顶层类按推荐顺序排列
- 错误示例：版权、package的顺序错误，分隔使用多个空行

```java
package com.puppycrawl.tools.checkstyle;

/**
 * Copyright (c) Huawei Technologies Co., Ltd. 2012-2019. All rights reserved.
 */

import java.util.List;

/**
 * JavaComponentOrder介绍
 *
 * @since 2023-08-29
 */
public class JavaComponentOrder {
}

```

#### G.FMT.03 import包应该按照先安卓、华为公司、其他商业组织、其他开源第三方、net/org开源组织、最后java的分类顺序出现，并用一个空行分组【建议】

**【描述】**
import包推荐按如下顺序排列：

- 静态导入置于所有其他导入之上。
- 从上往下，大致分类是：import static、安卓、华为公司com.huawei.*、其他商业组织com.*、其他开源第三方xxx.yyy.*、net/org开源组织、javacard、Java最基础的包、Java的其他包、Java的扩展包。
- 每一类内部按照字母顺序排序。几大分类也大致是按字母排序（android、com、net、org），只是java/javax在最后。

Java最基础的包，是指java.base模块中的包，参照[java.base中的包清单](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/module-summary.html)。Java的其他包，是指java.base模块之外的[其他SE模块的包](https://docs.oracle.com/en/java/javase/11/docs/api/index.html)。

三方开源，包含了商业公司的开源，例如com.alibaba.fastjson，com.intellij.openapi等，与非盈利组织的开源，例如net/org组织的。这里，“其他”，就是指除了前缀为com、net、org之外的其他三方开源，例如下面示例中的lombok、maven。

这个风格兼容于[安卓的import顺序](https://source.android.com/setup/contribute/code-style#order-import-statements)，如果没有最上面的安卓包，也适用于非安卓。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：
- 修复示例：

```java
import static all.statics.imports;  // 静态导入

import android.xx.Xyz; // 安卓
import androidx.xx.Xyz; // 安卓

import com.hisilicon.xx.Xyz; // 海思
import com.huawei.xx.Xyz; // 华为公司

import com.google.common.io.Files; // 其他商业组织

import harmonyos.xx.Xyz; // 开源第三方 鸿蒙
import lombok.extern.slf4j.Sl4j;
import maple.xx.Xyz;
import maven.xx.Xyz;
import ohos.xx.Xyz;

import net.sf.json.xx.Xyz; // net/org开源组织

import org.linux.apache.server.SoapServer;

import javacard.xx.Xyz;

import java.io.IOException; // Java最基础的包
import java.net.URL;
import java.rmi.RmiServer;
import java.rmi.server.Server;

import javax.swing.JPanel; // Java的扩展包
import javax.swing.event.ActionEvent;

```

**【反例】**
场景1：
- 错误示例：

```java
import static all.statics.imports; // 静态导入
import android.xx.Xyz;  // 安卓
import androidx.xx.Xyz; // 安卓
import lombok.extern.slf4j.Sl4j;   // 开源第三方
import maple.xx.Xyz; // 开源第三方
import maven.xx.Xyz; // 开源第三方
import net.sf.json.xx.Xyz; // net/org开源组织
import org.linux.apache.server.SoapServer; // net/org开源组织
import com.hisilicon.xx.Xyz; // 海思
import com.huawei.xx.Xyz;    // 华为公司
import com.google.common.io.Files; // 其他商业组织
import harmonyos.xx.Xyz; // 开源第三方 鸿蒙
import ohos.xx.Xyz; // 开源第三方 鸿蒙
import javacard.xx.Xyz;
import java.io.IOException; // Java最基础的包
import java.net.URL;
import java.rmi.RmiServer;  // Java的其他包
import java.rmi.server.Server;
import javax.swing.JPanel;  // Java的扩展包
import javax.swing.event.ActionEvent;
```

#### G.FMT.04 一个类或接口的声明部分应该按照类变量、静态初始化块、实例变量、实例初始化块、构造器、方法的顺序出现，且用空行分隔【建议】

**【描述】**
一个类或接口的声明部分应该按照以下顺序排列：

- 类（静态）变量
- 静态初始化块
- 实例变量
- 实例初始化块
- 构造器
- 方法或嵌套类，嵌套类可以与成员方法根据业务逻辑交替出现，把概念上相近的放在一起，无需把所有嵌套类都下移至文件底部
- 类（静态）变量、实例变量、构造器，均按访问修饰符从大到小排列：public、protected、package（default）、private

**说明：**

1. 对于自注释成员变量之间可以不加空行；
2. 非自注释成员变量应该加注释且成员变量间以空行分隔。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：部分类声明未空行分隔
- 修复示例：

  ```java

  public class DeclarationOrder {
      private static final Logger LOGGER = LoggerFactory.getLogger(DeclarationOrder.class);

      static class StaticClass {
          ...
      }

      private void privateMethod() {
          ...
      }   
  ```

**【反例】**
场景1：部分类声明未空行分隔
- 错误示例：

  ```java
  public class DeclarationOrder {
      private static final Logger LOGGER = LoggerFactory.getLogger(DeclarationOrder.class);

      private void privateMethod() {
          ...
      }   

      static class StaticClass {
          ...
      }

  }
  ```

#### G.FMT.05 在条件语句和循环块中应该使用大括号【建议】

**【描述】**
在 `if`， `else`， `switch`， `for`，`do`和 `while`等语句中，即使程序体是空的或只包含一个语句，也应该使用大括号。对`switch`里面的`case`和`default`，大括号是可选的。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：在条件语句和循环块中使用大括号
- 修复示例：

```java
// 【符合】在条件语句和循环块中使用大括号
public void doSomething() {
    ...
    if (condition()) {
        doSomethingElse();
    }
}
```

**【反例】**
场景1：在条件语句和循环块中使用大括号
- 错误示例：

```java
// 【不符合】在条件语句和循环块中应该使用大括号
public void doSomething() {
    ...
    if (condition())
        doSomethingElse();
}
```

#### G.FMT.06 对于非空块状结构，左大括号应该放在行尾，右大括号应该另起一行【建议】

**【描述】**
对于非空块状结构（含初始化块），大括号应该遵循K&R风格：

- 左大括号不换行；
- 右大括号自己单独一行；
- 右大括号后，可以跟逗号、分号等，也可以跟随 `else`、 `catch`、`finally`等关键字语句。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1
- 修复示例1：遵循K&R风格换行

  ```java
  try {
      if (condition()) {
          doSomething();
      } else {
          doSomethingElse();
      }
  } catch (MyException ex) {
      handleException(ex);
  }
  ```

**【反例】**
场景1
- 错误示例：

  ```java
  try {
      doSomething();
  } catch (MyException ex) { handleException(ex); } // 【不符合】代码块应该换行
  ```

#### G.FMT.07 应该避免空块，必须使用空块时，应采用统一的大括号换行风格【建议】

**【描述】**
程序中应避免空块，但对于工具自动生成的、用于被覆盖的场景（例如UI监听器），可能需要定义空的方法体；忽略异常时也可能使用空的catch块。

**【修改建议】**
建议将代码中的无效空块删除。

**【正例】**
场景1：代码中存在空块
- 修复示例：

  ```java
  class EmptyBlockDemo {
      ...
      public void doSomething() {
          int data = 1;
          ...        
      }

  }
  ```

**【反例】**
场景1：代码中存在空块
- 错误示例：

  ```java
  class EmptyBlockDemo {
      static {

      }
      ...
      public void doSomething() {
          int data = 1;
          ...
          for (String str : list) {
          }
          ...
      }

  }
  ```

#### G.FMT.08 使用空格进行缩进，每次缩进4个空格【建议】

**【描述】**
只允许使用空格（space）进行缩进，每次缩进为**4**个空格。不允许插入制表符tab、换页符等。

当前几乎所有的集成开发环境（IDE）和代码编辑器都支持配置将Tab键自动扩展为**4**空格输入，应在代码编辑器中配置使用空格进行缩进。

**【修改建议】**
使用空格进行缩进，每次缩进4个空格。

**【正例】**
场景1：代码缩进采用非4个空格
- 修复示例：以4的倍数的空格方式进行缩进

  ```java
      private int data;
      private int result;
  ```

**【反例】**
场景1：代码缩进采用非4个空格
- 错误示例：使用3个空格进行缩进

  ```java
     private int data;
     private int result;
  ```

#### G.FMT.09 每行不超过一个语句【建议】

**【描述】**
一行应该只写一条语句

#### G.FMT.10 行宽不超过120个窄字符【建议】

**【描述】**
建议代码每行不超过maxLineLength(默认值为120，支持动态配置)个窄字符，保证在屏幕中可以呈现完整代码行，不需要拖动横向滚动条来查看完整代码。

对于宽字符，实际在IDE中的呈现宽度可通过cnCharLength参数进行设置，该参数的默认值值为1.5（结合IntelliJ IDEA的实际呈现效果确定）。

**【修改建议】**
代码行宽超过maxLineLength个窄字符时，在合理的位置进行换行处理。

**【正例】**
场景1：
- 修复示例：在合适处断行

  ```java
  public void doSomething(HashMap<String, String> hashMap,
      HashSet<String> hashSet, List<String> stringList, String describe) {
         ...
  }
  ```

**【反例】**
场景1：
- 错误示例：

  ```java
  public void doSomething(HashMap<String, String> hashMap, HashSet<String> hashSet, List<String> stringList, String describe) {
      // 代码行宽超过120个窄字符
      ...
  }
  ```

#### G.FMT.11 建议换行起点在操作符之前【建议】

**【描述】**
当语句过长，或者可读性不佳时，需要在合适的地方换行。换行时建议将操作符、连接符放在新的一行。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：未合理换行
- 修复示例1：在合适处断行，尽量将操作符、连接符放在新的一行

  ```java
  Student student = Student.builder()
      .setName("zhangsan")
      .setAge(14)
      .setGrade("5年级")
      .setMajor("软件工程")
      .setNum("123456789")
      .build();
  ```

**【反例】**
场景1：未合理换行
- 错误示例：

  ```java
  Student student = Student.builder().setName("zhangsan").setAge(14).setGrade("5年级").setMajor("软件工程").
      setNum("123456789").build();
  ```

#### G.FMT.12 减少不必要的空行，保持代码紧凑【建议】

**【描述】**
减少不必要的空行，可以显示更多的代码，方便代码阅读。建议：

- 根据上下内容的相关程度，合理安排空行：空行出现在属性，构造方法，方法，嵌套类，静态初始化块之间；
- 方法内部、类型定义内部、初始化表达式内部，不使用**连续**空行；
- 不使用**连续3个**或更多空行；
- 大括号内的代码块**行首之前和行尾之后不要加空行**，包括类型和方法定义、语句代码块。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：空行过多
- 修复示例1：

  ```java
  int foo() {
      ...
  }

  int bar() { 
      ...
  }

  int baz() {
      doSomething();
      ...      
  }
  ```

**【反例】**
场景1：空行过多
- 错误示例：

  ```java
  int foo() {
      ...
  }

  int bar() { 
      ...
  }

  int baz() {

      doSomething();
      ...

  }
  ```
#### G.FMT.13 用空格突出关键字和重要信息【建议】

**【描述】**
水平空格应该突出关键字和重要信息。单个空格应该分隔关键字与其后的左括号、与其前面的右大括号，出现在任何二元/三元运算符/类似运算符的两侧，`,:;`或类型转换结束括号`)`之后使用空格。行尾和空行不应有空格space。总体规则如下：
**必须**加空格的场景：
- （包括复合）赋值运算符前后，例如`=`、`*= `等；
- 逗号`,`、非for-in的冒号`:`、for循环等分隔的`;`符号之后加空格；
- 二元运算符、类型并交的`|`和`&`符号、for-in的冒号`:`的前后两侧，例如`base + offset`；
- lambda表达式中的箭头前后，例如`str -> str.length()`；
- 方法声明、条件判断语句、循环语句等场景下的`)`与`{`之间加空格，例如：`void func() {...}`。

**禁止**加空格的场景：
- `super`、`this`等少数关键字之后（多数关键字之后自然地须加空格）；
- 成员访问操作符前后，例如`instance.member`；
- 圆括号、方括号、注解或数组等非换行的大括号内两侧；
- 一元运算符前后，例如`cnt++`；
- 方法声明或者方法调用的左括号之前。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：格式不正确，未加空格
- 修复示例1：在适当处加空格

  ```java
  String str = "";
  private void method(String str, boolean bool, List<String> list)
  ```

**【反例】**
场景1：格式不正确，未加空格
- 错误示例：

  ```java
  String str="";
  private void method(String str,boolean bool,List<String> list)
  ```

#### G.FMT.14 不应插入多余空格使代码垂直对齐【建议】

**【描述】**
不应通过插入空格的方式使代码垂直对齐，包括在Javadoc的注释性描述内容前。原因是：
* 如果参数/变量名长短差异较大，无规律插入的空白呈凹凸状，并不美观；
* 如果某个参数/变量名较长，例如gardenPlantingDetailViewModel，对应的描述内容也较长的话，就可能不得不换行，又可能会有换行对齐的顾忌；
* 后续的维护者可能会困扰是否在整个module/package都刻意追求对齐。

因此，代码垂直对齐的弊大于利；为了减少维护成本，不造成困扰，不对齐是最好的选择。

**【修改建议】**
删除不必要的空格。

**【正例】**
```java
private int size;
private String name;
```

**【反例】**
```java
private int size; // 维护者可能不得不修改这些对齐空格数
private String name; // 不必与上行对齐注释
```

#### G.FMT.15 枚举常量间用逗号隔开，换行可选【建议】

**【描述】**
下面是一个典型的枚举类声明示例：
```java
private enum Size {SMALL, MEDIUM, LARGE}
```
由于不涉及方法及常量的注释，采用的是数组初始化的格式。枚举常量之间使用逗号进行分隔。

在枚举常量后面的逗号之后，换行符是可选的。还允许额外的空白行（通常只有一行）。例如：
```java
private enum Encoding {
    UTF8 {
        @Override
        public String toString() {
          return "UTF-8";
        }
    },

    UTF16,
    US_ASCII
}
```
Java的枚举比较灵活强大，而且与switch/case结合较好，应优先使用。

枚举的使用场景：
* 布尔型的两元素值，例如isCelsius = true | false来表示摄氏|华氏可用；
```java
public enum TemperatureScale {CELSIUS, FAHRENHEIT}
```
* 变量值仅在一个固定范围内变化用enum类型来定义。例如G.DCL.04的Keyboard例子；
* 整数或字符串的枚举模式，蕴含有某种命名空间的，例如上面的Size例子，或者其他语言的ComparisonResult，避免-1、0、1的数字比较。
```java
public enum ComparisonResult {
    ORDERED_ASCENDING,
    ORDERED_SAME,
    ORDERED_DESCENDING
}
```

**【修改建议】**
删除多余空行。


**【反例】**
```java
public enum EnumBlankTest {
    ENUM_A, ENUM_B,

    ENUM_C,

    ENUM_D;
}
```

#### G.FMT.16 case语句块结束时如果不加break，需要有注释说明（fall-through）【建议】

**【描述】**
switch语句中，当没有终止语句（`break`，`return`或抛出异常）时会执行到switch语句的结束处。当case语句块中没有终止语句时，需要添加注释，表明会继续执行到下一个case语句块。任何符合fall-through概念的注释都可以（通常是`// $FALL-THROUGH$`）。

Eclipse和IntelliJ IDEA支持`$FALL-THROUGH$`这种特殊的注释来suppress缺少`break`的告警。尽管这不是Java的标准，但它被主流的IDE支持，推荐优先使用。

**注意**：

- 当javac开启 `-Xlint:fallthrough`选项编译时 ，加与不加`$FALL-THROUGH$`，可能都会告警；修复此告警可以考虑改用`if else if`写法替代`switch case`。
- continue不能单独用于switch中，可用于循环中的switch中，continue的作用是跳出本次循环，所以case语句中使用continue时，还会影响循环代码块中后续代码的执行。

如果`case`语句是空语句，则可以不用加注释特别说明。

**【修改建议】**
建议为每个case语句添加break，如果确实不需要添加break时，需要添加`$FALL-THROUGH$`注释。

**【正例】**
场景1： case语句块结束时无break
- 修复示例1：增加break

  ```java
  switch (label) {
      case 0:
      case 1:
          System.out.println("1");
          break;
      case 2:
          System.out.println("2");
          break;
      case 3:
          System.out.println("3");
          break;
      default:
          System.out.println("Default case!");
  ```
- 修复示例2：增加`$FALL-THROUGH$`注释

  ```java
  switch (label) {
      case 0:
      case 1:
          System.out.println("1");
          // $FALL-THROUGH$
      case 2:
          System.out.println("2");
          break;
      case 3:
          System.out.println("3");
          break;
      default:
          System.out.println("Default case!");
  ```

**【反例】**
场景1： case语句块结束时无break
- 错误示例：

  ```java
  switch (label) {
      case 0:
      case 1:
          System.out.println("1");
      case 2:
          System.out.println("2");
      case 3:
          System.out.println("3");
          break;
      default:
          System.out.println("Default case!");
  }
  ```

#### G.FMT.17 应用于类、方法、类属性的每个注解独占一行【建议】

**【描述】**
应用于类、方法（含构造方法）、类属性的注解应在其上部，且每个注解独占一行。

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：多个注解共处一行
- 修复示例1：每个注解独占一行

  ```java
  @Partial
  @Mock
  DataLoader loader;

  @Override
  @Nullable
  public String doSomething() {
      ...
  }
  ```

**【反例】**
场景1：多个注解共处一行
- 错误示例：

  ```java
  @Partial@Mock
  DataLoader loader;

  @Nullable@Override
  public String doSomething() {
      ...
  }
  ```

#### G.FMT.18 块注释的缩进级别应与上下文代码相同【建议】

**【描述】**
块注释的缩进级别应该与被注释代码相同。可以采用单行注释（`// ...`）风格或多行注释（`/* ... */`）风格，对于多行注释风格，每行注释要以`*`开头且保持前后对齐

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：注释与代码不对齐
- 修复示例1：遵循K&R风格换行

  ```java
  public void doSomething() {
      ...
      if(condition()) {
          /*
           * 第一行注释
           * 第二行注释
           */
          int value = 0;
      }
      ...
  }
  public void doSomething() {
      ...
      if(condition()) {
          // 第一行注释
          // 第二行注释
          int value = 0;
      }
      ...
  }
  ```

**【反例】**
场景1：注释与代码不对齐
- 错误示例：

  ```java
  public void doSomething() {
      ...
      if(condition()) {
           /*
            * 第一行注释
            * 第二行注释
            */
          int value = 0;
      }
      ...
  }
  public void doSomething() {
      ...
      if(condition()) {
            // 第一行注释
         // 第二行注释
          int value = 0;
      }
      ...
  }
  ```

#### G.FMT.19 类和成员修饰符（如果存在）按Java语言规范建议的顺序显示【建议】

**【描述】**
类和成员修饰符（如果存在）按推荐的顺序显示（如果存在）：

```java
public protected private abstract default static final transient volatile synchronized native strictfp
```

**【修改建议】**
对代码进行格式化处理。

**【正例】**
场景1：类和成员修饰符与推荐顺序不一致
- 修复示例1：

  ```java
  public class ModifierOrder {
      private static final int II = 0;

      private synchronized void doSomething(String str) throws IOException {
          int num = 0;
          ...
      }
  }
  ```

**【反例】**
场景1：类和成员修饰符与推荐顺序不一致
- 错误示例：

  ```java
  public class ModifierOrder {
      private final static int II = 0;

      synchronized private void doSomething(String str) throws IOException {
          int num = 0;
          ...
      }
  }
  ```

#### G.FMT.20 数字字面量应该设置合适的后缀，long类型应该使用L作为后缀【建议】

**【描述】**
对于long、float、double类型的数字要使用合理的后缀指定数值的类型。Java 10增加了局部类型推断LVTI，一些字面量如果不加后缀，类型推断时可能与预期不符。为了形成良好的习惯，写出更健壮的代码，应参考LVTI的Style Guidelines。如果不加后缀，数值推断为int，float可能会推断为double。因此，应该在字面量后面加上后缀。

long值必须使用L后缀，不能使用l做后缀。例如，使用500000L而不是500000l。对于较大数值，可以使用Java 7新增的数字下划线分隔符，增强代码的可读性，如30_000_000_000L。

d、f后缀不易引起混淆的，不强制采用大写字母。

**【修改建议】**
增加相应后缀。

**【正例】**
场景1：使用不合适的后缀
- 修复示例1：

  ```java
  long sum = 0L;
  float flt = 1.0f; 
  double dbl = 2.0d; 
  ```

**【反例】**
场景1：使用不合适的后缀
- 错误示例：

  ```java
  long sum = 0l; 
  float flt = 1;
  double dbl = 2.0;
  ```

# 2. 编程实践
## 2.1 声明和初始化

#### G.DCL.01 每行声明一个变量【要求】

**【描述】**
每行的变量声明（类属性或局部变量）都只声明一个变量。

**【修改建议】**
每个变量声明都单独占一行。

**【正例】**
场景1：代码块未换行
- 修复示例1：遵循K&R风格换行

  ```java
  int length;
  int result;
  ```

**【反例】**
场景1：代码块未换行
- 错误示例：

  ```java
  int length, result;
  ```

#### G.DCL.02 局部变量被声明在接近它们首次使用的行【建议】

**【描述】**
将局部变量声明在接近它们首次被使用的点，以最小化局部变量的范围。当前工具会检查变量声明与变量使用间隔的代码行，超过`maxInterval（默认值10）行时会告警`。maxInterval可动态配置。

局部变量通常在声明时初始化，或在声明后立即被初始化，无需在声明时为局部变量设置无效的null值；另外，局部变量在使用结束后也不需要主动设置为null，类的成员变量要集中声明。

**【修改建议】**
将局部变量声明接近它们首次被使用的点，并在声明时初始化。

**【正例】**
场景1：局部变量声明未尽量接近首次被使用的点，并在使用时才初始化
- 修复示例：

  ```java
  public List<String> getResult(String param1, String param2) {
      ...
      List<String> result = new ArrayList<>(); // 【GOOD】首次被使用时才初始化
      result.addAll(getResult(param1));
      result.addAll(getResult(param2));
      return result;
  }
  ```

**【反例】**
场景1：局部变量声明未尽量接近首次被使用的点，并在使用时才初始化
- 错误示例：

  ```java
  public List<String> getResult(String param1, String param2) {
      List<String> result = new ArrayList<>();  // 【POTENTIAL FLAW】初始化到首次被使用时超过10行
      ...
      ... // 此处省略超过10行代码
      ...
      result.addAll(getResult(param1));
      result.addAll(getResult(param2));
      return result;
  }
  ```

#### G.DCL.03 禁止C风格的数组声明【要求】

**【描述】**
数组类型由数据元素类型紧跟中括号（[]）组成，数组声明格式应该是`String[] nonEmptyArray`，而不是`String nonEmptyArray[]`。

初始化数组时，数组中的最后一个元素后不要添加**逗号**，例如`String[] nonEmptyArray = {"these", "can", "change",};`。

**【修改建议】**
使用类似`String[] array`风格的数组声明方式；

数组初始化时，删除数组中最后一个元素后多余的逗号。

**【正例】**
场景1：数组声明格式错误
- 修复示例：

  ```java
  String[] nonEmptyArray = {"these", "can", "change"};
  ```
场景2：数组初始化时，最后一个元素后有冗余的逗号
- 修复示例：

  ```java
  String[] nonEmptyArray = {"these", "can", "change"};
  ```

**【反例】**
场景1：数组声明格式错误
- 错误示例：

  ```java
  String nonEmptyArray[] = {"these", "can", "change"};
  ```
场景2：数组初始化时，最后一个元素后有冗余的逗号
- 错误示例：

  ```java
  String[] nonEmptyArray= {"these", "can", "change", };
  ```

#### G.DCL.04 避免枚举常量序号的产生依赖于ordinal()方法【建议】

**【描述】**
Java枚举类型通过`ordinal()`方法返回枚举常量的排列序号。默认情况下，序号是根据声明顺序从0开始累加，但某些情况下会希望指定某些枚举常量为某个固定值以代表特殊意义（例如，键盘某个按键的具体编码），返回该固定值的方法不应基于`ordinal()`方法来实现。

**【修改建议】**
为枚举常量赋固定的值，消除对ordinal()方法的依赖。

**【正例】**
场景1：新增枚举常量时可能会导致原有枚举常量的值发生变化
- 修复示例1：

  ```java
  enum Keyboard {
      MOUSE_KEY_LEFT(1),
      MOUSE_KEY_RIGHT(2),
      MOUSE_KEY_CANCEL(4),
      MOUSE_KEY_MIDDLE(8);

      private final int mouseKeyValue;

      Keyboard(int value) {
          this.mouseKeyValue = value;
      }

      public int getMouseKeyValue() {
          return mouseKeyValue;
      }
  }
  ```

**【反例】**
场景1：新增枚举常量时可能会导致原有枚举常量的值发生变化
- 错误示例：

  ```java
  enum Keyboard {
      MOUSE_KEY_LEFT,
      MOUSE_KEY_RIGHT,
      MOUSE_KEY_CANCEL,
      MOUSE_KEY_MIDDLE;

      public int getMouseKeyValue() {
          return ordinal() + 1;
      }
  }
  ```

#### G.DCL.05 禁止将mutable对象定义为常量【要求】

**【描述】**
使用public static final的意图是定义一个常量。如果用其修饰一个mutable（可变）对象，极易产生不当使用，造成功能异常。

**【修改建议】**
对于`public static final`修饰的mutable对象，应该使用小驼峰命名，或者是将mutable对象修改为immutable对象，并使用大写字母命名。

**【正例】**
场景1：两个List集合都是mutable，不应该定义为常量
- 修复示例1：

  ```java
  public static final List<String> EMPTY_RESULT_LIST = Collections.unmodifiableList(new ArrayList<>());
  public static final List<String> EMPTY_RESULT_LIST = Collections.emptyList();
  ```
- 修复示例2：

  ```java
  private static final List<String> infoList= new ArrayList<>();
  ```

**【反例】**
场景1：两个List集合都是mutable，不应该定义为常量
- 错误示例：

  ```java
  public static final List<String> EMPTY_RESULT_LIST = new ArrayList<>();
  public static final List<String> RESULT_LIST = Arrays.asList("result1", "result2");
  ```

#### G.DCL.06 应该优先使用枚举类型管理用于表示业务状态或类型的常量【建议】

**【描述】**
用于表示业务状态或类型的常量，如果放在类或接口中直接定义，将弱化该常量的内在业务含义，降低代码的可读性
使用枚举类型管理业务状态或类型，会提升代码的可读性。另外，使用枚举类型可以方便地对有效值的范围进行限制

**【正例】**

  ```java
  enum ReviewStatus {
    DRAFT(0),
    APPROVED(1),
    REJECT(2),
    EXPIRED(3);
  }
  ```

**【反例】**

  ```java
  interface ReviewStatus {
    int DRAFT = 0;
    int APPROVED = 1;
    int REJECT = 2;
    int EXPIRED = 3;
  }
  ```

## 2.2 数据类型

#### G.TYP.01 进行数值运算时，避免整数溢出【建议】

**【描述】**
在进行数值运算过程中，确保运算结果在特定的整数类型的数据范围内，避免溢出，导致非预期的结果。 

内置的整数运算符不会以任何方式来标识运算结果的上溢或下溢。常见的加、减、乘、除都可能会导致整数溢出。另外，Java数据类型的合法取值范围是不对称的（最小值的绝对值比最大值大1），所以对最小值取绝对值( java.lang.Math.abs())时，也会导致溢出。

**【修改建议】**
可以通过先决条件检测、使用Math类的安全方法、向上类型转换或者使用BigInteger 等方法进行规避。

**【正例】**
场景1：使用int类型统计文件大小
- 修复示例：使用long类型变量统计总文件大小，可以有效避免出现整数溢出问题。
 ```java
public void unzip(FileInputStream zipFileInputStream, String dir) throws IOException {
    try (ZipInputStream zis = new ZipInputStream(zipFileInputStream)) {
        long totalFileSize = 0L;
        int readSize = 0;
        while ((entry = zis.getNextEntry()) != null) {
            ...
            while ((readSize = zis.read(buf)) != -1) {
                totalFileSize += readSize; // 使用long型统计文件总大小，可避免出现整数溢出问题
                if(totalFileSize >= MAX_TOTAL_FILE_SIZE) {
                    ...
                }
            ...
```

**【反例】**
场景1：使用int类型统计文件大小
- 错误示例：在统计zip文件中解压文件的总大小时使用了int类型的变量，由于int类型的上限为2G，当统计的文件总大小超过2G时将发生整数溢出。

```java
public void unzip(FileInputStream zipFileInputStream, String dir) throws IOException {
    try (ZipInputStream zis = new ZipInputStream(zipFileInputStream)) {
        int totalFileSize = 0;
        int readSize = 0;
        while ((entry = zis.getNextEntry()) != null) {
            ...
            while ((readSize = zis.read(buf)) != -1) {
                totalFileSize += readSize; // 使用int型变量统计文件总大小，容易出现整数溢出问题
                if(totalFileSize >= MAX_TOTAL_FILE_SIZE) {
                    ...
                }
            ...
```

#### G.TYP.02 确保除法运算和模运算中的除数不为0【要求】

**【描述】**
除零错误。

如果除法或模运算中的除数为零可能会导致程序终止或拒绝服务（DoS），因此需要在运算前保证除数不为0。

**【修改建议】**
对除数进行非零判断，然后再进行除法或取余运算。

**【正例】**
场景1：除数未判断是否为0
- 修复示例：

```java
private HostAddress getAddr() {
    List<HostAddress> addr = nebulaSessPoolConfig.getGraphAddrArray();
    if (CollectionUtils.isNotEmpty(addr)) { // 校验addr是否为空
        int newPos = (pos.getAndIncrement()) % addr.size();
        return addr.get(newPos);
    }
    ... // 其他逻辑代码
}
```

**【反例】**
场景1：除数未判断是否为0
- 错误示例1：

```java
public void testcase() {
    long dividendNum = 0;
    int divisorNum1 = 0;
    Integer divisorNum2 = 0;
    // POTENTIAL FLAW: 使用除法运算或模运算没有判断除数大小。
    long result1 = dividendNum / divisorNum1;
    // POTENTIAL FLAW: 使用除法运算或模运算没有判断除数大小。
    long result2 = dividendNum % divisorNum2;
}
```
- 错误示例2：
```java
private HostAddress getAddr() {
    List<HostAddress> addr = nebulaSessPoolConfig.getGraphAddrArray();

    // 【POTENTIAL FLAW】 集合中的元素数量可能为0。
    int newPos = (pos.getAndIncrement()) % addr.size();
    return addr.get(newPos);
}
```

#### G.TYP.03 禁止使用浮点数作为循环计数器【要求】

**【描述】**
由于浮点数存在精度问题，用作循环计数器可能会导致非预期的结果（如循环次数与预期不符、导致死循环等）。

**【修改建议】**
使用整数作为循环计数器。

**【正例】**
场景1：浮点数作为循环计数器
- 修复示例1：

  ```java
  for (int index = 2000000000; index < 2000000050; index++) {
      ...
  }
  ```

**【反例】**
场景1：浮点数作为循环计数器
- 错误示例：由于浮点数的精度问题导致条件判断结果与预期不符：因为`(float) 2000000000 == 2000000050`结果为true，所以循环体不会执行。

  ```java
  for (float flt = (float) 2000000000; flt < 2000000050; flt++) {
      ...
  }
  ```

#### G.TYP.04 需要精确计算时使用BigDecimal，不要使用float和double【要求】

**【描述】**
浮点数在一个范围很广的值域上提供了很好的近似，但是它不能产生精确的结果。二进制浮点数不能用有限的位数表示0.1，或者10的其他任何负次幂。

正的float大致能表示1.4e-45到3.4e38范围内的数，精度约6位有效数字。

正的double大致能表示4.9e-324到1.7e308范围内的数，精度约15位有效数字。

涉及精确的数值计算（货币、金融等），建议使用int、long、BigDecimal等；在构造BigDecimal时，使用浮点数容易导致精度损失，应该使用字符串格式的数值构造BigDecimal，即应该用BigDecimal (String val)，而不是BigDecimal (double val) 。

**【修改建议】**
应当人工判断是否为精确计算浮点数场景，不应强制清理。

**【正例】**
```java
BigDecimal income = new BigDecimal("1.03");
BigDecimal expense = new BigDecimal("0.42");
System.out.println(income.subtract(expense));
```
上述示例中，输出结果是0.61。

**【反例】**
```java
System.out.println(1.03d - 0.42d);
```
上述示例中，输出结果是0.6100000000000001，而非预期的0.61。

#### G.TYP.05 浮点型数据判断相等不要直接使用==，浮点型包装类型不要用equals()或者flt.compareTo(another)==0作相等的比较【要求】

**【描述】**
由于浮点数在计算机表示中存在精度的问题，数学上相等的数字，经过运算后，其浮点数表示可能不再相等，因而不能使用相等运算符==、equals()或者flt.compareTo(another) == 0等方法比较浮点数是否相等。另外，也不应该把浮点数作为HashMap的Key使用。

**【修改建议】**
使用误差判等。

**【正例】**
考虑浮点数的精度问题，可在一定的误差范围内判定两个浮点数值相等。这个误差应根据实际需要进行定义。另外，对于符号不同的两个浮点数，即使在误差范围内也不应该判为相等。如下示例中，两个浮点数值误差在1e-6f内判为相等。
```java
private static final float EPSILON = 1e-6f;

float foo = ...;
float bar = ...;
if (Math.abs(foo - bar) < EPSILON) {
    ...
}
```
Float或Double包装类型可由BigDecimal代替做运算操作。

**【反例】**
```java
float f1 = 1.0f - 0.9f;
float f2 = 0.9f - 0.8f;
if (f1 == f2) {
    // 预期进入此代码块，执行其他业务逻辑
    // 但事实上 fl == f2 的结果为 false
}
Float flt1 = Float.valueOf(f1);
Float flt2 = Float.valueOf(f2);
if (flt1.equals(flt2)) {
    // 预期进入此代码块，执行其他业务逻辑
    // 但事实上 equals 的结果为 false
}
```

#### G.TYP.06 禁止尝试与NaN进行比较运算，相等操作使用Double或Float的isNaN()方法【要求】

**【描述】**
当任意一个操作数是NaN（Not a Number）时，数值比较运算符<、<=、>、>=会返回false，运算符==会返回false，运算符!=会返回true。因为无序的特性常常会导致意外结果，所以不能直接与NaN进行比较。

**【修改建议】**
用Double或Float的`isNaN()`方法判断浮点数是否为`NaN`。

**【正例】**
场景1：数值直接与NaN比较
- 修复示例1：

  ```java
  public class NanComparison {
      public void doSomething(double num) {
          // 如果num的值为0.0d，则Math.cos(infinity)返回NaN
          double result = Math.cos(1 / num);
          if (Double.isNaN(result)) {
              System.out.println("result is NaN");
          }
          ...
      }
  }
  ```

**【反例】**
场景1：数值直接与NaN比较
- 错误示例：

  ```java
  public class NanComparison {
      public void doSomething(double num) {
          // 如果num的值为0.0d，则Math.cos(infinity)返回NaN
          double result = Math.cos(1 / num);
          if (result == Double.NaN) { // 相等比较总是false
              System.out.println("result is NaN");
          }
          ...
      }
  }
  ```

#### G.TYP.07 不要在代码中硬编码用于表示换行、文件路径分隔的字符--不要在代码中硬编码用于表示换行字符【建议】

**【描述】**
换行符（回车“\\r”、换行“\\n”）、文件路径分隔符（“\\”、“/”）在不同操作系统下是有差别的，代码中硬编码这两类字符，可能影响代码的可移植性。

**换行符的硬编码问题主要影响写文件（导致文件中的换行符与操作系统中的实际换行符不匹配）**，这类操作需要换行时，尽量用`PrintStream`、`PrintWriter`的`println()`来代替在字符串中使用硬编码换行符，也可以使用`System.lineSeparator()`获取运行时环境的换行符。对于读文件，针对不同操作系统下的文件应使用与之相匹配的换行符。另外，当文件的最终使用场景为某种固定操作系统时（例如文件仅用于linux环境下，不会在windows环境下使用），写文件时应该使用目标操作系统相对应的换行符。

**文件路径分隔符仅限于操作系统中的文件/文件夹的访问路径中**，不适用于url等路径中 （这类路径在不同操作系统下都是使用“/”作为分隔符）。文件路径分割符可以使用`java.io.File`中的`separator`或`pathSeparator`静态属性；另外，考虑到Windows环境下可以兼容“/”用作文件路径分隔符，代码中也可以统一使用“/”作为文件路径分隔符。

**【修改建议】**
用`PrintStream`、`PrintWriter`的`println()`来代替在字符串中使用硬编码换行符，也可以使用`System.lineSeparator()`获取运行时环境的换行符。
使用`java.io.File`中的`separator`或`pathSeparator`静态属性或统一使用`/`作为文件路径分隔符。

**【正例】**
场景1：在代码中硬编码使用文件路径分隔的字符
- 修复示例1：

  ```java
  System.out.println("Hello,world!");
  ```
场景2：在代码中硬编码使用文件路径分隔的字符
- 修复示例1：使用`File.separator` 作为文件路径分隔符

```java
String filePath = path + File.separator + "temp.txt";
```
- 修复示例2：统一使用`/`作为文件路径分隔符

```java
String filePath = path + "/tmp/temp.txt";
```

**【反例】**
场景1：在代码中硬编码使用文件路径分隔的字符
- 错误示例：

  ```java
  System.out.print("Hello,world!\n");
  ```

场景2：在代码中硬编码使用文件路径分隔的字符
- 错误示例：

```java
String filePath = path + "\\\\temp.txt";
```

#### G.TYP.08 字符串大小写转换、数字格式化为西方数字时，必须加上Locale.ROOT或Locale.ENGLISH【要求】

**【描述】**
字符串大小写转换时要考虑地区语言上的差异。`String`类的`toUpperCase()`、`toLowerCase()`方法、`format()`方法，如果不指定输入参数，则会按当前系统默认的编码模式转换，可能会导致非预期的转换结果。

字符对区域不敏感的，例如协议关键字、HTML的tags等优先用ROOT，字符对区域敏感或者强调英文习惯的应使用ENGLISH。

如果确实需要在本地化GUI显示本地语言数字文字，也允许使用：

- Locale.getDefault(Locale.Category.DISPLAY)
- mystr.getBytes(StandardCharsets.UTF_8)

**【修改建议】**
数字格式化为西方数字或字符串大小写转换时，加上`Locale.ROOT`或`Locale.ENGLISH`；

**【正例】**
场景1：数字格式化为西方数字场景
- 修复示例1：

  ```java
  String testString = String.format(Locale.ROOT, "%d", 2);
  System.out.println(testString);
  ```
场景2：字符串大小写转换场景
- 修复示例1：

  ```java
  String testString = "i";
  System.out.println(testString.toUpperCase(Locale.ROOT));
  ```

**【反例】**
场景1：数字格式化为西方数字场景
- 错误示例：

  ```java
  String testString = String.format("%d", 2);
  System.out.println(testString); // locale设置为ar-SA，2格式化后输出'  '
  ```
场景2：字符串大小写转换场景
- 错误示例：

  ```java
  String testString = "i";
  System.out.println(testString.toUpperCase());
  ```

#### G.TYP.09 字符与字节的互相转换操作，要指明正确的编码方式【要求】

**【描述】**
Java虚拟机采用编码方式默认与操作系统的字符编码方式相同，String的编码方式、`String.getBytes()`默认采用Java虚拟机编码。当跨平台实现字符与字节之间的转换，可能会导致乱码，所以字符与字节之间转换时要明确指定编码方式，推荐优先采用UTF-8编码。

本地化的自然语言文本（非ASCII）的比较、排序、查找，用java.text.Collator。

**【修改建议】**
字符与字节的互相转换操作，要指明编码方式，推荐优先采用UTF_8编码。

**【正例】**
场景1：字符与字节的互相转换操作未指明编码方式
- 修复示例：

  ```java
  String data = "123ABC中国";
  byte[] buf = data.getBytes(StandardCharsets.UTF_8);
  // 跨平台传输buf
  ...
  String result = new String(buf, StandardCharsets.UTF_8);
  ```
场景2：读取文件时，指定对应的编码方式
- 修复示例：

  ```java
  String line;
  try (FileInputStream fis = new FileInputStream(fileName);
      InputStreamReader isr = new InputStreamReader(fis, StandardCharsets.UTF_8);
      BufferedReader br = new BufferedReader(isr)) {
      line = br.readLine();
      ...
  }
  ```

**【反例】**
场景1：字符与字节的互相转换操作未指明编码方式
- 错误示例：

  ```java
  String data = "123ABC中国";
  byte[] buf = data.getBytes();
  // 跨平台传输buf
  ...
  String result = new String(buf);
  ```
场景2：读取文件时，指定对应的编码方式
- 错误示例：

  ```java
  String line;
  try (FileReader fr = new FileReader(fileName);
      BufferedReader br = new BufferedReader(fr)) {
      line = br.readLine();
      ...
  }
  ```

#### G.TYP.10 内存中的敏感信息使用完毕后立即清0【建议】

**【描述】**
内存中的敏感信息使用结束后如果不及时清理，会存在敏感信息泄露的风险。应尽量减少敏感信息在内存中的生命周期，使用结束后立即清0。java中的string是不可变对象（创建后无法更改），使用string保存口令、密钥等敏感信息时，这些敏感信息会一直中内存中直到被垃圾收集器回收（其生命周期不可控），如果进程的内存被dump，会导致敏感信息泄露风险。

内存中的敏感信息不能依赖垃圾收集器回收的机制，应该在使用结束时主动将内存中的信息清0.为了方便内存的清理，推荐优先使用`char[]/byte[]`存储敏感信息。对于必须使用String进行数据处理的场景，不需要将String转为`char[]`这样的无效处理，但要对所有涉及敏感信息的String中的信息进行清理。

**【反例】**
  ```java
  void doSomething() {
    String password = getPassword();
    verifyPassword(password);
    ...
  }

  boolean verifyPassword(String pwd) {
    ...
  }
  ```

**【正例】**
对String类型中的信息进行清0处理
  ```java
  void doSomething() {
    String password = getPassword();
    verifyPassword(password);
    try {
        Field valueFieldOfString = String.class.getDeclaredField("value");
        valueFieldOfString.setAccessible(true);
        char[] value = (char[]) valueFieldOfString.get(password);
        Arrays.fill(value, (char)0x00);
    }
    ...
  }
  ```
使用char[]存储密码
  ```java
  void doSomething() {
    char[] password = getPassword();
    verifyPassword(password);
    ...
    // 清除password
    Arrays.fill(password, (char)0x00);
  }

  boolean verifyPassword(String pwd) {
    ...
  }
  ```


#### G.TYP.11 基本类型优于包装类型，注意合理使用包装类型【建议】

**【描述】**
Java有两种类型，基本类型（Primitive type）和引用类型（Reference type）。基本类型如`boolean`、`int`、`double`，引用类型如`String`、`List`。每一种基本类型都有其对应的包装类型（Wrapper classes），如对应`int`的是`Integer`。
检查如下场景：
1，for循环变量使用封装类
2，封装类直接使用`==`比较

**【修改建议】**
尽量直接使用基本类型

**【正例】**
场景1：
- 修复示例：for循环变量应该使用基本类型

  ```java
  for(int i = 0; i < 10; i++) {
      i++;
  }
  ```
场景2：
- 修复示例：封装类的比较应该使用equals()方法

  ```java
  Integer var1=1;
  Integer var2=2;
  if (var.equals(var2)) {
    ...
  }
  ```

**【反例】**
场景1：
- 错误示例：for循环变量使用封装类

  ```java
  for(Integer i = 0; i < 10; i++) {
      i++;
  }
  ```
场景2：
- 错误示例：封装类直接使用`==`比较

  ```java
  Integer var1=1;
  Integer var2=2;
  if (var == var2) {
    ...
  }
  ```

#### G.TYP.12 明确地进行类型转换，避免依赖隐式类型转换【建议】

**【描述】**
明确的类型转换表明程序员知道混合运算中所涉及的不同类型。通过明确的类型转换引导程序员考虑数据类型转换导致的数据截断、数据精度损失问题，提升系统的可靠性。

除了常见的将取值范围宽的类型转为取值范围较窄的类型导致数据截断问题之外，还要考虑如下两类问题：

1） **意外地**浮点数转换截取会导致误差被逐步放大；
2） 将整数转为浮点数时可能存在精度损失问题，包括`int`、`long`转`float`，`long`转`double`这三种场景。

- **在运算符的右边，要小心地使用更宽的操作数。尽量不要把复合赋值运算符应用于`byte`、`short`、`char`类型的变量。**

**【修改建议】**
直接明确进行类型转换

**【正例】**
场景1：计算时产生隐式转换
- 修复示例1：

  ```java
  short value1 = 459;
  int value2 = 5781;
  long value3 = 4664382371590666666L;

  float value4 = (float) value1 / 13.0f;  // 计算结果为 35.307693
  double value5 = (double) value2 / 30.0d; // 计算结果为 192.7
  BigDecimal bd = new BigDecimal(value3);
  BigDecimal bd2 = bd.multiply(new BigDecimal(2)); // 计算结果为9328764743181333332
  ```

**【反例】**
场景1：计算时产生隐式转换
- 错误示例：

  ```java
  short value1 = 459;
  int value2 = 5781;
  long value3 = 4664382371590666666L;

  float value4 = value1 / 13;  // 计算结果为35.0(截断)
  double value5 = value2 / 30; // 计算结果为192.0(截断)
  double value6 = value3 * 2;  // 计算结果为-9.1179793305282181E18
  double value7 = (double) value3 *2; // 计算结果为9.328764743181332E18(截断)
  ```

#### G.TYP.13 在引用类型向下转换前用instanceof进行判断【建议】

**【描述】**
没有判断类型直接进行类型转换，可能会因类型不匹配而导致运行时异常`java.lang.ClassCastException`。简单的修改方法是在强制转换之前使用`instanceof`进行判断，确认转换操作的可行性，除此之外其他的类型检查方式也是可行的（如直接判断Class类型），只要能保证类型可正确转换即可。

当集合或数组中保存多种类型的对象，当遍历这些数据使用时可以使用instanceof对每个元素的类型进行判断。但是运行时类型检查是一项耗时的操作，另外还可能带来修改点过多、工作量巨大的问题，同时维护的工作量也会倍增。最佳实现方式是改善设计，使集合/数组中只有同一种类型的对象。

**【修改建议】**
引用类型向下转换前用`instanceof`进行判断；除此之外其他的类型检查方式也是可行的（如直接判断Class类型），只要能保证类型可正确转换即可。

**【正例】**
场景1：类型强转前，未判断类型是否兼容，当类型不匹配时会抛出`java.lang.ClassCastException`
- 修复示例1：

  ```java
  public void doSomething(Object obj) {
      ...
      if(obj instanceof SomeResource) {
          SomeResource resouce = (SomeResource)obj;
          ...
      }
  }
  ```

**【反例】**
场景1：类型强转前，未判断类型是否兼容，当类型不匹配时会抛出`java.lang.ClassCastException`
- 错误示例：

  ```java
  public void doSomething(Object obj) {
      ...
      SomeResource resouce = (SomeResource)obj;
      ...
  }
  ```

## 2.3 表达式

#### G.EXP.01 不要在单个表达式中对相同的变量赋值超过一次【要求】

**【描述】**
对相同的变量进行多次赋值的表达式会产生混淆，并且容易产生非预期的行为。清晰的变量赋值会使代码更易懂，也更能保证程序按预期运行。

**【修改建议】**
不要在单个表达式中对相同的变量赋值超过一次

**【正例】**
场景1：使用count对循环计数，而实际count最终结果却为0
- 修复示例1：

  ```java
  int count = 0;
  for (int i = 0; i < 100; i++) {
      ...
      count++;
  }
  System.out.println(count); // count的值为100   
  ```

**【反例】**
场景1：使用count对循环计数，而实际count最终结果却为0
- 错误示例：

  ```java
  int count = 0;
  for (int i = 0; i < 100; i++) {
      ...
      count = count++;
  }
  System.out.println(count); // count的值为0
  ```

#### G.EXP.02 用括号明确表达式的操作顺序，避免过分依赖默认优先级【建议】

**【描述】**
涉及多种操作符混合使用并且优先级容易混淆的场景，建议使用括号明确表达式操作顺序。
```java
foo = a + b + c;    // 运算符相同，不需要括号
if (a && b && c)    // 运算符相同，不需要括号
foo = 1 << (2 + 3); // 运算符不同，优先级易混淆，需要括号
```

**【修改建议】**
用括号明确表达式的操作顺序，避免过分依赖默认优先级

**【正例】**
场景1：未用括号明确表达式的操作顺序，可能导致误读
- 修复示例1：

  ```java
  System.out.println(1 << (2 + 3)); // 运算符不同，优先级易混淆，需要括号
  ```

**【反例】**
场景1：未用括号明确表达式的操作顺序，可能导致误读
- 错误示例：

  ```java
  System.out.println(1 << 2 + 3);
  ```

#### G.EXP.03 条件表达式?:的第2和第3个操作数应使用相同的类型【建议】

**【描述】**
条件运算符?:使用第1个操作数的布尔值决定后续表达式哪个被执行。但是Java语言有相当复杂的规则去判定表达式的结果类型，不一致的操作数类型，可能导致意料之外的类型转换。如第2和第3个操作数在类型对齐时，可能会因为自动拆箱导致NullPointerException。

**【修改建议】**
三目运算符(`?:`)的第2和第3个操作数类型要保持一致。

**【正例】**
场景1：表达式?:的第2和第3个操作数类型不一致
- 修复示例1：

  ```java
  char ch = 'A';
  int value = 50;
  boolean condition = ...; 
  System.out.println(condition ? ch : ((char) value));  // condition为true时，输出A ； 为false 时，输出 2
  Integer integer = null;
  System.out.print(condition ? integer : Integer.valueOf(value)); // condition为true时，输出 null
  ```

**【反例】**
场景1：表达式?:的第2和第3个操作数类型不一致
- 错误示例：

  ```java
  char ch = 'A';
  int value = 50;
  boolean condition = ...; 
  System.out.println(condition ? ch : value); // condition为true时，输出65，自动将char类型转为int类型 ；为false 时，输出 50
  Integer integer = null;
  System.out.print(condition ? integer : value); // condition为true时，抛出NullPointerException
  ```

#### G.EXP.04 表达式的比较，应该遵循左侧倾向于变化、右侧倾向于不变的原则--表达式比较左变右不变【建议】

**【描述】**
当变量或方法调用与常量比较时，如果常量放左边，如`if (MAX == v)`不符合阅读习惯，而`if (MAX > v)`更是难于理解。

应该按人的正常阅读、表达习惯，将常量放右边。由于现代IDE都有较为强大的NullPointerException检测能力，可以考虑显式地注解`@NotNull`。

1. 对于`==`，变量放在左边，null或常量放在右边;
2. 如果变量明显不会为null，例如new、单例、非空注解后，可用`obj.equals("foo")`；如果必须使用null，或者这个变量有可能是null，应该使用`Objects.equals(variable, "foo")`或者显式用if判断或`"foo".equals(obj)`;
3. 描述区间时，前半段表达式常量在左，也是允许的，如`if (MIN < bar && bar < MAX)`。

**【修改建议】**
应该把常量放在比较表达式的右边

**【正例】**
场景1：常量放在比较表达式的右边
- 修复示例1：

  ```java
  if (var1 < CONST_VAR) {
      ...
  }
  ```

**【反例】**
场景1：常量放在比较表达式的左边
- 错误示例：

  ```java
  if (CONST_VAR > var1) {
      ...
  }
  ```

#### G.EXP.05 禁止直接使用可能为null的对象，防止出现空指针引用【要求】

**【描述】**
访问可能为null的对象的成员。

访问一个为null的对象时，会导致空引用问题，代码中抛出 NullPointerException 。该类问题应该通过预检查的方式进行消解，而不是通过 try...catch 机制处理 NullPointerException 。

**【修改建议】**
可以为null的字段声明为@Nullable。

**【正例】**
场景1：
- 修复示例：对于方法返回值可能为null时，方法返回值使用前进行判空处理
```java
@Nullable
protected JobResult executeJob(EdgeJobContext context) {
    JobResult jobResponse = null;
    if (StrUtil.equals(EdgeJobConstants.ShellJobExecuteType.COMMAND, executeType)) {
        jobResponse = edgeShellClient.executeByCommand(command);
    } else if (StrUtil.equals(EdgeJobConstants.ShellJobExecuteType.SCRIPT, executeType)) {
        jobResponse = edgeShellClient.executeByCommand(remotePath, command); 
    }

    return jobResponse;
}

JobResult jobResult = executeJob(context);
if （jobResult  != null）{
    jobResult.setId(startJobRequest.getId()); //jobResult有可能会返回null值，所有这个jobResult需要增强null处理
 }
```

**【反例】**
场景1：
- 错误示例：对于方法返回值可能为null时，方法返回值使用前未做判空处理

```java
@Nullable
protected JobResult executeJob(EdgeJobContext context) {
    JobResult jobResponse = null;
    if (StrUtil.equals(EdgeJobConstants.ShellJobExecuteType.COMMAND, executeType)) {
        jobResponse = edgeShellClient.executeByCommand(command);
    } else if (StrUtil.equals(EdgeJobConstants.ShellJobExecuteType.SCRIPT, executeType)) {
        jobResponse = edgeShellClient.executeByCommand(remotePath, command); 
    }

    return jobResponse;
}

JobResult jobResult = executeJob(context);
jobResult.setId(startJobRequest.getId()); //jobResult有可能会返回null值，所有这个jobResult需要增加null处理
```

#### G.EXP.06 代码中不应使用断言（assert）【建议】

**【描述】**
使用assert不当。

默认情况下，断言（assert）是被禁用的，可以通过-ea或-da选项开启或关闭。断言（assert）的判断条件为false时会抛出 AssertionError ，表示程序遇到了一个不可恢复的错误，对该错误不做处理会导致程序异常退出。断言（assert）只适用于开发调试阶段的问题定位。以下两种场景不应使用断言：

* 运行态错误检查：如下常见的运行态错误检查，不应使用断言（assert），否则可能因为运行态错误触发 AssertionError 导致程序异常终止或因为断言（assert）禁用而导致错误未处理。

1. 无效的用户输入（如环境变量、命令行参数等）;

2. IO错误（如文件操作、网络通信等）;

3. 权限不足（如文件权限、用户权限等）;

4. Java虚拟机运行时错误（如堆栈溢出等）;

5. 系统资源耗尽（如文件句柄数不足等）。

* 逻辑代码执行：在断言（assert）中执行业务逻辑代码，会导致程序因为断言（assert）的启用/禁用产生不同的逻辑。

**【修改建议】**
不应使用断言。

**【正例】**
场景1：使用了断言的代码。
- 修复示例1：使用其他方法代替断言，如if语句：
```java
String data = null;
...
if (data != null) {
    ...  
}
```

**【反例】**
场景1：使用了断言的代码。
- 错误示例：使用断言。

```java
String data = null;
...
assert data != null;
...
```

## 2.4 控制语句

#### G.CTL.01 不要在控制性条件表达式中执行赋值操作或执行复杂的条件判断【要求】

**【描述】**
控制性条件表达式常用于if、while、for、?:等条件判断中。

在控制性条件表达式中执行赋值或执行复杂的条件判断，常常导致意料之外的行为，且代码的可读性非常差。

复杂的条件判断是指在一个条件表达式中boolean运算符数量超过3。对于复杂的条件判断建议封装到一个独立的方法中，通过具有描述性的方法名让代码阅读者更容易理解复杂判断的目的，另外也方便对独立方法中的复杂条件判断逐步进行优化，最终使代码主流程和判断逻辑更加清晰可读。

**【修改建议】**
1、对于boolean型变量，在if判断中避免重复与true/false进行比较；
2、在条件判断中不要进行赋值操作；
3、对于复杂条件判断，建议结合业务场景进行合理的优化，比如：结合业务逻辑进行合理拆分、封装独立方法等，具体可参考代码示例中的场景3。

**【正例】**
场景1：boolean型变量不要直接与true/false比较
- 修复示例：

  ```java
  if (isFoo) 
  ```
场景2：不要在条件表达式中进行赋值操作
- 修复示例：

  ```java
  public void fun(boolean isBar) {
      boolean isFoo = isBar;   // 在上面赋值，if条件判断中直接使用
      if (isFoo) {
          ...
      }
  }
  ```
场景3：避免使用复杂的条件判断
- 修复示例1：将判断的条件以业务逻辑判断，单独抽取出method。

  ```java
  protected void addSpecialDataCol(String ciName, String ciLink, List<Object> rowList, String scriptPackageName) {
      String csvDir = "";
      if (this.scriptPackageName.toUpperCase(Locale.ROOT).contains("SWAP_")) {
          csvDir = this.objCIRM.getGlobalInfoMap().get("csvDir");
      }
      rowList.add(ciLink);

      // 将上述代码 if 逻辑判断部分，按照业务逻辑进行拆分。
      if (isLte() || isNr()) {
          String ciModeMark = getCIModeMark(ciName);
          rowList.add(ciModeMark);
      }
      rowList.add(csvDir);
      addNeCols(ciName, rowList);
  }
  private boolean isNr() {
      return "NR_NetworkInspection".equalsIgnoreCase(this.scriptPackageName)
      || "His_NR_NetworkInspection".equalsIgnoreCase(this.scriptPackageName);
  }
  private boolean isLte() {
      return StringUtil.containsIgnoreCase(this.scriptPackageName, "ONE_LTE")
          || "LTE_NetworkInspection".equalsIgnoreCase(this.scriptPackageName)
          || "His_LTE_NetworkInspection".equalsIgnoreCase(this.scriptPackageName);
  }
  ```
- 修复示例2：将复杂条件判断抽取为有含义的方法
  ```java
  private boolean isInvalidExecParams(String params) {
      return params.contains("!") || params.contains(";") || params.contains("&") || params.contains("$")
          || params.contains(">") || params.contains("<") || params.contains("`") || params.contains("\\\\")
          || params.contains(System.lineSeparator()) || params.contains("/") || params.contains("|");
  }
  ```
- 修复示例3：将复杂条件判断调整为正则检查
  ```java
  private static final Pattern CHAR_CHECK = Pattern.compile("[!;&$><`\\\\\\\\r\
/|]");

  private boolean isInvalidExecParams(String params) {
      return CHAR_CHECK.matcher(params).find();
  }  
  ```
- 修复示例4：将复杂的条件判断调整为集合包含检查
  ```java
  List<String> conditionList = new ArrayList<>();
  conditionList.add(TY_STRINGVALUETY_STRINGVALUE.toUpperCase(Locale.ROOT));
  conditionList.add(TY_BOOLEANVALUE.toUpperCase(Locale.ROOT));
  ...
  conditionList.add(TY_TIMESTAMPVALUE.toUpperCase(Locale.ROOT));

  // 条件判断可直接简化为判断集合中是否包含该条件元素
  if(conditionList.contains(table.toUpperCase(Locale.ROOT))) {
      // 其他代码...
  }  
  ```

**【反例】**
场景1：boolean型变量不要直接与true/false比较
- 错误示例：

  ```java
  if (isFoo = false)  // 在控制性判断中赋值不易理解
  if (isFoo == false) // 冗余不简洁，容易出错
  if (false == isFoo) // 冗余不简洁，容易出错
  ```
场景2：不要在条件表达式中进行赋值操作
- 错误示例：

  ```java
  public void fun(boolean isBar) {
      boolean isFoo;
      if (isFoo = isBar) {
          ...
      }
  }
  ```
场景3：避免使用复杂的条件判断
- 错误示例1：

  ```java
  protected void addSpecialDataCol(String ciName, String ciLink, List<Object> rowList, String scriptPackageName) {
      String csvDir = "";
      if (this.scriptPackageName.toUpperCase().contains("SWAP_")) {
          csvDir = this.objCIRM.getGlobalInfoMap().get("csvDir");
      }
      rowList.add(ciLink);

      // 此处的 if 逻辑判断较为复杂。
      if (StringUtil.containsIgnoreCase(this.scriptPackageName, "ONE_LTE")
          || "LTE_NetworkInspection".equalsIgnoreCase(this.scriptPackageName)
          || "His_LTE_NetworkInspection".equalsIgnoreCase(this.scriptPackageName)
          || "NR_NetworkInspection".equalsIgnoreCase(this.scriptPackageName)
          || "His_NR_NetworkInspection".equalsIgnoreCase(this.scriptPackageName)) {
          String ciModeMark = getCIModeMark(ciName);
          rowList.add(ciModeMark);
      }
      rowList.add(csvDir);
      addNeCols(ciName, rowList);
  }
  ```

#### G.CTL.02 含else if分支的条件判断应在最后加一个else分支【建议】

**【描述】**
含多个else if条件组合的判断逻辑，往往会出现被遗漏的分支，在最后设置一个else分支可对遗漏场景进行处理（类似于switch-case语句要有default分支）。

最后的else分支如果没有明确的处理场景，可以记录一条日志或抛出异常等，如：`log("unknown condition")`、`throw new IllegalStateException("non-exhaustive cases")`等。

**【修改建议】**
在含多个else if条件组合的判断逻辑最后增加else分支。

**【正例】**
场景1：缺少else分支
- 修复示例1：

  ```java
  if ((employee.flags & HOURLEY_FLAG) && (employee.age > RETIRED_AGE)) {
      ...
  } else if ((employee.flags & HOURLEY_FLAG) && (employee.age < RETIRED_AGE)) {
      ...
  } else if ((employee.flags & HOURLEY_FLAG) && (employee.age == RETIRED_AGE)) {
      ...
  } else {
      ...
  }
  ```

**【反例】**
场景1：缺少else分支
- 错误示例：

  ```java
  if ((employee.flags & HOURLEY_FLAG) && (employee.age > RETIRED_AGE)) {
      ...
  } else if ((employee.flags & HOURLEY_FLAG) && (employee.age < RETIRED_AGE)) {
      ...
  } else if ((employee.flags & HOURLEY_FLAG) && (employee.age == RETIRED_AGE)) {
      ...
  }
  ```

#### G.CTL.03 switch语句要有default分支【要求】

**【描述】**
每个switch语句都应该包含一个default分支，即使default分支没有业务逻辑代码。default分支中没有业务逻辑代码时，可以记录一条日志或抛出异常等，如：`log("unknown condition")`、`throw new IllegalStateException("non-exhaustive cases")`等。

**【修改建议】**
switch语句中增加default分支。

**【正例】**
场景1：缺乏default分支
- 修复示例1：

  ```java
  switch(d) {
  case 2:
      ...
      break;
  case 3:
      ...
      break;
  default:
      ...
      break;
  }
  ```

**【反例】**
场景1：缺乏default分支
- 错误示例：

  ```java
  switch(d) {
  case 2:
      ...
      break;
  case 3:
      ...
      break;
  }
  ```

#### G.CTL.04 循环必须保证可正确终止【要求】

**【描述】**
错误终止循环的条件可能会导致无限循环，性能不佳，错误结果以及其他问题。在用于终止循环的任何条件下，攻击者都可能影响这些错误，这些错误可被利用来导致拒绝服务或其他攻击。所以在实现循环语句时，要能保证循环可以安全的终止，避免出现无限循环的问题。

常见导致无限循环的场景包括但不限于以下场景：

- while(true)中缺少合适的break语句；
- 循环变量未正确修改；
- 直接使用外部输入作为循环终止的判断条件；
- 不当的循环终止条件判断；
- 使用浮点数作为循环计数器（浮点数章节已经说明）。

另外，代码中更不应该出现空的无限循环，编写一个空的循环体，不会完成具体功能，反倒可能会消耗CPU；另一方面，如果刻意编写空循环来消耗CPU，却又可能被编译器或者JIT优化而消除。

**【修改建议】**
要为循环语句设置合理的终止条件，或添加合理终止循环的语句。

**【正例】**
```java
public void notAlwaysRun() {
    while (true) {
        if(condition()) {
            doSomething();
            break;
        } else{
            doSomethingElse();
        }
    }
}
```

**【反例】**
```java
public void alwaysRun() {
    while (true) {
        if(condition()) {
            doSomething();
        } else{
            doSomethingElse();
        }
    }
}
```

#### G.CTL.05 避免在循环体中修改循环控制变量【建议】

**【描述】**
如果在循环体的操作中异向地修改循环控制参数的数值，可能导致循环退出条件永远达不到（死循环）或者循环执行次数不符合预期。

**【修改建议】**
避免在循环体中修改循环变量。

**【正例】**
场景1：在循环体中对循环变量进行逆向修改
- 修复示例：

  ```java
  public void doSomething() {
      ...
      for(int i = 1; i <= 10; i++){
          doSomething();
      }
      ...
  } 
  ```

**【反例】**
场景1：在循环体中对循环变量进行逆向修改
- 错误示例：

  ```java
  public void doSomething() {
      ...
      for(int i = 1; i <= 10; i++){
          if(condition()){
              doSomething();
          }else{
              i -= 2;
          }        
      }
      ...
  }
  ```

#### G.CTL.06 禁止switch语句中直接嵌套switch【要求】

**【描述】**
switch语句中直接嵌套switch语句，会增加代码的复杂度，代码的可读性也会变差。

**【修改建议】**
将嵌套的switch抽取成一个单独的方法。

**【正例】**
场景1：switch语句嵌套
- 修复示例： 

```java
switch (condition1) {
    case "case1":
        doSomething(condition2);
        break;
    case "case2":
        doSomethingElse();
        break;
    default:
        doSomethingDefault();
}
...
private void doSomething(String condition2) {
    switch (condition2) {
        case "case1":
            doSomethingCase1();
            break;
        case "case2":
            doSomethingCase2();
            break;
        default:
            doSomethingDefault();
    }
}
```

**【反例】**
场景1：switch语句嵌套
- 错误示例：

```java
switch (condition1) {
    case "case11":
        switch (condition2) {
            case "case21":
                doSomethingCase1();
                break;
            case "case22":
                doSomethingCase2();
                break;
            default:
                doSomethingDefault();
        }
        break;
    case "case12":
        doSomething();
        break;
    default:
        doSomethingDefault();
}
```

#### G.CTL.07 避免在条件/循环控制语句中包含过多的条件【建议】

**【描述】**
控制性条件表达式常用于if、while、for、?:等条件判断中。
复杂的条件判断是指在一个条件表达式中boolean运算符数量超过3.对于复杂的条件判断建议封装到一个独立的方法中，通过具有描述性的方法名让代码更容易理解，也方便对独立方法中的复杂条件判断逐步进行优化。

**【反例】**
```java
if (fileName == null || fis.availiabe() == 0 || fileName.equalsIgnoreCase("id") || fileName.equalsIgnoreCase("name") ||
    dh.getContentType() == null) {
    ...
}
```

**【正例】**
```java
boolean isFileNameCompliance = fileName == null || fileName.equalsIgnoreCase("id") || fileName.equalsIgnoreCase("name");
if (isFileNameCompliance || fis.availiabe() == 0 || dh.getContentType() == null) {
    ...
}
```

## 2.5 方法

#### G.MET.01 方法要简短--方法的参数不应超过5个【建议】

**【描述】**
复杂过长的方法往往意味着方法抽象层次不足或功能不够单一。建议方法要进行合理抽象分层，对功能不够单一的方法使用合理的手段进行重构，以提升代码的可读性、可维护性。

可以考虑从以下维度间接约束方法的尺寸和复杂度：

- 方法行数建议不超过50行（非空非注释）；
- 方法的参数，建议不超过5个；
- 方法最大代码块嵌套深度，建议不要超过4层。

**方法参数**

方法的参数过多，会使得该方法易于受外部（其他部分的代码）变化的影响，从而影响维护工作，同时也会增大测试的工作量。方法的参数个数如果超过5个，可以考虑如下优化方式：

- 对方法进行抽象或重构；
- 将相关参数合在一起，定义成类，用对象封装；
- 当构造方法含有多个参数时，尝试建造者（Builder）或工厂模式，JDK源码中有很多示例可供参考，例如Calendar.Builder，HttpClient.Builder。

**代码块嵌套深度**

方法的代码块嵌套深度指的是方法中的代码控制块（例如：if、for、while、switch等）之间互相包含的深度。方法本身算一层，try-catch不算一层嵌套。方法内的lambda表达式、局部类和匿名类嵌套层次以最内层方法来计算，不累计enclosing method的嵌套层次。使用卫语句可以有效的减少if相关的嵌套层次。

**【修改建议】**
重构和简化方法。

**【正例】**
```java
class Parameters {
    private int var1;
    private int var2;
    private int var3;
    private int var4;
    private int var5;
    private int var6;
    ...
}
public void doSomething(Parameters parameters) {
...
}
```
使用卫语句减少函数嵌套层次
```java
private static boolean checkNum(List<Object> list) {
    if (list.size() <= ZERO) {
        return false;
    }
    if (list.size() == ONE) {
        return false;
    }
    if (list.size() == TWO) {
        return false;
    }
    return true;
}
```

**【反例】**
```java
方法参数过多：
public void doSomething(int var1, int var2, int var3, int var4, int var5, int var6) {
...
}
```
代码嵌套过深：
```java
private static boolean checkNum(List<Object> list) {
    if (list.size() <= ZERO) {
        return false;
    } else {
        if (list.size() == ONE) {
            return false;
        } else if (list.size() == TWO) {
            return false;
        } else {
            return true;
        }
    }
}
```

#### G.MET.02 不要使用已标注为@Deprecated的方法、类、类的属性等【要求】

**【描述】**
标注为@Deprecated的方法、类、类的属性等，是由于各种原因被废弃的，为了保持兼容性而没有删除。新写的代码应避免继续使用这些方法、类等，而应该使用推荐的代替实现。

**【修改建议】**
不要使用已标注为@Deprecated的方法、类、类的属性等

**【正例】**
场景1：不要使用已标注为@Deprecated的方法、类、类的属性等
- 修复示例：使用非Deprecated的方法、类、类属性。

```java
    private static String message() {
        return "";
    }

    private String message2() {
        return "";
    }

    private void doSomething1() {
        String message = testClass.message();
        if (StringUtils.isEmpty(message)) {
            return;
        }
    }

    private void doSomething2() {
        String message = message2();
        if (StringUtils.isEmpty(message)) {
            return;
        }
    }
```

**【反例】**
场景1：不要使用已标注为@Deprecated的方法、类、类的属性等
- 错误示例：

```java
    @Deprecated
    private static final String deprecated = "";

    @Deprecated
    private static String message() {
        return "";
    }

    @Deprecated
    private String message2() {
        return "";
    }

    private void doSomething1() {
        // 【POTENTIAL FLAW】 Do not use deprecated class, method or field.
        String message = message();
        if (StringUtils.isEmpty(message)) {
            return;
        }
    }

    private void doSomething2() {
        // 【POTENTIAL FLAW】 Do not use deprecated class, method or field.
        String message = DeprecatedClass.message();
        if (StringUtils.isEmpty(message)) {
            return;
        }
    }

    private void doSomething3() {
        // 【POTENTIAL FLAW】 Do not use deprecated class, method or field.
        DeprecatedClass deprecatedClass = new DeprecatedClass();

        // 【POTENTIAL FLAW】 Do not use deprecated class, method or field.
        if (StringUtils.isEmpty(deprecatedClass.a)) {
            return;
        }
    }
```

#### G.MET.03 不应把方法的参数当做临时变量【建议】

**【描述】**
不应把方法的参数当做临时变量，因为每个变量/参数都有自己独特的功用，让一个变量承担多个职责，变量名将无法清晰表达其功能，会使程序难以理解。

**【修改建议】**
在方法体中，应该避免对方法参数进行修改，包括重新赋值、自增/自减运算。如果需要，可以定义一个新的临时变量替代方法参数。

**【正例】**
场景1：
- 修复示例：在方法中定义临时变量替代方法参数

```java
// 【GOOD】使用final能够帮助判断，避免意外修改。
int doSomething(final int basicSalary) {
    int performanced = basicSalary * getMultiplier(basicSalary);
    int bonused = performanced + getAdder(performanced);
    ...
    return bonused;
}
```

**【反例】**
场景1：
- 错误示例：方法参数用作临时变量，在方法中对其进行了修改

```java
// 【POTENTIAL FLAW】方法参数用作临时变量。
int doSomething(int inputData) {
    inputData = inputData * getMultiplier(inputData);
    inputData = inputData + getAdder(inputData);
    return inputData;
}
```

#### G.MET.04 谨慎使用可变数量参数【建议】

**【描述】**
在Java 5版本中初次引入可变数量参数（variable number of arguments）特性，该特性支持方法接受指定类型的零个到多个参数。使用可变数量参数时，要注意如下两类问题：
1. 不建议使用可变数据参数方法重写使用一个固定长度数组作为参数的方法，这样会导致代码可读性变差；
2. 可变类型参数的类型要明确，避免使用Object等模糊类型，方便Java编译器对参数类型进行检查。

**【修改建议】**
1. 删除对可变数量参数方法进行重载的方法（参考场景1）。
2. 明确可变类型参数的类型，避免使用Object等模糊类型（参考场景2）。

**【正例】**
场景1：对可变数量参数方法进行重写
- 修复示例：
```java
public double sum(double... values) {
    ...
}

// 【GOOD】删除对可变数量参数方法进行重写的方法。
```
场景2：可变数量参数的类型为Object
- 修复示例：
```java
// 【GOOD】可变类型参数的类型明确，方便Java编译器对参数类型进行检查。
public void doSomething(String... args) {
    ...
}
```

**【反例】**
场景1：对可变数量参数方法进行重写
- 错误示例：对可变数量参数方法进行了重载，可能会导致对于sum(23d, 32d)不确定实际执行的是哪个方法。
```java
public double sum(double... values) {
    ...
}

// 【POTENTIAL FLAW】对可变数量参数方法sum()进行了重载。
public double sum(double value1, double value2) {
    ...
}
```
场景2：可变数量参数的类型为Object
- 错误示例：
```java
// 【POTENTIAL FLAW】可变类型使用Object等模糊类型，不方便Java编译器对参数类型进行检查。
public void doSomething(Object... args) {
    ...
}
```

#### G.MET.05 对于返回数组或者容器的方法，应返回长度为0的数组或者容器，代替返回null【建议】

**【描述】**
在方法返回值中，用长度为`0`的数组或者容器，来代替返回`null`，则上层调用代码在使用此返回的数组或者容器前，无需再判断是否为空，业务逻辑一气呵成，代码更简洁。

同时，也避免了程序员因为忘记了对返回值进行空指针检查，而导致的NullPointerException。

**【修改建议】**
用长度为`0`的数组或者容器，来代替返回`null`,或者通过@Nullable标明返回值可以为`null`

**【正例】**
场景1：
- 修复示例1：返回空的集合

  ```java
    public static List<String> decorate(String[] personDescs) {
        if (personDescs == null || personDescs.length == 0) {
            return Collections.emptyList(); // 返回空的集合，上层调用不需要判空，代码书写更流畅
        }
        List<String> personNames = new ArrayList<>(personDescs.length);
        for (String personDesc : personDescs) {
            String personName = getPersonName(personDesc);
            personNames.add(personName);
        }
        return personNames;
    }
  ```
- 修复示例2：通过`@Nullable`标明返回值可以为`null`

  ```java
    @Nullable
    public static List<String> decorate(String[] personDescs) {
        if (personDescs == null || personDescs.length == 0) {
            return null; // 返回null，上层代码需要对该返回值判null，否则会出现NPE
        }
        List<String> personNames = new ArrayList<>(personDescs.length);
        for (String personDesc : personDescs) {
            String personName = getPersonName(personDesc);
            personNames.add(personName);
        }
        return personNames;
    }
  ```

**【反例】**
场景1：
- 错误示例：

  ```java
    public static List<String> decorate(String[] personDescs) {
        if (personDescs == null || personDescs.length == 0) {
            return null; // 返回null，上层代码需要对该返回值判null，否则会出现NPE
        }
        List<String> personNames = new ArrayList<>(personDescs.length);
        for (String personDesc : personDescs) {
            String personName = getPersonName(personDesc);
            personNames.add(personName);
        }
        return personNames;
    }
  ```

#### G.MET.06 使用Optional代替null作为返回值或者可能的缺失值；禁止对Optional对象赋值为null【建议】

**【描述】**
使用`Optional`代替`null`作为返回值或者可能的缺失值；禁止对`Optional`对象赋值为`null`
工具检查场景:
- 检查是否将`null`赋值给`Optional`对象
- 检查是否将`Optional`对象和`null`进行比较（==或!=）
- 检查方法返回类型是否为`Optional<Integer>`、`Optional<Long>`或`Optional<Double>`
- 检查方法返回类型是否为`Optional<集合或数组>`

**【修改建议】**
**禁止对Optional对象赋值/返回为null，或与null比较**，例如: `Optional<Foo> foo = null;`；
不应该返回`Optional<Integer>`、`Optional<Long>`、`Optional<Double>`，而应该使用`OptionalInt`、`OptionalLong`、`OptionalDouble` ；
一般不应该返回`Optional<集合或数组>`，而用空集合或空数组替代。

**【正例】**
场景1：对于返回集合类型，应返回空集合
- 修复示例：返回空的集合

  ```java
    public Optional<List<String>> doSomething() {
        ...
        return Collections.emptyList();
    }
  ```
场景2：对于包装类型应该使用OptionalInt、OptionalLong、OptionalDouble
- 修复示例：使用OptionalInt

  ```java
    public OptionalInt doSomething() {
        ...
        return OptionalInt.of(1);
    }
  ```
场景3：禁止对Optional对象赋值/返回为null
- 修复示例：返回Optional.empty()
  ```java
    public OptionalInt doSomething() {
        ...
        return Optional.empty();
    }
  ```
场景4：禁止Optional与null进行比较
- 修复示例：使用Optional.empty()来做判空逻辑
  ```java
    public void doSomething(Optional<String> opt) {
        ...
        if(opt.isEmpty()) {
        ...
        }
    }
  ```

**【反例】**
场景1：对于返回集合类型，应返回空集合
- 错误示例：使用了Optional<集合或数组>

  ```java
    public Optional<List<String>> doSomething() {
        ...
        return Optional.empty();
    }
  ```
场景2：对于包装类型应该使用OptionalInt、OptionalLong、OptionalDouble
- 错误示例：使用了Optional<Integer>

  ```java
    public Optional<Integer> doSomething() {
        ...
        return Optional.of(1);
    }
  ```
场景3：禁止对Optional对象赋值/返回为null
- 错误示例：返回值为Optional<>的方法返回了null

  ```java
    public Optional<String> doSomething() {
        ...
        return null;
    }
  ```
场景4：禁止Optional与null进行比较
- 错误示例：将`Optional`对象和`null`进行比较（==或!=）

  ```java
    public void doSomething(Optional<String> opt) {
        ...
        if(opt==null) {
        ...
        }
    }
  ```

#### G.MET.07 不要忽略方法的返回值【建议】

**【描述】**
方法调用者应该对方法的返回值进行合理的处理，否则可能因为忽略方法返回值导致安全风险。 资源操作类方法会通过返回值来指示本次操作是否成功（例如File.delete()），这类方法调用后必须根据返回值对资源操作失败的场景进行防护处理。

**【修改建议】**
1. 资源操作类方法（例如File.delete()）调用后必须根据返回值对资源操作失败的场景进行防护处理。
2. Java中的String是不可变类型，对于字符串的修改要赋值给新的String变量。

**【正例】**
场景1：调用文件操作相关方法。
- 修复示例：

```java
public void deleteFile() {
    File someFile = new File("someFileName.txt");

    // Do something with someFile
    if (!someFile.delete()) {
        // Handle failure to delete the file
        ...
    }
}
```
场景2：String类操作
- 修复示例：

```java
String original = "insecure";
original = original.replace('i', '9');
System.out.println(original); // 输出 9nsecure
```

**【反例】**
场景1：调用文件操作相关方法。
- 错误示例：

```java
public void deleteFile() {
    File someFile = new File("someFileName.txt");

    // Do something with someFile
    someFile.delete();
}
```
场景2：String类操作
- 错误示例：

```java
String original = "insecure";
original.replace('i', '9');
System.out.println(original); // 输出 insecure
```

## 2.6 类与接口
#### G.OBJ.01 应避免定义public且非final的类属性【建议】

**【描述】**
应避免定义public且非final的类属性。将类的属性设置为私有（private）的理由是：不希望类的外部代码依赖这个属性，依赖类内部的实现细节。这样，当内部实现需要变更时，影响面就比较小，变更的成本就比较低。

**【修改建议】**
将public类型的属性更改为private或设置为final。

**【正例】**
场景1：
- 修复示例：将public类型的成员变量改为private类型

```java
public class UserInfo {
    private String userName;
    private String addr;
    private int age;

    ...
}
```

**【反例】**
场景1：
- 错误示例：类含有public类型的成员变量

```java
public class UserInfo {
    public String userName;
    public String addr;
    public int age;

    ...
}
```

#### G.OBJ.02 不要在父类的构造方法中调用可能被子类覆写的方法【要求】

**【描述】**
在父类的构造方法中调用可能被子类覆写的方法。

如果父类构造器中调用被子类重写的方法，会导致子类重写的方法在子类成员变量初始化之前和构造器执行之前执行，从而导致子类重写的方法无法访问到子类实例变量的值，因为此时这些变量还没有被初始化。

当在父类的构造方法中调用可能被子类覆写的方法时，构造方法的表现是不可预知的，很可能会导致异常。而问题出现后，往往难以快速定位。

这是由于在Java中，当子类初始化时，会调用父类的构造方法，当父类构造方法调用了被子类覆写的方法，往往会由于子类的初始化未完成而导致异常。

**【修改建议】**
不要在父类的构造方法中调用可能被子类覆写的方法。

**【正例】**
父类构造方法中调用println()，但是是私有方法，不会被子类覆写。
  ```java
  public class SeniorClass {
      public SeniorClass() {
          println(); 
      }
      private void println() {
          System.out.println("IAmSeniorClass");
      }
  }
  public class JuniorClass extends SeniorClass {
      private String name;
      public JuniorClass() {
          super(); 
          name = "JuniorClass";
      }
  }
  ```

**【反例】**
父类在构造函数中使用了可被子类覆写的toString()函数，导致子类调用父类的构造方法时，导致空指针异常。
  ```java
public class SeniorClass {
    public SeniorClass() {
        toString(); // 如果toString()被覆写了，可能会导致异常
    }

    @Override
    public String toString() {
        return "IAmSeniorClass";
    }
}

public class JuniorClass extends SeniorClass {
    private String name;
    public JuniorClass() {
        super(); // 调用父类的构造方法，导致NullPointerException异常
        name = "JuniorClass";
    }

    @Override
    public String toString() {
        return name.toUpperCase();
    }
}
  ```

#### G.OBJ.03 构造方法如果有多个，尽量重用【建议】

**【描述】**
由于可选参数导致的存在多个构造方法时，参数少的构造方法可以重用参数更多的构造方法，这样可以是代码更加简洁。

**【修改建议】**
由于可选参数导致的存在多个构造方法时，参数少的构造方法重用参数更多的构造方法。

**【正例】**
场景1：
- 修复示例：复用参数更多的构造方法

  ```java
    public class Student {
        private String name;
        private String sex;
        private int weight; // 可选参数
        private int height; // 可选参数
        private int age;    // 可选参数
        public Student(String name, String sex) {
            this(name, sex, 0);
        }
        public Student(String name, String sex, int weight) {
            this(name, sex, weight, 0);
        }
        public Student(String name, String sex, int weight, int height) {
            this(name, sex, weight, height, 0);
        }
        public Student(String name, String sex, int weight, int height, int age) {
            this.name = name;
            this.sex = sex;
            this.weight = weight;
            this.height = height;
            this.age = age;
        }
        ...
    }
  ```

**【反例】**
场景1：
- 错误示例： 

  ```java
    public class Student {
        private String name;
        private String sex;
        private int weight; // 可选参数
        private int height; // 可选参数
        private int age;    // 可选参数
        public Student(String name, String sex) {
            this.name = name;
            this.sex = sex;
        }
        public Student(String name, String sex, int weight) {
            this.name = name;
            this.sex = sex;
            this.weight = weight;
        }
        public Student(String name, String sex, int weight, int height) {
            this.name = name;
            this.sex = sex;
            this.weight = weight;
            this.height = height;
        }
        public Student(String name, String sex, int weight, int height, int age) {
            this.name = name;
            this.sex = sex;
            this.weight = weight;
            this.height = height;
            this.age = age;
        }
        ...
    }
  ```

#### G.OBJ.04 避免在无关的变量或无关的概念之间重用名字，避免隐藏（hide）、遮蔽（shadow）和遮掩（obscure）【要求】

**【描述】**
一个变量、方法或类可以分别遮蔽（shadow）在类内部具有相同名字的变量、方法或类。如果一个实体被遮蔽了，那么就无法用简单名引用到它。

对于以下场景工具不会告警：

- 构造器参数变量
- setter方法参数变量

**【修改建议】**
对于方法中的临时变量，避免与类的属性重名。

**【正例】**
场景1：
- 修复示例： 

```java
    public class HiddenField {
      Object obj;

      public void doSomething(Object prama) {
          ...
      }
      ...
  }
```

**【反例】**
场景1：
- 错误示例： 

```java
  public class HiddenField {
      Object obj;

      public void doSomething(Object obj) {
          ...
      }
      ...
  }
```

#### G.OBJ.05 避免基本类型与其包装类型的同名重载方法【建议】

**【描述】**
方法的重载特性允许声明名字相同、参数不同的方法（含构造方法），编译器在每次调用时都会去探查与调用参数相匹配的方法。但在自动装箱和泛型场景下，可能会导致各个重载方法之间的边界变得模糊，增加代码维护的难度，弄不清楚实际调用的是哪个方法。

**【修改建议】**
对于重载方法，方法的参数类型要清晰明确，避免出现参数类型差别为封装类型与基本类型的重载方法。当方法的参数类型确实仅存在封装类型与基本类型的差别时，建议通过方法名进行区分。

**【正例】**
场景1：
- 修复示例：

```java
class SomeResource {
    HashMap<Integer, Integer> hm = ...;
    public static Employee createSomeResourceByInt(int id, String name) {
        // 非重载，使用int类型的id构造对象
    }
    public static Employee createSomeResourceByInteger(Integer id, String name) {
        // 非重载，使用Integer类型的id构造对象
    }
    public Integer getDataByIndex(int id) {
        // 非重载
    }
    public String getDataByValue(Integer id) {
        // 非重载
    }
}
```

**【反例】**
场景1：
- 错误示例：

```java
class SomeResource {
    HashMap<Integer, Integer> hm = ...;
    public SomeResource(int id, String name) {
        ...
    }
    public SomeResource(Integer id, String name) {
        ...
    }
    public String getData(Integer id) {
        // 获取一个特定的记录
        String str = hm.get(id).toString();
        return str + SUFFIX;
    }
    public Integer getData(int id) {
        // 获取在位置id的记录
        return hm.get(id);
    }
}
```

#### G.OBJ.06 覆写equals方法时，要同时覆写hashCode方法【要求】

**【描述】**
当对象需要进行逻辑相等的比较时（比如判断String、Integer对象中的值是否相同），应对Object的equals()方法进行覆写，实现具体的判断逻辑。覆写equals()方法时，要同步覆写hashCode()方法。Java对象在存放到基于Hash的集合（如HashMap、HashTable等）时，会使用其Hash码进行索引，如果只覆写了equals()方法，而没有正确覆写hashCode()方法，则会导致效率低下甚至出错。Java对象的hashCode()方法有如下约定：

- 同一次运行中，同一个对象如果equals方法中用到的信息没有改变，多次调用其hashCode方法返回值必须相同；
- 如果对两个对象调用equals方法时相等，则这两个对象的hashCode方法，也必须返回相同的值；
- 如果对两个对象调用equals方法时不相等，则对这两个对象的hashCode方法，不要求其返回值不同，但是出于减少哈希碰撞的性能考虑，最好能不同。

**【修改建议】**
覆写`equals()`方法时，需要同步覆写`hashCode()`方法。

**【正例】**
场景1：
- 修复示例：同步覆写`equals()`方法和`hashcode()`方法

```java
public class Entity {
    private String id;
    private String value;
    @Override
    public boolean equals(Object obj) {
        ...
        if (obj instanceof Entity) {
            Entity that = (Entity) obj;
            return Objects.equals(this.id, that.id)
                && Objects.equals(this.value, that.value);
        }
        ...
        return false;
    }

    // 【GOOD】覆写`equals()`方法时，需要同步覆写`hashCode()`方法
    @Override
    public int hashCode() {
        int result = 0;
        ...
        return result;        
    }
}
```

**【反例】**
场景1：
- 错误示例：仅覆写`equals()`方法，未同步覆写`hashcode()`方法

```java
public class Entity {
    private String id;
    private String value;
    @Override
    public boolean equals(Object obj) {
        ...
        if (obj instanceof Entity) {
            Entity that = (Entity) obj;
            return Objects.equals(this.id, that.id)
                && Objects.equals(this.value, that.value);
        }
        ...
        // 【POTENTIAL FLAW】未覆写`hashCode()`方法
        return false;
    }
}
```

#### G.OBJ.07 子类覆写父类方法或实现接口时必须加上@Override注解【要求】

**【描述】**
加上`@Override`注解的好处是，如果覆写时因为疏忽，导致子类方法的参数同父类不一致，编译时会报错，使问题在编译期就被发现；如果父类修改了方法定义造成子类不再覆写父类方法，也能使问题在编译期尽早被发现。

**【修改建议】**
子类重载的父类方法，要添加@Override注解注解。

**【正例】**
场景1：
- 修复示例： 

  ```java
    class BaseClass {
        public void doSomething() {
            ...
        }
    }

    class SubClass extends BaseClass {
        @Override
        public void doSomething() {
            ...
        }
    }
  ```

**【反例】**
场景1：
- 错误示例： 

  ```java
    class BaseClass {
        public void doSomething() {
            ...
        }
    }

    class SubClass extends BaseClass {
        public void doSomething() {
            ...
        }
    }
  ```

#### G.OBJ.08 正确实现单例模式【建议】

**【描述】**
单例模式（Singleton Pattern）属于创建型模式，它确保在同一个进程内，单例类只有一个对象，并且该对象对所有其他对象提供访问，常见的如Windows系统下的资源管理器、Spring Bean等都会采用这种方式。

**【修改建议】**
可通过如下方式保证正确实现单例模式：
- 将其构造方法设为私有；
- 防止对象在初始化被多个线程同时运行；
- 确保该对象不可序列化；
- 确保该对象无法克隆。

**【正例】**
场景1：将构造方法设置为private
- 修复示例： 

  ```java
  public class Singleton {
      private static Singleton instance = null;
      private Singleton() {
      }
      public static synchronized Singleton getSingletonInstance() {
          if (instance == null) {
              instance = new Singleton();
          }
          return instance;
      }
  }
  ```
场景2：双重检查锁实现单例模式
- 修复示例： 

  ```java
  public class Singleton {
      private static volatile Singleton instance = null;
      private Singleton() {
          ...
      }
      public static Singleton getSingletonInstance() {
          if (instance == null) {
              synchronized (Singleton.class) {
                  if (instance == null) {
                      instance = new Singleton();
                  }
              }
          }
          return instance;
      }
  }
  ```
场景3：单例模式的Class禁止支持序列化操作
- 修复示例： 

  ```java
  public class Singleton { // 不实例化Serializable接口
      private static volatile Singleton instance = null;
      private Singleton() {
          ...
      }
      public static Singleton getSingletonInstance() {
          ...    
      }
  }
  ```
场景4：单例模式的Class禁止实现Clone功能
- 修复示例： 

  ```java
  public class Singleton { // 不实例化Cloneable接口
      private static volatile Singleton instance = null;
      private Singleton() {
          ...
      }
      public static Singleton getSingletonInstance() {
          ...    
      }
  }
  ```

**【反例】**
场景1：将构造方法设置为private
- 错误示例：非私有构造方法

  ```java
  public class Singleton {
      private static Singleton instance = null;
      protected Singleton() {
          ...
      }
      public static Singleton getSingletonInstance() {
          if (instance == null) {
              instance = new Singleton();
          }
          return instance;
      }
  }
  ```
场景2：双重检查锁实现单例模式
- 错误示例：并发场景导致无法正确实现单例模式

  ```java
  public class Singleton {
      private static Singleton instance = null;
      private Singleton() {
          ...
      }
      public static Singleton getSingletonInstance() {
          if (instance == null) {
              instance = new Singleton();
          }
          return instance;
      }
  }
  ```
场景3：单例模式的Class禁止支持序列化操作
- 错误示例：通过反序列化来构造多个实例

  ```java
  public class Singleton implements Serializable {
      private static final long serialVersionUID = 6289738106308341737L;
      private static volatile Singleton instance = null;
      private Singleton() {
          ...
      }
      public static Singleton getSingletonInstance() {
          ...    
      }
  }
  ```
场景4：单例模式的Class禁止实现Clone功能
- 错误示例：通过clone机制获得新的实例

  ```java
  public class Singleton implements Cloneable {
      private static volatile Singleton instance = null;
      private Singleton() {
          ...
      }
      public static Singleton getSingletonInstance() {
          ...    
      }
  }
  ```

#### G.OBJ.09 使用类名调用静态方法，而不要使用实例或表达式来调用【要求】

**【描述】**
明确地使用类名调用静态方法不容易造成混淆。使用实例调用静态方法时，调用的静态方法是声明类型的静态方法，与实例的实际类型无关，可能会导致与预期的结果不一致。当父类和子类有同名静态方法时，声明父类变量引用子类实例，使用该实例调用同名的静态方法调用的是父类的静态方法，而非子类的静态方法。类的静态属性也要使用类名进行调用。

**【修改建议】**
使用类名来调用静态方法或静态变量。

**【正例】**
场景1：使用类名调用静态方法
- 修复示例： 用类名来调用静态方法

```java
class Dog {
    public static void bark() {
        System.out.print("woof");
    }
}

class Basenji extends Dog {
    public static void bark() {
        System.out.println("miao");
    }
}

public class Bark {
    public static void main(String[]  args) {
        Dog.bark();
        Basenji.bark();
    }
}
```

**【反例】**
场景1：使用类名调用静态方法
- 错误示例： 上述示例中，对bark()的两次调用，实际调用的都是Dog.bark()方法。

```java
class Dog {
    public static void bark() {
        System.out.println("woof");
    }
}

class Basenji extends Dog {
    public static void bark() {
        System.out.println("miao");
    }
}

 public class Bark {
    public static void main(String[]  args) {
        Dog woofer = new Dog();
        Dog nipper = new Basenji();
        woofer.bark();
        nipper.bark();
    }
}
```

#### G.OBJ.10 接口定义中去掉多余的修饰词【建议】

**【描述】**
在接口定义中，属性缺省具有public static final修饰词，非默认方法缺省具有public abstract修饰词。代码中不需要再次提供这些修饰词。

**【修改建议】**
删除接口中的属性与非默认方法的缺省修饰符。

通过类名调用

**【正例】**
场景1：接口中的属性缺省修饰符需省略
- 修复示例： 接口属性声明中不使用冗余修饰符

  ```java
    public interface ParameterSetNameInterface {
        int STATIC_VAR = 100;
    }
  ```

**【反例】**
场景1：接口中的属性缺省修饰符需省略
- 错误示例：接口的属性声明使用了冗余的`public static final`修饰符

  ```java
    public interface ParameterSetNameInterface {
        public static final int STATIC_VAR = 100;
    }
  ```

#### G.OBJ.11 可以在接口中加上静态方法表示相关的工厂或助手方法【建议】

**【描述】**
推荐在接口中添加静态方法表示相关的工厂或助手方法，这样不需要在“接口名字 + s”的工具类/助手类中放置各种静态方法了。例如可以把Collections的方法放到Collection接口里面。

## 2.7 异常处理
#### G.ERR.01 不要通过一个空的catch块忽略异常【要求】

**【描述】**
异常表示程序运行发生了错误，发生异常会中断程序的正常处理流程。不应该使用空的catch块会忽略发生的异常，发生异常要么在catch块中对异常情况进行处理，要么将异常抛出，交由上层调用方进行处理。

**【修改建议】**
代码中避免出现空的catch块，确实需要空catch块，建议添加注释，解释为什么可以忽略该异常。

**【正例】**
场景1：代码中应避免空的catch块
- 修复示例： 消除代码中的空catch块
  ```java
  InputStream inputStream = null;
  try {
      inputStream = new InputStream(null);
      doSomething();
  } catch (Exception t) {
      logger.error("something is wrong");
  }    
  ```

**【反例】**
场景1：代码中应避免空的catch块
- 错误示例： 使用空catch块忽略异常
  ```java
  InputStream inputStream = null;
  try {
      inputStream = new InputStream(null);
      doSomething();
  } catch (Exception t) {
  }
  ...
  ```

#### G.ERR.02 不要直接捕获异常的基类Throwable、Exception、RuntimeException【建议】

**【描述】**
不应该捕捉throwable或Error异常。

捕获异常的目的是为了进行恢复，而如果不加区分的捕获所有异常，则无法进行对应异常的恢复处理。因此，应该区分并捕获具体的异常。捕获时，列出多种具体异常，如果用同一个处理逻辑，应该用并语法 (ExceptionType1 | ... | ExceptionTypeN 变量) 来减少重复代码。
从Java 7开始，允许将catch子句组合成一个代码块，而无需使用危险的catch-all子句或复制整个代码块。捕获异常的目的是为了进行恢复，而如果不加区分的捕获所有异常，则无法进行对应异常的恢复处理。因此，应该区分并捕获具体的异常。

**【修改建议】**
在异常的设计上应区分应用程序异常和系统异常，从而对可恢复的异常和不可恢复的异常采用不同的恢复策略。

* 例外场景：
  1. 编码过程中遇到了第三方api直接抛出 Exception 异常，代码中需要使用 catch (Exceptionex)；
  2. 在框架中属于“公共服务”性质的“兜底”处理，例如事件循环。

**【正例】**
```java
catch (ParseException | IOException exception) {
    // 处理异常
}
```

**【反例】**
```java
try { 
    /* ... */ 
} catch (Throwable t) { 
    /* ... */ 
}

try { 
    /* ... */ 
} catch (Error e) { 
    /* ... */ 
}
```

#### G.ERR.03 不要直接捕获可通过预检查进行处理的RuntimeException，如NullPointerException、IndexOutOfBoundsException等【建议】

**【描述】**
可通过预检查的方式进行消除的RuntimeException，这类异常一般表示程序逻辑错误，不应该通过try...catch的方式进行处理（这也可能会影响代码的可读性及系统的运行效率）。推荐通过预检查方式进行消除，该类运行期异常包括：NullPointerException、IndexOutOfBoundsException等。对于NumberFormatException、IllegalArgumentException、IllegalStateException等可通过try...catch方式处理。

**【修改建议】**
不要捕获NullPointerException异常。

**【正例】**
场景1：
- 修复示例1：

```java
public class SomeDemo {
    private boolean doSomething(String str) {
        if (str == null) {
            return false;
        }
        String[] names = str.split(" ");
        if (names.length != 2) {
            return false;
        }
        return (isCapitalized(names[0]) && isCapitalized(names[1]));
    }

    private boolean isCapitalized(String str) {
        for (int i = 0; i < str.length(); i++) {
            if (!(str.charAt(i) >= 'A' && str.charAt(i) <= 'Z')) {
                return false;
            }
        }
        return true;
    }
}
```

**【反例】**
场景1：
- 错误示例：
```java
public class SomeDemo {
    private boolean doSomething1(String str) {
        try {
            String[] names = str.split(" ");

            if (names.length != 2) {
                return false;
            }
            return (isCapitalized(names[0]) && isCapitalized(names[1]));
            /* POTENTIAL FLAW: Do not catch NullPointerException or any of its ancestors because it cannot help locate where the exception is thrown. */
        } catch (NullPointerException e) {
            return false;
        }
    }

    private boolean doSomething2(String str) {
        if (str == null) {
            return false;
        }
        try {
            String[] names = str.split(" ");
            return (isCapitalized(names[0]) && isCapitalized(names[1]));
            /* POTENTIAL FLAW: Do not catch NullPointerException or any of its ancestors because it cannot help locate where the exception is thrown. */
        } catch (ArrayIndexOutOfBoundsException e) {
            return false;
        }
    }

    private boolean doSomething3(String str) {
        try {
            String[] names = str.split(" ");
            return (isCapitalized(names[0]) && isCapitalized(names[1]));
            /* POTENTIAL FLAW: Do not catch NullPointerException or any of its ancestors because it cannot help locate where the exception is thrown. */
        } catch (ArrayIndexOutOfBoundsException | NullPointerException e) {
            return false;
        }
    }

    private boolean isCapitalized(String str) {
        for (int i = 0; i < str.length(); i++) {
            if (!(str.charAt(i) >= 'A' && str.charAt(i) <= 'Z')) {
                return false;
            }
        }
        return true;
    }
}
```

#### G.ERR.04 防止通过异常泄露敏感信息【要求】

**【描述】**
异常信息通过日志造成敏感信息泄露。

程序抛出的异常中，可能会包含一些敏感信息，将这些异常直接记录到日志或反馈给用户，会导致敏感信息泄露风险。另外，即使异常中不含敏感信息，但是直接将异常反馈给用户，该动作本身可能就会导致敏感信息泄露风险，比如系统访问用户指定的文件路径，当该路径不存在时，系统给用户反馈一个过滤了敏感信息的异常，恶意用户可以根据系统是否抛出异常来构造文件路径，达到对系统的文件目录结构进行探测的目的。除此之外，三方件也可能会抛出携带敏感信息的异常，如 JSONException 等。

**【修改建议】**
提取异常信息的具体内容，并对敏感信息做匿名化处理后再输出到日志中。

**【正例】**
```java    
public class Exception_Sensitive_Information_into_Log {
    public void good() {
        try {
            ...
        } catch (Exception e) {
            // 对异常信息做匿名化处理
            Log.error(sensitiveInfoFilter(e));
        }
    }
}
```

**【反例】**
```java  
public class Exception_Sensitive_Information_into_Log {
    public void bad(){
      try {
          ...
      } catch (Exception e) {
          // 直接输出会打印全路径、堆栈等系统敏感信息
          Log.error(e);
      }
    }
}
```

#### G.ERR.05 方法抛出的异常，应该与本身的抽象层次相对应【要求】

**【描述】**
方法抛出异常时，应该避免直接抛出RuntimeException，更不应该直接抛出Exception或Throwable，因为这些父类异常无法与异常发生的场景相关联，直接抛出父类异常会降低代码可读性。方法抛出的异常应该与方法本身的抽象层次相对应，这些异常可以是JDK中定义的标准异常，也可以是业务层自定义的异常。另外，抛出的异常中应该包含理解该异常产生原因的所有信息。

**【修改建议】**
方法抛出的异常应该是含有明确异常产生原因的具体异常类型（非基类异常）。

**【正例】**
场景1：
- 修复示例： 

  ```java
    public class Employee {
        ...
        public String getSomeInfo() throws MyBizException{
            ...
            throw new MyBizException("xxx");
        }
        ...
    }
  ```

**【反例】**
场景1：
- 错误示例：直接抛出RuntimeException

  ```java
    public class Employee {
        ...
        public String getSomeInfo() {
            ...
            throw new RuntimeException("xxx");
        }
        ...
    }
  ```

#### G.ERR.06 在catch块中抛出新异常时，避免丢失原始异常信息【建议】

**【描述】**
丢失原始异常信息。

在catch代码块中更改异常类型时，如果只是使用原始异常中的message（ originalException.getMessage() ）或新的错误描述构造新异常，可能会导致原始异常中的有价值的信息丢失，例如异常类型、调用堆栈等信息，增加问题定位的难度。

原始异常含敏感信息时，可先对敏感信息进行匿名化处理。

**【修改建议】**
在捕获 IOException 后，异常信息记录到日志中，或基于异常构造了一个与业务代码相对应的异常。注意异常信息的清理和过滤，避免信息泄露。

**【正例】**
场景1：丢失原始异常信息。
- 修复示例1：在新抛出的异常中放入原始异常信息ex：
```java
try {
    new File("").createNewFile();
} catch (IOException ex) {
    throw new CustomException("file not found",ex);
}
```
- 修复示例2：原始异常记录日志后，再抛出新异常：
```java
try {
    new File("").createNewFile();
} catch (IOException ex) {
    LOG.error("file not found: " + ex);
    throw new CustomException("file not found");
}
```

**【反例】**
场景1：丢失原始异常信息。
- 错误示例：原始异常ex没有打印到日志中，也没有被包含在新抛出的异常中。

```java
try {
    new File("").createNewFile();
} catch (IOException ex) {
    throw new CustomException("file not found");
}
```

#### G.ERR.07 一个方法不应抛出超过5个异常，并在Javadoc的@throws标签中记录每个抛出的异常及其条件【建议】

**【描述】**
方法抛出过多的异常，会增加上层调用方法中的异常处理的工作，同时也表明方法承担了过多的职责，推荐一个方法最多抛出maxThrowNum（默认值为5，支持动态配置）类异常，包括受检异常和运行时异常。方法抛出的异常中应该避免存在继承关系，存在继承关系时，仅保留父类异常。

**【修改建议】**
方法抛出异常的类型超过maxThrowNum时，建议对方法进行合理拆分或对异常进行封装。

**【正例】**
场景1：
- 修复示例：减少throw的异常种类

  ```java
  private static byte[] getNewBytes(byte[] password, byte[] tmpByte) throws NoSuchAlgorithmException, NoSuchPaddingException { 
      ...
  }
  ```

**【反例】**
场景1：
- 错误示例：方法throw的异常种类超过5种

  ```java
  private static byte[] getNewBytes(byte[] password, byte[] tmpByte) throws NoSuchAlgorithmException, NoSuchPaddingException,         
      InvalidKeyException,InvalidAlgorithmParameterException, IllegalBlockSizeException, BadPaddingException { 
      ...
  }
  ```

#### G.ERR.08 不要使用return、break、continue或抛出异常使finally块非正常结束【要求】

**【描述】**
在finally代码块中，直接使用return、break、continue、throw语句，或由于调用方法的异常未处理，会导致finally代码块无法正常结束。非正常结束的finally代码块会影响try或catch代码块中异常的抛出，也可能会影响方法的返回值。所以要保证finally代码块正常结束。

**【修改建议】**
移除在finally块中的return、break、continue、throw语句。

**【正例】**
场景1：
- 修复示例： 

  ```java
  public int doSomething() {    
      int result = 0;
      ... 
      try {
          result = doSomethingElse();
          ... 
          return result;
      } catch (IOException ex) {
          ...
      }
      return -1;   
  }
  ```

**【反例】**
场景1：
- 错误示例：finally代码块中含有return语句

  ```java
  public int doSomething() {    
      int result = 0;
      ... 
      try {
          result = doSomethingElse();
          ... 
          return result;
      } catch (IOException ex) {
          ...
      } finally {
          return -1;
      }   
  }
  ```

#### G.ERR.09 不要调用System.exit()终止JVM【建议】

**【描述】**
不要调用System.exit()。

System.exit()会结束当前正在运行的Java虚拟机（JVM），导致拒绝服务攻击。例如，在某个web请求的处理逻辑中调用System.exit()，会导致web容器停止运行。系统中应避免无意和恶意地调用System.exit()。

**【修改建议】**
不要调用System.exit()终止JVM。

**【正例】**
场景1：调用System.exit()。
- 修复示例：程序正确运行：
```java
LOGGER.info("exit");
```

**【反例】**
场景1：调用System.exit()。
- 错误示例：调用exit函数导致结束当前正在运行的Java虚拟机。

```java
System.exit(1);
LOGGER.info("exit");
```

#### G.ERR.10 尽量消除非受检的异常，不应该在整个类上使用SuppressWarning【建议】

**【描述】**
在源代码中通过@SuppressWarning("unchecked")屏蔽告警，是个坏的实践。它丢失了类型安全和描述性的好处。

然而有些Java API，是用Object obj来存储数据对象的，当数据被取出来用时，不得不转换为用户数据对象。这时可能会有强制类型转换的告警，例如：[unchecked] unchecked method invocation。

非受检警告很重要，不要轻易忽略它们。应该始终在最小的范围内使用@SuppressWarning注解，一般是在变量声明，简短的语句或方法上。

**【修改建议】**
如果需要使用@SuppressWarning注解来抑制告警信息，@SuppressWarning注解的应用范围应该最小化，避免直接为Class、Enum添加@SuppressWarning注解。

**【正例】**
场景1：@SuppressWarning注解的范围最小化
- 修复示例： 

  ```java
    public class SuppressWarnings {

        @SuppressWarnings("uncheck")
        public void doSomething(List<String> list) {
        }
    }
  ```

**【反例】**
场景1：@SuppressWarning注解的范围最小化
- 错误示例：

  ```java
    @SuppressWarnings("uncheck")
    public class SuppressWarnings {

        public void doSomething(List<String> list) {
        }
    }
  ```

#### G.ERR.11 对于GeneralSecurityException及其子类异常应记录日志【建议】

**【描述】**
java.security.GeneralSecurityException是一个一般安全异常类，其子类定义了各种跟安全相关的异常，比如加解密操作相关异常、证书验证相关异常。当系统中抛出这些异常时，表示系统中的一些安全相关的功能出现问题或遇到一些非预期的场景。所以对于这些异常建议在日志中进行详细记录，方便后续进行问题分析定位及对系统的安全性进行优化完善。这些异常中如果含有秘钥、口令等敏感信息时，记录日志前应该对这些敏感信息进行过滤。
 java.security 中 GeneralSecurityException 的子类包括： DigestException 、 InvalidAlgorithmParameterException 、 InvalidKeyException 、 KeyException 、 KeyManagementException 、 KeyStoreException 、 NoSuchAlgorithmException 、 NoSuchProviderException 、 SignatureException 、 UnrecoverableEntryException 、 UnrecoverableKeyException 等。

**【修改建议】**
当系统中抛出GeneralSecurityException及其子类异常时，对于这些异常在日志中进行详细记录。

**【正例】**
场景1：
- 修复示例：将NoSuchAlgorithmException异常产生原因记录到日志中

```java
public static String random(int count) {
    try {
        SecureRandom RANDOM = SecureRandom.getInstanceStrong();
        StringBuilder stringBuilder = new StringBuilder();
        while (count-- > 0) {
            stringBuilder.append(RANDOM.nextInt(10));
        }
        return stringBuilder.toString();
    } catch (NoSuchAlgorithmException ex) {
        // 【GOOD】日志中进行详细记录
        LOGGER.error("No strong secure random available to generate strong AES key" + ex);
        throw new IllegalArgumentException("No strong secure random available to generate strong AES key", ex);
    }
}
```

**【反例】**
场景1：
- 错误示例：对于NoSuchAlgorithmException异常未记录日志

```java
public static String random(int count) {
    try {
        SecureRandom RANDOM = SecureRandom.getInstanceStrong();
        StringBuilder stringBuilder = new StringBuilder();
        while (count-- > 0) {
            stringBuilder.append(RANDOM.nextInt(10));
        }
        return stringBuilder.toString();
    } catch (NoSuchAlgorithmException ex) {
        // 【POTENTIAL FLAW】未对异常情况进行日志记录。
        throw new IllegalArgumentException("No strong secure random available to generate strong AES key", e);
    }
}
```
## 2.8 并发与多线程

- 优先使用Java标准库提供的高级同步机制在多线程中共享数据
- 针对线程安全性，需要进行文档说明
- 可以使用CompletableFuture编写异步任务
- `Thinking in parallel`，可以使用stream做隐式的自动并行化，替代显式的循环
- 对于锁的使用需要考虑性能损耗，必须使用锁时，尽量减少加锁范围，能锁代码块的时候不要对方法加锁，能锁对象的时候不要对类加锁
- 使用`lock.trylock()`获取锁时，要考虑是否成功获取到锁的处理逻辑
- 不推荐使用`ThreadGroup`，其中很多方法已经不被推荐使用，另外部分方法本身就非线程安全，可以使用线程池替换
- 推荐优先使用不可变对象在多线程间传递信息
- JDK中很多线程控制相关API都已经被标注为`@Deprecated`，这些方法应该被禁止使用。因为其中有些API可能会导致死锁问题。

#### P.03 使用相同的顺序请求和释放锁来避免死锁【要求】

**【描述】**
当两个不同的线程试图以相反的顺序获取两个锁时，就会发生死锁。
当程序涉及到使用多个锁对资源进行同步时，编码过程中，要仔细考虑锁的顺序，尽量以相同的顺序来请求和释放锁，避免发生死锁。不能为了避免死锁的发生，扩大锁的使用范围，影响系统性能。

**【修改建议】**
两个不同的线程需要以相同的顺序获取两个锁。

**【正例】**
相同的顺序获取两个锁。
```java
final class BankAccount implements Comparable<BankAccount> {
    private static AtomicLong nextId = new AtomicLong(0); // 下一个未使用的ID
    private double balanceAmount; // 银行账户中的总金额
    private final long id; // 每一个银行账户的id都是唯一的
    private BankAccount(double balance) {
        this.balanceAmount = balance;
        this.id = nextId.getAndIncrement();
    }
    @Override
    public int compareTo(BankAccount ba) {
        return (this.id > ba.id) ? 1 : (this.id < ba.id) ? -1 : 0;
    }
    // 将当前账户对象的存款转寄给另一个银行账号实例ba
    public void depositAmount(BankAccount ba, double amount) {
        BankAccount former;
        BankAccount latter;
        if (compareTo(ba) < 0) {
            former = this;
            latter = ba;
        } else {
            former = ba;
            latter = this;
        }
        synchronized (former) {
            synchronized (latter) {
                if (amount > balanceAmount) {
                    throw new IllegalArgumentException("XXX...");
                }
                ba.balanceAmount += amount;
                this.balanceAmount -= amount;
            }
        }
    }
    public static void initiateTransfer(BankAccount first, BankAccount second, double amount) {
        Thread transfer = new Thread(new Runnable() {
            @Override
            public void run() {
                first.depositAmount(second, amount);
            }
        });
        transfer.start();
    }
}
```

**【反例】**
不同顺序获取两个锁。
```java
final class BankAccount {
    private double balanceAmount; // 银行账户中的总金额
    BankAccount(double balance) {
        this.balanceAmount = balance;
    }
    // 将当前账户对象的存款转寄给另一个银行账号实例ba
    private void depositAmount(BankAccount ba, double amount) {
        synchronized (this) {
            synchronized (ba) {
                if (amount > balanceAmount) {
                    throw new IllegalArgumentException("Transfer cannot be completed");
                }
                ba.balanceAmount += amount;
                this.balanceAmount -= amount;
            }
        }
    }
    public static void initiateTransfer(BankAccount first, BankAccount second, double amount) {
        Thread transfer = new Thread(new Runnable() {
            public void run() {
              first.depositAmount(second, amount);
            }
        });
        transfer.start();
    }
    public static void main(String[] args) {
        BankAccount bankA = new BankAccount(15000);
        BankAccount bankB = new BankAccount(9000);
        initiateTransfer(bankA, bankB, 500);
        initiateTransfer(bankB, bankA, 1400);
        ...
    }
}
```

#### G.CON.01 对共享变量做同步访问控制时需避开同步陷阱【要求】

**【描述】**
避免使用class类对象作为锁传递给synchronized。

如果使用class类对象作为同步对象，父子类继承关系增加了class类对象归属的复杂度，开发人员容易犯错，导致同步行为不符合预期；故应避免使用class这类容易造成歧义的对象，而应使用明确的对象。

**【修改建议】**
禁止基于getClass()返回的类对象进行同步。

**【正例】**
场景1：错误使用getClass()对象
- 修复示例：使用明确Class对象作为锁

```java
class Base {
    static DateFormat format = DateFormat.getDateInstance(DateFormat.MEDIUM);

    public Date parse(String str) throws ParseException {
        try {
            synchronized (Class.forName("Base")) {
                return format.parse(str);
            }
        }
        catch (ClassNotFoundException x) {
            // "Base" not found; handle error
        }
        return null;
    }
}

class Derived extends Base {
    public Date doSomethingAndParse(String str) throws ParseException {
        synchronized (Base.class) {
            ...
            return format.parse(str);
        }
    }
}
```

**【反例】**
场景1：错误使用getClass()对象
- 错误示例：基于getClass()返回的类对象进行同步。

```java
class Base {
    static DateFormat format = DateFormat.getDateInstance(DateFormat.MEDIUM);

    public Date parse(String str) throws ParseException {
        synchronized (getClass()) {
            return format.parse(str);
        }
    }
}

class Derived extends Base {
    public Date doSomethingAndParse(String str) throws ParseException {
        synchronized (Base.class) {
            ...
            return format.parse(str);
        }
    }
}
```

**【描述】**
避免使用 Lock或Condition实现类(高级并发类) 对象本身 作为锁传递给synchronized。

使用了基于高级并发对象的synchronized块。高级并发类是指实现java.util.concurrent.locks包中的Lock或Condition接口的类，其本身提供了lock与unlock来实现同步，不应将这些类的对象作为synchronized块的同步对象使用。当使用基于高层并发对象的synchronized块时，容易被误认为这种方式与正常使用lock接口的方式是同一个锁，而实际是两个不同的锁，会导致无法实现同步控制。

**【修改建议】**
使用Lock接口提供的lock()和unlock()方法。

**【正例】**
场景1：并发对象
- 修复示例1：updateResource() 和 doSomething() 方法中使用了Lock接口提供的lock()和unlock()方法。
```java
public class SomeSharedResource {
    private final Lock lock = new ReentrantLock();
    public void updateResource() {
        lock.lock();
        try {

            // 更新共享的资源
            ...
        } finally {
            lock.unlock();
        }
    }
    public void doSomething() {
        lock.lock();
        try {

            // 更新共享的资源
            ...
        } finally {
            lock.unlock();
        }
    }
}
```

**【反例】**
场景1：并发对象
- 错误示例：updateResource() 和 doSomething() 方法中使用不是同一个锁。

```java
public class SomeSharedResource {
    private final Lock lock = new ReentrantLock();
    public void updateResource() {
        // 【POTENTIAL FLAW】 
        synchronized (lock) {

            // 更新共享的资源
            ...
        }
    }
    public void doSomething() {
        lock.lock();
        try {

            // 更新共享的资源
            ...
        } finally {
            lock.unlock();
        }
    }
}
```

**【描述】**
禁止使用一个实例锁来同步静态共享数据。

实例锁的同步效果仅限于此实例本身，无法用来同步静态共享变量；如果试图使用实例锁来同步静态共享变量，在多实例情况下无法实现符合预期的同步效果。

**【修改建议】**
禁止使用一个实例锁来同步静态共享数据。

**【正例】**
场景1：同步块
- 修复示例：使用静态锁来同步静态共享变量。
```java
public class SomeSharedResource {
    private static volatile int counter;
    private static final Object lock = new Object();
    public void updateResource() {
        synchronized (lock) {
            counter++;
        }
    }
}
```
场景2：同步方法
- 修复示例1：同步静态方法访问静态资源
```java
public class SomeSharedResource {
    private static volatile int counter;

    public static synchronized void updateResource() {
        counter++;
    }
}
```

**【反例】**
场景1：同步块
- 错误示例：使用实例锁来同步静态共享变量。

```java
public class SomeSharedResource {
    private static volatile int counter;

    // 【POTENTIAL FLAW】 非静态
    private final Object lock = new Object();
    public void updateResource() {
        synchronized (lock) {
            counter++;
        }
    }
}
```
场景2：同步方法
- 错误示例：同步非静态方法中访问静态资源

```java
public class SomeSharedResource {
    private static volatile int counter;

    // 【POTENTIAL FLAW】 同步方法
    public synchronized void updateResource() {
        counter++;
    }
}
```

#### G.CON.02 在异常条件下，保证释放已持有的锁【要求】

**【描述】**
锁对象如果不能正确释放，可能会导致阻塞或死锁问题。为了保证锁被正确释放，建议在finally中释放锁。

对于加锁操作应在try代码块外部实现，避免因为加锁操作出现异常导致加锁失败，进而导致在finally中释放锁时发生异常。

**【修改建议】**
释放锁操作在finally代码块中实现。

**【正例】**
场景1：加锁期间抛出受检异常
- 修复示例：

```java
public final class Foo {
    private final Lock lock = new ReentrantLock();

    public void correctReleaseLock() {
        lock.lock();
        try {
            doSomething();
        } catch (MyBizException ex) {
            ... // 处理异常
        } finally {
            lock.unlock();
        }
    }

    private void doSomething() throws MyBizException {
        ...
    }
}
```
场景2：加锁期间可能抛出运行时异常
- 修复示例：

```java
final class Foo {
    private final Lock lock = new ReentrantLock();

    public void correctReleaseLock(String value) {
        lock.lock();
        try {
            ...
            int index = Integer.parseInt(value);
            ...
        } finally {
            lock.unlock();
        }
    }
}
```

**【反例】**
场景1：加锁期间抛出受检异常
- 错误示例：

```java
public final class Foo {
    private final Lock lock = new ReentrantLock();

    public void incorrectReleaseLock() {
        try {
            lock.lock();
            doSomething();
            lock.unlock();
        } catch (MyBizException ex) {
            ... // 处理异常
        }
    }

    private void doSomething() throws MyBizException {
        ...
    }
}
```
场景2：加锁期间可能抛出运行时异常
- 错误示例：

```java
final class Foo {
    private final Lock lock = new ReentrantLock();

    public void incorrectReleaseLock(String value) {
        lock.lock();
        ...
        int index = Integer.parseInt(value);
        ...
        lock.unlock();
    }
}
```

#### G.CON.03 避免在持有锁时执行耗时或阻塞性的操作【建议】

**【描述】**
持有锁时执行耗时或阻塞性操作会严重降低系统性能，且可能导致线程饥饿。此外可能会导致依赖本线程的其它线程无限期阻塞。阻塞性操作包括网络、文件、控制台I/O和对象序列化等，线程无限期的等待也属于阻塞性的操作。
加锁期间执行Sleep()操作，锁并不会释放，但是会让出CPU，这是一种非常低效的操作：当前线程在无有效业务操作期间持有锁资源，导致其他线程阻塞。

**【修改建议】**
程序应该避免在持有锁的时候执行阻塞性的操作，加锁代码块内不要执行Sleep()操作。

**【正例】**
场景1：不调用可能导致线程阻塞的方法
- 修复示例1：
```java
public void doSomething() {
    Thread thread = new Thread(new MyDemo());
    thread.start();
    lock.lock();
    try {
        doSomethingElse();
    } catch (InterruptedException e) {
        ...
    } finally {
        lock.unlock();
    }
}
```

- 修复示例2：
```java
private List<Message> messageBuff = new ArrayList<>();
public void good(Socket socket, String targetUid) throws IOException {
    List<Message> candidateMessage = getCandidateMessage(targetUid);
    if (!candidateMessage.isEmpty()) {
        writeMessageToStream(socket, candidateMessage);
    }
}
public List<Message> getCandidateMessage(String targetUid) {
    List<Message> candidates = new ArrayList<>();
    synchronized (messageBuff){
        Iterator<Message> iterator = messageBuff.iterator();
        while (iterator.hasNext()) {
            Message msg = iterator.next();
            if (msg.getTargetUid().equals(targetUid)) {
                candidates.add(msg);
            }
            iterator.remove();
        }
    }
    return candidates;
}
public void writeMessageToStream(Socket socket, List<Message> messages) throws IOException {
    try (ObjectOutputStream out = new ObjectOutputStream(socket.getOutputStream())) {
        for (Message message : messages) {
            out.writeObject(message);
        }
    }
}
```

#### G.CON.04 避免使用不正确形式的双重检查锁【要求】

**【描述】**
不正确的使用双重检查锁。

双重检查锁（double-checked locking）是一种软件设计模式，通常用于延迟初始化单例。主要通过在进行获取锁之前先检查单例对象是否创建（第一次检查），在获取锁以后，再次检查对象是否创建（第二次检查），以此减少并发获取锁的开销。

但是不正确的使用双重检查锁，存在延迟初始化的Java优化问题隐患。也就是会导致一个线程发布一个未初始化或部分初始化的对象给另外的线程使用。

**【修改建议】**
把instance声明为volatile，当一个线程初始化Singleton对象时，会在这个线程和其他任何获取该实例的线程之间建立起happens-before关系，避免使用到未初始化完全的对象引用。

**【正例】**
场景1：双重检测同步延迟加载。
- 修复示例：

```java
final class Singleton {
    // 使用 volatile 修饰，保证不同线程对这个变量进行操作时的可见性，并禁止进行指令重排序。
    private static volatile Singleton instance = null;
    private static final Object LOCK = new Object();

    private Singleton() {
        ...
    }

    public static Singleton getSingletonInstance() {
        if (instance == null) {
            synchronized (LOCK) {
                if (instance == null) {
                    instance = new Singleton();
                }
            }
        }
        return instance;
    }
}
```

**【反例】**
场景1：双重检测同步延迟加载。
- 错误示例：

```java
final class Singleton {
    private static Singleton instance = null;
    private static final Object LOCK = new Object();

    private Singleton() {
        ...
    }

    public static Singleton getSingletonInstance() {
        if (instance == null) {
            synchronized (LOCK) {
                if (instance == null) {
                    instance = new Singleton();
                }
            }
        }
        return instance;
    }
}
```

#### G.CON.05 禁止使用非线程安全的方法来覆写线程安全的方法【要求】

**【描述】**
使用非线程安全的方法来重写线程安全的方法。

对于线程安全的方法，如果子类将其重写为非线程安全的方法，可能会导致不正确的同步，导致难以定位的问题产生。

**【修改建议】**
如果某个子方法的父方法声明为synchronized，则必须将该子方法也声明为synchronized或者用私有常量锁锁定。

**【正例】**
场景1：同步方法。
- 修复示例：

```java
class SeniorClass {
    public synchronized void doSomething() {
        ...
    }
}

class JuniorClass extends SeniorClass {
    @Override
    public synchronized void doSomething() { // 保持与父类一致。
        ...
    }
}
```

**【反例】**
场景1：同步方法。
- 错误示例：

```java
class SeniorClass {
    public synchronized void doSomething() {
        ...
    }
}

class JuniorClass extends SeniorClass {
    @Override
    public void doSomething() { // doSomething()在被子类覆写时，改为了非线程安全的方法。
        ...
    }
}
```

#### G.CON.06 使用新并发工具代替wait()和notify()【要求】

**【描述】**
Java 5开始提供了更高级的并发工具，这些工具可以有效替代wait()和notify()。新开发的代码应该优先使用这些并发工具。

这些高级的并发工具主要位于java.util.concurrent中，包括：

Executor Framework：可参考G.CON.12 避免不加控制地创建新线程，应该使用线程池来管控资源;
并发集合（Concurrent Collection）：提供了高性能的并发实现的集合接口，在其内部实现了同步管理，不需要额外加锁，常用的并发集合包括ConcurrentHashMap、ConcurrentSkipListSet、ConcurrentLinkedQueue等；
同步器（Synchronizer）：为每种特定的同步需求提供了解决方案，常用的同步器包括Phaser、CountDownLatch、Semaphore等。

**【修改建议】**
新开发的代码应避免使用wait()和notify()方法。

**【正例】**
场景1：
- 修复示例： 

  ```java
    public class ProducerConsumerExample {
        private static final Lock lock = new ReentrantLock();
        private static final Condition product = lock.newCondition();
        private static final Condition consume = lock.newCondition();

        public static void main(String[] args) {
            LinkedList<Integer> buffer = new LinkedList<>();
            int maxSize = 10;
            Thread producer = new Thread(new Producer(buffer, maxSize));
            Thread consumer = new Thread(new Consumer(buffer));
            producer.start();
            consumer.start();
        }

        static class Producer implements Runnable {
            private LinkedList<Integer> buffer;
            private int maxSize;

            public Producer(LinkedList<Integer> buffer, int maxSize) {
                this.buffer = buffer;
                this.maxSize = maxSize;
            }

            public void run() {
                int num = 0;
                while (true) {
                    try {
                        lock.lock();
                        while (buffer.size() == maxSize) {
                            try {
                                product.await();
                            } catch (InterruptedException e) {
                                e.printStackTrace();
                            }
                        }
                        buffer.add(num++);
                        System.out.println("Produced: " + num);
                        try {
                            Thread.sleep(1000);
                        } catch (InterruptedException e) {
                            e.printStackTrace();
                        }
                        consume.signal();
                    } finally {
                        lock.unlock();
                    }
                }
            }
        }

        static class Consumer implements Runnable {
            private final LinkedList<Integer> buffer;

            public Consumer(LinkedList<Integer> buffer) {
                this.buffer = buffer;
            }

            public void run() {
                while (true) {
                    try {
                        lock.lock();
                        while (buffer.isEmpty()) {
                            try {
                                consume.await();
                            } catch (InterruptedException e) {
                                e.printStackTrace();
                            }
                        }
                        int num = buffer.removeFirst();
                        System.out.println("Consumed: " + num);
                        try {
                            Thread.sleep(1000);
                        } catch (InterruptedException e) {
                            e.printStackTrace();
                        }
                        product.signal();
                    } finally {
                        lock.unlock();
                    }
                }
            }
        }
    }
  ```

**【反例】**
场景1：
- 错误示例：

  ```java
    public class ProducerConsumerExample {
        public static void main(String[] args) {
            LinkedList<Integer> buffer = new LinkedList<>();
            int maxSize = 10;
            Thread producer = new Thread(new Producer(buffer, maxSize));
            Thread consumer = new Thread(new Consumer(buffer));
            producer.start();
            consumer.start();
        }

        static class Consumer implements Runnable {
            private final LinkedList<Integer> buffer;

            public Consumer(LinkedList<Integer> buffer) {
                this.buffer = buffer;
            }

            public void run() {
                while (true) {
                    synchronized (buffer) {
                        while (buffer.isEmpty()) {
                            try {
                                buffer.wait();
                            } catch (InterruptedException e) {
                                e.printStackTrace();
                            }
                        }
                        int num = buffer.removeFirst();
                        System.out.println("Consumed: " + num);
                        buffer.notifyAll();
                    }
                }
            }
        }

        static class Producer implements Runnable {
            private LinkedList<Integer> buffer;
            private int maxSize;

            public Producer(LinkedList<Integer> buffer, int maxSize) {
                this.buffer = buffer;
                this.maxSize = maxSize;
            }

            public void run() {
                int num = 0;
                while (true) {
                    synchronized (buffer) {
                        while (buffer.size() == maxSize) {
                            try {
                                buffer.wait();
                            } catch (InterruptedException e) {

                            }
                        }
                        buffer.add(num++);
                        System.out.println("Produced: " + num);
                        try {
                            Thread.sleep(1000);
                        } catch (InterruptedException e) {
                            e.printStackTrace();
                        }
                        buffer.notifyAll();
                    }
                }
            }
        }
    }
  ```

#### G.CON.07 创建新线程时必须指定线程名【要求】

**【描述】**
指定线程名可以给问题定位带来很多方便。日志或者dump文件中会包含线程的名字，但缺省的线程名Thread-n无法区分出是哪个线程，不便于问题定位。

**【修改建议】**
创建线程时为线程指定具体的名称。

**【正例】**
场景1：
- 修复示例： 

  ```java
    Thread t1 = new Thread();
    t1.setName("xxx");
    t1.start();

    Thread t2 = new Thread();
    t2.setName("xxx");
    t2.start();
  ```

**【反例】**
场景1：
- 错误示例：

  ```java
    Thread t1 = new Thread();
    t1.start(); // 没有指定线程名

    Thread t2 = new Thread();
    t2.start();
    t2.setName("xxx"); // 线程启动后再指定线程名无效
  ```

#### G.CON.08 使用Thread对象的setUncaughtExceptionHandler方法注册未捕获异常处理者【要求】

**【描述】**
Java多线程程序中，所有线程都不允许抛出未捕获的checked exception，也就是说各个线程需要自己把自己的checked exception处理掉。但是无法避免未捕获的RuntimeException。当子线程抛出异常时，子线程会结束，但主线程不会知道，因为主线程通过try-catch是无法捕获子线程异常的。

Thread对象提供了setUncaughtExceptionHandler方法用来获取线程中产生的异常。还可以使用Thread.setDefaultUncaughtExceptionHandler，为所有线程设置默认异常处理方法。

应注意的是，在执行周期性任务例如ScheduledExecutorService时，为了程序的健壮性，可考虑在提交的Runnable的run方法内捕获高层级的异常。

ScheduledExecutorService的各种schedule方法，可以通过其返回的ScheduledFuture对象获取其异常。

**【修改建议】**
创建线程时设置异常处理方法，保证线程抛出的异常可以被正确处理。

**【正例】**
场景1：
- 修复示例： 

  ```java
    public class TestUncaughtException {
        public static void main(String[] args) {
            TestThread thread = new TestThread("meaningful-name");
            thread.setUncaughtExceptionHandler(new Thread.UncaughtExceptionHandler() {
                @Override
                public void uncaughtException(Thread tr, Throwable ex) {
                    System.out.println(tr.getName() + " : " + ex.getMessage());
                }
            });
            thread.start();
        }
        public static class TestThread extends Thread {
            public TestThread(String name) {
                super.setName(name);
            }

            @Override
            public void run() {
                ...
                throw new RuntimeException("just a test");
            }
        }
    }
  ```

**【反例】**
场景1：
- 错误示例：

  ```java
    public class TestUncaughtException {
        public static void main(String[] args) {
            TestThread thread = new TestThread("meaningful-name");
            thread.start();
        }
        public static class TestThread extends Thread {
            public TestThread(String name) {
                super.setName(name);
            }

            @Override
            public void run() {
                ...
                throw new RuntimeException("just a test");
            }
        }
    }
  ```

#### G.CON.09 不要依赖线程调度器、线程优先级和yield()方法【要求】

**【描述】**
Java中的线程调度，是基于操作系统以及JVM的实现，在不同的操作系统中，或者不同厂商的JVM中，即使是同一套代码，其多线程的调度机制也是不一样的。因此，在多线程的程序中，不要依赖于操作系统的线程调度器来决定程序的工作逻辑，如果程序依赖于线程调度器来达到正确性或者性能要求，会导致不可移植

线程的优先级是高度依赖于系统的，当虚拟机依赖于系统的线程实现机制时，Java线程的优先级会被映射到系统的线程优先级上，Java线程优先级的数量会发生变化，甚至会被忽略，所以程序功能的正确性不能依赖于线程的优先级

而`Thread.yield()`对线程调度器仅仅是个提示，不保证确定的效果，因此代码也不能依赖`Thread.yield()`方法。

#### G.CON.10 线程中断由业务代码来协作完成，慎用Thread.interrupt方法【建议】

**【描述】**
线程中断由业务代码来协作完成，__慎用Thread.interrupt方法，它依赖执行线程对interrupted status的处理逻辑__。在使用Thread.interrupt()方法请求目标线程中止时，仅仅是在目标线程上将interrupted status标记为true，目标线程本身需用Thread.interrupted()方法检查该标记，当状态为true时，应主动执行清理，并抛出InterruptedException。

在编写需要中止的多线程程序时，必须选用能够响应interrupt的标准库或第三方库。Java标准库中的会阻塞的方法（如Thread.sleep()或者SocketChannel.write()）一般会在interrupt之后抛出InterruptedException。但有些方法则不理会interrupt，如Socket.write()，必须回避这些方法。

**【修改建议】**
1、优先使用协作式的线程同步机制来通知一个线程中止作业，如java.util.concurrent包中的各种synchronizer，加锁的共享变量、volatile共享变量等。

2、如果需要一个线程让另一个线程中止执行，Java API推荐的方式是，让被中止的线程在运行中周期性地查询自己是否被中止。如果发现自己被中止，则应该主动清理状态并中止执行，而不是忽略请求继续执行。

**【正例】**
场景1：
- 修复示例： 

```java
public static void main(String[] args) {    
    Thread thread = new MyThread();
    thread.start();
    ...
    thread.requestStop(); // 【GOOD】使用通知变量机制来控制线程的终止
}

class MyThread extends Thread {
    private volatile boolean hasStopRequested;

    public void requestStop() {
        hasStopRequested = true;
    }

    @Override
    public void run() {
        while (!hasStopRequested) {
            doSomething();
        }
    }
}
```

**【反例】**
场景1：
- 错误示例：

```java
public static void main(String[] args) {    
    Thread thread = new MyThread();
    thread.start();
    ...
    thread.interrupt(); // 【POTENTIAL FLAW】预期使用interrupt机制终止线程，但线程无法被正确终止
}

class MyThread extends Thread {
    ...
    public void run() {
        boolean running = true;
        while (running) {
            try {
                doSomething();
            } catch (InterruptedException ex) {
                running = false;
            }
        }
    }
}
```

#### G.CON.11 禁止使用Thread.stop()来终止线程【要求】

**【描述】**
禁止调用Thread.stop()。

Thread.stop()已经被标记为@Deprecated，该方法是不安全的，调用Thread.stop()来终止线程会使其释放它所持有的所有锁，可能会导致这些锁保护的对象处于不一致的状态。

**【修改建议】**
禁止调用Thread.stop()。

**【正例】**
场景1：
- 修复示例：设置线程结束标志，在线程中迭代检查该标志来结束线程

```java
public final class Foo implements Runnable {
    private volatile boolean shouldAbort = false;

    public void stop() {
        shouldAbort = true;
    }

    @Override
    public void run() {
        ...
        while (!shouldAbort) {
           ...
        }
    }

    public static void main(String[] args){
        Foo foo = new Foo();
        Thread thread = new Thread(foo);
        thread.start();
        ...
        foo.stop(); // 此处使用 foo 对象终止线程
    }
}
```

**【反例】**
场景1：
- 错误示例：使用`Thread.stop()`终止线程

```java
public final class Foo implements Runnable {
    private volatile boolean shouldAbort = false;

    public void stop() {
        shouldAbort = true;
    }

    @Override
    public void run() {
        ...
        while (!shouldAbort) {
           ...
        }
    }

    public static void main(String[] args){
        Foo foo = new Foo();
        Thread thread = new Thread(foo);
        thread.start();
        ...
        thread.stop(); // 禁止使用Thread.stop()来终止线程
    }
}

```

#### G.CON.12 避免不加控制地创建新线程，应该使用线程池来管控资源【建议】

**【描述】**
Java虚拟机能够管理的线程数量有限，不加控制的创建新线程可能会导致Java虚拟机崩溃。

推荐使用Java 5之后提供的线程池ThreadPoolExecutor来管理线程资源，这样可以更加明确线程池的运行规则，避免资源耗尽的风险。另外，线程池要合理规划，避免任意重复创建。

不推荐使用Executors创建线程池，因为存在以下问题：

1）Executors.newFixedThreadPool()和Executors.newSingleThreadExecutor()允许请求队列的最大长度为Integer.MAX_VALUE，可能会因为堆积大量的请求导致OOM。

2）Executors.newCachedThreadPool()允许创建线程的最大数量为Integer.MAX_VALUE，可能会因为创建大量的线程导致OOM。Executors.newScheduledThreadPool()会自动增长工作队列大小。Executors.newWorkStealingPool()实际的工作窃取线程数量会动态地增减。

**【修改建议】**
避免单独创建线程，尽量使用线程池来复用线程。线程池的从创建推荐使用ThreadPoolExecutor。

**【正例】**
场景1：
- 修复示例： 使用线程池机制

  ```java
    private BlockingQueue blockingQueue = new LinkedBlockingQueue(100);
    private ThreadPoolExecutor threadPool = new ThreadPoolExecutor(2, 64, 60L,
        TimeUnit.SECONDS, blockingQueue,
        new SelfThreadFactory("ProductName", "ThreadName", false),
        new DiscardOldestPolicy(LOGGER, "ThreadName"));
    public void processEntity2(List<Entity> items) {
        for (Entity entity : items) {
            threadPool.execute(new EntityProcessor(entity));
        }
    }
  ```

**【反例】**
场景1：
- 错误示例1：单独创建线程

  ```java
    public void processEntity(List<Entity> items) {        
        ...       
        new Thread(new EntityProcessor(entity)).start();
        ...       
    }
  ```
- 错误示例2：在循环中创建多个线程

  ```java
    public void processEntity(List<Entity> items) {
        for (Entity entity : items) {
            new Thread(new EntityProcessor(entity)).start();
        }
    }
  ```

#### G.CON.13 线程池中的任务结束后必须清理其自定义的ThreadLocal变量【要求】

**【描述】**
线程池中的任务结束后必须清理其自定义的ThreadLocal变量。

ThreadLocal基于弱引用实现，如果线程栈随着线程一起被JVM回收，ThreadLocal中存放的值也会在之后的GC被回收。而线程池技术则会重复使用线程以减少线程创建开销。这种线程的复用，导致ThreadLocal变量的使用存在以下两类问题：

1.脏数据问题：当前任务未正确初始化ThreadLocal变量，导致ThreadLocal变量取到该线程之前执行的某一个任务中设置的未清除的值；  
2.内存泄露问题：任务中没有手动清理ThreadLocal中存放的值，且该线程池中的核心线程持有了ThreadLocal的引用，使得ThreadLocal中的值对象不会被JVM主动释放，最终造成这一片内存无法被回收从而导致内存泄露。

**【修改建议】**
线程结束后必须调用ThreadLocal变量的remove方法。

**【正例】**
场景1：
- 修复示例：线程池中线程在finaly代码块中对ThreadLoacl变量进行清理
```java
class TestThreadLocalTask implements Runnable {
    private static ThreadLocal<Integer> localValue = new ThreadLocal<>();

    @Override
    public void run() {
        localValue.set(STATE1);
        try {
            ...
            localValue.set(STATE3);
            doSomething(localValue.get());
            ...
        } finally {
            localValue.remove(); // 【GOOD】需要执行remove方法清理线程局部变量
        }
    }
}
```

**【反例】**
场景1：
- 错误示例：线程池中线程对于ThreadLoacl变量使用结束后未清理

```java
public class TestThreadLocal {
    public static void main(String[] args) {
        ThreadPoolExecutor pool = new ThreadPoolExecutor(1, 2, 100,
            TimeUnit.MILLISECONDS, new LinkedBlockingQueue<Runnable>(),
            Executors.defaultThreadFactory(), new ThreadPoolExecutor.CallerRunsPolicy());
        for (int i = 0; i < 20; i++) {
            pool.execute(new TestThreadLocalTask());
        }
    }
}

class TestThreadLocalTask implements Runnable {
    private static ThreadLocal<Integer> localValue = new ThreadLocal<>();

    @Override
    public void run() {
        localValue.set(STATE1);
        try {
            ...
            doSomething(localValue.get());
            ...
        } catch(MyBizException ex){ 
        ...
        }
        // 【POTENTIAL FLAW】 ThreadLocal变量未清理
    }
}
```


**【反例】**
场景1：避免在持有锁时调用阻塞性的函数。
- 错误示例1：

```java
public void doSomething() {
    Thread thread = new Thread(new MyDemo());
    thread.start();
    lock.lock();
    try {
        // 【POTENTIAL FLAW】 线程的sleep方法属于阻塞操作
        Thread.sleep(10000);
    } catch (InterruptedException e) {
        ...
    } finally {
        lock.unlock();
    }
}
```

- 错误示例2：

```java
private List<Message> messageBuff = new ArrayList<>();
public void bad(Socket socket, String targetUid) throws IOException {
    try (ObjectOutputStream out = new ObjectOutputStream(socket.getOutputStream())) {
        synchronized(messageBuff){
            Iterator<Message> iterator = messageBuff.iterator();
            while (iterator.hasNext()) {
                Message message = iterator.next();
                if (message.getTargetUid().equals(targetUid)) {
                    // 【POTENTIAL FLAW】 持有锁时执行耗时或有阻碍性的操作
                    out.writeObject(message);
                    iterator.remove();
                }
            }
        }
    }
}
```

## 2.9 泛型和集合

#### G.COL.01 方法的设计可以优先考虑泛型【建议】

**【描述】**
使用泛型的优点包括：可以使代码更简洁，最大限度的重用代码，保护类型的安全，消除强制类型转换，如果可以尽量使用泛型方法
静态方法如果要使用泛型，由于静态方法无法访问类上定义的泛型，必须将静态方法定义成泛型方法。如果方法有3个以上对类型的instanceof判断分类处理，也可以考虑使用泛型。

**【正例】**
泛型方法就像泛型一样，使用起来比要求客户端转换输入参数并通过返回值返回的方式更加安全
```java
public static <E> List<E> uion (List<E> List1, List<E> List2) {
    List<E> resultList = new ArrayList<>(list1.size() + list2.size());
    resultList.addAll(list1);
    resultList.addAll(list2);
    return resultList;
}
```

#### G.COL.02 优先使用泛型集合，而不是数组【建议】

**【描述】**
泛型是不可变的，数组是协变的。当向数组中添加类型不匹配的元素时，在运行期才会发生错误，而对于集合，在编译期就会报错。另外，由于类型不安全无法创建泛型数组。

泛型与数组不能很好地混合使用，如果需要使用一个“泛型化的数组”，更好地选择是使用集合。

**【修改建议】**
相对于数组，推荐优先使用泛型集合。

**【正例】**
场景1：
- 修复示例： 

  ```java
    private final List<T> lists; // 泛型列表
    private final List<String> longs; // 具体化的列表

    List<Object> objectList = new ArrayList<String>(DEFAULT_CAPACITY); // 不兼容类型，编译报错
    objectList.add("test value");
  ```

**【反例】**
场景1：
- 错误示例：

  ```java
    private final T[] someArray; // 泛型数组，不建议
    private final Object[] objArray; // 协变化的数组声明，不建议

    Object[] objectArray = new Integer[10]; // 协变化的数组初始化，不建议
    objectArray[0] = "test value"; // 运行时抛出ArrayStoreException
  ```

#### G.COL.03 声明一个泛型类通过限定符限制可用的泛型类型【建议】

**【描述】**
Java的泛型可以按PECS(Producer Extends, Consumer Super)原则来设计上界和下界类型，声明一个带泛型的类或接口的时候，建议限制可以用的泛型类型，避免接口使用者乱用

`<? extends T>`实现了泛型的协变，表现在泛型的集合中，适合从集合中读取元素，不能添加元素
`<? super T>`实现了泛型的逆变，表现在泛型的集合中，适合从集合中添加元素，不适合读取元素

`Collections`的`public static <T> void copy(List<? super T> dest, List<? extends T> src)`是一个典型的使用场景

#### G.COL.04 不要在foreach循环中通过remove()/add()方法更改集合【要求】

**【描述】**
java.util.concurrent包之外的（非concurrent）集合在foreach循环中不要更改，否则可能会导致ConcurrentModificationException。当需要遍历集合并删除部分元素时，可采用removeIf()方法或Iterator的remove()方法。个别集合（例如CopyOnWriteArrayList）的Iterator中remove()方法会抛出UnsupportedOperationException。

**【修改建议】**
在遍历集合中的元素时，如果需要对集合进行更改，应该使用迭代器。

**【正例】**
场景1：
- 修复示例： 

  ```java
  // 使用Java 8 Collection中的removeIf方法
  list.removeIf(item -> shouldDelete(item));

  // 使用Iterator删除元素
  Iterator<String> iterator = list.iterator();
  while (iterator.hasNext()) {
      String item = iterator.next();
      if (shouldDelete(item)) {
          iterator.remove();
      }
  }
  ```

## 2.10 输入和输出

#### G.FIO.01 使用外部数据构造的文件路径前必须进行校验，校验前必须对文件路径进行规范化处理【要求】

**【描述】**
使用外部数据构造的文件路径。

文件路径来自外部数据时，必须对其合法性进行校验，否则可能会产生路径遍历（Path Traversal）漏洞。

文件路径有多种表现形式，如绝对路径、相对路径，路径中可能会含各种链接、快捷方式、影子文件等，这些都会对文件路径的校验产生影响，所以在文件路径校验前要对文件路径进行规范化处理，使用规范化的文件路径进行校验。对文件路径的规范化处理必须使用getCanonicalPath() ，禁止使用getAbsolutePath() （该方法无法保证在所有的平台上对文件路径进行正确的规范化处理）。

**【修改建议】**
对外部数据进行白名单校验。

**【正例】**
场景1：使用外部数据构造文件路径
- 修复示例1：对外部构造的文件路径先规范化，在进行校验
```java
public void doSomething() {
    File file = new File(HOME_PATH, fileName);
    try {
        String canonicalPath = file.getCanonicalPath();
        if (!validatePath(canonicalPath)) {
            throw new IllegalArgumentException("Path Traversal vulnerability!");
        }
        ... // 对文件进行读写等操作
    } catch (IOException ex) {
        throw new IllegalArgumentException("An exception occurred ...", ex);
    }
}
private boolean validatePath(String path) {
    return path.startsWith(HOME_PATH);
}
```

- 修复示例2：按业务场景，自定义实现文件路径校验逻辑
```java
public void doSomething() throws IOException {
    fileName = request.getParameter("filename");
    ...
    if (FileConfig.filePathIsValid(fileName)) {
        File file = new File(fileName);
        ...
    }
}

public class FileConfig {
    public static boolean filePathIsValid(String filePath) throws UnsupportedEncodingException {
        if (filePath != null && !filePath.equals("")) {
            if (filePath.contains("%")) {
                filePath = filePath.replaceAll("%(?![0-9a-fA-F]{2})", "%25");
            }

            filePath = URLDecoder.decode(filePath, "utf-8");
            return !filePath.contains("..") && !filePath.contains("./") && !filePath.contains(".\\\\") && !filePath.contains("%00");
        } else {
            return true;
        }
    }
}
```

**【反例】**
场景1：使用外部数据构造文件路径
- 错误示例：对使用外部数据构造的文件路径，校验前未进行规范化处理（恶意用户可利用../构造访问HOME_PATH之外的路径）。
```java
public void doSomething() {
    fileName = request.getParameter("filename");
    ...
    File file = new File(HOME_PATH, fileName);
    String path = file.getPath();

// 【POTENTIAL FLAW】 使用非规范化的路径进行校验
    if (!validatePath(path)) {
        throw new IllegalArgumentException("Path Traversal vulnerabilities may exist！");
    }
    ... // 对文件进行读写等操作
}
private boolean validatePath(String path) {
    return path.startsWith(HOME_PATH);
}
```

#### G.FIO.02 从ZipInputStream中解压文件必须进行安全检查【要求】

**【描述】**
使用ZipEntry.getSize()进行解压尺寸大小的检查。

使用java.util.zip.ZipInputStream 解压zip文件时，可能会有两类安全风险：
1. 将文件解压到目标目录之外
   压缩包中的文件名中如果包含.. ，可能导致文件被解压到目标目录之外，造成任意文件注入、文件恶意篡改等风险。因此，压缩包中的文件在解压前，要先对解压的目标路径进行校验，如果解压目标路径不在预期目录之内，要么拒绝将其解压出来，要么将其解压到一个安全的位置。
2. 解压的文件消耗过多的系统资源
   zip压缩算法可能有很大的压缩比，可以把超大文件压缩成很小的zip文件（例如可以将上G的文件压缩为几K大小），这样的文件解压可能会导致zip炸弹（zip bomb）攻击。所以zip文件解压时，要对解压的实际文件大小进行检查，若解压之后的文件大小超过一定的限制，必须拒绝解压。具体的大小限制根据实际情况来确定。除此之外，解压时，还需要对解压出来的文件数量进行限制，防止zip压缩包中是数量巨大的小文件。

**【修改建议】**
禁止通过ZipEntry.getSize()进行解压尺寸判断。

**【正例】**
场景1：
- 修复示例：

```java
    static final int BUFFER = 512;
    static final int TOOBIG = 0x6400000; // max size of unzipped data, 100MB
    static final int TOOMANY = 1024; // max number of files

    // ...
    // The code validates the name of each entry before extracting the entry.
    // If the name is invalid, the entire extraction is aborted.
    private String sanitizeFileName(String entryName, String intendedDir) throws IOException {
        File f = new File(intendedDir, entryName);
        String canonicalPath = f.getCanonicalPath();
        File iD = new File(intendedDir);
        String canonicalID = iD.getCanonicalPath();
        if (canonicalPath.startsWith(canonicalID)) {
            return canonicalPath;
        } else {
            throw new IllegalStateException("File is outside extraction target directory.");
        }
    }

    public final void doSomething(String fileName, String destDir) throws java.io.IOException {
        FileInputStream fis = new FileInputStream(fileName);
        ZipInputStream zis = new ZipInputStream(new BufferedInputStream(fis));
        ZipEntry entry;
        int total = 0;
        int entries = 0;
        try {
            while ((entry = zis.getNextEntry()) != null) {
                BufferedOutputStream dest = null;
                int count;
                byte data[] = new byte[BUFFER];

                // Write the files to the disk, but ensure that the entryName is valid,and that the file is not insanely big
                String name = sanitizeFileName(entry.getName(), destDir);

                // process file
                FileOutputStream fos = new FileOutputStream(name);
                dest = new BufferedOutputStream(fos, BUFFER);

                // check every entry's size
                while ((count = zis.read(data, 0, BUFFER)) != -1) {
                    total += count;
                    if (total > TOOBIG) {
                        break;
                    }
                    dest.write(data, 0, count);
                }
                entries++;

                // if the total number of entry is larger than the max number,it will throw exception.
                if (entries > TOOMANY) {
                    //handle exception
                }
                // if the total size of zip file is bigger than the max size value,it will throw exception.
                if (total > TOOBIG) {
                    //handle exception
                }
                …
            }
        } finally {
            zis.close();
        }
    }
```

**【反例】**
场景1：
- 错误示例：

```java
    public static final int BUFFER = 512;
    public static final int TOOBIG = 0x6400000; // 100MB

    public final void doSomething(String filename) throws java.io.IOException {
        FileInputStream fis = new FileInputStream(filename);
        ZipInputStream zis = new ZipInputStream(new BufferedInputStream(fis));
        ZipEntry entry;
        try {
            while ((entry = zis.getNextEntry()) != null) {
                System.out.println("Extracting: " + entry);
                int count;
                byte data[] = new byte[BUFFER];

                // Write the files to the disk, but only if the file is not
                // insanely big
                int temp = (int) entry.getSize();

                // 【POTENTIAL FLAW】 检查if语句中是否使用ZipEntry.getSize()来做文件大小的判断，如果是，则报告警。
                if (temp > TOOBIG) {
                    throw new IllegalStateException("File to be unzipped is huge.");
                }
                // 【POTENTIAL FLAW】 检查if语句中是否使用ZipEntry.getSize()来做文件大小的判断，如果是，则报告警。
                if (entry.getSize() == -1) {
                    throw new IllegalStateException("File to be unzipped might be huge.");
                }
                FileOutputStream fos = new FileOutputStream(entry.getName());
                BufferedOutputStream dest = new BufferedOutputStream(fos, BUFFER);
                while ((count = zis.read(data, 0, BUFFER)) != -1) {
                    dest.write(data, 0, count);
                }
                dest.flush();
                dest.close();
                zis.closeEntry();
            }
        } finally {
            zis.close();
        }
    }

```

#### G.FIO.03 对于从流中读取一个字符或字节的方法，使用int类型的返回值【要求】

**【描述】**
从流中读取一个字符或字节的方法，未使用int类型的返回值。

Java中InputStream.read()和Reader.read()方法用于从流中读取一个字节（byte）或字符（char）。InputStream.read()读取一个字节，返回值的范围为0x00-0xFF（补码），8位；Reader.read()读取一个字符，返回值的范围为0x0000-0xFFFF（补码），16位。当读取到流的末尾时，以上方法均返回int类型的-1（补码表示为0xFFFFFFFF），32位。因此，如果在未判断返回值是否是流末尾标志-1（补码表示为0xFFFFFFFF）前将返回值转为byte或 char，会导致无法正确判断返回值是流中的内容还是结束标识。

**【修改建议】**
使用int类型的变量来保存read()的返回值，并使用该返回值判断是否读取到流的末尾，流未读完时，将读取的内容转换为char或者byte类型。

**【正例】**
场景1：
- 修复示例：

```java
public static void readBytesFromStream() {
    try (FileInputStream in = new FileInputStream("demo.txt")) {
        // Initialize stream
        int data;
        while ((data = in.read()) != -1) {
            LOGGER.info(data);
        }
    } catch (Exception e) {
        LOGGER.error("error");
    }
}

public static void readCharsFromStream() {
    try (FileReader in = new FileReader("demo.txt")) {
        // Initialize stream
        int data;
        while ((data = in.read()) != -1) {
            LOGGER.info(data);
        }
    } catch (Exception e) {
        LOGGER.error("error");
    }
}
```

**【反例】**
场景1：
- 错误示例：

```java
public static void readBytesFromStream() {
    try (FileInputStream in = new FileInputStream("demo.txt")) {
        // Initialize stream
        byte data;

        // 【POTENTIAL FLAW】 对于从流中读取一个字符或字节的方法，使用int类型的返回值
        while ((data = (byte) in.read()) != -1) {
            LOGGER.info(data);
        }
    } catch (Exception e) {
        LOGGER.error("error");
    }
}

public static void readCharsFromStream() {
    try (FileReader in = new FileReader("demo.txt")) {
        // Initialize stream
        char data;

        // 【POTENTIAL FLAW】 对于从流中读取一个字符或字节的方法，使用int类型的返回值
        while ((data = (char) in.read()) != -1) {
            LOGGER.info(data);
        }
    } catch (Exception e) {
        LOGGER.error("error");
    }
}
```

#### G.FIO.04 防止外部进程阻塞在输入输出流上【要求】

**【描述】**
防止外部进程阻塞在输入输出流上。

Java中有两种方式启动一个外部进程并与其交互：
1. java.lang.Runtime的exec()方法。
2. java.lang.ProcessBuilder的start()方法。

他们都返回一个java.lang.Process对象，该对象封装了这个外部进程。每个Process对象，包含输入流、输出流及错误流各一个。应该恰当地处理这些流，避免外部进程阻塞在这些流上。不正确的处理会产生异常、DoS，及其他安全问题。

**【修改建议】**
在运行一个外部进程时，如果此进程往其输出流发送任何数据，则必须将其输出流清空。类似的，如果进程会往其错误流发送数据，其错误流也必须被清空。

**【正例】**
场景1：
- 修复示例1：分别处理外部进程的输出流、错误流

```java
public class ProcessExecutor {
    public void callExtProcess() throws IOException, InterruptedException {
        Process proc = Runtime.getRuntime().exec("ProcessHasOutput");

        StreamConsumer errConsumer = new StreamConsumer(proc.getErrorStream());
        StreamConsumer outputConsumer = new StreamConsumer(proc.getInputStream());

        errConsumer.start();
        outputConsumer.start();

        int exitVal = proc.waitFor();

        errConsumer.join();
        outputConsumer.join();
    }

    class StreamConsumer extends Thread {
        InputStream is;

        StreamConsumer(InputStream is) {
            this.is = is;
        }

        @Override
        public void run() {
            try {
                byte data;
                int result;
                while ((result = is.read()) != -1) {
                    data = (byte) result;
                    handleData(data);
                }
            } catch (IOException ex) {
                ... // 处理异常
            }
        }

        private void handleData(byte data) {
            ...
        }
    }
}
```
- 修复示例2：将错误流重定向到输出流中，单独处理输出流

```java
public class ProcessExecutor {
    public void callExtProcess() throws IOException, InterruptedException {
        ProcessBuilder proc = new ProcessBuilder("ProcessHasOutput");
                proc.start();

        proc.redirectErrorStream(true);
        StreamConsumer outputConsumer = new StreamConsumer(proc.getInputStream());
        outputConsumer.start();

        int exitVal = proc.waitFor();

        outputConsumer.join();
    }

    class StreamConsumer extends Thread {
        InputStream is;

        StreamConsumer(InputStream is) {
            this.is = is;
        }

        @Override
        public void run() {
            try {
                byte data;
                int result;
                while ((result = is.read()) != -1) {
                    data = (byte) result;
                    handleData(data);
                }
            } catch (IOException ex) {
                ... // 处理异常
            }
        }

        private void handleData(byte data) {
            ...
        }
    }
}
```

**【反例】**
场景1：
- 错误示例：处理进程的返回值前、或等待进程结束前，未处理外部进程的输出流、错误流

```java
// 处理进程的返回值前未处理外部进程的输出流、错误流
public void execExtProcess() throws IOException {
    Process proc = Runtime.getRuntime().exec("ProcessMaybeStillRunning");
    int exitVal = proc.exitValue();
}

// 等待进程结束前未处理外部进程的输出流、错误流
public void execExtProcess() throws IOException, InterruptedException {
    Process proc = Runtime.getRuntime().exec("ProcessHasOutput");
    int exitVal = proc.waitFor();
}
```

#### G.FIO.05 临时文件使用完毕必须及时删除【要求】

**【描述】**
临时文件使用完毕必须及时删除。

程序中有很多使用临时文件的场景，比如用于进程间的数据共享，缓存内存数据，动态构造的类文件，动态连接库文件等。临时文件可能创建于操作系统的共享临时文件目录，例如，POSIX系统下的/tmp与/var/tmp目录，Windows系统下的C:\TEMP目录，这类目录中的文件可能会被定期清理。创建在其他路径下的临时文件不会被自动清理。如果文件未被安全地创建或者用完后还是可访问的，具备本地文件系统访问权限的恶意用户便可以利用共享目录中的文件进行恶意操作，另外，临时文件不清理也可能会导致大量垃圾文件占用磁盘的存储空间。

**【修改建议】**
在临时文件使用完毕之后、系统终止之前，及时对其进行删除。

**【正例】**
场景1：临时文件未删除
- 修复示例：使用了delete方法删除了tempFile文件

```java
private void doSomething(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException{
    File tempFile = null;
    try {
        tempFile = File.createTempFile("temp", "1234");

        /* Set the permissions to avoid insecure temporary file incidentals  */
        if (!tempFile.setWritable(true, true)) {
            System.out.println("Could not set Writable permissions");
        }
        ...
    } catch (IOException exceptIO) {
        System.out.println("Could not create temporary file");
    } finally {
        /* Delete the temporary file manually */
        if (tempFile.exists()) {
            tempFile.delete();
        }
    }
}
```

**【反例】**
场景1：临时文件未删除
- 错误示例：tempFile没有删除操作

```java
@Override
public void doSomething(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
    File tempFile = null;
    try {
        // POTENTIAL FLAW: 临时文件使用完毕应及时删除
        tempFile = File.createTempFile("temp", "1234");

        // 当调用deleteOnExit()方法时，只是相当于对deleteOnExit()作一个声明，当程序运行结束，JVM终止时才真正调用deleteOnExit()方法实现删除操作。
        tempFile.deleteOnExit();

        /* Set the permissions to avoid insecure temporary file incidentals */
        if (!tempFile.setWritable(true, true)) {
            System.out.println("Could not set Writable permissions");
        }
        ...
    } catch (IOException exceptIO) {
        System.out.println("Could not create temporary file");
    }
}
```

## 2.11 序列化

#### G.SER.01 尽量避免实现Serializable接口【建议】

**【描述】**
对于支持序列化操作的类，其实例属性如果不支持序列化操作，在对该类进行序列化操作时会出异常。class中的静态属性、transient修饰的非静态属性不会进行序列化操作。

**【修改建议】**
对于支持序列化操作的类，其实例属性需支持序列化操作，不需要进行序列化操作的属性可以设置为transient。

**【正例】**
场景1：
- 修复示例1：使用transient修饰属性
  ```java
  public class AvoidSerialization implements Serializable {

     public transient AttributeClass attribute= new AttributeClass ();
     ...
  }

   class AttributeClass{
   ...
   }
  ```
- 修复示例2：使用static修饰属性
  ```java
  public class AvoidSerialization implements Serializable {

     public static AttributeClass attribute= new AttributeClass ();
     ...
  }

   class AttributeClass{
   ...
   }
  ```
- 修复示例3：属性类实例化Serializable 
  ```java
  public class AvoidSerialization implements Serializable {

     public static AttributeClass attribute= new AttributeClass ();
     ...
  }

   class AttributeClass implements Serializable{
   ...
   }
  ```

**【反例】**
场景1：
- 错误示例：支持序列化操作的类的属性不支持序列化操作

  ```java
  public class AvoidSerialization implements Serializable {

     public AttributeClass attribute= new AttributeClass ();
     ...
  }

   class AttributeClass{

   }
  ```

#### G.SER.02 实现Serializable接口的可序列化类应该显式声明serialVersionUID【建议】

**【描述】**
如果可序列化类未显式声明serialVersionUID，则序列化运行时将基于该类的各个方面计算该类的默认serialVersionUID值，如“Java(TM) 对象序列化规范”中所述。但是，强烈建议所有可序列化类都显式声明serialVersionUID值，原因是计算默认的serialVersionUID对类的详细信息具有较高的敏感性，根据编译器实现的不同可能千差万别，这样在反序列化过程中可能会导致意外的`InvalidClassException`。因此，为保证serialVersionUID值跨不同java编译器实现的一致性，序列化类必须声明一个明确的serialVersionUID值。

同时强烈建议使用private显式声明serialVersionUID，原因是这种声明仅应用于当前声明类，serialVersionUID作为继承成员没有用处。

**【修改建议】**
对于需要实现序列化接口的Class，应该显式声明serialVersionUID。

**【正例】**
场景1：
- 修复示例：显式声明serialVersionUID

  ```java
  public class BeanType implements Serializable {
      private static final long serialVersionUID = -2589766491699675794L;
      ...
  }
  ```

**【反例】**
场景1：
- 错误示例：实现Serializable接口的类未显式声明serialVersionUID

  ```java
  public class BeanType implements Serializable {
      ...
  }
  ```

#### G.SER.03 序列化对象中的HashMap，HashSet或HashTable等集合禁止包含对象自身的引用【要求】

**【描述】**
如果一个被序列化的对象中包含HashMap，HashSet或HashTable集合，则这些集合中不允许保存当前被序列化对象的直接或间接引用。因为这些集合类型在反序列化的时候，会调用到当前序列化对象的hashCode方法，而此时如果序列化对象还未完全加载，计算出的hashCode可能不正确，从而导致对象位置放置错误，破坏反序列化的实例。

**【反例】**
Sub对象放入了对象中的HashSet，在反序列化set时，因为id属性还未完成初始化，导致hashCode的结果为0，从而导致Sub对象在set中的位置放置错误，对象被破坏
```java
class Super implements Serializable {
    private static final long serialVersionUID = -289127917292179172L;
    final Set<Super> set = new HashSet<>();
}

final class Sub extends Super {
    private int id;

    public Sub(int id) {
        this.id = id;
        set.add(this);
    }

    public void checkInvar() {
        if (!set.contains(this)) {
            throw new AssertionError("invariant violated");
        }
    }

    public int hashCode() {
        return id;
    }

    public boolean equals(Object obj) {
        return obj instanceof Sub && id == ((Sub) obj).id;
    }
}
```

#### G.SER.04 禁止直接序列化指向系统资源的信息【要求】

**【描述】**
当序列化结果中含有指向系统的资源时，这些信息很容易被篡改。当恶意用户篡改了指向系统的资源时，反序列化的对象会直接操作这些被攻击者指定的系统资源，导致任意文件读取或修改。

**【修改建议】**
禁止直接序列化指向系统资源的信息，如实现Serializable的类，其成员变量为File或FileDescriptor时，用transient修饰，避免这些对象被序列化。

**【正例】**
场景1： 类成员变量为File，且被序列化
- 修复示例1：用transient修饰类成员变量File

  ```java
  final class SomeResource implements Serializable {
      private static final long serialVersionUID = 6562477636399915529L;

      private transient File file;

      public SomeResource(String fileName) {
          file = new File(fileName);
          ...
      }
  }
  ```

**【反例】**
场景1： 类成员变量为File，且被序列化
- 错误示例：

  ```java
  final class SomeResource implements Serializable {
      private static final long serialVersionUID = -2589766491699675794L;

      private File file;

      public SomeResource(String fileName) {
          file = new File(fileName);
          ...
      }
  }
  ```

#### G.SER.05 禁止序列化非静态的内部类【要求】

**【描述】**
内部类是没有显式或隐式声明为静态的嵌套类。内部类（包括本地类和匿名类）的序列化很容易出错。

在使用非静态内部类时，实际上隐含着对外部类实例的非transient引用，在对内部类进行序列化时，会一起将外部类也序列化。
内部类的实现与synthetic属性有关，对synthetic关键字，不同的编译器的实现不同，会影响程序的兼容性。并且会跟默认的serialVersionID产生冲突。
内部类不能声明静态成员以外的运行时常量，所以不能使用serialPersistentFields机制来指定可以序列化的属性。
与外部实例关联的内部类没有无参构造方法（此内部类的构造方法隐式的接收外部实例作为前置参数）。内部类无法实现Externalizable接口，Externalizable接口要求实现对象通过writeExternal()和readExternal()方法手动保存和恢复其状态。
基于以上原因，禁止序列化非静态内部类。但是这些原因不适用于静态内部类，所以静态内部类可以进行序列化。

**【修改建议】**
对于支持序列化操作类，其内部类设置为静态类。

**【正例】**
场景1：
- 修复示例1：支持序列化的类其内部类为静态类
```java
public class TestClass implements Serializable {
    private int rank;

    static class InnerSer implements Serializable {
        protected String name;
    }
}
```

**【反例】**
场景1：
- 错误示例：支持序列化的类的内部类为非静态类

```java
public class SomeResource implements Serializable {
    private int rank;

    // 【POTENTIAL FLAW】 禁止序列化非静态的内部类
    class InnerSer implements Serializable {
        protected String name;
    }
}
```

#### G.SER.06 序列化操作要防止敏感信息泄露【要求】

**【描述】**
敏感数据传输过程中要防止被窃取和恶意篡改。使用安全的加密算法加密传输对象可以保护数据。这就是所谓的对对象进行密封。而对密封的对象进行数字签名则可以防止对象被非法篡改，保持其完整性。在以下场景中， 需要对对象密封和数字签名来保证数据安全：**支持序列化的对象中含有敏感信息，该对象需要通过非加密通道传递（如http）或该需要在本地持久化保存（如在硬盘驱动器上）**。
应该避免使用私有加密算法，因为这样会引入不必要的漏洞。在readObject()和writeObject()函数中使用私有加密算法的应用是典型的反面示例。
含有敏感数据（如口令、秘钥等）的对象进行序列化操作，其中的敏感数据会被明文转为文本或二进制格式，容易出现敏感信息泄露问题。

**【修改建议】**
含有敏感数据的对象，在序列化操作前要对敏感数据进行防泄漏和防篡改处理，即先签名后加密处理。
对于敏感信息字段，建议使用transient修饰符，该字段不写入序列化结果中；或者是重写writeObject(),不将敏感字段写入序列化结果中。

**【正例】**
场景1：重写writeObject方法，避免将敏感信息写入序列化结果中
- 修复示例1：不应该将含有敏感信息的数据直接写入磁盘
```java
public class SomeInfo implements Serializable {
    private static final long serialVersionUID = 9078808681344666097L;
    private String pwd;
    private String user;

    private void writeObject(ObjectOutputStream out) throws IOException {
        out.writeObject(this.user);     
    }
}
```
场景2：通过`transient`修饰符，避免将敏感信息写入序列化结果中
- 修复示例1：
```java
public class SomeInfo implements Serializable {
    private static final long serialVersionUID = 9078808681344666097L;
    private transient String pwd;
    private String user;
    ...
}
```
场景3：对象序列化后本次存储
- 修复示例：先为对象签名然后再加密。 这样既能保证数据的真实可靠性，又能防止“中间人攻击”（man-inmiddle attacks）。
```java
public class UserInfo implements Serializable {
    private static final long serialVersionUID = -2589766491699675794L;
    private String id;
    private String name;
    private String phone;
    private String address;
    ...
    private void writeObject(ObjectOutputStream outputStream) throws IOException {
        outputStream.writeObject(id);
        outputStream.writeObject(name);

        // 敏感信息序列化前先进行加密
        outputStream.writeObject(encryptData(phone));
        outputStream.writeObject(encryptData(address));
    }
}
// 将UserInfo中的信息通过序列化的方式写入指定文件中
public void saveUserInfoToFile(UserInfo info) {
    ...
    FileOutputStream fos = null;
    try {
        fos = new FileOutputStream("bizFile");
        ObjectOutputStream oos = new ObjectOutputStream(fos);
        oos.writeObject(info);
        ...
    } catch (IOException ex) {
        ... // 处理异常
    }
    ...
}
```
场景4：对象序列化后通过网络传递
- 修复示例：先为对象签名然后再加密。 这样既能保证数据的真实可靠性，又能防止“中间人攻击”（man-inmiddle attacks）。
```java
public void sendUserInfoOverNetwork(UserInfo info) {
    ...
    try {
        ...
        String json = JSON.toJSONString(info);
        String signJson = sign(json);
        String encryptJson = encrypt(signJson);

        // 发送加密后的encryptJson
        ...
    } catch (IOException ex) {
        ... // 处理异常
    }
    ...
}
```

**【反例】**
场景1：重写writeObject方法，避免将敏感信息写入序列化结果中
- 错误示例：直接将敏感数据通过writeObject方法写入序列化结果中

```java
public class SomeInfo implements Serializable {
    private static final long serialVersionUID = 9078808681344666097L;
    private String pwd;
    private String user;

    private void writeObject(ObjectOutputStream out) throws IOException {
        // 【POTENTIAL FLAW】 敏感信息被明文写入序列化结果中
        out.writeObject(this.user);     
        out.writeObject(this.pwd);
    }
}
```
场景2：通过`transient`修饰符，避免将敏感信息写入序列化结果中
- 错误示例：

```java
public class SomeInfo implements Serializable {
    private static final long serialVersionUID = 9078808681344666097L;
    private String pwd;
    private String user;
    ...
}
```
场景3：对象序列化后本次存储
- 错误示例：含敏感数据的对象序列化后写入文件，未对数据进行加密、签名处理。
```java
// 将UserInfo中的信息通过序列化的方式写入指定文件中
public class UserInfo implements Serializable {
    private static final long serialVersionUID = 6562477636399915529L;
    private String id;
    private String name;
    private String phone;
    private String address;
    ...
}

// 将UserInfo中的信息通过序列化的方式写入指定文件中
public void saveUserInfoToFile(UserInfo info) {
    ...
    FileOutputStream fos = null;
    try {
        fos = new FileOutputStream("bizFile");
        ObjectOutputStream oos = new ObjectOutputStream(fos);
        oos.writeObject(info);
        ...
    } catch (IOException ex) {
        ... // 处理异常
    }
    ...
}
```
场景4：对象序列化后通过网络传递
- 错误示例：对敏感数据先加密后签名，无法防止信息被恶意篡改
```java
public void sendUserInfoOverNetwork(UserInfo info) {
    ...
    try {
        ...
        String json = JSON.toJSONString(info);
        String encryptJson = encrypt(signJson);
        String signJson = sign(encryptJson);

        // 发送加密后的signJson
        ...
    } catch (IOException ex) {
        ... // 处理异常
    }
    ...
}
```

#### G.SER.07 防止反序列化被利用来绕过构造方法中的安全操作【要求】

**【描述】**
防止反序列化被利用来绕过构造方法中的安全操作。

反序列化操作可以在不执行构造方法的情况下创建对象的实例，所以反序列化操作中的行为应该设计为与构造方法保持一致，这些行为包括：

1. 对参数的校验；

2. 安全管理器的检查；

3. 对属性赋初始值，特别是transient修饰的属性反序列化操作默认不会赋值；

否则，攻击者就可能会通过反序列化操作构造出与预期不符合的对象实例。

**【修改建议】**
如果可序列化的类的构造方法中存在SecurityManager检查，请确保readObject()方法中存在相同的SecurityManager检查。

**【正例】**
场景1：安全管理器的检查。
- 修复示例1：方法中有安全检查器：
```java
public final class SecureSerializeDemo implements Serializable {
    private static final long serialVersionUID = 9078808681344666097L;

    // Private internal state
    private String town;

    private static final String UNKNOWN = "UNKNOWN";

    void performSecurityManagerCheck() throws SecurityException {
        // verify whether current user has rights to access the file
        SecurityManager securityManager = System.getSecurityManager();
    }

    public SecureSerializeDemo () {
        performSecurityManagerCheck();

        // Initialize town to default value
        town = UNKNOWN;
    }

    private void readObject(ObjectInputStream in) throws Exception {
        performSecurityManagerCheck();
        in.defaultReadObject();
    }
}
```

**【反例】**
场景1：安全管理器的检查。
- 错误示例：方法中没有安全检查器。

```java
public final class SecureSerializeDemo implements Serializable {
    private static final long serialVersionUID = 9078808681344666097L;

    // Private internal state
    private String town;

    private static final String UNKNOWN = "UNKNOWN";

    void performSecurityManagerCheck() throws SecurityException {
        // verify whether current user has rights to access the file
        SecurityManager securityManager = System.getSecurityManager();
    }

    public SecureSerializeDemo () {
        performSecurityManagerCheck();
        // Initialize town to default value
        town = UNKNOWN;
    }

    // 【POTENTIAL FLAW】 实现Serializable接口，并且在实现类的构造函数中包含安全检查器 2）基于第一点，工具检测readObject和writeObject方法中是否包含安全检查器，如果没有则报告警。
    private void readObject(ObjectInputStream in) throws Exception {
        in.defaultReadObject();
    }

}
```

#### G.SER.08 禁止直接将外部数据进行反序列化【要求】

**【描述】**
直接将外部数据进行反序列化。

反序列化操作是将一个二进制流或字符串反序列化为一个Java对象。当反序列化操作的数据是外部数据时，恶意用户可利用反序列化操作构造指定的对象、执行恶意代码、向应用程序中注入有害数据等。不安全反序列化操作可能导致任意代码执行、特权提升、任意文件访问、拒绝服务等攻击。

实际应用中，通常采用三方件实现对json、xml、yaml格式的数据序列化和反序列化操作。常用的三方件包括：fastjson、jackson、XMLDecoder、XStream、SnakeYmal等。

**【修改建议】**
使用白名单的方式对外部数据进行校验。

**【正例】**
场景1：使用`ScriptEngineManager`执行脚本代码
- 修复示例：
```java
private static void doSomething() {        
    String jsCode = request.getParameter("jscode");
    ...
    NashornSandbox sandbox = new NashornSandboxes();
    sandbox.allow(File.class);  // 使用sandbox.allow()来设置允许使用的java类
    sandbox.eval(jsCode);
    ...
}
```

场景2：使用Fastjson 1.2.68以前版本
- 修复示例：禁用AutoType功能,并设置白名单校验
```java
private static void doSomething() {        
    String jsonStr = request.getParameter("jsonData");
    ...
    ParserConfig.getGlobalInstance().setAutoTypeSupport(false); // 或者是直接删除该行代码
    ParserConfig.getGlobalInstance().addAccept("com.func.test.User"); // 进一步设置白名单校验规则
    User user = (User) JSONObject.parse(jsonStr);
    ...
}
```

场景3：使用Fastjson 1.2.68及以上新版本
- 修复示例1：开启SafeMode
```java
private static void doSomething() {        
    String jsonStr = request.getParameter("jsonData");
    ...
    ParserConfig.getGlobalInstance().setSafeMode(true);
    User user = (User) JSONObject.parse(jsonStr);
    ...
}
```
- 修复示例2：解析Json字符串时，开启SafeMode模式
```java
private static void doSomething() {        
    String jsonStr = request.getParameter("jsonData");
    ...
    ParserConfig.getGlobalInstance().setSafeMode(true);
    User user = JSON.parseObject(jsonStr, User.class, Feature.SafeMode);
    ...
}
```

场景4：使用Jackson
- 修复示例1：对于Jackson 2.10.0以前的版本
```java
private static void doSomething() {        
    String jsonStr = request.getParameter("jsonData");
    ...
    ObjectMapper mapper = new ObjectMapper();
    mapper.disableDefaultTyping();
    UserInfo demo = (UserInfo)mapper.readValue(jsonStr, UserInfo.class);
    ...
}
```
- 修复示例2：对于Jackson 2.10.0及新版本
```java
private static void doSomething() {        
    String jsonStr = request.getParameter("jsonData");
    ...
    ObjectMapper mapper = new ObjectMapper();
    mapper.activeDefaultTyping(...);
    UserInfo demo = (UserInfo)mapper.readValue(jsonStr, UserInfo.class);
    ...
}
```

场景5：使用XStream
- 修复示例1：启用白名单校验
```java
private static void doSomething() {        
    String xmlStr = request.getParameter("xmlData");
    ...
    XStream xst = new XStream(new DomDriver());

    // 首先清除默认设置，然后进行自定义设置
    xst.addPermission(NoTypePermission.NONE);

    // 添加一些基础的类型，如Array、NULL、primitive
    xst.addPermission(ArrayTypePermission.ARRAYS);
    xst.addPermission(NullPermission.NULL);
    xst.addPermission(PrimitiveTypePermission.PRIMITIVES);

    // 添加自定义的类列表
    xst.addPermission(new ExplicitTypePermission(new Class[] { XStreamTest.class }));

    // 添加同一个package下的多个类型
    xst.allowTypesByWildcard(new String[] { XStreamTest.class.getPackage().getName() + ".*" });
    xst.fromXML(xmlStr);
}
```
- 修复示例2：XStream-1.4.10及以上版本,设置默认安全校验
```java
private static void doSomething() {        
    String xmlStr = request.getParameter("xmlData");
    ...
    XStream xst = new XStream(new DomDriver());
    XStream.setupDefaultSecurity(xst);
    xst.fromXML(xmlStr);
}
```

场景6：使用XMLDecoder
- 修复示例：将XMLDecoder改为XStream
```java
private static void doSomething() {        
    String xmlStr = request.getParameter("xmlData");
    ...
    XStream xst = new XStream(new DomDriver());
    XStream.setupDefaultSecurity(xst);
    xst.fromXML(xmlStr);
}
```

场景7：使用SnakeYaml
- 修复示例1：
```java
private static void doSomething() {        
    String yamlStr = request.getParameter("yamlData");
    ...
    Yaml yaml = new Yaml(new SnakeYamlSecureConstructor());
    yaml.load(yamlStr);
}

class SnakeYamlSecureConstructor extends Constructor {
    SnakeYamlSecureConstructor(DeserializeAcceptedClassList whiteList) {
        super();

        this.yamlConstructors.put(null, undefinedConstructor); // 禁止所有的未定义的类进行构造
        addWhiteList(whiteList);  // 增加白名单类的构造
    }

    private void addWhiteList(DeserializeAcceptedClassList whiteList) {
        if (whiteList == null) {
            return;
        }

        for (String whiteName: whiteList) {
            this.yamlConstructors.put(new Tag(Tag.PREFIX + whiteName), new SecureConstructObject());
        }
    }

    /**
     * ConstructYamlObject是Constructor类中的保护类，非静态，所以内部含有Constructor的指针，不能在外部直接引用
     * 所以使用继承的方式，将SnakeYamlDeserializeConstructor指针赋值到SecureConstructObject内部，并保持ConstructYamlObject
     * 的行为不变化
     */
    protected class SecureConstructObject extends ConstructYamlObject {
        SecureConstructObject() {
            super();
        }
    }
}
```
- 修复示例2：使用自定义函数校验外部数据。
```java
private static void doSomething() {        
    String yamlStr = request.getParameter("yamlData");
    ...
    Yaml yaml = new Yaml();
    if (!validYaml(yamlStr)) { // valid开头的自定义校验函数校验
        throw new Exception("XXX");
    }
    yaml.load(yamlStr);
}

private static Boolean validYaml(String yamlStr){
    ...// 自定义校验逻辑
}
```

**【反例】**
场景1：使用`ScriptEngineManager`执行脚本代码
- 错误示例：
```java
private static void doSomething() {        
    String jsCode = request.getParameter("jscode");
    ...
    ScriptEngineManager manager = new ScriptEngineManager();
    ScriptEngine engine = manager.getEngineByName("javascript");
    engine.eval(jsCode);
    ...
}
```

场景2：使用Fastjson 1.2.68以前版本
- 错误示例：开启AutoType功能
```java
private static void doSomething() {        
    String jsonStr = request.getParameter("jsonData");
    ...
    ParserConfig.getGlobalInstance().setAutoTypeSupport(true);
    User user = (User) JSONObject.parse(jsonStr);
    ...
}
```

场景3：使用Fastjson 1.2.68及以上新版本
- 错误示例：禁用SafeMode
```java
private static void doSomething() {        
    String jsonStr = request.getParameter("jsonData");
    ...
    ParserConfig.getGlobalInstance().setSafeMode(false);
    User user = (User) JSONObject.parse(jsonStr);
    ...
}
```

场景4：使用Jackson
- 错误示例：
```java
private static void doSomething() {        
    String jsonStr = request.getParameter("jsonData");
    ...
    ObjectMapper mapper = new ObjectMapper();
    mapper.enableDefaultTyping();
    UserInfo demo = (UserInfo)mapper.readValue(jsonStr, UserInfo.class);
    ...
}
```

场景5：使用XStream
- 错误示例：
```java
private static void doSomething() {        
    String xmlStr = request.getParameter("xmlData");
    ...
    XStream xst = new XStream(new DomDriver());
    xst.fromXML(xmlStr);
    ...
}
```

场景6：使用XMLDecoder
- 错误示例：
```java
private static void doSomething() {
    ...
    InputStream is = request.getInputStream();
    ...
    XMLDecoder decoder = new XMLDecoder(is);
    decoder.readObject();
}
```

场景7：使用SnakeYaml
- 错误示例：
```java
private static void doSomething() {        
    String yamlStr = request.getParameter("yamlData");
    ...
    Yaml yaml = new Yaml();
    yaml.load(yamlStr);
}
```

## 2.12 外部数据校验

#### P.05 外部数据使用前必须进行合法性校验【要求】

**【描述】**
- LDAP注入：
    当不受控制的数据被传递给 LDAP 查询时，就会产生此类漏洞。注入被污染的数据可能会更改查询的目的，这可能会绕过安全检查或泄露未经授权的数据。

- OGNL注入：
    禁止外部数据直接拼接(OGNL)语句以执行任意代码。
    对象图导航语言(OGNL)是一种针对Java的开源表达式语言(EL)，它允许在由开发者提供的环境中计算并执行EL表达式。允许在任何环境下计算未验证的表达式将允许攻击者执行任意代码。

- Eval注入：
    当前程序执行不可信的代码，就会产生code injection问题，比如对当前的用户对象进行计算或修改用户的状态。

- 跨站脚本攻击：
    当应用程序收到含有不可信的数据，在没有进行适当的校验和转义的情况下就将它发送给Web浏览器，这就会产生跨站脚本攻击（简称XSS）。XSS允许攻击者在受害者的浏览器上执行脚本，从而劫持用户会话、危害网站、或者将用户转向恶意网站。

- 外部输入导致XPath表达式注入：
    直接使用外部数据更改XPath查询的意图，此漏洞会造成信息泄露或允许对应用程序功能进行未经授权的访问。

- 外部控制的哈希算法：
    使用外部不可信的数据来初始化哈希算法。

- 指向未可信站点的URL重定向(开放重定向)：
    用户控制输入被用于指定至外部站点的链接的情况。攻击者可以创建链接，指向被重定向至恶意网站的受信任网站。这可以让攻击者实施钓鱼攻击，以允许他们窃取用户凭证。

- 外部数据进入Map：
    来自程序外部的数据通常被认为是不可信的，在使用这些数据前需要进行合法性校验，否则可能会导致不正确的计算结果、运行时异常、不一致的对象状态，甚至引起各种注入攻击，对系统造成严重影响。当程序使可信赖和不可信赖的分界线模糊不清时，就会发生Trust Boundary Violation漏洞。

- 资源注入：
    使用来自上游组件的输入来标识某个资源（文件、端口号）前，没有对其进行限制或限制不正确，导致可能访问预期受控范围之外的资源。

**【修改建议】**
- 使用白名单的方式对外部数据进行校验。
- 对于Java的标准库或开源组件已经提供的功能，应使用标准库或开源组件的API，避免产生XSS注入问题。
- 对外部参数进行白名单校验。
- 对用户输入的URL进行合法校验，只允许使用合法的URL，从而过滤不可信URL。

**【正例】**
场景1：外部数据直接作为响应头的值
- 修复示例：
```java
private static void doSomething(String userSN, String userPassword) {        
    ...
    DirContext dctx = new InitialDirContext(env);
    String base = ""dc=example,dc=com"";
    if (!userSN.matches(""[\\\\w\\\\s]*"") || !userPassword.matches(""[\\\\w]*"")) {
        throw new IllegalArgumentException(""Invalid input"");
    }
    String filter = ""(&(sn="" + userSN + "")(userPassword="" + userPassword + ""))"";
    dctx.search(base, filter, sc);
    ...
}
```

通过安全框架中的API或者业界开源组件ESAPI中的API进行转义。
```java
void foo(HttpServletRequest request, HttpServletResponse response) {
    String data = request.getCookies()[0].getValue();
    OgnlContext ctx = new OgnlContext();

    Object expr = null;
    try {
        data = HWEncoder.encodeForOS(new WindowsCodec(), data);
        expr = Ognl.parseExpression(data);
        Object value = Ognl.getValue(expr, ctx, ""xxx"");
    } catch (OgnlException e) {
        IO.writeLine(e.getMessage());
    }
}
```

OWASP开源组件esapi就提供了XSS防护的编码API。
```java
@Override
public void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
    String safe = ESAPI.encoder().encodeForHTML(request.getParameter(""xss""));
    Object[] obj = { ""a"", ""b"" };
    response.getWriter().format(safe, obj);
}
```

对外部不可信数据algorithm进行校验。
```java
public void userControlledAlgorithm() throws Throwable {
    Properties properties = new Properties();
    properties.load(new FileInputStream(""file""));
    String algorithm = properties.getProperty(""hashAlg2"");
    if (isSafeAlgorithm(algorithm)) {
        MessageDigest md = MessageDigest.getInstance(algorithm);
    }            
}
```

对外部输入进行白名单校验，确定输入的url是合法的url。
```java
void sendRedirect(HttpServletRequest request, HttpServletResponse response) {
    String url = request.getCookies()[0].getValue();
    if (checkUrl(url)) {
      return;
  }
    response.sendRedirect(url); 
}
public boolean checkUrl(String url) {
  //TODO 使用白名单进行校验
}
```

**【反例】**
外部数据直接作为响应头的值
- 错误示例：

```java
private static void doSomething(String userSN, String userPassword) {        
    ...
    DirContext dctx = new InitialDirContext(env);
    String base = ""dc=example,dc=com""; 
    String filter = ""(&(sn="" + userSN + "")(userPassword="" + userPassword + ""))"";
    dctx.search(base, filter, sc);
    ...
}
```

不可信数据从cookie中读取，允许攻击者远程执行任意代码。
```java
void foo(HttpServletRequest request, HttpServletResponse response) {
    String data = request.getCookies()[0].getValue();
    OgnlContext ctx = new OgnlContext();

    Object expr = null;
    try {
        expr = Ognl.parseExpression(data);
        Object value = Ognl.getValue(expr, ctx, ""xxx"");
    } catch (OgnlException e) {
        IO.writeLine(e.getMessage());
    }
}
```

不可信数据未经校验就被执行。
```java
String data = req.getParameter(""input"");
ScriptEngineManager manager = new ScriptEngineManager();
ScriptEngine engine = manager.getEngineByName(""javascript"");
try {
    Object res = engine.eval(data);
} catch (ScriptException e) {
    IO.writeLine(e.getMessage());
}
```

将不可信的外部参数直接通过response传递到web浏览器。
```java
@Override
public void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
    String param = request.getParameter(""xss"");
    Object[] obj = { ""a"", ""b"" };
    response.getWriter().format(param, obj);
}
```

通过用户提供的（被污染的）数据用户名和密码注入了 XPath 查询。如果攻击者的用户名为 `admin` 并且密码为 `' or @loginID='admin`，则完整的 XPath 查询现在为 `/employees/employee[@loginID='admin' and @passwd='' or @loginID='admin']`。如果此查询被用于验证用户身份，攻击者可能会被验证为管理员用户。

```java
public void xpathInjection() {
    XPathFactory factory = XPathFactory.newInstance();
    XPath xPath = factory.newXPath();
    String expression = ""/employees/employee[@loginID='"" + username + ""' and @passwd='"" + password + ""']"";
    nodes = (NodeList) xPath.evaluate(expression, inputSource, XPathConstants.NODESET);
}
```

使用外部不可信数据algorithm初始化hash算法。
```java
public void userControlledAlgorithm() throws Throwable {
    Properties properties = new Properties();
    properties.load(new FileInputStream(""file""));
    String algorithm = properties.getProperty(""hashAlg2"");
    MessageDigest md = MessageDigest.getInstance(algorithm);
}
```

外部输入可能导致重定向至恶意网站。
```java
void sendRedirect(HttpServletRequest request, HttpServletResponse response) {
    String url = request.getCookies()[0].getValue();
    response.sendRedirect(url); 
}
```

Map中将可信数据和不可信数据混合使用，会导致错误地信赖未验证的数据。
```java
public void foo(HttpServletRequest request, HttpServletResponse response) {
    String data = request.getCookies()[0].getValue();
    Model model = new ConcurrentModel();
    Map map = new HashMap();
    map.put(""data"", data);
    map.put(""name"", ""张三"")
    model.mergeAttributes(map);
}
```

外部不可信数据未经校验直接创建URl。
```java
    public HttpURLConnection getUrlConnection(String serviceUrl,String requestMethodType) throws IOException {
        URL url = new URL(serviceUrl);
        HttpURLConnection conn = (HttpURLConnection) url.openConnection();
        conn.setRequestMethod(requestMethodType);
        return conn;
    }
```

#### G.EDV.01 禁止直接使用外部数据来拼接SQL语句【要求】

**【描述】**
使用外部数据构建SQL语句。  

SQL注入是指使用外部数据构造的SQL语句所代表的数据库操作与预期不符，这样可能会导致信息泄露或者数据被篡改。SQL注入产生的根本原因是使用外部数据直接拼接SQL语句，参数化查询是一种简单有效的防止SQL注入的查询方式，应该被优先考虑使用。另外，参数化查询还能提高数据库访问的性能，例如，SQL Server与Oracle数据库会为其缓存一个查询计划，以便在后续重复执行相同的查询语句时无需编译而直接使用。对于常用的ORM框架（如Hibernate、iBATIS等），同样支持参数化查询。

**【修改建议】**
SQL注入产生的根本原因是使用外部数据直接拼接SQL语句，防护措施主要有以下三类
* 使用参数化查询：最有效的防护手段，但对SQL语句中的表名、字段名等不适用。
* 对外部数据进行白名单校验：适用于拼接SQL语句中的表名、字段名。
* 对外部数据中的与SQL注入相关的特殊字符进行转义：适用于必须通过字符串拼接 构造SQL语句的场景，转义仅对由引号限制的字段有效。

**【正例】**
场景1：使用参数化查询替代SQL语句拼接
- 修复示例1：使用参数化查询
```java
PreparedStatement stmt = null;
ResultSet rs = null;
try {
    String userName = request.getParameter("name");
    String password = request.getParameter("password");
    ... // 确保userName和password的长度是合法的
    String sqlStr = "SELECT * FROM t_user_info WHERE name=? AND password =?";
    stmt = connection.prepareStatement(sqlStr);
    stmt.setString(1, userName);
    stmt.setString(2, password);

    // 【GOOD】
    rs = stmt.executeQuery();
    ... // 结果集处理
} catch (SQLException ex) {
    ... // 处理异常
}
```
- 修复示例2：使用自定义校验函数去校验外部数据。
```java
Statement stmt = null;
ResultSet rs = null;
try {
    String userName = request.getParameter("name");
    String password = request.getParameter("password");
    ...
    String sqlStr = "SELECT * FROM t_user_info WHERE name = '" + userName
        + "' AND password = '" + password + "'";
    stmt = connection.createStatement();
    if (!validSqlStr(sqlStr) ) { // validSqlStr 校验函数，校验 sqlStr
        return;
    }
    rs = stmt.executeQuery(sqlStr);
    ... // 结果集处理
} catch (SQLException ex) {
    ... // 处理异常
}
```

**【反例】**
场景1：使用参数化查询替代SQL语句拼接
- 错误示例：使用外部数据拼接SQL语句

```java
Statement stmt = null;
ResultSet rs = null;
try {
    String userName = request.getParameter("name");
    String password = request.getParameter("password");
    ...
    String sqlStr = "SELECT * FROM t_user_info WHERE name = '" + userName
        + "' AND password = '" + password + "'";
    stmt = connection.createStatement();

    // POTENTIAL FLAW
    rs = stmt.executeQuery(sqlStr);
    ... // 结果集处理
} catch (SQLException ex) {
    ... // 处理异常
}
```

#### G.EDV.02 禁止直接使用外部数据构造格式化字符串【要求】

**【描述】**
直接使用外部数据构造格式化字符串。

Java中的Format可以将对象按指定的格式转为某种格式的字符串，格式化字符串可以控制最终字符串的长度、内容、样式，当格式化字符串中指定的格式与格式对象不匹配时还可能会抛出异常。当攻击者可以直接控制格式化字符串时，可导致信息泄露、拒绝服务、系统功能异常等风险。

**【修改建议】**
对外部数据白名单进行校验。

**【正例】**
对外部格式化字符串做白名单校验。
```java
public String formatInfo() {
    String formatStr = req.getParameter("format");

    if(!whiteListVarify(formatStr)){
        return "";
    }

    String value = getData();
    return String.format(formatStr, value);
}
```

**【反例】**
直接使用外部指定的格式对字符串数据进行格式化，当外部指定的格式为非字符类型 如%d，会导致格式化操作出现异常。
```java
public String formatInfo(String formatStr) {
    String value = getData();
    return String.format(formatStr, value);
}
String formatStr = req.getParameter("format");
String formattedValue = formatInfo(formatStr);
```

#### G.EDV.03 禁止直接向Runtime.exec()方法或java.lang.ProcessBuilder类传递外部数据【要求】

**【描述】**
命令注入。

Runtime.exec()方法或java.lang.ProcessBuilder类被用来启动一个新的进程，在新进程中执行命令。命令执行通常会有两种方式：

* 直接执行具体命令：例如Runtime.getRuntime().exec("ping 127.0.0.1")；
* 通过shell方式执行命令：windows下使用cmd.exe、linux下通过sh方式执行命令，或通过脚本文件（*.bat/*.sh）执行命令。

直接使用外部数据构造命令行，会存在以下风险：
* shell方式执行命令时，需要命令行解释器对命令字符串进行拆分，该方式可执行多条命令，存在命令注入风险；
* 直接执行具体的命令时，可以通过空格、双引号或以 -/ 开头的字符串向命令行中注入参数，存在参数注入风险。

**【修改建议】**
针对命令注入或参数注入，具体的解决方案如下：
* 对于Java的标准库或开源组件已经提供的功能，应使用标准库或开源组件的API，避免执行命令。
* 外部数据用于拼接命令行时，可使用白名单方式对外部数据进行校验，保证外部数据中不含注入风险的特殊字符。
* 在执行命令行时，如果输入校验不能禁止有风险的特殊字符，需先外部输入进行转义处理，转义后的字段拼接命令行可有效防止命令注入的产生。

**【正例】**
场景1：
- 修复示例1：外部数据用于拼接命令行时，可使用白名单方式对外部数据进行校验，保证外部数据中不含注入风险的特殊字符。

```java
// str值来自用户输入
public void doSomething() {
    String data = System.getenv("data");
    String osCommand;
    if (System.getProperty("os.name").toLowerCase().indexOf("win") >= 0) {
        osCommand = "c:\\WINDOWS\\SYSTEM32\\cmd.exe /c dir ";
    } else {
        osCommand = "/bin/ls ";
    }
    Process process = null;
    try {
        // 【POTENTIAL FLAW】command injection
        if (!Pattern.matches("[0-9A-Za-z@]+", data )) {
             throw new IllegalArgumentException("...");
        }
        process = Runtime.getRuntime().exec(osCommand + data);
    } catch (IOException e) {
        IO.writeLine(e.getMessage());
    }
    ...
}
```
- 修复示例2：对外部数据中存在命令注入风险的特殊字符进行转义

```java
String encodeIp = HWEncoder.encodeForOS(new WindowsCodec(), ip);
String cmd = "cmd.exe /c ping " + encodeIp;
Runtime rt = Runtime.getRuntime();
Process proc = rt.exec(cmd);
...
```

**【反例】**
场景1：
- 错误示例：对于外部数据直接调用exec，未做合法性校验

```java
public void doSomething() {
    String data = System.getenv("data");
    String osCommand;
    if (System.getProperty("os.name").toLowerCase().indexOf("win") >= 0) {
        osCommand = "c:\\WINDOWS\\SYSTEM32\\cmd.exe /c dir ";
    } else {
        osCommand = "/bin/ls ";
    }
    Process process = null;
    try {
        // 【POTENTIAL FLAW】command injection
        process = Runtime.getRuntime().exec(osCommand + data);
        ...
    } catch (IOException e) {
        IO.writeLine(e.getMessage());
    }
    ...
}
```

#### G.EDV.04 禁止直接使用外部数据来拼接XML【要求】

**【描述】**
使用外部数据来拼接XML，可能导致XML注入。

使用未经校验的数据来构造XML会导致XML注入漏洞。如果用户被允许输入结构化的XML片段，则用户可以在XML的数据域中注入XML标签来改写目标XML文档的结构和内容，XML解析器会对注入的标签进行识别和解释，引起注入问题。

**【修改建议】**
使用白名单的方式对外部数据进行校验。

**【正例】**
场景1：对象是外部用户可控，字段被恶意设置
- 修复示例1：白名单校验
```java
private static final Pattern INPUT_VALIDATER = Pattern.compile("[\\w\\d]+"); // 【GOOD】利用正则匹配对数据做白名单处理。

public String buildXmlStr(User user) {
    if (INPUT_VALIDATER.matches(user.getUserId()) && INPUT_VALIDATER.matches(user.getDescription())) {
        return "<user><role>operator</role><id>" + user.getUserId() + "</id><description>" + user.getDescription()
            + "</description></user>";
    }
}
```
- 修复示例2：转义
```java
public String buildXmlStr(User user) {
    String encodeUserId = HWEncoder.encodeForXML(user.getUserId()); // 【GOOD】对数据进行编码转义。
    String encodeDec = HWEncoder.encodeForXML(user.getDescription()); // 【GOOD】对数据进行编码转义。
    return "<user><role>operator</role><id>" + encodeUserId + "</id><description>" + encodeDec
        + "</description></user>";

}
```
- 修复示例3：使用自定义校验函数去校验外部数据
```java
public String buildXmlStr(User user) {
    String xmlString = "<user><role>operator</role><id>" + user.getUserId() + "</id><description>"
        + user.getDescription() + "</description></user>";
	...
    if (!validXml(xmlString)) { // validXml 校验函数，校验 xmlString
        return;
    }
    return xmlString;
}
```

**【反例】**
场景1：对象是外部用户可控，字段被恶意设置。
- 错误示例：
```java
// 【POTENTIAL FLAW】如果User对象是外部用户可控的，最终构造的XML可被恶意篡改
public String buildXmlStr(User user) {
    String xmlString = "<user><role>operator</role><id>" + user.getUserId() + "</id><description>"
        + user.getDescription() + "</description></user>";
	...
    return xmlString;
}
```

#### G.EDV.05 防止解析来自外部的XML导致的外部实体（XML External Entity）攻击【要求】

**【描述】**
XML外部实体攻击。

XML实体包括内部实体和外部实体。外部实体格式：<!ENTITY 实体名 SYSTEM "URI">  或者 <!ENTITY 实体名 PUBLIC "public_ID" "URI"> 。Java中引入外部实体的协议包括http、https、ftp、file、jar、netdoc、mailto等。XXE漏洞发生在应用程序解析来自外部的XML数据或文件时没有禁止外部实体的加载，造成任意文件读取、内网端口扫描、内网网站攻击、DoS攻击等危害。

**【修改建议】**
为了避免 XXE 注入，应对 XML 解析器进行安全配置，使它不允许将外部实体包含在传入的 XML 文档中。

**【正例】**
禁止解析外部一般实体和外部参数实体。

```java
private void parserXmlFileDisableExternalEntityes(String filePath) {
    try {
        DocumentBuilderFactory dbf = DocumentBuilderFactory.newInstance();
        dbf.setFeature("http://apache.org/xml/features/disallow-doctype-decl", false);
        dbf.setFeature("http://xml.org/sax/features/external-general-entities", false);
        dbf.setFeature("http://xml.org/sax/features/external-parameter-entities", false);
        DocumentBuilder db = dbf.newDocumentBuilder();
        Document doc = db.parse(new File(filePath));
        ... // 解析xml文件中的内容
    } catch (ParserConfigurationException ex) {
        // 处理异常
    }
        ...
}

```

**【反例】**
下列示例中解析XML文件时未进行安全防护，当解析的XML文件是恶意用户精心构造的，系统会受到XXE攻击。
```java
private void parseXmlFile(String filePath) {
    try {
        DocumentBuilderFactory dbf = DocumentBuilderFactory.newInstance();
        DocumentBuilder db = dbf.newDocumentBuilder();
        Document doc = db.parse(new File(filePath));
        ... // 解析xml文件中的内容
    } catch (ParserConfigurationException ex) {
        // 处理异常
    }
    ...
}
```

#### G.EDV.06 防止解析来自外部的XML导致的内部实体扩展（XML Entity Expansion）攻击【要求】

**【描述】**
XML内部实体攻击。

XML内部实体格式： <!ENTITY 实体名 "实体的值"\> 。内部实体攻击比较常见的是XML Entity Expansion攻击，它主要试图通过消耗目标程序的服务器内存资源导致DoS攻击。

**【修改建议】**
为了避免 XXE 注入，应对 XML 解析器进行安全配置，使它不允许将外部实体包含在传入的 XML 文档中。

**【正例】**
场景1：不使用XML实体
- 修复示例：完全禁用该工厂的DTD。
```java
XMLInputFactory xmlInputFactory = XMLInputFactory.newInstance();

// 【GOOD】这将完全禁用该工厂的DTD
xmlInputFactory.setProperty(XMLInputFactory.SUPPORT_DTD, false);
XMLStreamReader reader = xmlInputFactory.createXMLStreamReader(new FileInputStream(fileName));
```
场景2：不使用外部实体，需要使用内部实体
- 修复示例：禁止外部实体解析，且限制内部实体数量为10个以内
```java
XMLInputFactory xmlInputFactory = XMLInputFactory.newInstance();

// 【GOOD】禁用外部实体
xmlInputFactory.setProperty(XMLInputFactory.IS_SUPPORTING_EXTERNAL_ENTITIES, false);

// 【GOOD】使用系统属性限制
System.setProperty("entityExpansionLimit", "10");
XMLStreamReader reader = xmlInputFactory.createXMLStreamReader(new FileInputStream(fileName));
```

**【反例】**
场景1：不使用XML实体
- 错误示例：XML解析器默认开启实体解析
```java
XMLInputFactory xmlInputFactory = XMLInputFactory.newInstance();
XMLStreamReader reader = xmlInputFactory.createXMLStreamReader(new FileInputStream(fileName)); // POTENTIAL FLAW: 未禁止实体解析
```
场景2：不使用外部实体，需要使用内部实体
- 错误示例：禁止外部实体解析，但未限制内部实体数量
```java
XMLInputFactory xmlInputFactory = XMLInputFactory.newInstance();

// POTENTIAL FLAW: 未限制内部实体数量
xmlInputFactory.setProperty(XMLInputFactory.IS_SUPPORTING_EXTERNAL_ENTITIES, false);
XMLStreamReader reader = xmlInputFactory.createXMLStreamReader(new FileInputStream(fileName));
```

#### G.EDV.07 禁止使用不安全的XSLT转换XML文件【要求】

**【描述】**
XSLT是一种样式转换标记语言，可以将XML数据转换为另外的XML或其他格式，如HTML网页，纯文字。因为XSLT的功能十分强大，可以导致任意代码执行，当使用TransformerFactory转换XML格式数据的时候，需要添加安全策略禁止不安全的XSLT代码执行。

**【修改建议】**
使用TransformerFactory对xml进行格式转换操作时，要开启其安全防护策略，参考修复示例。

**【正例】**
场景1：使用TransformerFactory转换XML格式数据需开启安全策略
- 修复示例：开启安全防护策略
```java
//create transformer after executing setFeature
public static void XsltTrans(String src, String dst, String xslt) {
    TransformerFactory tf = TransformerFactory.newInstance();
    tf.setAttribute(XMLConstants.ACCESS_EXTERNAL_DTD, "");
    tf.setAttribute(XMLConstants.ACCESS_EXTERNAL_STYLESHEET, "");
    try {

        // 【GOOD】转换器工厂设置黑名单，禁用一些不安全的方法，类似XXE防护
        tf.setFeature("http://javax.xml.XMLConstants/feature/secure-processing", true);

        // 获取转换器对象实例
        Transformer transformer = tf.newTransformer(new StreamSource(xslt));

        // 进行转换
        transformer.transform(new StreamSource(src), new StreamResult(new FileOutputStream(dst)));
    } catch (Exception e) {
        LOGGER.error(e.getMessage());
    }
}
```

**【反例】**
场景1：使用TransformerFactory转换XML格式数据需开启安全策略
- 错误示例：不添加安全策略。

```java
// transformer of StreamSource without setFeature
public static void XsltTrans(String src, String dst, String xslt) {
    TransformerFactory tf = TransformerFactory.newInstance();
    tf.setAttribute(XMLConstants.ACCESS_EXTERNAL_DTD, "");
    tf.setAttribute(XMLConstants.ACCESS_EXTERNAL_STYLESHEET, "");
    try {
        // 获取转换器对象实例
        /* 【POTENTIAL FLAW】XSLT是一种样式转换标记语言，可以将XML数据档转换为另外的XML或其它格式，
         * 如HTML网页，纯文字。因为XSLT的功能十分强大，可以导致任意代码执行，
         * 当使用TransformerFactory转换XML格式数据的时候，需要添加安全策略禁止不安全的XSLT代码执行。
         */
        Transformer transformer = tf.newTransformer(new StreamSource(xslt));

        // 进行转换
        transformer.transform(new StreamSource(src), new StreamResult(new FileOutputStream(dst)));
    } catch (Exception e) {
        LOGGER.error(e.getMessage());
    }
}
```

#### G.EDV.08 正则表达式要尽量简单，防止ReDos攻击【要求】

**【描述】**
正则编写不当导致ReDos攻击。

ReDos攻击是正则编写不当导致的常见安全风险。Java中的正则匹配使用的是NFA引擎。NFA引擎的回溯机制，导致当字符串文本与正则表达式不匹配时，所花费的时间要比匹配时多，即要确定匹配失败， 需要与所有可能的路径进行对比匹配，证明都不匹配时，才返回匹配失败。当使用简单的非分组正则表 达式时，一般不会存在ReDos攻击。容易存在ReDos攻击的正则表达式主要有两类：
* 包含具有自我重复的重复性分组的正则，例如：^(\d+)+$、^(\d*)*$、^(\d+)*$、^(\d+|\s+)*$
* 包含替换的重复性分组，例如：^(\d|\d|\d)+$、^(\d|\d?)+$

**【修改建议】**
对于ReDos攻击的防护手段主要包括：
* 进行正则匹配前，先对匹配的文本的长度进行校验；
* 在编写正则时，尽量不要使用过于复杂的正则，尽量少用分组，例如对于正则 ^(([a-z])+\.)+[A-Z]([a-z])+$ （存在ReDos风险），可以将多余的分组删除： ^([a-z]+\.)+[A-Z][a-z]+$ ，这样在不改变检查规则的前提下消除了ReDos风险；
* 避免动态构建正则，当使用外部数据构造正则时，要使用白名单进行严格校验。

**【正例】**
将正则表达式精简为a[bc]+d。与a(b|c+)+d相比，可以在实现相同功能的前提下消除ReDos风险。
```java
private static final Pattern REGEX_PATTER = Pattern.compile("a[bc]+d");
public static void main(String[] args) {
    ...
    Matcher matcher = REGEX_PATTER.matcher(args[0]);
    if (matcher.matches()) {
        ...
    } else {
        ...
    }
    ...
}
```

**【反例】**
正则表达式 a(b|c+)+d 存在ReDos风险，当匹配的字符串格式类似"accccccccccccccccx"时，随中间的字符"c"的增加，代码执行时间将成指数级增长。
```java
private static final Pattern REGEX_PATTER = Pattern.compile("a(b|c+)+d");
public static void main(String[] args) {
    ...
    Matcher matcher = REGEX_PATTER.matcher(args[0]);
    if (matcher.matches()) {
        ...
    } else {
        ...
    }
    ...
}
```

#### G.EDV.09 禁止直接使用外部数据作为反射操作中的类名/方法名【要求】

**【描述】**
直接使用外部数据作为反射操作中的类名/方法名。

反射操作中直接使用外部数据作为类名或方法名，会导致系统执行非预期的逻辑流程（Unsafe Reflection）。这可被恶意用户利用来绕过安全检查或执行任意代码。当反射操作需要使用外部数据时，必须对外部数据进行白名单校验，明确允许访问的类或方法列表；另外也可以通过让用户在指定范围内选择的方式进行防护。

**【修改建议】**
使用白名单的方式对外部类名/方法名进行校验。

**【正例】**
场景1：
- 修复示例1：外部只能指定要反射的类的代号

```java
String classIndex = request.getParameter("classIndex");
String className = (String) reflectClassesMap.get(classIndex);
if (className != null) {
    Class objClass = Class.forName(className);
    BaseClass obj = (BaseClass) objClass.newInstance();
    obj.doSomething();
} else {
    throw new IllegalStateException("Invalid reflect class!");
}
...
```
- 修复示例2：对外部数据进行白名单校验
```java
String classIndex = request.getParameter("classIndex");
if (whiteList.contains(classIndex)) {
    Class objClass = Class.forName(className);
    BaseClass obj = (BaseClass) objClass.newInstance();
    obj.doSomething();
} else {
    throw new IllegalStateException("Invalid reflect class!");
}
...
```

**【反例】**
场景1：
- 错误示例：直接使用外部指定的类名通过反射构造了一个对象

```java
String className = request.getParameter("class");
...
Class objClass = Class.forName(className);
BaseClass obj = (BaseClass) objClass.newInstance();
obj.doSomething();
```

## 2.13 日志
#### G.LOG.01 记录日志应该使用Facade模式的日志框架【要求】

**【描述】**
专用日志工具与控制台打印（System.out、System.err）相比，提供了更丰富的日志记录功能，且使用更加简单。日志打印推荐使用Facade模式的日志框架，如第三方slf4j、产品自研日志框架等，不要使用System.out与System.err进行控制台打印。

**【修改建议】**
使用日志打印。

**【正例】**
采用日志工具输出日志，例如slf4j+logback。
```java
start = System.currentTimeMillis();
// 其他加载数据的代码
LOGGER.info("items loaded, use {}ms.", (System.currentTimeMillis() - start));
```

**【反例】**
```java
start = System.currentTimeMillis();
// 其他加载数据的代码
System.out.println ("items loaded, use " + (System.currentTimeMillis() - start) + "ms.");
```

#### G.LOG.02 日志工具Logger类的实例必须声明为private static final或者private final【要求】

**【描述】**
对于工具类的实例，如果声明时并进行了初始化，应该声明为private static final，如果只是声明但未初始化，则应声明为private final。

- 声明为private是出于访问封装的考虑，防止Logger类的实例对象被其他类非法使用；
- 声明为static是为了防止重复new出Logger类的实例，造成资源的浪费，同时防止实例被序列化，造成安全风险（精心设计的library除外）；
- 声明为final是因为在类的生命周期内无需变更Logger类的实例。

**【修改建议】**
日志工具实例，应该声明为`private static final`或`private final`。

**【正例】**
场景1：
- 修复示例：
```java
private static final Logger logger = LoggerFactory.getLogger(CheckUpdateToAutoRenewStep.class);
```

**【反例】**
场景1：
- 错误示例：没有使用final修饰日志实例
```java
private static Logger logger = LoggerFactory.getLogger(CheckUpdateToAutoRenewStep.class);
```

#### G.LOG.03 日志必须分等级【要求】

**【描述】**
如果日志不分等级，则定位问题时，无法快速有效屏蔽大量低级别信息，给快速定位带来难度。

日志可分为以下级别：trace（有的也叫verbose）、debug、info、warning、error、fatal。

**【修改建议】**
推荐与具体实现有关的日志记录trace或debug级，一般的业务处理日志用info级，不影响业务进行的错误用warning级，例如用户输入参数错误。而error或fatal级，只记录系统逻辑出错、异常或者重要的错误信息，常常向运维系统报警。

建议生产环境不输出trace或debug日志；有选择地输出info日志；输出warning、error、fatal日志。

对info及以下级别的日志，应使用条件形式或占位符的方式进行输出。

**【正例】**
场景1： 对于info及以下级别的日志，应该避免直接进行日志内容拼接
- 修复示例：对info及以下级别的日志，使用条件形式或占位符的方式进行日志内容的构造

  ```java
  // 如果日志库提供了带"msgSupplier"的API，如下这样调用可以消除不必要的消息创建
  LOGGER.debug(() ->
      "Processing trade with id: " + id + " and symbol: " + symbol.fetchBigMessage());

  // 采用条件方式
  if (LOGGER.isDebugEnabled()) {
      LOGGER.debug("Processing trade with id: " + id + " and symbol: " + symbol);
  }

  // 或者使用占位符
  LOGGER.debug("Processing trade with id: {} and symbol: {}" , id, symbol);
  ```

**【反例】**
场景1： 对于info及以下级别的日志，应该避免直接进行日志内容拼接
- 错误示例：对info及以下级别的日志，直接进行字符串拼接

  ```java
  LOGGER.debug("Processing trade with id: " + id + " and symbol: " + symbol);
  ```

#### G.LOG.04 非仅限于中文区销售产品禁止用中文打印日志【要求】

**【描述】**
建议日志内容统一只用英文字符，避免使用中文字符，尤其是注意中文标点符号。统一日志的字符集，有利于对日志的自动化分析处理。

**【修改建议】**
将日志中的中文字符、标点等替换为英文。

**【正例】**
场景1： 出现用中文打印日志
- 修复示例1：用英文打印日志

  ```java
  String body = getRequestBodyData(request);
  try {
      handeData(body);
  }catch(MyBizException ex) {
      LOG.error("handle request data failed!");
  }
  ```

**【反例】**
场景1： 出现用中文打印日志
- 错误示例：

  ```java
  String body = getRequestBodyData(request);
  try {
      handeData(body);
  }catch(MyBizException ex) {
      LOG.error("在处理请求数据时出现了异常！");
  }
  ```

#### G.LOG.05 禁止直接使用外部数据记录日志【要求】

**【描述】**
日志注入。

直接将外部数据记录到日志中，可能存在以下风险：
* 日志注入：恶意用户可利用回车、换行等字符注入一条完整的日志；
* 敏感信息泄露：当用户输入敏感信息时，直接记录到日志中可能会导致敏感信息泄露；
* 垃圾日志或日志覆盖：当用户输入的是很长的字符串，直接记录到日志中可能会导致产生大量垃圾 日志；当日志被循环覆盖时，这样还可能会导致有效日志被恶意覆盖。

**【修改建议】**
外部数据应尽量避免直接记录到日志中，如果必须要记录到日志中，要进行必要的校验及过滤处理，对于较长字符串可以截断。对于记录到日志中的数据含有敏感信息时，对于秘钥、口令类的敏感信息，将这些敏感信息替换为固定长度的*，对于其他类的敏感信息（如手机号、邮箱等）需要做匿名化处理。

**【正例】**
场景1：
- 修复示例：外部数据写入日志前，先将其中的`\r\n`等导致换行的字符进行替换，消除日志注入风险。

```java
String jsonData = getRequestBodyData(request);
if (!validateRequestData(jsonData)) {
    LOG.error("Request data validate fail! Request Data : " + replaceCRLF(jsonData));
}

public String replaceCRLF(String message) {
    if (message == null) {
        return "";
    }
    return message.replace('\n', '_').replace('\r', '_');
}

```

**【反例】**
场景1：
- 错误示例：当请求的json数据校验失败，会直接将json字符串记录到日志中，可能导致发生敏感数据泄露、或者日志注入、日志冗余。

```java
String jsonData = getRequestBodyData(request);
if (!validateRequestData(jsonData)) {
    LOG.error("Request data validate fail! Request Data : " + jsonData);
}
```

## 2.14 性能和资源管理
#### G.PRM.01 将集合转为数组时使用Collection<T>.toArray(T[])方法；Java 11后使用Collection<T>.toArray(IntFunction<T[]>)【要求】

**【描述】**
对于将集合转为数组操作，Java 11引入了`Collection<T>.toArray(IntFunction<T[]> generator)`，它更好的原因是不需要创建临时数组，一方面节省空间，另一方面这样就不用去考虑`toArray(T[])`里的参数长度对方法行为以及结果的影响。

另外，java.util.stream中各Stream的`toArray()`、`toArray(IntFunction<A[]>)`也是常用的。

Java 11前`toArray(T[] a)`的参数应采用**零长度的数组**，这样可保证有更好的性能。数组容量大小产生的影响如下：

- 等于0，动态创建与size相同的数组，性能最好；
- 大于0但小于size，重新创建大小等于size的数组，增加GC负担；
- 等于size，在高并发情况下，数组创建完成之后，size正在变大的情况下，负面影响与上相同；
- 大于size，空间浪费，且在size处插入null值，存在NullPointerException隐患。

**【修改建议】**
将集合转为数组时推荐使用`Collection<T>.toArray(T[])`方法，参数应采用**零长度的数组**；Java 11后使用`Collection<T>.toArray(IntFunction<T[]>)`

**【正例】**
场景1：集合转数组操作
- 修复示例1：

  ```java
  List<String> list = new ArrayList<>(DEFAULT_CAPACITY);
  list.add(getElm());
  ...
  String[] array = list.toArray(new String[0]);
  ```
- 修复示例2：Java11+

  ```java
  List<String> list = new ArrayList<>(DEFAULT_CAPACITY);
  list.add(getElm());
  ...
  String[] array = list.toArray(String[]::new);
  ```

**【反例】**
场景1：集合转数组操作
- 错误示例：

  ```java
  List<String> list = new ArrayList<>(DEFAULT_CAPACITY);
  list.add(getElm());
  ...
  String[] array = list.toArray(new String[DEFAULT_CAPACITY + 1]);
  ```

#### G.PRM.02 使用System.arraycopy()或Arrays.copyOf()进行数组复制【建议】

**【描述】**
在将一个数组对象复制成另外一个数组对象时，不要自己使用循环复制，可以使用Java提供的`System.arraycopy()`功能来复制数据对象，这样做可以避免出错，而且效率会更高。`java.util.Arrays.copyOf()`是对`System.arraycopy()`便利化封装。数组复制有如下特性：

- 对于一维数组，且数组元素为基本类型或String类型时，数组复制属于深复制，即复制后的数组与原始数组的元素互不影响；
- 对于多维数组，或一维数组中的元素是引用类型时，数组复制属于浅复制，即复制后的数组与原始数组的元素引用指向的是同一个对象。

**【修改建议】**
使用`System.arraycopy()`或`Arrays.copyOf()`进行数组复制。

**【正例】**
场景1： 使用for循环进行数组复制
- 修复示例1：使用`System.arraycopy()`进行数组复制

  ```java
  int[] src = {1, 2, 3, 4, 5};
  int[] dest = new int[5];
  System.arraycopy(src, 0, dest, 0, 5);
  ```

**【反例】**
场景1： 使用for循环进行数组复制
- 错误示例：

  ```java
  int[] src = {1, 2, 3, 4, 5};
  int[] dest = new int[5];
  for (int i = 0; i < 5; i++) {
      dest[i] = src[i];
  }
  ```

#### G.PRM.03 初始化集合时，如果可预估元素数量，应该指定初始化大小【建议】

**【描述】**
集合有扩容机制，每次向集合中添加元素时，都会检测当前元素数量是否达到触发扩容的阈值。达到阈值后，会重新生成一段更大的内存段，然后将原来的内存里面的数据拷贝到新的内存段中，这个过程比较消耗资源，有性能损耗，尤其是集合需要添加大量元素时会导致集合多次扩容。

在集合初始化时指定其初始化容量，可以有效避免向集合中添加元素时触发其扩容机制。如果无法预估集合的容量或者集合中仅存放少量元素时，可以直接使用其默认值DEFAULT_INITIAL_CAPACITY.
对于HashMap这类具有负载因子的集合，在设置初始化容量时考虑负载因子的影响，这样才能正确避免扩容。

**【正例】**
```java
public static ListM<String> decorate(String[] personDescs) {
    List<String> personNames = new ArrayListM<>(personDescs.length);
    for (String personDesc : personDescs) {
        String personName = getPersonName(personDesc);
        personName.add(personName);
    }
    return personNames;
}
```

**【反例】**
```java
public static ListM<String> decorate(String[] personDescs) {
    List<String> personNames = new ArrayListM<>();
    for (String personDesc : personDescs) {
        String personName = getPersonName(personDesc);
        personName.add(personName);
    }
    return personNames;
}
```

#### G.PRM.04 不要对正则表达式进行频繁重复预编译【要求】

**【描述】**
在频繁调用的场景（例如在方法体内或循环语句中）中，定义Pattern会导致重复预编译正则表达式，降低程序执行效率。另外，对于JDK中的某些API会接受字符串格式的正则表达式作为参数，如`String.replaceAll`、`String.split`等，对于这些API的使用也要考虑性能问题。

**【修改建议】**
扩大Pattern的作用域，如用类属性的方式，避免正则表达式从重复编译。

**【正例】**
场景1： 方法内定义Pattern，方法频繁被调用时导致正则表达式重复预编译
- 修复示例：将Pattern定义为类属性

  ```java
  public class RegexExp {
      private static final Pattern CHARSET_REG = Pattern.compile("[a-z]+");

      // 该方法被频繁调用
      private boolean isLowerCase(String str) {
          if (CHARSET_REG.matcher(str).find()) {
              return true;
          }
          return false;
      }
  }
  ```
场景2： for循环内定义Pattern，导致正则表达式重复预编译
- 修复示例：将Pattern定义为类属性

  ```java
  public class RegexExp {
      private static final Pattern CHARSET_REG = Pattern.compile("[a-z]+");

      private void doSomething(String[] args) {
          int count = 0;
          for (String str : args) {
              if (CHARSET_REG.matcher(str).find()) {
                  count++;
              }
          }
          ...
      }
  }
  ```

**【反例】**
场景1： 方法内定义Pattern，方法频繁被调用时导致正则表达式重复预编译
- 错误示例：

  ```java
  public class RegexExp {
      // 该方法被频繁调用
      private boolean isLowerCase(String str) {
          Pattern pattern = Pattern.compile("[a-z]+");
          if (pattern.matcher(str).find()) {
              return true;
          }
          return false;
      }
  }
  ```
场景2： for循环内定义Pattern，导致正则表达式重复预编译
- 错误示例：

  ```java
  public class RegexExp {
      private void doSomething(String[] args) {
          int count = 0;
          for (String str : args) {
              Pattern pattern = Pattern.compile("[a-z]+");
              if (pattern.matcher(str).find()) {
                  count++;
              }
          }
          ...
      }
  }
  ```
#### G.PRM.05 禁止创建不必要的对象【要求】

**【描述】**
重用一个已经创建的对象比创建一个新的对象要好得多，除非确实需要重新创建。创建重复不必要的对象会导致资源浪费，严重时可能会导致性能问题。

**【修改建议】**
对于基本数据类型，建议避免使用封装类型导致的重复创建冗余对象；对于字符串常量避免使用`new String("xxx")`操作。

**【正例】**
场景1：
- 修复示例：直接用基本类型创建数据或直接使用字符串常量，避免创建冗余对象

  ```java
  String foo = "string";
  Integer bar = Integer.valueOf(90);
  ...
  Integer baz = Integer.valueOf(90); // 默认在-128~127间，会重用内存中缓存的对象
  ```

**【反例】**
场景1：
- 错误示例：创建冗余的String、封装的基本类型对象

  ```java
  String foo = new String("string"); // 建立了2个String对象
  Integer bar = new Integer(90);
  ...
  Integer baz = new Integer(90);
  ```

#### G.PRM.06 将对象存入HashSet，或作为Key存入HashMap(或HashTable)后，必须确保该对象的HashCode值不变【要求】

**【描述】**
对于Hash集合（HashMap, HashSet等）而言，对象的hashcode至关重要，在Hash集合内查找该对象完全依赖此值。如果一个对象存入Hash集合后hashcode随即发生变化，结果就是无法在集合内找到该对象，进而不能删除该对象，最终导致内存泄露

**【反例】**
```java
public class Email {
    public String address;

    public Email(String address) {
        this.address = address;
    }

    public int hashCode() {
        return address.hashCode();
    }

    public static void main(Stringp[] args) {
        HashSet<Email> set = new HashSet<>();
        Email email = new Email("xxx.com");
        set.add(email);
        email.address = "xxx1.com"; // 修改地址值，导致hashcode值变化
        System.outprintln(set.contains(email)); // 错误
        set.remove(email); // 泄露
    }
}
```

#### G.PRM.07 进行IO类操作时，必须在try-with-resource或finally里关闭资源【要求】

**【描述】**
申请的资源不再使用时，需要及时释放，否则会导致资源泄露问题。释放后的资源不要继续使用，否则可能导致系统抛出异常或其他未知不安全行为。

**【修改建议】**
系统异常可能导致资源释放操作被跳过，因此对于IO、数据库操作等需要显式调用关闭方法（如`close()`）来释放资源的场景，必须在try-catch-finally的finally中调用关闭方法。如果有多个资源需要`close()`，需要分别对每个资源`close()`时的异常进行try-catch处理，防止某个资源关闭失败导致其他资源无法正常关闭，最终保证所有资源都能被正确释放。

Java 7有自动资源管理的特性try-with-resource，不需手动关闭。该方式应该优先于try-finally，这样得到的代码将更加简洁、清晰，产生的异常也更有价值。特别是对于多个资源关闭发生异常时，try-finally可能丢失掉前面的异常，而try-with-resource会保留第一个异常，并把后续的异常作为Suppressed exceptions，可通过`getSuppressed()`获取这些异常信息。

**【正例】**
场景1：
- 修复示例1：在finally中释放资源

  ```java
  public void doSomething() {
      FileInputStream in = null;
      try {
          in = new FileInputStream(inputFileName);
      } catch (IOException e) {
          ...
      } finally {
          ...
          in.close();
      }
  }
  ```
- 修复示例2：使用try-with-resource机制，保证资源正确释放

  ```java
  try (FileOutputStream fop = new FileOutputStream(file)) {
      fop.write(buf);
  }
  ```

**【反例】**
场景1：
- 错误示例：方法抛出异常时，资源可能无法正确释放

  ```java
  public void doSomething() {
      FileInputStream in = null;
      try {
          in = new FileInputStream(inputFileName);
          in.close();
      } catch (IOException e) {
          int aaaa = 1;
      }
  }
  ```

#### G.PRM.08 禁止使用主动GC（除非在密码、RMI等方面），尤其是在频繁/周期性的逻辑中【要求】

**【描述】**
虽然主动调用GC方法时JVM规范不承诺立即进行垃圾回收操作，但是Oracle Java SE JVM在绝大多数情况下响应此方法调用，会触发JVM的全量GC操作，这会增加GC的次数，也就增加了程序因为GC而停顿的时间；而且在GC过程中的某些阶段程序会完全停顿，这会让程序失去响应，对系统造成非常大的风险。在频率/周期性的逻辑（for循环、定时器）中更要尽量避免主动GC的调用。

**【修改建议】**
避免主动执行GC操作，尤其是不能在循环中频繁调用GC操作。

**【正例】**
场景1：
- 修复示例：不主动调用GC操作

  ```java
  for (String bookName : bookNames) {
      Book book = new Book(bookName);
      checkBook(book);
      ... // 其他操作
  }
  ```

**【反例】**
场景1：
- 错误示例：在循环中调用了`System.gc()`

  ```java
  for (String bookName : bookNames) {
      Book book = new Book(bookName);
      checkBook(book);
      ... // 其他操作
      System.gc();
  }
  ```

#### G.PRM.09 禁止使用Finalizer机制【要求】

**【描述】**
禁止主动调用对象的`finalize()`方法;
禁止覆写`finalize()`方法；
禁止调用`System.runFinalization()`与`Runtime.runFinalization()`。

**【修改建议】**
删除对象的`finalize()`方法调用。
删除覆写`finalize()`方法;
删除调用`System.runFinalization()`与`Runtime.runFinalization()`。

**【正例】**
场景1：
- 修复示例1：

```java
void doSomething() {
    NetworkDemo demo = new NetworkDemo();
    ...     
}
```

**【反例】**
场景1：
- 错误示例1：主动调用对象的`finalize()`方法

```java
  void doSomething() {
      NetworkDemo demo = new NetworkDemo();
      ...
      demo.finalize();        
  }
```

- 错误示例2：调用`System.runFinalization()`与`Runtime.runFinalization()`

```java
void doSomething() {
    NetworkDemo demo = new NetworkDemo();
    ...
    System.runFinalization();
}
```

#### G.PRM.10 不要创建临时变量作为return语句的返回值【建议】

**【描述】**
不要创建临时变量作为return语句的返回值，保持代码简洁。

**【修改建议】**
去除临时变量和赋值，直接内联到return语句中

**【正例】**
场景1：
- 修复示例： 

  ```java
  private List<String> func() {
      return solve();
  }
  ```

**【反例】**
场景1：
- 错误示例：

  ```java
  private List<String> func() {
      List<String> res = solve();
      return res;
  }
  ```

## 2.15 平台安全
#### G.SEC.01 进行安全检查的方法必须声明为private或final【要求】

**【描述】**
安全检查方法可能被子类重写。

实现安全检查功能（主要是指调用SecurityManager执行的安全检查）的方法，如果可以被子类重写，恶意子类可以重写安全检查方法，忽略这些安全检查，使安全检查失效。所以安全检查相关的方法必须声明为private或final，防止被子类重写。

**【修改建议】**
请确保所有执行安全操作的方法都已在 final 类中声明，或者这些方法本身已声明为final/private。

**【正例】**
场景1：安全检查的方法不声明为private或final。
- 修复示例1：安全检查的方法声明为private
```java
// 【GOOD】安全检查的方法声明为private
private void doSomething() {
    AccessController.checkPermission(new SecurityPermission("SomeAction"));
    ...
}
```
- 修复示例2：安全检查的方法声明为final
```java
// 【GOOD】安全检查的方法声明为final
public final void doSomething() {
    AccessController.checkPermission(new SecurityPermission("SomeAction"));
    ...
}
```

**【反例】**
场景1：安全检查的方法不声明为private或final。
- 错误示例：安全检查的方法声明为public

```java       
// 【POTENTIAL FLAW】用于执行安全检查的非最终方法可能会被绕过安全检查的多种方式覆盖
public void doSomething() {
    AccessController.checkPermission(new SecurityPermission("SomeAction"));
    ...
}
```

#### G.SEC.02 自定义类加载器覆写getPermission()时，必须先调用父类的getPermission()方法【要求】

**【描述】**
自定义类加载器未调用父类的getPermissions()方法。

自定义类加载器，如果需要重写getPermissions()方法时，在给其它代码设置权限之前，必须要先调用父类的getPermissions()方法来应用默认的安全策略。自定义类加载器如果忽略调用父类的getPermissions()方法，该类加载器可以加载提升权限的不可信类。

**【修改建议】**
继承URLClassLoader类时，重载getPermissions(CodeSource)方法时需要调用super.getPermissions()。

**【正例】**
场景1：忽略调用父类的getPermissions()方法。
- 修复示例1：
```java
@Override
protected PermissionCollection getPermissions(CodeSource cs) {

    super.getPermissions(cs); // 【GOOD】调用父类的getPermissions方法
    PermissionCollection pc = new Permissions();

// allow exit from the VM anytime
    pc.add(new RuntimePermission("exitVM"));
    return pc;
}
```

**【反例】**
场景1：忽略调用父类的getPermissions()方法。
- 错误示例：

```java
@Override
protected PermissionCollection getPermissions(CodeSource cs) {

     // 【POTENTIAL FLAW】没有调用父类的getPermissions方法。
    PermissionCollection pc = new Permissions();

    // allow exit from the VM anytime
    pc.add(new RuntimePermission("exitVM"));
    return pc;
}
```

#### G.SEC.03 加载外部JAR文件时,不要依赖URLClassLoader和java.util.jar提供的默认自动签名检查机制【要求】

**【描述】**
当一些第三方代码需要提升权限执行某些操作时，供应方一般会对JAR文件进行签名以保证代码来源的可靠性和合法性。在JAVA中，URLClassLoader和java.util.jar提供了默认的自动签名检查机制，该机制通过JAR文件中包含的证书对加载的类进行检查，却没有检查证书本身的合法性。如果在加载时，合法的JAR文件被恶意JAR文件替换，并且恶意的JAR文件中也包含一个证书和被适当修改过的摘要值，那么默认的自动签名检查机制可能会被绕过，系统存在被恶意攻击的风险。

因此，仅仅靠默认的签名检查机制不足以保证JAR文件的合法性，使用者需要提供额外的程序化检查机制，比如通过一个已知的受信任的签名者来校验JAR文件中的签名信息

**【正例】**
```java
public class SafeJarLoader {
    private static final String TRUSTED_SIGNER = "CN=TrustedPublisher, OU=Security, O=MyCompany";
    
    public void loadJarSafely(String jarPath) throws Exception {
        // 1. 首先验证JAR签名
        verifyJarSignatures(jarPath);
        
        // 2. 验证通过后才加载
        URL jarUrl = new URL("file:" + jarPath);
        URLClassLoader classLoader = new URLClassLoader(new URL[]{jarUrl});
        
        // 加载并使用jar中的类
        Class<?> loadedClass = classLoader.loadClass("com.example.ExternalClass");
        Object instance = loadedClass.newInstance();
        
        // 使用加载的类...
    }
    
    private void verifyJarSignatures(String jarPath) throws Exception {
        try (JarFile jarFile = new JarFile(new File(jarPath))) {
            // 检查JAR是否已签名
            if (jarFile.getManifest() == null || jarFile.getManifest().getEntries().isEmpty()) {
                throw new SecurityException("JAR文件未签名");
            }
            
            // 验证每个条目的签名
            Enumeration<JarEntry> entries = jarFile.entries();
            while (entries.hasMoreElements()) {
                JarEntry entry = entries.nextElement();
                if (entry.isDirectory()) continue;
                
                // 读取条目以触发签名验证
                try (InputStream is = jarFile.getInputStream(entry)) {
                    while (is.read() != -1) {
                        // 只是读取内容以验证签名
                    }
                }
                
                // 检查签名者
                Certificate[] certs = entry.getCertificates();
                if (certs == null || certs.length == 0) {
                    throw new SecurityException("条目 " + entry.getName() + " 未签名");
                }
                
                // 验证签名者是否受信任
                boolean trusted = false;
                for (Certificate cert : certs) {
                    if (cert.toString().contains(TRUSTED_SIGNER)) {
                        trusted = true;
                        break;
                    }
                }
                
                if (!trusted) {
                    throw new SecurityException("条目 " + entry.getName() + " 的签名者不受信任");
                }
            }
        }
    }
}
```

**【反例】**
```java
import java.net.URL;
import java.net.URLClassLoader;

public class UnsafeJarLoader {
    public void loadJarUnsafe(String jarPath) throws Exception {
        // 反例：直接使用URLClassLoader加载，依赖默认的签名检查机制
        URL jarUrl = new URL("file:" + jarPath);
        URLClassLoader classLoader = new URLClassLoader(new URL[]{jarUrl});
        
        // 加载并使用jar中的类
        Class<?> loadedClass = classLoader.loadClass("com.example.ExternalClass");
        Object instance = loadedClass.newInstance();
        
        // 使用加载的类...
    }
}
```
#### G.SEC.04 使用安全管理器来保护敏感操作【建议】

**【描述】**
敏感操作缺少安全管理器。
所有的敏感操作必须经过安全管理器的检查，防止被不可信的代码调用。对于Java API 中的敏感操作，例如文件操作、向远程主机开放套接字连接以及创建ClassLoader 等，在源码中已经添加了安全检查的代码逻辑，开发者只需要安装安全管理器即可；对于应用本身的敏感操作，除了安装安全管理器之外，还需要自定义安全策略，并在合适的位置添加安全检查的代码。

**【修改建议】**
所有的敏感操作必须经过安全管理器的检查，防止被不可信的代码调用。

**【正例】**
场景1：
- 修复示例：

```java
public class SensitiveInfoManage {
    private static final SensitiveResourcePermission REMOVE_ENTRY_PERMISSION =
        new SensitiveResourcePermission("removeInfo");

    private final Map<Integer, String> resourceMap = new HashMap<>();

    public final boolean remove(Integer id) {
        securityCheck(); // 【GOOD】增加安全管理器检查
        return resourceMap.remove(id) != null;
    }

    private void securityCheck() {
        SecurityManager securityManager = System.getSecurityManager();
        if (securityManager != null) {
            securityManager.checkPermission(REMOVE_ENTRY_PERMISSION);
        }
    }
    ... // 其他代码
}
```
同时需要在protect.policy文件进行如下的权限配置，授权基于路径在"file:${{trusted.code.dirs}}/*"的class和jar包，所有权限。
```
grant codeBase "file:${{trusted.code.dirs}}/*" {
    permission com.huawei.security.SensitiveResourcePermission "removeInfo";
};
```

**【反例】**
场景1：
- 错误示例：

```java
public class SensitiveInfoManage {
    private final Map<Integer, String> resourceMap = new HashMap<>();

    // 【POTENTIAL FLAW】未进行安全管理器检查
    public boolean remove(Integer id) {
        return resourceMap.remove(id) != null;
    }

    ... // 其他代码
}
```

## 2.16 其他
#### G.OTH.01 安全场景下必须使用密码学意义上的安全随机数【要求】

**【描述】**
安全场景下必须使用密码学意义上的安全随机数。

不安全的随机数可能被部分或全部预测到，导致系统存在安全隐患，安全场景下使用的随机数必须是密码学意义上的安全随机数。密码学意义上的安全随机数分为两类：
1.真随机数产生器产生的随机数；
2.以真随机数产生器产生的少量随机数作为种子的密码学安全的伪随机数产生器产生的大量随机数。

已知的可供产品使用的密码学安全的非物理真随机数产生器有：Linux操作系统的/dev/random设备接口（存在阻塞问题）和Windows操作系统的CryptGenRandom接口。Java中的SecureRandom是一种密码学安全的伪随机数产生器，对于使用非真随机数产生器产生随机数时，要使用少量真随机数作为种子。常见安全场景包括但不限于以下场景：
1.用于密码算法用途，如生成IV、盐值、秘钥等；
2.会话标识（sessionId）的生成；
3.挑战算法中的随机数生成；
4.验证码的随机数生成。

**【修改建议】**
使用安全的随机数。

**【正例】**
明确指定采用sun.security.provider.SecureRandom作为随机数产生器，然后使用generateSeed()方法产生的随机数作为种子，该方法产生的随机数默认为真随机数（如linux下从/dev/random获取）。下述代码实际是使用少量真随机数作为种子（种子长度推荐不少于64bytes），然后采用伪随机数产生器来产生随机数，避免linxu下阻塞问题。对于需要生成大量随机数的场景，需要周期性补充种子，SHA1PRNG算法目前业界没有明确标准，推荐获取2^32次随机数后设置一次种子（调用一次nextBytes()、nextInt()等都计为一次获取随机数操作）。
```java
public byte[] generateSalt() {
    byte[] salt = new byte[8];
    try {
        SecureRandom random = SecureRandom.getInstance("SHA1PRNG", "SUN");
        random.setSeed(random.generateSeed(SEED_LEN));
        random.nextBytes(salt);
    } catch (NoSuchAlgorithmException ex) {
        // 处理异常
    }
    return salt;
}
```

**【反例】**
Random生成是不安全随机数，不能用做盐值。
```java
public byte[] generateSalt() {
    byte[] salt = new byte[8];
    Random random = new Random();
    random.nextBytes(salt);
    return salt;
}
```

#### G.OTH.02 必须使用SSLSocket代替Socket来进行安全数据交互【要求】

**【描述】**
在 Web 应用程序中使用基于套接字的通信往往容易出错。

当网络通信中涉及明文的敏感信息时，需要使用SSLSocket而不是Socket，Socket是明文通信，攻击者可以通过网络监听获取其中的敏感信息，通过中间人攻击对报文进行恶意篡改。SSLSocket是在Socket的基础上进行了一层安全性保护，包括身份认证、数据加密和完整性保护。

**【修改建议】**
当网络通信中涉及明文的敏感信息时，需要使用SSLSocket而不是Socket。

**【正例】**
场景1：
- 修复示例：使用加密通道传递敏感信息

```java
// server端
try {
    byte[] ip = new byte[4];
    // ...

    // 【GOOD】在敏感数据传递时，使用SSLSocket代替Socket来进行安全数据交互
    SSLServerSocketFactory sslServerSocketFactory =
        (SSLServerSocketFactory) SSLServerSocketFactory.getDefault();
    SSLServerSocket sslServerSocket =
        (SSLServerSocket) sslServerSocketFactory.createServerSocket(9999, 10, InetAddress.getByAddress(ip));
    SSLSocket sslSocket = (SSLSocket) sslServerSocket.accept();
    // ...sslSocket交由其他线程处理
} catch (IOException ex) {
    // ...处理异常
}

// client端
try {
    // 【GOOD】在敏感数据传递时，使用SSLSocket代替Socket来进行安全数据交互
    SSLSocketFactory sslSocketFactory =
        (SSLSocketFactory) SSLSocketFactory.getDefault();
    SSLSocket sslSocket = (SSLSocket) sslSocketFactory.createSocket(ip, port);
    os = sslSocket.getOutputStream();
    os.write(userInfo.getBytes(StandardCharsets.UTF_8));
    ...
} catch (IOException ex) {
    // ...处理异常
} finally {
    // ...关闭流
}
```

**【反例】**
场景1：
- 错误示例：使用明文通道传递敏感信息

```java
// server端
try {
    // 【POTENTIAL FLAW】在敏感数据传递时，直接使用了Socket，易导致信息被窃取或受中间人攻击
    ServerSocket serverSocket = new ServerSocket(8080, 10);
    Socket socket = serverSocket.accept();

    // ...socket交由其他线程处理
}catch(IOException ex) {
    // ...处理异常
}

// client端
try {
    // 【POTENTIAL FLAW】在敏感数据传递时，直接使用了Socket，易导致信息被窃取或受中间人攻击
    Socket socket = new Socket();
    socket.connect(new InetSocketAddress(ip, port), 10000);
    os = socket.getOutputStream();
    os.write(userInfo.getBytes(StandardCharsets.UTF_8));
    ...
} catch (IOException ex) {
    // ...处理异常
} finally {
    // ...关闭流
}
```

#### G.OTH.03 不用的代码段包括import，直接删除，不要注释掉【要求】

**【描述】**
不用的import，增加了代码的耦合度，不利于维护。

被注释掉的代码，无法被正常维护；当企图恢复使用这段代码时，极有可能引入易被忽略的缺陷。

正确的做法是，不需要的代码直接删除掉。若再需要时，考虑移植或重写这段代码。

这里说的注释掉代码，包括用 /** *\*/，*/* */和//。

**【修改建议】**
删除注释或无用import语句。

**【正例】**
```java
public class CodeInCommentTest {
    // [GOOD] CodeInComment
    private int age;
}
```

**【反例】**
```java
public class CodeInCommentTest {
    // 无用的注释代码
    // [BAD] CodeInComment
    // public void doSomething() {}
    /*private short a;*/
}
```

#### G.OTH.04 禁止代码中包含公网地址【要求】

**【描述】**
硬编码公网IP地址。

代码或脚本中包含用户不可见，不可知的公网地址，可能会引起客户质疑。对产品发布的软件（包含软件包/补丁包）中包含的公网地址（包括公网IP地址、公网URL地址/域名、 邮箱地址）要求如下：

1. 禁止包含用户界面不可见、或产品资料未描述的未公开的公网地址。

2. 已公开的公网地址禁止写在代码或者脚本中，可以存储在配置文件或数据库中。对于开源/第三方软件自带的公网地址必须至少满足上述第1条公开性要求。

**【修改建议】**
不要硬编码公网IP地址

**【正例】**
场景1：代码中存在硬编码IP。
- 修复示例1：可以将IP放入配置文件中：

```java
config.ip = 10.90.0.1 // 【GOOD】公网IP地址调整为在配置文件中配置，代码从配置文件中读取该IP地址并使用。
```

**【反例】**
场景1：代码中存在硬编码IP。
- 错误示例：代码中硬编码IP。

```java
public void test01Bad() {
    String publicIp = "10.90.0.1"; // 【POTENTIAL FLAW】IP地址硬编码
}
```

#### G.OTH.05 删除无效或永不执行的代码【要求】

**【描述】**
无效或永不会执行的代码通常是编程错误的结果，并且可能导致意外行为。通常在编译时，编译器会对此类代码进行优化，但是为了提高可读性并确保解决逻辑错误，应该将此类代码直接删除

**【正例】**
```java
boolean canDel = false;
if (condition()) {
    canDel = true;
}
...
if (canDel) {
    doSomething();
}
```

**【反例】**
```java
boolean canDel = false;
if (condition()) {
    canDel = false;
}
...
if (canDel) {
    doSomething();
}
```

#### G.OTH.06 禁止在用户界面、日志中暴露不必要信息【要求】

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
```java
// 用户界面友好提示
"系统暂时不可用，请稍后再试。如问题持续，请联系客服。"

// 安全的日志记录
logger.error("用户登录验证失败 - 用户名: {}，原因: {}", 
             maskSensitiveData("johndoe"), 
             "无效凭证");
             
// 敏感数据处理工具方法
public String maskSensitiveData(String input) {
    if(input == null || input.length() < 3) {
        return "***";
    }
    return input.substring(0, 2) + "****" + input.substring(input.length() - 1);
}
```

**【反例】**
```java
// 用户界面错误提示
"数据库连接失败 - 无法连接到 MySQL@10.0.0.123:3306，用户名: admin，密码验证失败"

// 日志记录
logger.error("用户登录失败 - 用户名: johndoe，尝试密码: Password123，来源IP: 192.168.1.100");
```

#### G.OTH.07 安全随机数生成器尽量复用【建议】

**【描述】**
java中的SecureRandom是一种密码学安全的伪随机数生成器，对于使用非真随机数生成器产生随机数时，要使用少量真随机数作为种子。

**【修改建议】**
为了提升真随机数种子的利用效率，应避免每次创建的SecureRandom对象仅生成一次安全随机数：
- 很多情况下，频繁获取真随机数会导致阻塞，所以应该充分利用每次获取的真随机数作为种子，尽量多的产生安全随机数
- 使用SecureRandom对象生成一次安全随机数，新生成的安全随机数的量可能小于其种子的量，伪随机数生成器完全失去其应用的价值

**【正例】**
```java
public byte[] generateSalt() {
    byte[] salt = new byte[16];
    SecureRandom random = SecureRandomUtil.getSecureRandomInstance();
    random.nextBytes(salt);
    return salt;
}
```

**【反例】**
```java
public byte[] generateSalt() {
    byte[] salt = new byte[16];
    try {
        SecureRandom random = SecureRandom.getInstance("DRBG", DrbgParameter.instantiation(256, RESEED_ONLY, NULL));
        random.setSeed(random.generateSeed(SEED_LEN));
        random.nextBytes(salt);
    }
    return salt;
}
```