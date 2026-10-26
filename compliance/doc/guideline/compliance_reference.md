# 开发者开源合规实践参考手册

## 0 关于本手册

本手册针对开发过程遇到的合规情况给出参考建议，开发者可根据自身开发情况借鉴此手册，尽量规避开源合规风险。

本文由 security SIG 合作编写。

本手册内容依据 “CC-BY-SA-4.0” 许可证进行授权，详见CC-BY-SA-4.0。

## 1 README文件参考

开源软件通常都会提供Readme文件，用于说明项目基本信息，使用户快速了解上手该项目。绝大多数代码托管平台通常也将Readme文件内容默认展示在项目首页，可以说Readme文件就是开源项目的“脸面”。
一个优秀的Readme文件，其内容通常包含项目简介、安装构建步骤、帮助反馈等栏目。

- 项目简介一般包括项目背景、主要功能、同类软件对比等，部分优秀的项目也会提供设计架构、开发路线图等内容。
- 安装构建步骤提供软件包直接安装和源码编译构建安装的详细步骤，列出编译安装环境要求及关键配置等信息。
- 帮助反馈部分提供项目详细文档链接、常见问题解答及问题反馈方式等。

以上这些栏目内容通常无固定格式，由开发者自行编写。
除此之外，强烈建议开发者在Readme文件中声明本项目的版权及开源许可证（Copyright&License）信息。

a、 一般开源项目Readme文件声明版权及开源许可证（Copyright&License）参考模板如下：

```
##Copyright&License

Copyright（c）[time] [ name of copyright holder ]
[Project Name] is licensed under [LICENSE].Please check the LICENSE file for more information.

```

b、若为从其他开源项目衍生而来的项目，其Readme文件除上述声明内容之外还需声明上游开源项目相关信息，同时说明维护策略（例如独立发展或跟踪上游适配等策略）。示例如下：

```
[Project Name] is a fork of [Original open source software name]；
```
或
```
[Project Name] fork from [Original open source software name];
You can access the source open source software address through this URL：
                                  XXXX;
```

## 2 License声明参考
开源软件必须提供开源许可证（即通常所说的License），未指定开源许可证的软件仅为代码可公开查看的软件，而不能称为开源软件。
因大多数开源许可证要求项目源代码和发行件中均需携带开源许可证全文副本，当前最佳实践为在开源软件源代码根目录下提供名为LICENSE的文件或文件夹，用于提供本项目开源许可证全文副本。

一个开源许可证文本通常包含许可证条款，条款附录，免责声明，copyright声明格式，许可证查找链接等部分或全部内容。例如MIT License全文如下：
```
MIT License

Copyright (c) <year> <copyright holders>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
 
The above copyright notice and this permission notice (including the next paragraph) shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
可以看到MIT License中提供了版权声明格式，理论上应将LICENSE文件中和替换为当前项目实际版权人信息。但因最佳实践的普遍应用，目前约定俗成LICENSE文件中类似版权信息无需强制修改也同样生效，开源项目在Readme文件或代码文件头中声明版权信息，即使未单独声明开源许可证信息，也默认该项目开源许可证为LICENSE文件提供的开源许可证。

LICENSE文件一般在项目的根目录或LICENSE文件夹中，选择依据主要是当前项目是简单项目还是大型复杂项目：

a、简单项目

只存在一种LICENSE的简单项目，其LICENSE文件一般在此项目的根目录下，将本项目对外开源所使用的许可证全文作为LICENSE文件内容。

b、大型项目

大型项目一般存在多种License需要声明，包括项目本身和其引用的第三方开源组件。
当项目本身需要声明多种许可证时，可将多种许可证统一罗列在创建的项目级LICENSE文件中。
当项目引入第三方开源组件时，第三方开源组件的License可采用两种放置方式：

- 根目录下创建项目LICENSE文件夹，并在LICENSE文件夹下以引入的第三方开源组件名称创建新文件夹，并将其对应的LICENSE文件放入该文件夹下。该方式优点是第三方组件对应License明确，缺点是后续维护较为琐碎，容易遗漏。
- 根目录下创建项目LICENSE文件夹，直接将引入的第三方开源组件所使用的License全文以License名称命名放入该文件夹下。该方式优点是维护简单，多个第三方开源组件如采用相同License只需一份LICENSE文件即可，缺点是License与第三方开源组件对应关系缺失，确认较为繁琐。

## 3 文件头版权信息编写参考

文件头版权信息一般包括copyright信息和LICENSE声明，其中copyright信息是一种软件作品署名权的体现方式，而LICENSE声明能够帮助使用者在使用时准确接收并继续传递该权属信息。

文件头版权信息原则上应该按照项目LICENSE文件中规定的格式编写。

a、部分LICENSE文件中会提供文件头版权信息格式，如项目LICENSE文件存在推荐格式，可直接按照LICENSE文件的格式编写，如下图为Mulan PSL v2 LICENSE文件提供的文件头版权信息格式：

```
Copyright (c) [Year] [name of copyright holder]
[Software Name] is licensed under Mulan PSL v2.
You can use this software according to the terms and conditions of the Mulan PSL v2. 
You may obtain a copy of Mulan PSL v2 at:
               http://license.coscl.org.cn/MulanPSL2 
