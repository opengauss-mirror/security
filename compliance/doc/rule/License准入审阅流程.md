# openGauss License 准入审阅流程

1. **流程目标**: 识别一个新的 License 与开源领域相关的风险情况，为 openGauss 开源项目的引入管理打下基础。根据识别的风险情况，制定不同场景下该 License 的准入情况。分为如下 4 种情况:
  1. “广泛认可开源的 License”（FSF or OSI approved）>> 推荐使用 >> 可用作 openGauss 组织下社区主导仓库的项目级 License。
  2. “可使用”License >> 可使用 >> 可用作社区仓库所依赖的第三方组件的 License。
  3. “受限使用”的 License >> 限制使用（需备案）>> 备案，追踪该类 License 的使用情况，告知 maintainer 该类 License 的风险。Maintainer 应寻求替换、隔离、限制使用场景等多种方式降低风险并自担责任。
  4. 禁止引入的 License，不属于上述 3 种情况的 License。
2. **输入件（流程发起资料表单）**：
  1. License ID：如果该 License 在 SPDX list 中，则使用 SPDX identifier，否则参考使用最多的名字，定义一个 ID。
  2. License SPDX Identifier：如果不在 SPDX list 中，则该项必须为空。
  3. License 别名：可以有多个。
  4. License 原文。
  5. License 原始出处：该 License 原始出处的项目网站（如有）和该 License 出处的描述。
  6. License 是否被 FSF 或者 OSI 认可：FSF: Yes|No; OSI: Yes|No。
  7. License 相近版本：请给出该 License 与 FSF 或 OSI 认证相近的版本，并给出 Diff（如有）。
  8. License 使用情况：请列明该 License 在其他社区中的认可度，必须覆盖 Debian、Fedora、openSUSE。
  9. License 影响范围：请给出该 License 影响哪些 openGauss 仓库，并说明是否进入安装包、容器镜像或其他二进制发布。
  10. License 涉及的负面诉讼和争议情况：描述该类情况的文字（如有）。
3. **输出件**：
  1. 该 License 是否为 openGauss approved 的“开源的”License。
  2. 该 License 是否为 openGauss 标记的“非开源需限制使用的”（简称：受限使用）License。
  3. 如果以上都不是，则该 License 为“禁止”引入 License。
4. **审阅原则**:
  1. 是否为 openGauss approved 的“开源的”License:
    1. FSF or OSI approved，再减去 openGauss 黑名单（很少）。
    2. 如果该 License 有相近且已被 FSF 或 OSI approved 的 License，则对比两个 License 的差异部分，按照 OSD 的 10 条开源定义进行对比。
  2. 是否为 openGauss 标记的“受限使用”License:
    1. 不属于 openGauss approved 的“开源的”License。
    2. 语言表述对分发、修改、使用等开源场景较为宽松。
    3. 在开源领域被广泛使用。
    4. 没有负面的诉讼和争议事件。
5. **审阅流程**：
  1. 申请人按输入件要求准备申请材料。
  2. 在 security SIG 例会上进行审阅。
  3. security SIG Maintainer 按审阅原则进行投票。参与投票的 Maintainer 数量不低于全体 Maintainer 的 60%，且赞成票不低于参与投票人数的 60%，为通过某标记。
6. **结果发布和过程存档**：
  1. 审阅申请资料和投票情况，通过 security SIG 会议纪要发出。
  2. 审阅申请资料和投票情况，在本仓库 `compliance` 目录存档。
7. **参考资料**:
  1. FSF 查询站点：[https://www.gnu.org/licenses/license-list.html](https://www.gnu.org/licenses/license-list.html)
  2. OSI 查询站点：[https://opensource.org/licenses](https://opensource.org/licenses/)
  3. 其他社区 License 认可度查询站点：
    1. Debian: [https://wiki.debian.org/DFSGLicenses](https://wiki.debian.org/DFSGLicenses)
    2. Fedora: [https://docs.fedoraproject.org/en-US/legal/license-approval/](https://docs.fedoraproject.org/en-US/legal/license-approval/)
    3. openSUSE: [https://en.opensuse.org/openSUSE:Accepted_licences](https://en.opensuse.org/openSUSE:Accepted_licences)

