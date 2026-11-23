# grill-me：动手之前先对齐

> 来源：Matt Pocock《Skills For Real Engineers》里的 grill-me（MIT 开源，仓库 mattpocock/skills）。原文是 Claude Code 的 skill，这里按 Muse 的用法改写。核心理念：**对齐了再动手**。

## 什么时候用

- 用户说「grill me」「先对齐再动手」「拷问我一下」，或者要做一个还没想清楚的决定、方案、改动时。
- 任何一次你发现自己要凭猜测动手之前，先走一轮 grill-me。
- 这是用户主动调用的 skill：只有用户点了名才进入拷问模式，不要自己悄悄套用。

## 做法

调用 grilling skill（`~/workspace/custom-skills/grilling/SKILL.md`）执行整场访谈。

## 结束后

- 访谈结束的标准：设计树的前沿为空，每条分支都走过，没有任何默许的假设。
- 结束时把达成的共识写成一份简短的书面记录（决定、理由、待定项），存进相关目标或工作文件，再动手。
- 用户确认达成共识之前，绝不动手。