THIS SOFTWARE IS PROVIDED ON AN "AS IS" BASIS, WITHOUT WARRANTIES OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO NON-INFRINGEMENT, MERCHANTABILITY OR FIT FOR A PARTICULAR PURPOSE.  
See the Mulan PSL v2 for more details.  
```

则版权信息为XXXX，时间为YYYY，许可证采用Mulan PSL v2 LICENSE的项目，文件头版权信息如下：

```
Copyright (c) XXXX  Co., Ltd. YYYY . All rights reserved.
XXX is licensed under the Mulan PSL v2.
You can use this software according to the terms and conditions of the Mulan PSL v2.
You may obtain a copy of Mulan PSL v2 at:
     http://license.coscl.org.cn/MulanPSL2
THIS SOFTWARE IS PROVIDED ON AN "AS IS" BASIS, WITHOUT WARRANTIES OF ANY KIND, EITHER EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO NON-INFRINGEMENT, MERCHANTABILITY OR FIT FOR A PARTICULAR
PURPOSE.
See the Mulan PSL v2 for more details.
```

采用其他LICENSE的项目可参考上述示例修改提供的格式。

b、 如项目LICENSE文件未提供推荐格式，可参考如下模板进行编写：

```
Copyright (c) [Year] [name of copyright holder]
[Software Name] is licensed under [Your LICENSE].
See LICENSE file for more details.  
```

如某项目版权信息为XXXX，时间为YYYY，许可证采用MIT LICENSE，文件头版权信息如下：


```
Copyright (c) XXXX Co., Ltd. YYYY. All rights reserved.
XXX is licensed under MIT LICENSE.
See LICENSE file for more details.  
```


c、 在开发过程中如需引用开源软件，则引用的开源软件文件头版权信息需完整保留，不得随意修改。如需对引用的开源软件进行修改，若修改的部分较少，可在修改文件文件头版权信息中添加修改声明，如该软件采用GPL-2.0或Apache系列LICENSE，则必须标注修改声明。修改声明格式示例如下： 

```
This file was modified by XXXX（Copyright owner）on YYYY（Time）
```


标注修改声明的文件文件头版权信息的格式示例如下：

```
Copyright (c) [Year] [name of copyright holder]
[Software Name] is licensed under [Your LICENSE].
See LICENSE file for more details.
This file was modified by XXXX（Copyright owner）on YYYY（Time）.
```

d、 若修改的篇幅较大或较有价值，需添加版权信息。

如新增代码文件，可参考上文添加版权头信息，注意LICENSE应与开源软件保持一致。

如新增较有价值的代码片段，可以注释的形式对该片段进行版权声明，参考格式如下：

```
***THE COPYRIGHT NOTICE START***
The copyright notice of this code snippet is as follows:
Copyright (c) XXXX（Copyright owner） Co., Ltd. YYYY. All rights reserved.
*******************************

……新增代码片段……

