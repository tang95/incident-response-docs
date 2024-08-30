---
cover: assets/img/covers/blameless.png
description: 编写有效的事后分析报告使我们能够快速从错误中学习，并改进我们的系统和流程，惠及所有人。我们希望确保我们编写的事后分析报告详细且准确，以便从中获得最大的益处。本指南列出了一些我们可以做的事情，以确保我们的事后分析报告有效。
---
编写有效的事后分析报告使我们能够快速从错误中学习，并改进我们的系统和流程，惠及所有人。我们希望确保我们编写的事后分析报告详细且准确，以便从中获得最大的益处。本指南列出了一些我们可以做的事情，以确保我们的事后分析报告有效。

## 应该做的

* 确保时间线准确反映了事件。
* 描述任何新手可能不理解的技术术语/缩略词。
* [讨论事件如何符合我们对受影响服务健康和弹性的理解](https://www.pagerduty.com/blog/postmortem-understand-service-reliability/)。

## 不应该做的

* 除非真的是服务中断，否则不要使用“中断”这个词。我们希望确保准确反映事件的影响，而“中断”通常是一个过于宽泛的术语。它可能让客户误以为我们完全不可用，而实际情况远非如此。
* 不要改变细节或事件以使事情“看起来更好”。我们需要在事后分析报告中保持诚实，即使是对我们自己，否则它们就会失去效力。
* 不要点名批评某人。我们保持事后分析报告无责备。如果某人部署了一个破坏性的变更，那不是他们的错，而是我们的错，因为我们有一个允许他们部署破坏性变更的系统，等等。

## 建议

* 避免使用“人为错误”的概念。这与上面的“点名批评”有关，但有一个微妙的区别——很少有错误“根植”于人的行为，通常有多个促成因素（人运行的脚本没有速率限制，文档已过时，等等）可以而且应该被解决。
* 避免在时间线或描述部分讨论“替代现实”。例如，“服务X今天早上开始看到流量增加，并停止响应请求。*如果服务X对客户的请求进行了速率限制，*它就不会失败。”和“服务X今晚开始缓慢响应请求，*监控不足*无法检测到CPU使用率升高。”这两个例子将描述实际问题与假设的修复混合在一起——将改进与描述分开，以便可以分别讨论。
* 这些视频更详细地讨论了上述观点：
  * “[事故调查中的三个分析陷阱](https://www.youtube.com/watch?v=TqaFT-0cY7U)”
  * “[关于人为错误的两种观点](https://www.youtube.com/watch?v=rHeukoWWtQ8)”

## 审查

我们在Slack上有一个专门用于在预定会议前审查事后分析报告的房间。以下是我们关注的一些事项：

* 它是否提供了足够的细节？
* 它是否不仅仅是指出哪里出了问题，而是深入挖掘问题的根本原因？
* 它是否将“发生了什么？”与“如何修复？”分开？
* 提出的行动项是否合理？它们是否足够明确？
* 事后分析报告是否写得好且易于理解？
* 对外信息是否能引起客户的共鸣，还是可能会引起愤怒？

审查事后分析报告不是关于挑剔拼写错误（尽管我们应该确保对外信息没有充满拼写错误）。它是为了提供建设性的反馈，以便从事后分析报告中获得最大的益处。

## 示例
以下是其他公司的一些事后分析报告示例，供参考，

* [LastPass](https://blog.lastpass.com/2015/06/lastpass-security-notice/)
* [AWS](https://aws.amazon.com/message/5467D2/)
* [Twilio](https://www.twilio.com/blog/2013/07/billing-incident-post-mortem-breakdown-analysis-and-root-cause.html)
* [Heroku](https://status.heroku.com/incidents/151)
* [Netflix](https://netflixtechblog.com/post-mortem-of-october-22-2012-aws-degradation-efcee3ab40d5)
* [GOV.UK 铁路事故调查](https://www.gov.uk/government/publications/kyle-beck-safety-digest/near-miss-at-kyle-beck-3-august-2016)
* [事后分析报告列表！](https://github.com/danluu/post-mortems)

## 有用资源

* [高级事后分析技巧和人为错误101（Velocity 2011）](https://www.slideshare.net/jallspaw/advanced-postmortem-fu-and-human-error-101-velocity-2011)
* [责备。语言。分享。](https://fractio.nl/2015/10/30/blame-language-sharing/)