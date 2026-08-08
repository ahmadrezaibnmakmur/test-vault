# 1. Introduction

SaaS firms compete not only through product features but also through the reliability of customer support [1]. Live-chat support records show whether product-related inquiries are solved at first contact or become repeat work [2]. In this setting, first contact resolution (FCR) is a critical-to-quality measure because it captures whether a customer receives a complete answer without additional follow-up, handoff, or escalation.

For a subscription-based software provider, unresolved issue inquiries create a double burden. Customers experience waiting time and repeated explanation [1], while the support organization absorbs rework through additional validation, technical escalation, and delayed closure [2]. Therefore, non-first-contact-resolution (Non-FCR) inquiries can be treated as service-process defects rather than only as isolated customer complaints.

In service operations, repeated follow-up, technical handoff, waiting, and extra validation are forms of waste in lean service [3]. Such waste can be classified and made visible through process data [4]. Lean Six Sigma is suitable for this problem because it links that waste view to defect measurement and structured process control [5]. The DMAIC structure also helps prevent the analysis from jumping directly to solutions before the defect pattern is measured.

The baseline also indicates that the problem is not only the existence of defects but also the instability of monthly performance. As shown in Fig. 1, Non-FCR and SLA-breach rates fluctuate across the year, suggesting that the process needs a structured improvement logic that can define the defect, identify the dominant source, and monitor the result after improvement.

The empirical context of this study is a SaaS live-chat support process. The 2025 baseline contained 39,414 issue inquiries, of which 34,675 were resolved at first contact and 4,739 became Non-FCR defects. This means that 12.02% of issue inquiries required additional handling beyond the first interaction.

![](assets/figure-01.png)

Fig. 1. Baseline fluctuation of Non-FCR and SLA breach in 2025.

Prior Lean Six Sigma research in call-centre operations shows that DMAIC can improve resolution performance [5]. Later call-centre and customer-support studies report similar lean improvement logic [6], business-process improvement [7], and delay reduction [8]. Service-improvement studies also use SIPOC, DPMO, Pareto, improvement actions, and control planning for diagnosis and control [9]. This study extends that logic to SaaS live-chat support, where issue-category data and CS-engineering follow-up notes trace recurring defects from customer symptoms to process and system causes.

Accordingly, this study asks two research questions: RQ1, how are Non-FCR defects distributed across product and issue-tag dimensions in SaaS live-chat support? RQ2, how can a DMAIC-based process diagnose dominant Non-FCR causes and indicate early changes in FCR, DPMO, and SLA-breach performance?