***THE COPYRIGHT NOTICE END***
```
### 扩展：采用SPDX标准声明文件头版权信息

SPDX标准同样提供了文件头版权信息推荐格式，但目前并未广泛使用。新建项目可以考虑采用该种格式，便于SCA工具识别。

标准格式如下，其中xxxx为SPDX标准下的许可证名称，yyy-yyyy为项目时间：

```
SPDX-FileCopyrightText: yyyy-yyyy [name of copyright holder] <name@example.com>
SPDX-License-Identifier: XXXX
```

首行为版权声明，次行为许可证声明，实际使用时需注明括号中的内容。

首行按顺序说明版权信息：年份，姓名，联系地址。示例如下：项目于2015年由zzzz首次发布，最后一次更新版本在2022年，则项目的版权声明如下：

```
SPDX-FileCopyrightText: 2015-2022 [zzzz] <zzzz@example.com>
```

次行内容为声明本文件所采用的开源许可证标识符。为保证开源许可证使用规范统一，防止产生歧义，该字段需按照SPDX标准规范填写，常见的开源许可证标识符可通过SPDX License 列表查询。
 
## 4 Notice文件编写参考
开源软件需提供NOTICE文件，用于显著声明开源软件的版权和许可证声明，一般将NOTICE文件放置于源代码根目录下。NOTICE文件是对开源项目中具体文件的版权与许可证的集合，其中包括：本开源软件以及第三方开源组件的相关信息。

### 4.1、新增NOTICE文件

首先需在NOTICE文件中展示本开源项目的一些信息，建议最少包括：项目名称、版权信息、许可证信息，开发人员也可根据实际情况增加其他信息。编写格式可参考如下示例：

```
%% 软件名称 NOTICE
===========================================
Copyright (c) [Year] [name of copyright holder]    
（可参考文件头版权信息编写规范）
The  xxxx   License （xxxx为该开源许可证SPDX格式）
===========================================
END OF 软件名称 NOTICE
```

如果该项目为开源衍生项目，建议给出衍生自开源软件链接。示例如下所示：

```
Fork from: https://XXXXX     #衍生项目的链接
```

为保障开发者权益，建议针对当前项目给出免责声明。在此给出参考示例如下所示：

```
THE OPEN SOURCE SOFTWARE IN THIS SOFTWARE IS DISTRIBUTED IN THE HOPE THAT IT WILL BE USEFUL, BUT WITHOUT ANY WARRANTY, WITHOUT EVEN THE IMPLIED WARRANTY OF MERCHANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE. SEE THE APPLICABLE LICENSES FOR MORE DETAILS.
```
### 4.2、添加第三方开源组件时修改NOTICE文件

在开源项目中用到新的第三方开源组件时，为保留第三方开源组件的版权和许可证声明需在NOTICE文件中进行体现，以履行通知义务。为在NOTICE文件中显著区分本开源项目和第三方开源组件，可以用THIRD-PARTY SOFTWARE NOTICES字段进行分割。建议第三方开源组件的NOTICE信息至少包括：组件名称、版权信息、许可证信息。书写格式可参考如下示例：

```
--------THIRD-PARTY SOFTWARE NOTICES---------

%% 软件名称1 NOTICE
===========================================
Copyright (c) [Year] [name of copyright holder]    
The  xxxx   License （xxxx为该开源许可证SPDX格式）
===========================================
END OF 软件名称1 NOTICE

%% 软件名称2 NOTICE
===========================================
Copyright (c) [Year] [name of copyright holder]    
The  xxxx   License （xxxx为该开源许可证SPDX格式）
===========================================
END OF 软件名称2 NOTICE
  		  .
		  .
		  .
