# Growth Experiment Planner：别急着 A/B，先判断值不值得测

很多增长实验不是失败在结果，而是从一开始就不该进入实验：流量不够、指标不对、变量混在一起，或者即使赢了也不知道下一步做什么。

`growth-experiment-planner` 是一个面向增长、产品和运营团队的开源 Agent Skill。它会先做可测试性判断，再把想法整理成一张能执行、能复盘的实验卡。

## 它会帮你做什么

- 判断问题应该做实验、做用户研究，还是直接修复
- 把模糊想法改写为可证伪的假设
- 指定主指标、护栏指标和决策阈值
- 在低流量场景下给出替代验证方案
- 生成实验结束后的结论与后续动作

## 直接这样用

```text
用 $growth-experiment-planner 评估这个想法：
我们想把注册页从 6 个字段改成 3 个字段，希望提高注册完成率。
目前每周约 300 个访问，完成率 18%。
```

默认输出包括：`可测试性判断`、`实验卡`、`测量方案`、`停止规则`和`结果解释模板`。

## 安装

```bash
cp -R skills/growth-experiment-planner ~/.codex/skills/
```

然后在对话中调用 `$growth-experiment-planner`，或者直接描述你要评估的增长想法。

## 设计原则

- 先定义决策，再收集数据
- 不用一个实验同时回答多个问题
- 不为了“显著”而提前停止
- 不把点击率自动当成业务价值
- 数据不足时明确说不足，不制造确定性

## 方法参考

本项目独立实现。问题域与实验设计常识参考了 [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) 中公开的增长实验方向，该项目采用 MIT License。本项目未复制其文字、模板、脚本或目录结构。

## License

MIT License。
