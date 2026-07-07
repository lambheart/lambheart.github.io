---
title: "China’s Agent Governance Framework: Implications for AI Safety"
date: 2026-05-20
weight: 1
---
2026 05 20

*This memo was written for [Project Synesis](project-synesis.org) in collaboration with Yilin Huang. Project Synesis is a multilingual discovery dashboard for primary source foreign AI governance documents.*

#### TLDR

* The Chinese government’s [*Implementation Opinions on Standardized Application and Innovative Development of Intelligent*](https://www.cac.gov.cn/2026-05/08/c_1779979789523320.htm)  is the first major government document specifically regulating agents as distinct from models, ahead of comparable efforts in the US or EU.  
* Western safety researchers should take note of this document as a signal that China is building agent governance infrastructure now, including safety evaluation systems and sector-specific compliance requirements, and design decisions being made in following months will determine whether these policies have substantive safety content. The window to influence design is open now.  
* Vocabulary overlap with Western AI safety concepts, but the underlying decision-making authority framework may neglect covert failure modes.  
* Agents are being embedded into critical infrastructure: electric grids, financial systems, public security, judicial procedures. CAC and sector regulators will determine rules in sensitive domains.  
* China’s proposed agent identity registration and interconnection protocol, if implemented, would be first-mover infrastructure setting a global precedent.  
* Overall, the document warrants cautious optimism about continued regulatory development, demonstrating regulatory ambition and outlining a compliance framework, and community members can likely expect Chinese regulation of more AI domains in the near future.   
* Open questions to be answered as details of regulation are determined in the coming months:  
  * How Provision 11’s sensitive sector “testing” is specified; concretely, whether this encompasses safety testing.  
  * Whether Provision 12’s third-party evaluation allows for real technical access.  
  * What TC260’s binding agent security standards ultimately require.  
* See [Implications for Action](#implications-for-action) for recommendations on what you might take from this document.   
* The authors will release a followup in the coming months detailing the specific regulations that result from this document.

### Context

This memo, written for readers without a China policy background, examines what China's new agent governance framework reveals about its risk perception and what it implies for researchers, practitioners, and funders working on AI safety. 

On May 8, 2026, three Chinese government agencies jointly released the [*Implementation Opinions on Standardized Application and Innovative Development of Intelligent Agents*](https://www.cac.gov.cn/2026-05/08/c_1779979789523320.htm),[^1] a 38-provision policy document guiding the development, deployment, and governance of AI agent systems. Implementation Opinions[^2] are non-binding directives that create regulatory expectations without enforceable legal obligations. A provision appearing in this document signals intent rather than guaranteed implementation; subsequent binding regulations and technical standards will determine what compliance actually requires. 

The document defines agents as "intelligent systems possessing autonomous perception, memory, decision-making, interaction, and execution capabilities".[^3] It is likely that the definition is intentionally broad to tie in with the definition in the TC260[^4] agent safety report, which distinguishes between "soft agents",[^5] such as LLM-based chatbots and coding assistants, and "hard agents",[^6] such as autonomous vehicles and industrial robots.[^7] **By covering both, the CAC document claims a wider regulatory scope than Western agent safety research typically addresses, which focuses primarily on risks from LLM-based agents.**

The document positions agents as economic infrastructure, envisioning a future where agents will "profoundly transform human modes of production, daily life, and social governance",[^8] and where safety regulations are framed as a *precondition* for large-scale deployment. Half of the provisions of the document is spent calling for exploration and research of 19 agent application scenarios.[^9] Beyond typical mentions of healthcare, education and finance, there are interesting inclusions such as:

* Electric power dispatch and grid maintenance (Provision 18\)  
* Public safety monitoring, early-warning systems, and embodied agents for disaster relief and hazardous material disposal (Provision 31\)  
* Information services including public opinion guidance[^10] and emotion regulation (Provision 28\)

Together, these point toward embedding agents across the critical functions of the Chinese state and economy, under the direction of the State Council’s “AI+” action plan.

### Principal-agent framing difference

The document’s safety framework is consequential both for its underlying assumptions and downstream implications. The document's main safety enforcement mechanism stipulates that users retain the right to know and final authority over the scope of actions taken by the agent, framing safety risk as agents acting outside scope boundaries rather than agents developing goals users didn't intend.[^11] This framework works for systems without high scheming capabilities but becomes increasingly insufficient as capability increases—where covert pursuit of misaligned goals becomes salient—as in Western control conceptions. 

In accordance with the decision authority focus, the document prioritizes verifiability and traceability mechanisms that can trace breaches of authority.[^12] What verifiable and traceable mean in practice is not detailed. In Western safety discourse, verifiable systems often implies interpretability tools that expose model internals; here it likely refers to logging and audit trails of observable outputs. Whether the document intends the stronger sense will be revealed as TC260's technical standards are developed.

For comparison, the EU AI Code of Practice defines loss of control risk as "the human inability to modify or shut down models due to misalignment, autonomy, or resistance," specifically accounting for the scenario where capable systems appear compliant while misaligned. As opposed to framing AI agents as tools, the Western community assesses control risk across capability and propensity dimensions, wherein covert compliance and deceptive alignment are failure modes that may bypass the authorization scope mechanism. For failure modes such as weight exfiltration, sabotage, sandbagging, and resource acquisition, traceability may fail to address violations.

### The three risk categories (Provisions 8-10)

The document demonstrates meaningful awareness of loss-of-control, misuse risk, and endogenous safety. These concepts overlap with the vocabulary of the Western AI safety community, though this overlap should not be misconstrued for shared conceptual frameworks, as the policy mechanisms differ in noteworthy ways.

* Provision 8 (提升内生安全能力) names loss of operational control, data poisoning, algorithm tampering, and system vulnerabilities.  
* Provision 9 (加强供应链安全) calls for strengthened security management of model access, API calls, and extended tool use.  
* Provision 10 (化解应用衍生风险) lists automated attacks, privacy invasion, generation and spread of disinformation, and internet fraud as unlawful use cases to prevent.

Overall, the document frames loss of control as an external security threat rather than emergent misalignment. As a result, the framework is better equipped to address adversarial interference than goal divergence that Western safety research considers most concerning as systems become more capable. Notably, CBRN, otherwise named in the TC260 Framework 2.0,[^13] and internal deployment is omitted from the misuse risks listed.

**More importantly, the currently unspecified agent safety evaluation system in Provision 8 is where Western capability evaluation methodology will be impactful.** The document calls for safety evaluation in two places: Provision 8's agent safety evaluation system and Provision 12's third-party evaluation service for independent testing of agent function, performance, quality, and compliance. Provision 8's safety evaluation system is currently unspecified in its content, methodology, and responsible institutions. Thus, it is a direct opening for Western capability evaluation methodology to shape Chinese practice: specifically, whether the eventual system requires capability and propensity assessment or only behavioral compliance testing will determine whether it can address covert failure modes. 

Both face structural obstacles from precedent and architecture. Currently, Chinese third-party evaluation of generative AI models primarily assesses whether models produce prohibited content—agent evaluation would require substantially deeper technical access. Additionally, the actors being assessed possess more knowledge of their own systems than any external evaluator can independently verify, creating incentives to optimize for what is measurable rather than the underlying safety objective. 

Whether these mechanisms produce substantive outcomes hinges on whether evaluators gain genuine system access and whether evaluation encompasses capability and propensity assessment rather than behavioral output testing alone. Provision 8's safety evaluation system, currently unspecified, is the most direct opening for Western capability evaluation methodology to shape Chinese practice.

### Enforcement dependent on high- or low-stakes deployment context (Provision 11)

Provision 11 calls for a tiered governance framework that regulates agents based on deployment context rather than model capability thresholds (e.g. compute, general capability, systematic risk designation). For sensitive domains, the CAC and sector regulators jointly designate permissible use cases and implement measures such as filing requirements, safety testing, and defective product recall mechanisms. For low-risk domains, the framework relies on industry self-regulation.

This means compliance standards will likely fragment by sector and involve far more actors than just frontier developers. Energy regulators, financial regulators, and public safety authorities each co-determine the rules for agent deployment in their domain, and each operates with different risk tolerances, existing stakeholders, and political dynamics. Leading firms that participate in sector-specific standard-setting both influence what compliance means and gain an early advantage in demonstrating it.

Two open questions will determine how consequential this framework becomes. First, who designates sensitive domains and what "testing" concretely entails. Specification will likely be accelerated by firms seeking deployment approval, since labs need regulatory clarity before they can ship. Second, once sector-specific standards are set and agents are operating under them (especially in critical infrastructure with high uptime requirements), revisions may become costly. Future standards must accommodate existing deployments, narrowing the window for new safety requirements that could reshape practice.

### Implications for Action{#implications-for-action}

* AI governance researchers should track how this directive is operationalized through TC260’s standards pipeline, where agent security standards currently in development will determine the compliance surface.   
* Monitor Provision 11’s sensitive domain testing specification, likely concretized within months. The central question is whether it encompasses safety testing. [Kyle Chan](https://x.com/kyleichan), [Paul Triolo](https://x.com/pstAsiatech), [Zilan Qian](https://x.com/ZilanQian), and [Poe Zhao](https://x.com/poezhao0605) are worth following for timely coverage of new developments here, though viewpoints vary. Cross-referencing between them is advisable. IAPS’s China work is a more analytically consistent resource for deeper context.  
* AI control researchers should watch for agent integration in critical domains—listed in Provisions 18 and 29-31. Early warning signals in these sectors will help evaluate the effectiveness of governance mechanisms in practice.  
* Provision 12’s third-party evaluation and Provision 8’s safety evaluation system are both still being designed. Researchers and practitioners with capability evaluation expertise should confirm directly with Concordia and Safe AI Forum whether either organization is currently working on Chinese evaluation methodology; if so, these are the appropriate institutions to engage.  
* China’s Agent Interconnection Protocol is first-mover infrastructure for global agent identity standards; NIST only launched its equivalent initiative in February 2026, so the window is currently open.  
* Grantmakers and field builders should slightly update priors on China’s regulatory ambition. This document suggests ongoing investment in China-focused AI safety governance work is warranted.

[^1]:  智能体规范应用与创新发展实施意见

[^2]:  实施意见

[^3]:  “具备自主感知、记忆、决策、交互与执行能力的智能系统”

[^4]:  TC260 (全国信息安全标准化技术委员会, National Information Security Standardization Technical Committee) is China's primary body for developing cybersecurity and AI security standards. Its technical standards form the binding compliance underpin broader policy directives such as this.

[^5]:  软智能体

[^6]:  硬智能体

[^7]:  TC260-TR-005-2026, Section 1.2 Table 3 and Appendix C

[^8]:  深刻改变人类生产生活方式和社会治理模式

[^9]:  Research, industrial production, energy, transport, agriculture, finance, consumer, education, healthcare, public administration, judicial, public safety, urban governance, procurement.

[^10]:  舆论引导

[^11]:  Provision 6 (明确决策权限, "Clarify Decision-making Authority").

[^12]:  Provision 7 (加强行为管控, "Strengthen Behavioral Control") specifically mandates the establishment of rule-embedding and behavioral fence (规则内嵌、行为围栏) technologies, as well as verifiable and traceable mechanisms (可验证、可追溯机制).

[^13]:  TC260's AI Safety Governance Framework 2.0 (人工智能安全治理框架, September 2025\) is TC260’s broader risk taxonomy document. It includes catastrophic and CBRN risks absent from this document.