---
cover: assets/img/covers/severity_levels.png
description: 事件通常按严重性或优先级分类。在PagerDuty，我们使用“SEV”级别，编号越低的严重性越紧急。操作问题可以归类为这些严重性级别之一，通常您可以采取更具风险的措施来解决更高严重性的问题。
---
任何事件响应过程的第一步是确定实际[构成事件的内容](../before/what_is_an_incident.md)。然后，事件可以按严重性分类，通常使用“SEV”定义进行，编号越低的严重性越紧急。操作问题可以归类为这些严重性级别之一，通常您可以采取更具风险的措施来解决更高严重性的问题。任何高于SEV-3的事件都会自动被视为“重大事件”，并得到比正常事件更密集的响应。

!!! 提示 "始终假设最坏情况"
     如果您不确定事件的级别（例如不确定是SEV-2还是SEV-1），**将其视为更高的级别**。在事件期间不是讨论或争论严重性的时间，只需假设最高级别并在事后审查。

!!! 问题 "SEV-3可以是重大事件吗？"
     所有SEV-2都是重大事件，但并非所有重大事件都需要是SEV-2。如果您需要协调响应，即使是较低严重性的问题，也要触发我们的应急响应流程。事件指挥官可以决定是否需要全面的事件响应。

<table class="custom-table">
  <thead>
    <tr>
      <th class="sev">严重性</th>
      <th>描述</th>
      <th>典型响应</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="sev-1">SEV-1</td>
      <td>
        <p class="intent">需要公开通知并与执行团队联络的严重问题。</p>
        <ul>
          <li>系统处于危急状态，正在积极影响大量客户。</li>
          <li>功能严重受损已久，违反了SLA。</li>
          <li>我们注意到了一个暴露客户数据的安全漏洞。</li>
        </ul>
      </td>
      <td>
        <p class="response">重大事件响应。</p>
        <ul>
          <li>在Slack中呼叫IC <code>!ic page</code>。</li>
          <li>参见<a href="/during/during_an_incident">事件期间</a>。</li>
          <li>通知内部利益相关者。</li>
          <li>公开通知。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td class="sev-2">SEV-2</td>
      <td>
        <p class="intent">正在积极影响许多客户使用产品的关键系统问题。</p>
        <ul>
          <li>通知管道严重受损。</li>
          <li>事件响应功能（确认、解决等）严重受损。</li>
          <li>Web应用对大多数/所有用户不可用或性能严重下降。</li>
          <li>PagerDuty系统重大事件条件的监控受损。</li>
          <li>PagerDuty员工认为需要事件响应的任何其他事件。</li>
        </ul>
      </td>
      <td>
        <p class="response">重大事件响应。</p>
        <ul>
          <li>在Slack中呼叫IC <code>!ic page</code>。</li>
          <li>参见<a href="/during/during_an_incident">事件期间</a>。</li>
        </ul>
    </tr>
    <tr>
      <td class="warning" colspan="3">此行以上的任何事件都被视为“重大事件”。对于任何重大事件，都应触发我们的应急响应流程。</td>
    </tr>
    <tr>
      <td class="sev-3">SEV-3</td>
      <td>
        <p class="intent">需要服务所有者立即关注的稳定性或轻微客户影响问题。</p>
        <ul>
          <li>部分功能丧失，不影响大多数客户。</li>
          <li>如果不采取措施，有可能成为SEV-2的问题。</li>
          <li>服务中没有冗余（再有一个节点故障将导致中断）。</li>
        </ul>
      </td>
      <td>
        <p class="response">高紧急度呼叫服务团队。</p>
        <ul>
          <li>将问题作为您的最高优先级处理。</li>
          <li>与受影响系统的工程师联络以确定原因。</li>
          <li>如果与最近部署相关，回滚。</li>
          <li>监控状态并注意是否/何时升级。</li>
          <li>如果您认为有可能升级，请在Slack中提及。</li>
          <li>必要时触发事件响应（<code>!ic page</code>）。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td class="sev-4">SEV-4</td>
      <td>
        <p class="intent">需要采取行动的轻微问题，但不影响客户使用产品。</p>
        <ul>
          <li>性能问题（延迟等）。</li>
          <li>单个主机故障（即集群中的一个节点）。</li>
          <li>延迟作业失败（不影响事件和通知管道）。</li>
          <li>Cron失败（不影响事件和通知管道）。</li>
        </ul>
      </td>
      <td>
        <p class="response">低紧急度呼叫服务团队。</p>
        <ul>
          <li>将问题作为您的首要优先级处理（高于“正常”任务）。</li>
          <li>监控状态并注意是否/何时升级。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td class="sev-5">SEV-5</td>
      <td>
        <p class="intent">不影响客户使用产品的外观问题或错误。</p>
        <ul>
          <li>不影响系统立即使用能力的错误。</li>
        </ul>
      </td>
      <td>
        <p class="response">JIRA工单。</p>
        <ul>
          <li>创建JIRA工单并分配给受影响系统的所有者。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

!!! 注意 "具体明确"
    这些严重性描述已从PagerDuty内部定义修改为更通用。对于您自己的文档，建议您使定义非常具体，通常指受影响的用户/账户的百分比。您通常希望您的严重性定义是基于指标的。