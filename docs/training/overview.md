---
封面: assets/img/covers/training_overview.png
标题: 培训概览
描述: 了解PagerDuty重大事件响应流程是成为PagerDuty有效待命工程师的重要部分。本节概述了我们针对参与事件响应的各种角色的培训材料，以及来自政府机构的额外信息和培训材料。
---
了解PagerDuty重大事件响应流程是成为PagerDuty有效待命工程师的重要部分。本节概述了我们针对参与事件响应的各种角色的培训材料，以及来自政府机构的额外信息和培训材料。

## 培训指南
我们的培训指南按角色划分，但我们鼓励您阅读不属于您角色的培训指南，因为这可以为您提供在重大事件期间这些人将如何行动的良好洞察。

* [事件指挥官培训](../training/incident_commander.md) - “IC”是推动重大事件解决的人。他们是指挥其他人的人。
* [副指挥官培训](../training/deputy.md) - 副指挥官是支持事件指挥官的人，必要时可以接替他们。
* [记录员培训](../training/scribe.md) - 这是为在事件期间担任记录员的人准备的。
* [专家/解决者培训](../training/subject_matter_expert.md) - 这对PagerDuty所有待命的团队成员都相关。
* [客户联络培训](../training/customer_liaison.md) - 这是为公开代表我们并与客户互动的人准备的。
* [内部联络培训](../training/internal_liaison.md) - 这对可能在事件期间被要求与内部团队合作的人都相关。

## 培训课程
我们还发布了部分培训课程的幻灯片和视频。最初在PagerDuty内部用于培训我们的员工，我们后来将其改编为更广泛的受众，以便您可以在自己的组织中利用它们。

* [事件响应培训课程](../training/courses/incident_response.md) - 关于事件响应和事件指挥官角色的入门课程。

