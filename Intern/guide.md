# 实习生指南

oerv 实习生一般以修复软件包[<sup>修包的一般流程是什么?</sup>](./FAQ.md#修包的一般流程是什么)为主，每月按量结算。或者认领一个项目，并且定期汇报进展，月底进行评估结算。在完成前置任务的基础上，可以灵活选择任务。

实习生面对的任务可以分为：`pretask`，`easywork`，`hardwork`。所有实习生都必须完成 `pretask`，`pretask` 作为社区入门探索，建议在一个星期之内完成。 完成 `pretask` 就具备了正式实习生的资格，可以开始 `easywork` 的工作。完成三个 `easywork`时，可以选择挑战 `hardwork`。`hardwork` 属于探索性项目，完成者或者有显著进展者，mentor 会帮助一起完善简历。当然，如果觉得项目困难难以入手，可以选择及时退出项目，升阶失败。

## 工作分类

### `pretask`

`pretask` 的目的是帮助实习生一起搭建工作环境，熟悉 oerv 的工作流程和合作方式。 `pretask` 分为三个步骤：

- 任务一：通过 QEMU 仿真 RISC-V 环境并启动 openEuler RISC-V 系统，设法输出 neofetch 结果并截图提交
- 任务二：在 openEuler RISC-V 系统上通过 obs 命令行工具 osc，从源代码构建 RISC-V 版本的 rpm 包，比如 `pcre2`。（提示首先需要在 openEuler的 OBS[<sup>什么是 OBS？</sup>](./FAQ.md#什么是-obs) 上注册账号 https://build.openeuler.openatom.cn/project/show/openEuler:Mainline:RISC-V）
- 任务三：尝试使用 qemu user & nspawn 或者 docker 加速完成任务二

任务完成的方式为在本仓库提交 PR，并在 PR 的 *Conversation* 中附上任务完成截图，在 Intern/intern_message.md 的 *实习生信息* 下中加入自己的信息（pretask 考核的一部分）。这个阶段希望实习生养成积极提问和正确提问的习惯，并且构建属于自己的工作流和环境。

### `easywork`

`easywork` 会被计算为产出，一般来说如简单升级一个包，解决一个 OBS 包构建错误都属于 `easywork`，注意 `easywork`范畴并不一定都是简单工作，某些包修复的复杂程度会很高，在作为产出计算时也会被加大权重。

一个完整的 `easywork` 包括发现问题，找出解决办法，OBS工程验证，提交 PR。 mentor 会协助 PR 的合入。

`easywork` 一般可以通过一下几种途径寻找：

- 本仓库带有 `easywork` 标签的 issue，这是最简单的寻找方式，一般属于 mentor 的临时任务，难度合适。
- 在 OBS 构建工程中寻找riscv架构失败状态的包，这里的难度不一，注意在进行之前向 mentor 询问，mentor 会给出一定建议。
- RISC-V SIG gitee 主页 issue，这里会有各种难度的任务，要注意甄别并且询问 mentor 是否合适。
- 在仓库目录下上传送一个包含自己思考的修包案例 case，可以计算为 `easywork`。

无论如何，在进行 `easywork` 之前最好提前声明，因为 `easywork` 是最多的工作，声明有助于避免重复性工作。

如果在 `easywork` 的进行中，遇到重量级别问题并且产生一定进展，有可能在 mentor 的评估下帮助建立对应 issue，并在月底进行评估升阶。

`easywork` 由于难度不一，薪资评定时不会简单计算为同样的产出。

### `hardwork`

`hardwork` 是 oerv 团队打造的面向简历项目的工作，它具有一定的挑战性，完成者可以被协助制作简历项目对应部分，非常优秀者，有可能获得一份毕业后提供 offer 的承诺。

`hardwork` 一般是一个社区期待的特性或者长期期待解决的问题，所有的`hardwork` 都会在本仓库带有 `hardwork` 标签的issue下描述和进行后续跟踪。有自己想法的实习生也可以申请新的 `hardwork`，由 mentor 审核并且发布在 issue。

`harwork` 难度一定高于 `easywork` 的下限，但是有可能低于 `easywork` 的上限，薪资计算参考 issue 底下的任务追踪，一般而言是会高于简单修包类工作。同时有突破性进展的实习生会被推荐在公开平台进行汇报演讲。

完成更多 `hardwork` 会有更多的实习薪资评价和对应简历项目的建议帮助，但是没有其他额外的奖励。

依据 `hardwork` 的完成度，月底会有保持定阶评估，完成度一般的会降阶。

## 定阶方式
oerv 拥有一套独立的实习生定阶方式，这与实习生的资源获取能力，长期实习生评定和实习生转正条件直接相关。
详见：
- [OERV 实习生定阶体系](./intern_stage.md)

## 汇报方式

实习生需要在 reports 当月汇报文件末尾附加可见产出[<sup>什么是公开可见交付?</sup>](./FAQ.md#什么是公开可见交付)贡献，这也是每月薪资评价的重要参考。

## 资源获取

1. 所有正式实习生会获得一个临时的软件所工作邮箱，邮箱的管理方式是通过提交PR [<sup>实习生加入和离开的 PR 规范</sup>](./Intern-Transition.md)。

2. 「雨水」阶会获得一个远程的 EPYC 服务器账号(waiting)。

3. 「惊蛰」阶会获得一个远程的 RISCV 服务器账号(waiting)。

## 注意事项

1. 若实习开始半个月后仍未完成 `pretask`，或实习期内出现月度产出评估为 0 情况，则需要接受强制评估，与 mentor 通电话确认是否能够继续留在组内工作。
2. `easywork`/`hardwork` 不代表难度，只代表当前工作可以模仿学习的程度。
3. 主观性经验分享是一件被鼓励的事情，这里面包含了贡献者对项目的个人思考与如何解决问题的探讨。对应的内容可以提交在 `cases` 文件夹。
3. 实习结束的实习生，名字会被从文档中移除。表现优异的同学，会被记录在 archive 中，简单介绍所做工作。
4. 注意开源社区规范和对软件所的公开影响，如果有行为恶劣者，会被直接开除。
5. 提交 PR 要遵守和 openEuler 社区一致的 *a simple commit* 原则，即修改完毕可供审阅的 PR 应当遵循 openEuler 社区的提交规范 squash commit 成一个，有明确有说服力理由的除外。
6. 不同阶段的实习生没有明确的优劣之分，定阶的目的是为了对 oerv 贡献阶段。


## 参考资料

1. https://gitee.com/openEuler/RISC-V
2. https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/main/README-zh_CN.md
3. https://github.com/sparanoid/chinese-copywriting-guidelines
4. [FAQ](./FAQ.md)