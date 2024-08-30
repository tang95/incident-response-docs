---
style: slides
cover: assets/slides/incident_response/incident_response.001.jpeg
title: 事件响应培训
description: 这是PagerDuty事件响应培训课程的开源版本。最初作为PagerDuty内部培训新事件指挥官的课程，现已发展成为我们现在公开提供的培训。了解更多关于事件响应和事件指挥官角色的信息。
pdf: /assets/pdf/pagerduty_incident_response_training_public.pdf
---

!!!info "事件响应培训课程（2018）"
    这是“事件响应培训”的开源版本，我们为事件响应和事件指挥提供的PagerDuty培训课程。它最初是作为培训新事件指挥官的内部课程，现已发展成为我们现在公开提供的课程。这是2018年培训的快照。最新版本现已是我们[PagerDuty大学](https://university.pagerduty.com/)课程的一部分。

    它包含大量关于我们流程的介绍性信息，特别是关于事件指挥官角色的详细信息。所有信息已经作为我们[公开文档](https://response.pagerduty.com)的一部分提供，这只是以一种希望更具吸引力的方式呈现它。欢迎您将其作为自己组织培训的基础。

    这里呈现的文本是通常交付培训的半准确转录。如果您更喜欢，还可以观看这个课程更早版本的[视频](#video)。

---

### 引言

<input type="checkbox" id="001" /><label for="001">![001](../../assets/slides/incident_response/incident_response.001.jpeg)</label>
_001. "事件响应培训"._

嗨，我是Rich，欢迎参加“事件响应培训”。这是我们PagerDuty内部培训的简短版本，我们用它来培训我们的新事件指挥官。它已经稍微改编以适应更广泛的受众，但大部分内容正是我们自己运行的内容。我们无法涵盖所有内容，否则我们将在这里待上几天，但我会介绍我们流程中一些最重要的部分。我会尽量简短。

实际上，我们有多少时间？有人能帮我计时吗？那太好了，谢谢！

---

### 学习如何有效管理事件

<input type="checkbox" id="002" /><label for="002">![002](../../assets/slides/incident_response/incident_response.002.jpeg)</label>
_002. 学习如何有效管理事件._

本次会议的目标是让您了解如何在组织内有效管理事件。我将描述我们在PagerDuty管理关键事件所使用的流程，并更详细地谈论一个特定的角色，称为“事件指挥官”。

这不是销售宣传。我不是销售团队的成员，这也不是关于如何使用PagerDuty管理您的事件的演讲（尽管如果您这样做显然会很棒）。今天的目的是向您介绍我们在PagerDuty内部如何管理事件，并为您提供大量实用的信息，您可以将其带回自己的组织，以开始或改进您自己的事件响应流程。

---

### 用平静取代混乱

<input type="checkbox" id="003" /><label for="003">![003](../../assets/slides/incident_response/incident_response.003.jpeg)</label>
_003. 用平静取代混乱._

让我们从一个快速问题开始。今天在您的组织中事件响应通常是如何进行的？是一个顺畅和精简的过程，还是很多人互相交谈？对大多数人来说，可能介于两者之间。

我们希望减少后者，增加前者。我们希望用平静取代混乱。恐慌和混乱在事件中不好，它们只会加剧事情并导致更多混乱。我们希望事情平静有序。

---

### 什么是事件响应？

<input type="checkbox" id="004" /><label for="004">![004](../../assets/slides/incident_response/incident_response.004.jpeg)</label>
_004. 什么是事件响应？ [文档参考](../../before/what_is_an_incident/#what-is-incident-response)_

因此，当我们谈论事件响应时，我们真正谈论的是一种有组织的方法来处理和管理事件。这是我们在PagerDuty对事件响应的定义。关键在于“有组织”这个词。我们不希望在每次警报响起时都惊慌失措。我们希望我们的响应几乎是例行的，每个人都像一台运转良好的机器一样协同工作。

有一句我很喜欢的名言，来自一本很棒的书，叫做[《运营中的事件管理》](https://learning.oreilly.com/library/view/~/9781491917619/)，这里很合适，

> 火灾对消防部门来说不是紧急情况……[Y]ou expect a rapid response from a group of professionals, skilled in the art of solving whatever issues you are having.

---

### 事件响应的目标

<input type="checkbox" id="005" /><label for="005">![005](../../assets/slides/incident_response/incident_response.005.jpeg)</label>
_005. 事件响应的目标。 [文档参考](../../before/what_is_an_incident.md#what-is-incident-response)_

您可能会惊讶地发现，事件响应的目标不仅仅是解决问题。给一千只猴子一个键盘，足够的时间，它们可能会解决您的问题。这不是好的事件响应。我们希望以一种限制造成的损害，减少恢复时间和成本的方式解决问题。我不仅仅是指财务成本，还有与工程师健康相关的成本。不断在凌晨3点叫醒人们可能会对他们的健康和幸福产生戏剧性的负面影响。

如果财务影响是您唯一关心的，那么不要忘记**人很贵**。在一个大型组织中，一个有100人坐在那里大部分时间闲置几个小时的电话桥并不罕见。如果每个人每小时花费约100美元，那就是每小时1万美元！这对企业来说真的很贵。

---

### 什么是事件？

<input type="checkbox" id="006" /><label for="006">![006](../../assets/slides/incident_response/incident_response.006.jpeg)</label>
_006. 什么是事件？ [文档参考](../../before/what_is_an_incident.md#what-is-an-incident)_

但在我们能够响应事件之前，我们需要[定义什么是事件](../../before/what_is_an_incident.md)。听起来很傻，但如果你不确定某件事是否是事件，你就不知道是否要响应它。

这是PagerDuty对事件的定义，

> 一个未计划的干扰或服务降级，正在积极影响客户使用产品。

这里的“客户”不仅仅指外部客户，还可以指内部客户。

您的定义可能不同，这没关系。我只是想给您一个可以开始的定义的想法。您希望您的定义简单，不超过一句话，并且任何人都能轻松理解。

您可能会注意到，这是一个相当广泛的定义。一个打字错误在技术上符合这个描述。以及全面中断。显然这些是非常不同的场景。所以我们还有别的东西。

---

### 什么是重大事件？

<input type="checkbox" id="007" /><label for="007">![007](../../assets/slides/incident_response/incident_response.007.jpeg)</label>
_007. 什么是重大事件？ [文档参考](../../before/what_is_an_incident.md#what-is-a-major-incident)_

我们还有我们称之为**重大事件**的东西。这是任何需要团队之间协调响应的事件。再次强调，这只是我们在PagerDuty的定义，欢迎您使用自己的定义。

这个定义背后的意图是，有时事件可以由单个团队处理，可能是遇到麻烦的服务的所有者。这很少需要大规模响应。但一旦他们需要涉及另一个团队，无论是客户支持还是数据库管理员，那么我们就宣布它为重大事件，并启动一个更大的响应。这里的**协调**是关键，我们稍后会详细讨论。

但这仍然涵盖了相当广泛的潜在事件。我们可以更具体。

---

### 严重性级别

<input type="checkbox" id="008" /><label for="008">![008](../../assets/slides/incident_response/incident_response.008.jpeg)</label>
_008. 严重性级别。 [文档参考](../../before/severity_levels.md)_

我们还使用[严重性级别](../../before/severity_levels.md)来确定事件的严重程度，以及它得到的响应类型。我们使用`SEV-5`到`SEV-1`作为我们的级别，但您可能使用不同的方案，`P0`到`P5`，或者甚至是表情符号，🔥到💩，等等。

假设您正在查看网站流量的图表。您通常可以根据受影响的指标来确定严重性。因此，随着网站流量的下降，严重性增加。

您通常会达到某个预定义的目标或水印，一旦指标超过，您就自动认为某事是重大事件。在PagerDuty，这是`SEV-3`和`SEV-2`之间的区别，但对您的组织来说可能不同。然后，随着事情变得更加严峻，我们进入我们的`SEV-2`和`SEV-1`，当事情完全平线时。

拥有预定义的阈值和指标可以让您为响应流程设置自动触发器。

???+ aside hide-arrow "我们建议使用与业务影响相关的指标。"
    指标非常有用，通常在它们与业务影响相关时效果最好。例如，我们在PagerDuty监控的指标是“每秒出站通知数”，在亚马逊可能是“每秒订单数”，在Netflix可能是“每秒流开始数”，等等。监控这些重要的业务指标将让您使用自动化来确定事件的严重性和使用的响应类型。

    如果您使用与业务影响无关的指标（例如，“主机CPU使用率高”），那么很难，有时甚至不可能确定与该指标相关的事件的严重性。

    您希望使用一个指标，让您知道您的业务状况如何，而不是某个特定设备的状况如何。

---

### 任何人都可以触发事件响应

_<input type="checkbox" id="009" /><label for="009">![009](../../assets/slides/incident_response/incident_response.009.jpeg)</label>_
_009. 任何人都可以随时触发事件响应。_

但有时您不会立即知道影响。或者也许您的指标还没有达到预定义的阈值。我们仍然需要一种方法让一个人跳进来并称某事为重大事件。

因此，尽管我们在PagerDuty有自动化，但我们也有一个机制，任何人都可以随时触发我们的重大事件响应流程。这对我们非常重要。我们发现，**降低触发事件响应的障碍已经导致事件解决速度的显著增加**。

我们不希望人们因为正式警报还没有响起而坐在某件事上。如果客户支持迅速收到大量请求，这是一个很好的迹象表明有问题，我们需要他们能够拉响警报。我们甚至有实习生在第一周就触发了我们的事件响应流程。如果清洁工走过一张图表并认为它看起来不对，我希望他们能够触发事件响应。

我们最初犹豫是否引入这一点，因为我们担心这会导致大量的误报。人们出于过度谨慎触发警报，但实际上并不是事件。但我们看到了相反的情况，人们非常擅长自我监管。只有两次我们遇到了误报，而且根据当时可用的信息，这两次都是合理的。即使您偶尔遇到误报，您也可以将其作为免费练习。

---

### 通过聊天触发事件

<input type="checkbox" id="010" /><label for="010">![010](../../assets/slides/incident_response/incident_response.010.jpeg)</label>
_010. 通过聊天触发事件。 [文档参考](../../resources/chatops.md#ic-page)_

那么我们如何让人类触发流程呢？我们用一个[聊天命令](../../resources/chatops.md)来做，但不要觉得这是唯一正确的方式。我只是想展示我们是如何做的，给您一个想法。您可以随心所欲地做。空气喇叭，办公室里的闪光灯，雇佣一个mariachi乐队，等等。

关键是您希望有一种快速、简单且对每个人都可用的触发响应的方式。

---

### 和平时期与战时

<input type="checkbox" id="011" /><label for="011">![011](../../assets/slides/incident_response/incident_response.011.jpeg)</label>
_011. 和平时期与战时。 [文档参考](../../before/what_is_an_incident.md#mentality-shift)_

一旦事件被触发，我们需要切换我们的思维模式。我们需要一个[心态转变](../../before/what_is_an_incident.md#mentality-shift)。我们希望在“正常运营”和“正在进行事件”之间有所区别。我们需要从和平时期的决策转向战时。从日常运营转向保卫业务。

在正常运营中被认为完全不可接受的事情，比如部署代码而不运行任何测试，在重大事件期间当您需要快速恢复服务时可能是完全可以接受的。

您