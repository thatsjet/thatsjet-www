---
author: Jet Anderson
categories:
- Engineering
keywords:
- DevOps, DevSecOps, Chef, automation and orchestration, CI, CI pipeline, serverless, alex ethier, Tower 3
date: 2018-03-01T01:00:00-00:00
title: "The Ultimate Shift-left: Education"
leadImage: "/images/posts/2018-03-01-secure_coder_sticker.jpg"
type: post
featured: true
draft: true
comments: false
---

At SourceClear we spend a lot of time thinking about how to get application security testing further left in the SDLC, especially for open source vulnerabilities. We build our platform to be ready for DevSecOps and use the same practices in our company that we encourage for our customers: scan early and often, fix critical defects fast, and embed security checks into continuous-integration pipelines.

And yet, as much as we see companies moving this direction I see another way we can move even further left:

**Education**

I recently completed a survey of CS degree requirements from United States Universities and found not a single degree program for computer scientists or programmers includes software security as a requirement for graduation. I've spoken to countless students over the past two years who are looking to learn more about secure coding and each time I've asked them about their experience in university all responded alike.

If you want to learn about software security you take cryptography... as an elective. No OWASP Top 10, threat modeling, no advanced secure coding, nothing.

## Where do security defects come from?
With this in mind let's explore where security defects in software come from, especially in open source.

At first glance our answer might be the obvious "from the programmers," but that would only tell part of the story. If you're a programmer yourself, think back to where you first heard of the OWASP top 10 or SQL Injection, or even Cross-site Scripting attacks. Many of the young programmers I meet are absolutely interested in exploring secure code but don't know where to start. Many times they're either working as an intern or starting their first full-time role as a Junior Programmer and are already overwhelmed at the complexities of working in an enterprise software development team.

For many, the first time they hear about security defects is either a) when a mentor starts reviewing their code, or b) when they see their first defect report from static analysis or software composition analysis tools like SourceClear.

This is obviously not the way to teach secure programming.

So, how would a good "Secure Programming" degree program unfold?

## Start with threat modeling (lite)

I believe in starting with a *"healthy dose of fear"* as the first step in teaching secure coding.  By embedding some simple threat modeling language into their vocabulary, we begin training young developers to think proactively about injecting security into their software.

Three questions for threat modeling light:

- What could go wrong?
- What will happen if it does?
- How can I avoid that?

**What could go wrong?**
This is the first step in thinking like a secure coder. I like to start by demonstrating some attack techniques to show new developers what it looks like when an application gets attacked p0wn3d. When they first see a SQL Injection flaw in a program and realize a database can be fully mapped and exfiltrated it's an eye-opener.

Also, make sure they have at least *heard* of STRIDE:

- Spoofing
- Tampering
- Repudiation (It wasn't me!)
- Information disclosure
- Elevation of Privilege

**What will happen if it does?**
Next, exploring the impact of a flaw ensures that junior programmers understand the cost of a threat being realized. When they see "DROP DATABASE; or DROP TABLES;" and understand they could spend their on-call time restoring their app they really start to get it. Teach new programmers about threats to **Confidentiality, Integrity, and Availability** and the threat becomes real.

**How can I avoid that?**
Now that a healthy dose of fear is achieved, new programmers are ready to learn about ways to protect their applications. The [OWASP Top 10 Proactive Controls](https://www.owasp.org/index.php/OWASP_Proactive_Controls) is an EXCELLENT resource to train new developers. Spend time walking through each of the  these simple to learn and easily implemented techniques and you'll have secure coders in no time.

## Conclusion
I believe a big part of achieving this kind of training as a reality is for application security practitioners to realize one thing: developers want to do good work, especially new developers. They are learning to build things they can be proud of, and learning to do things securely (and not do them over again when flaws are found) is a big part of that.

As a minimum, ensure that every developer in your company understands secure coding threats and controls, whether they're just starting out or have been programming for decades.
