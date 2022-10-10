---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
style: |
  .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
  }
  
---
![bg left:40% 80%](https://avatars.githubusercontent.com/u/54452117?s=200&v=4)

# **Agile Security**

Incorporating Security in the Agile Process

_by Ramiro Salas, CISSP_
_@ramirosalas_

---
<!-- _class: lead -->
# Context and Motivation

---
# What's 'Agile' Anyways?

![bg center:60% 60%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

---
# 2001: The Manifesto

![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

- Values:
  * **Individuals and interactions** over processes and tools
  * **Working software** over comprehensive documentation
  * **Customer collaboration** over contract negotiation
  * **Responding to change** over following a plan

---
# Agile software development
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)


* Promotes well-planned, small iterations by highly collaborative, cross-functional teams
* Emphasizes continuous self-organization, testing, and monitoring that results in fast and frequent delivery of software

---
# What Agile really means

![bg left:25%](https://www.blocshop.io/wp-content/uploads/2021/06/agile-metrics.png)

> Embracing the iterative nature of continuous innovation through open communication and fast feedback loops between developers, business stakeholders, and customers.

---
# The Landscape
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

### > Methodologies

- Agile software development
- Lean development
- User-centered design (UCD)

---
# The Landscape
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

### > Frameworks

- Extreme programming (XP)
- Scrum
- Kanban
- Scaled agile framework (SAFe)

---
# Risk in Assumptions
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

All Agile frameworks and methodologies emphasize deep partnership with customers/stakeholders, but sice **Security** is a non-functional requirement, it's not called out explicitly anywhere. 

**It's _expected_ it will naturally emerge
as a requirement**

---
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)
<div class="columns">
<div>

## Expectation

The right security requirements will always be uncovered

</div>
<div>

## Reality

No domain expert or stakeholder from the customer was present during the initial project meeting. Therefore, not all security requirements were captured.

</div>
</div>

---
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)
<div class="columns">
<div>

## Expectation

The MVP will be refactored later to include security features.

</div>
<div>

## Reality

MVP moves to pre-prod or prod stage “as is” and never has the chance to be refactored for security until a future iteration, leaving a potential gap that can be exploited.

</div>
</div>

---
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)
<div class="columns">
<div>

## Expectation

Most threats can be simulated and coded into CI/CD tools.

</div>
<div>

## Reality

New threat vectors are being discovered constantly, adding pressure and complexity to CI/CD workflows.

</div>
</div>

---
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)
<div class="columns">
<div>

## Expectation

 Any group of smart engineers can address most security requirements.

</div>
<div>

## Reality

Domain expertise and experience continues to prove itself crucial, as threats come in a variety of forms, not all well-known outside specialist circles.

</div>
</div>

---
# The danger of 2x2 oversimplification

![bg center:55% 55%](https://buildd.s3.amazonaws.com/impact-effort-matrix.jpg)
<br>
<br>
<br>
<br>
_Security stories are at risk of being labeled as “difficult” and of “less impact,” hence being relegated to a lower place in Icebox._

---
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)
<div class="columns">
<div>

## Expectation

Security stories will be naturally high in the backlog.

</div>
<div>

## Reality

Security-related stories have no more chance of being prioritized higher in the backlog than any other type of story and can even be prioritized lower.

</div>
</div>

---
<!-- _class: lead -->
# So, how do we solve this?

---
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

# Tag Security Stories
1) Any story labeled with Security, MUST be delivered and accepted before an MVP can be declared available.

2) Security concerns brought up via sticky cards in problem discovery exercises cannot be de-scoped, regardless if they are considered difficult. The Security SME has veto power to force the stickiness of the label.

_(tech previews and POCs may be exempt)_

---
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

# Leverage Security SMEs

1) Asking the right questions to the customer during each inception or iteration zero, and ensuring stories and epics properly capture the security outcomes.

3) Ensuring the language in each security-related story is clear, descriptive, and narrow, without assuming developers have previous experience in the area.

---
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

# Develop Expertise
- Encourage security as a career path
- Incentivize, fund and prioritize training and certifications such as ISC2's [CSSLP](https://www.isc2.org/Certifications/CSSLP#).
- Create mentoring models such as the [Champion Program](https://www.devseccon.com/ep-79-ep-training-security-champions/)


---
# Agile _Rituals_
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)
- **At Standups**
  - Have the Security SME share an interesting fact or tip, or discuss a recent public incident, bringing security awareness to the forefront.
- **At Retros**
  - Include a Security element in the retro. What have we learnt this week?
---
# Adversarial Personas
![bg left:20%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)
<style scoped>
    section {
        display: block;
    }
    table {
        width: max-content;
        float: left;
    }
</style>
Include adversarial personas in design exercises.

|Role|Name|Explanation|
|--------|--------|--------|
|Adversaries |Eve|Passive Eavesdroper|
||Mallory|Active interceptor|
||Fred|Forger|
||Daffy|Disruptor|
||Mother Nature|Natural events|
||Brutus|Users (intentional or not)|

---
# Adversarial Personas
![bg left:20%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

<style scoped>
    section {
        display: block;
    }
    table {
        width: max-content;
        float: left;
    }
</style>

|Role|Name|Explanation|
|--------|--------|--------|
|Adversary Agents |Dopey|Dim attacker|
||Einstein|Smart attacker|
||Rockefeller|Rich attacker|
||Klaus|Inside spy|
||Vlad|Nation-state attacker|

---
# Agile and Systems Architecture
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

In some Agile frameworks, systems architecture is considered an antipattern.

Methodologies like [SAFe](https://scaledagile.com/) see architecture as a pattern that emerges as a result of collaboration, while embracing rapid iteration, prototyping & testing, and active stakeholder participation.

---
# Tech Debt on Security
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

It emerges when security-centric refactoring is skipped or delayed in favor of other priorities.

Think in terms of **Minimum Viable Secure Product** (MVSP).

---
# Declare & Automate!
![bg left:25%](https://d1fto35gcfffzn.cloudfront.net/images/og/topic-agile.jpg)

- Embrace DevSecOps by autmating as many security processes as early as possble.
  - [SAST](https://www.synopsys.com/glossary/what-is-sast.html), [DAST](https://www.microfocus.com/en-us/what-is/dast) and [RASP](https://www.checkpoint.com/cyber-hub/cloud-security/what-is-runtime-application-self-protection-rasp/)

- Use declarative techniques to drive everything-as-code (i.e. policy, compliance, etc).
  - [OpenSCAP](https://www.open-scap.org/)
  - [OpenControl](https://open-control.org/)
  - [OPA](https://www.openpolicyagent.org/)

---
# <!-- _class: lead -->
# Thank you

`https://github.com/RamXX/agile-security`

---
# References

- [1][The original Agile Manifesto](http://agilemanifesto.org/)
- [2][Agile in Tanzu](https://tanzu.vmware.com/agile)
- [3]Innovate Magazine, Issue 14, p22, VMware R&D, February 2020
- [4][Adversarial personas](https://courses.cs.washington.edu/courses/cse599r/08au/LectureNotes/Crypto599class1.pdf)
