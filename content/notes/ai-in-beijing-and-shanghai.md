---
description: "Notes from two Chinese AI conferences, based on observation and informal, unattributed conversations."
title: "What I Heard about AI in Beijing and Shanghai"
date: 2026-09-08
weight: 1
---
2026 09 08

*This essay is crossposted from [Substack](https://lambheart.substack.com/p/what-i-heard-about-ai-in-beijing).*

**TL;DR:** Notes from two Chinese AI conferences, based on observation and informal, unattributed conversations.

- Researchers consistently name resources as their largest bottleneck. Talent is abundant.
- A lot of attention and capital is directed toward embodied intelligence, downstream of state policy.
- Safety researchers say safety talent is incredibly scarce.
- The US-China race frame was mostly absent in conversations.

---

In June and July, I attended two AI conferences in China: the June 12–13 BAAI Conference in Beijing, and the July 17–20 World AI Conference in Shanghai. I spoke with early-career technical researchers, investors, and AI safety researchers in informal conversations. I will distill my findings in this article, focusing particularly on the phenomena and sentiments that surprised me. I weigh sentiments shared over meals more than those shared in talks and panels, as public statements often thematically mirror governance documents and papers. Given my exchanges with attendees were of an informal and spontaneous nature, none of my takeaways will be attributed.

Naturally, one should always receive accounts such as these with a healthy amount of doubt. Firms are incentivized to generate publicity and encourage investment in their own ventures, for example. However, the enthusiasm for embodied intelligence appears equally salient in researchers and presenters. Some personal sentiments expressed to me, additionally, are contested. I note where this is the case.

### Young Talent is Abundant, Resources are the Main Bottleneck

I met several undergraduate and high school students performing research as interns at top firms. The junior talent pipeline looks robust and researchers were even younger than I expected. A BAAI session was dedicated to lightning talks by student researchers, many of them having interned at one or more private labs.

In conversation, multiple researchers said that their bottleneck was resources, not talent. For academics scarcity was in both capital and compute: university compute allocation is restricted to a small number of leading research groups, and the [first thousand-card GPU cluster](https://eastfrontier.com/2026/08/17/tongji-and-hygon-put-a-domestic-ai-cluster-to-work-in-engineering-research/) at any Chinese university was announced only in April 2026. Beijing municipal grants for young researchers run in the hundreds of thousands of RMB. Private capital, in contrast, is abundant and flows to firms: embodied intelligence startup TARS raised $120M in a record March 2025 angel round, then $455M in its April 2026 Pre-A.

Some researchers at private labs doubted that their lab was competitive, given rapid repricing in a competitive domestic environment could endanger their lab if they fell behind in model releases. These sentiments, however, were contested by the evaluations of other entry-level and safety researchers, who were more optimistic about the same firms. The anxiety may reflect the general intensity of domestic competition more than any firm’s actual position.

### Embodied Intelligence

Embodied intelligence remained a central topic, largely due to state strategy and perceived profitability. BAAI’s Zhang Tao credited the 2025 policy cycle that classified embodied intelligence as a national future industry, and the Unitree Spring Festival performance as a catalyst for the large influx in attention on robotics and embodied intelligence.[^1] Senior employees left large firms to found embodied startups. Correspondingly, many investors I met were eager to get in contact with prospective researcher-founders. Both groups hoped to get a head start on what they predicted is an extremely profitable application domain: embodied intelligence could provide services in life and health services (particularly elder care), high-end manufacturing, intelligent goods transport, and national security.

Though attendees qualified they either didn’t know about or didn’t have a clear idea on what AGI meant, many believed embodied intelligence was a prerequisite to AGI—embodied intelligence keynote speakers qualified “physical AGI” as their end goal. Nearly every attendee I spoke with held some version of the same belief that world models are a prerequisite to reliable embodied intelligence, which could then be used for a vast range of applications.

Data is the binding constraint on robotics, as real-world interaction data is expensive to collect, rendering self-evolution techniques attractive to some researchers. TARS co-founder and chief scientist Ding Wenchao argued that embodied intelligence should follow the scaling logic that worked for LLMs: human-collected interaction data would train a model, which, deployed at scale, would generate the next round of data. Self-evolution and simulation-driven training, presented in several BAAI talks, are cheaper substitutes to physical data collection. During a Q&A on recursive self-learning, an academic researcher specifically cited the resource constraints of their group as motivation for asking whether self-learning would be a viable technique for their research. Just a few rooms over, however, recursive self-improvement (RSI) was classified a critical risk.

### Safety Faces a Talent Bottleneck

In public-facing safety forums, coverage of failure modes was more exhaustive than I expected in June, focusing substantially on misuse and loss-of-control failure modes, beyond standard content regulation concerns. RealAI classified autonomous weapons and recursive self-improvement (RSI) as top tier risks in its L1–L5 taxonomy. Qi Anxin, a prominent cybersecurity firm, illustrated the scope of cybersecurity expanding from network infrastructure toward agent architecture, naming agent deployment and Mythos-level attacks as new dangers that could not be sufficiently addressed by vulnerability-driven defense.

The audience, however, did not obviously share safety concerns. When polled on whether a self-driving car would kill someone within the next year, about half of the audience did not vote—of those who participated, more voted no, appearing to express a baseline confidence in deployed-system safety, perhaps of domestic systems specifically. Attendees at a safety forum are presumably more safety-minded than those of the conference as a whole, so the wider population likely skews further in this direction.

In discussions, Chinese AI safety peers were less worried about public sentiment than about the lack of domestic safety talent. Technical talent is abundant in China, but those with safety context—and willing to devote their career to a field with scarce opportunities—are few and far between. My colleague Jasmine Li [expounds](https://jasminexli.substack.com/p/ai-safety-in-china-a-primer) on the Chinese safety landscape in detail.

### The Absent US-China Framing

The geopolitical framing in WAIC was oriented more toward the Global South than to US-China dynamics. During the conference, the World AI Cooperation Organization was founded with 29 signatory states, composed largely of states from Central Asia, Southeast Asia, Africa, and Latin America, with the mission of closing the “intelligence gap” between developing and developed countries. Forums on international cooperation, similarly, centered on coordination with and capacity building in the Global South. Of course, a state-organized conference will present the state’s preferred framing; state policy documents repeatedly state their commitment to supporting the Global South. However, I was also surprised by the apparent lack of awareness toward US-China competition from people I spoke to.

Entry-level researchers demonstrated far less awareness of great-power race dynamics than I expected, given how prominent the frame is among lab leadership, national security commentators, and parts of the safety community in the US. While I don’t have a good model of the median US researcher, my conversations with Chinese researchers were starkly different from those in the Western safety community. Some had not heard of Mythos or Glasswing. Some were unaware that the US viewed China through a race framing at all. Others knew of it and were uninterested, arguing that nurturing domestic development on their own terms was more important. Where the US was mentioned, it was framed as a standard against which domestic work is measured, rather than an adversary. Consistent with this lens, many people I spoke to, especially outside conferences, were often sharply critical of or unsatisfied with domestic models for lagging that standard, which read as self-criticism rather than opposition.

### Conclusion

Unfortunately, two conferences and a few dozen conversations cannot support claims about the Chinese AI landscape as a whole. However, my experiences updated my priors in various ways: resources, not talent, are the constraint researchers name; embodied intelligence is receiving a great amount of attention and capital, a phenomenon emerging first from policy; and the great-power race frame was mostly absent in conversations and presentations.

In dynamics where each side’s threat perception drives the behavior that, in turn, confirms the other’s, competing well requires knowing what you’re competing for, and perhaps whether you should compete at all. In the instance of US-China AI dynamics, more than ever, strategic empathy should be a precondition to setting one’s expectations. I left my time in China with a clearer picture of what Chinese researchers are optimizing for, and I recall most clearly conversations with bright, young researchers who were astounded that counterparts held an adversarial mindset toward them at all.

[^1]: Specifically, embodied is deemed a priority in the [March 2025 Government Work Report](https://english.www.gov.cn/news/202503/12/content_WS67d17f57c6d0868f4e8f0c0d.html), the [August 2025 State Council AI+ opinion,](https://cset.georgetown.edu/publication/china-ai-plus-opinions-2025/) and the [October 2025 Fourth Plenum 15th Five Year Plan proposals](https://cset.georgetown.edu/publication/china-fourth-plenum-proposal-2026/).