## 事件示例
这段录音是对2017年1月在PagerDuty发生的实际重大事件的重现。为了简洁和隐私，一些细节已被更改，但事件本身基本保持不变。关于录音的更多细节，您可以阅读[PagerDuty博客文章](https://www.pagerduty.com/blog/incident-response-reenactment/)。

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/yoY_pDxc0TA?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## 国家事件管理系统（NIMS）
我们的事件响应流程在很大程度上基于[美国国家事件管理系统（NIMS）](https://www.fema.gov/national-incident-management-system)，该系统被描述为，

  _一种系统性的、前瞻性的方法，指导各级政府、非政府组织和私营部门的部门和机构无缝合作，管理涉及所有威胁和危害的事件——无论其原因、大小、位置或复杂性如何——以减少生命、财产和环境的损失。_

虽然最初可能看起来这不适用于IT运营环境，但我们发现，从这些情况下的重大事件中吸取的许多教训可以直接应用于我们的行业。原则是相同的，并跨越许多不同的环境。

[![NIMS](../assets/img/thumbnails/nims_core.png)](https://www.fema.gov/pdf/emergency/nims/NIMS_core.pdf) [![NIMS培训](../assets/img/thumbnails/nims_training.png)](https://www.fema.gov/pdf/emergency/nims/nims_training_program.pdf)

如果您想了解更多关于NIMS的信息，我们推荐[ICS-100](https://training.fema.gov/is/courseoverview.aspx?code=IS-100.b)和[ICS-700](https://training.fema.gov/is/courseoverview.aspx?code=IS-700.a)在线培训课程，这些课程涵盖了NIMS和事件指挥系统（您也可以在培训后参加在线考试，以获得FEMA的证书）。还有大量的[FEMA提供的额外培训材料和课程](https://training.fema.gov/nims/)关于NIMS，我们鼓励您查看。

如果您位于美国并对在社区中担任更积极的事件响应角色感兴趣，我们建议您调查当地的[CERT项目](https://www.ready.gov/cert)（社区应急响应团队）。许多城市提供CERT培训，之后您可以在社区中作为CERT贡献者自愿服务。这不仅是一个获得实际灾难响应经验的机会，而且您学到的技能也可以应用于日常生活。

还可以查看[附加阅读](../resources/reading.md)页面。

## 全球事件响应
虽然NIMS是美国的事件响应框架，但许多国家都有自己的类似框架。有些是基于美国的系统，但许多是独立开发的。通过调查世界各地国家使用的方法和框架，可以学到大量的额外信息。

一本名为“[比较应急管理：理解来自世界各地的灾难政策、组织和倡议](https://training.fema.gov/hiedu/aemrc/booksdownload/compemmgmtbookproject/)”的书（可从[FEMA网站](https://training.fema.gov/hiedu/aemrc/)获得）比较了30多个不同国家使用的系统，是关于世界各地使用的应急管理框架的惊人信息集合。

以下是我们为了在PagerDuty适应和改进我们自己的流程而详细研究的一些系统。

### 英国

英国紧急服务使用一种称为[**黄金-白银-青铜指挥结构**](https://en.wikipedia.org/wiki/Gold%E2%80%93silver%E2%80%93bronze_command_structure)的指挥层级进行重大操作。该框架涉及三个级别，负责战略（黄金）、战术（白银）和操作（青铜）指挥决策。

如果您有兴趣了解更多信息，以下是一些有用的阅读材料：

* [英国政府 - 紧急响应和恢复](https://www.gov.uk/guidance/emergency-response-and-recovery)。
* [英国政府 - 事件指挥 - 第三版（2008年）](https://www.gov.uk/government/publications/fire-and-rescue-manual-volume-1-incident-command)。
* [英国内政部 - 关键事件管理](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/735103/critical-incident-management-v12.0ext.pdf)（PDF）。

### 新西兰

新西兰的系统称为[**协调事件管理系统（CIMS）**](https://en.wikipedia.org/wiki/Coordinated_Incident_Management_System)，基于美国使用的事件指挥系统。我们特别喜欢CIMS的一个方面是它对通用术语的关注，这有助于防止事件期间的混乱，并允许更快、更有效的响应。一些术语已从ICS更改（例如，“控制”而不是“指挥”来描述管理功能），但应该仍然熟悉。

如果您有兴趣了解更多信息，以下是一些有用的阅读材料：

* [民防与应急管理部 - 新西兰协调事件管理系统（CIMS）](https://www.civildefence.govt.nz/resources/coordinated-incident-management-system-cims-third-edition/)（[PDF](https://www.civildefence.govt.nz/assets/Uploads/CIMS-3rd-edition-FINAL-Aug-2019.pdf)）。
* [Devereux-Blum培训与发展 - 应急管理培训](https://www.emergencymanagement.co.nz/)

### 澳大利亚

澳大利亚使用一种称为[**澳大拉西亚跨服务事件管理系统（AIIMS）**](https://en.wikipedia.org/wiki/Australasian_Inter-Service_Incident_Management_System)的系统，该系统是基于美国使用的NIMS框架的衍生。虽然基于ICS，AIIMS更注重_控制范围_，而不是其他框架。与新西兰的系统一样，使用的术语有一些差异（例如，“事件控制者”而不是“事件指挥官”），但对于了解ICS的人来说应该仍然熟悉。

如果您有兴趣了解更多信息，以下是一些有用的阅读材料：

* [澳大拉西亚跨服务事件管理系统，第三版](https://training.fema.gov/hiedu/docs/cem/comparative%20em%20-%20session%2021%20-%20handout%2021-1%20aiims%20manual.pdf)（PDF）。
* [澳大利亚事件管理手册](https://knowledge.aidr.org.au/resources/handbook-14-incident-management-in-australia/)

### 加拿大

加拿大使用自己的[**事件指挥系统**](https://www.icscanada.ca/images/upload/ICS%20OPS%20Description2012.pdf)（PDF）。该标准由一个称为[ICS Canada](https://www.icscanada.ca/en/home.html)的组织网络维护。他们的网站有一系列关于如何在加拿大根据您的省份找到当地培训课程的信息。

如果您有兴趣了解更多信息，以下是一些有用的阅读材料：

* [ICSCanada - I-100 事件指挥系统简介](https://www.svffa.ca/s/ICS100-Self-Paced-Student-Workbook_2016.pdf)（PDF）。
* [加拿大ICS表格](https://www.icscanada.ca/en/Forms.html) - _标准ICS表格，您可以下载并在自己的事件中使用（[FEMA有美国等效表格](https://training.fema.gov/icsresource/icsforms.aspx)）。_