```

NOTICE中建议说明第三方开源组件License的完整信息。如果该组件的License信息已经在源代码目录中声明，可以将该文件位置声明添加至该NOTICE中。参考格式如下所示，文件位置可根据实际情况进行修改：

```
%% 软件名称3 NOTICE
===========================================
Copyright (c) [Year] [name of copyright holder]    
The  xxxx   License （xxxx为该开源许可证SPDX格式）
See：./LICENSE/LICENSE-XXX
===========================================
END OF 软件名称3 NOTICE
```

NOTICE中也可添加第三方开源组件的功能描述，或放置第三方开源组件的官方地址/来源链接。编写格式参考如下：

```
%% 软件名称4 NOTICE
===========================================
Copyright (c) [Year] [name of copyright holder]    
The  xxxx   License （xxxx为该开源许可证SPDX格式）
Description：xxxxxxxxx
URL：xxxxx
===========================================
END OF 软件名称4 NOTICE
```

## 5 License兼容性问题判断方法
开源许可证的种类有很多，即使主流经常使用的也有上百种，大型复杂开源项目通常因引用较多第三方开源组件，会携带多种开源许可证，这些开源许可证的限制或条件是否存在冲突，能否共存于同一个项目，即称为开源许可证（License）兼容问题。例如某项目存在Apache-2.0和GPL-2.0-only两种开源许可证，因Apache-2.0中带有的专利条款与GPL-2.0-only中不得附加其他任何限制的条款冲突，整个项目既不能按照Apache-2.0协议来发布，也不能用GPL-2.0-only发布，这种冲突统称为License兼容性问题。

### 5.1 兼容性情况分类

LICENSE之间的兼容性分为三种兼容情况：双向兼容，单向兼容和互不兼容。假设两个开源许可证分别为A和B，以下举例说明三种情况：

双向兼容是指两种许可证可任意组合成其中一种许可证。

$$
A + B => A  \\  A + B => B
$$
单向兼容是指两种许可证组合只可组合成一种许可证。

$$
A + B => A  \\
A + B \neq> B
$$
互不兼容是指两种许可证互相都不能组合。
$$
A + B \neq> A  \\  A + B \neq> B
$$



### 5.2 兼容性问题的情境概述

通常在以下两种情境需要考虑LICENSE兼容性问题：

- 新项目立项时，确定项目自身开源许可证

  新项目需确定是否引用第三方开源组件作为核心组件，如不存在此类引用，可根据个人喜好或商业策略等因素自行确定项目开源许可证；
  如存在此类引用，则需梳理全部第三方开源组件采用的开源许可证列表，采用与该列表兼容（双向或单向兼容均可）的开源许可证作为新项目开源许可证。

- 项目本身开源许可证已确定，引入第三方开源组件或代码

  引入第三方开源组件或代码时，需确保其开源许可证与项目开源许可证双向兼容或单向兼容的结果为项目开源许可证。

  为什么不能单向兼容引入组件的开源许可证呢？如单向兼容的结果为引入组件开源许可证，则项目开源许可证需要变更至引入组件开源许可证，此情况下项目开源许可证变更可能导致与已引入的其他第三方开源组件或代码开源许可证冲突，因此不建议采用此种方案。

### 5.3 LICENSE兼容性判断

a、首先根据上述情境确定项目基本情况，即哪些开源许可证是我们的判断内容，其对应开源组件以何种方式引入本项目（一般只需判断是否为动态库原样引用）。

b、寻找合适的工具或文档判别上述开源许可证之间是否存在冲突，推荐工具或文档如下：

- [可信开源/开源许可证兼容性指南](https://gitee.com/trustworthy-open-source-community/License-Compatibility/blob/master/开源许可证兼容性指南.md/)
- [GPL系列开源许可证与其他开源许可证兼容性](https://www.gnu.org/licenses/license-list.html#GPLCompatibleLicenses)

c、若查询结束仍存在不理解或未查询到想要的结果，可以选择：

- 咨询公司法务，协助阅读相应开源许可协议，判断是否兼容
- 与 security SIG 交流。提交两种许可证辨别是否冲突的 issue。

d、如最终结论为两种开源许可证之间存在冲突，则可以采取以下措施解决兼容冲突问题：

- 放弃引入带有冲突开源许可证的三方开源组件或代码，转而寻找替代品或自研实现
- 如可满足软件功能需求，在符合开源许可证限制的前提下，可考虑进程隔离，分别分发
- 小型简单项目可以考虑更换项目本身开源许可证（建议以大版本号更新＋显著声明明确告知用户许可证变更）

## 6 项目 License 声明书写参考
项目 License 声明代表软件整体应遵守的开源许可证情况，为解决因许可证格式不统一引起的歧义(例如Apache-2.0，被简写为ASL-2.0、Apache-2、Apache License v2.0等)，应按照SPDX格式要求统一 License 声明的书写格式。书写规范如下：
###  6.1、针对单一许可证

在确定好开源许可证的前提下，以 SPDX 格式书写项目 License 声明，可通过[https://spdx.org/licenses/](https://spdx.org/licenses/) 查找开源许可证的书写格式，现给出常见开源许可证的书写格式如下表所示：

| ***\*开源许可证完整名称\****                                          | ***\*SPDX格式标识符\**** |
| ------------------------------------------------------------ | -------------------- |
| BSD Zero Clause License                                      | 0BSD                 |
| GNU Affero General Public License v3.0 only                  | AGPL-3.0-only        |
| GNU Affero General Public License v3.0 or later              | AGPL-3.0-or-later    |
| Apache License 2.0                                           | Apache-2.0           |
| Artistic License 2.0                                         | Artistic-2.0         |
| BSD 1-Clause License                                         | BSD-1-Clause         |
| BSD 2-Clause "Simplified" License                            | BSD-2-Clause         |
| BSD 3-Clause "New" or "Revised" License                      | BSD-3-Clause         |
| BSD 4-Clause "Original" or "Old" License                     | BSD-4-Clause         |
| Creative Commons Attribution 4.0 International               | CC-BY-4.0            |
| Creative Commons Attribution Non Commercial 4.0 International | CC-BY-NC-4.0         |
| Creative Commons Attribution Non Commercial No Derivatives 4.0 International | CC-BY-NC-ND-4.0      |
| Creative Commons Attribution Non Commercial Share Alike 4.0 International | CC-BY-NC-SA-4.0      |
| Creative Commons Attribution No Derivatives 4.0 International | CC-BY-ND-4.0         |
| Creative Commons Attribution Share Alike 4.0 International   | CC-BY-SA-4.0         |
| Creative Commons Zero v1.0 Universal                         | CC0-1.0              |
| GNU General Public License v1.0 only               | GPL-1.0-only                  |
| GNU General Public License v1.0 or later           | GPL-1.0-or-later              |
| GNU General Public License v2.0 only               | GPL-2.0-only                  |
| GNU General Public License v2.0 or later           | GPL-2.0-or-later              |
| GNU General Public License v3.0 only               | GPL-3.0-only                  |
| GNU General Public License v3.0 or later           | GPL-3.0-or-later              |
| GNU Library General Public License v2 only         | LGPL-2.0-only                 |
| GNU Library General Public License v2 or later     | LGPL-2.0-or-later             |
| GNU Lesser General Public License v2.1 only        | LGPL-2.1-only                 |
| GNU Lesser General Public License v2.1 or later    | LGPL-2.1-or-later             |
| GNU Lesser General Public License v3.0 only        | LGPL-3.0-only                 |
| GNU Lesser General Public License v3.0 or later    | LGPL-3.0-or-later             |
| MIT License                                        | MIT                           |
| MIT No Attribution                                 | MIT-0                         |
| Mozilla Public License 2.0                         | MPL-2.0                       |
| Mozilla Public License 2.0 (no copyleft exception) | MPL-2.0-no-copyleft-exception |
| Mulan Permissive Software License, Version 1       | MulanPSL-1.0                  |
| Mulan Permissive Software License, Version 2       | MulanPSL-2.0                  |
| Do What The F*ck You Want To Public License        | WTFPL                         |
### 6.2、针对多许可证

项目 License 声明应包含软件本身及引用的全部第三方开源组件（由依赖软件包或包管理器提供的除外）所涉及到的开源许可证，因此常见需要同时声明多个开源许可证。对于多许可证情况，除每个许可证均需采用SPDX格式相应标识符外，根据上游许可证约束要求，可使用AND、OR、WITH三种连接符进行组合。

(1) 当要求同时受多个开源许可证约束时，需使用AND连接符对许可证进行连接，参考示例如下：

License：Apache-2.0 AND MIT，表明该软件同时受Apache-2.0和MIT许可证约束。

(2) 当存在多个许可证，并且可由被许可人选择接受其中之一许可证进行约束时，需使用OR连接符对许可证进行连接，参考示例如下：

License：Apache-2.0 OR MIT，表明该软件可由被许可人选择受Apache-2.0或MIT其中之一许可证约束。

(3) 在现有许可证约束的条件下，被许可人希望获取额外权限时，需使用WITH连接符进行连接，参考示例如下：

License：GPL-3.0-only WITH Classpath-exception-2.0，表明该软件仅被GPL-3.0约束，被许可人还可选择Classpath-exception-2.0，从而获取额外权限。

### 附A 常见字符简介

项目 License 声明中会有一些字符经常与开源许可证组合使用，现对常见字符进行简介。

(1) 对于GNU许可证需使用only表明仅受GNU中的单一许可证约束。参考示例如下：

License: GPL-2.0-only，表明仅受GPL-2.0许可证约束。

(2) 单一许可证后加“+”字符，表明受单一许可证约束，也可由该单一许可证任何更高版本约束，由被许可方选择，参考示例如下：

License: EPL-1.0+，表明该软件受EPL 1.0或EPL许可证任何更高版本约束。

(3) 对于GNU许可证需使用later字符表示受GNU当前版本或更高版本的GNU许可证约束，由被许可方选择，参考示例如下：

License: GPL-2.0-or-later，表明该软件受GPL 2.0版本或更高版本的GPL许可证约束。

许可证组合及常见字符的详细介绍，可通过 https://spdx.dev/ids/ 进行参考。
