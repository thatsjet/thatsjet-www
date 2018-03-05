---
title: "Securing the SDLC"
date: 2016-05-02T01:00:00-00:00
---

I had the opportunity to speak last week at my local [ISSA chapter](http://portland.issa.org/) on the topic of ***Securing the Software Development Lifecycle.***  Given the interest it generated among the attendees I realized that this is a topic for **MUCH** further discussion worthy of at least a few blog posts on thatsjet.com. Today's post is just a high level introduction, hitting the high points of my talk and in the coming weeks I'll be writing a few follow up posts with greater detail around the finer points.

## Software Powers The World
Today's organizations buy or build software at a rate MUCH quicker than we can secure it. That is just a fact. In a 2011 article on [Forbes](http://www.forbes.com), Author David Kirkpatrick described the problem well.

> "Ford sells computers-on-wheels. McKinsey hawks consulting-in-a-box. FedEx boasts a developer skunkworks. The era of separating traditional industries and technology industries is over—and those who fail to adapt right now will soon find themselves obsolete." - David Kirkpatrick

I've heard top CEOs of the Fortune 100 say much the same, realizing that where yesterday they were managing the business, relationships, and customers; today they are managing teams of software developers, advanced persistent threats, and mountains of critical data.

## With Innovation Comes Risk

So, with the volume of software increasing it's no wonder that the number of security incidents reported globally are increasing year over year. According to the **[2016 Data Breach Investigations Report](http://www.verizonenterprise.com/verizon-insights-lab/dbir/2016/)** from **Verizon Enterprise Labs** (Figure 1.1), web applications were the TOP attack vector, comprising 40% of the total number of breaches in 2015. Add to that the various other attack vectors that fall into the "software" category, and we have a serious problem of scale for our efforts to secure them.


![Image](/images/posts/2016/2016-verizondbir-webtopvector.png)

*Figure 1.1- Verizon's '2016 Data Breach Investigations Report - Incidents by Attack Vector*


## So What Do We Do?
Next Week I'll talk more about the problem of Resourcing Secure Software Development, but before we all hang ourselves over the scope of the problem, let's examining a few ways to start today with becoming part of the solution.

### Be Agile
As a developer for many years, one of the great migrations I've seen  is less about technology and more about process. Software projects used to take months or even years of planning, development, and testing. With the shift towards Agile and Agile-like methodologies such as Kanban, XP, and others, we've broken changes down to smaller bits that we attack on a daily, weekly, or monthly schedule in "sprints" which drastically improves time to market and our ability to innovate.

The problem though, is much of the information security process has failed to adapt to this change. A large part of our threat modeling and risk analysis was so tied to the long term schedules of the waterfall process days gone by, that we failed to keep pace with the change. It's easy to blame the lack of qualified Practitioners or budget dollars, but the truth is, we desperately need to re-think how we engage with our innovation minded peers.

So what can we do to catch up?

***Think Agile!***

Agile development isn't just about changing the development timeline, scope or process. It centers around some other key elements that I belive hold the key for information security.

#### 1) Collaborate

A key function of Agile processes is the heavy emphasis placed on good collaboration. Daily stand up meetings, which are simply a quick hallway chat, round table, or conference call (by quick we mean like 15-30 minutes) are a standard practice.

So, the first thing to do is ask yourself, how can I better collaborate with software teams?

Three ways I've found to bridge the collaboration gap are:

- **Get Involved Early:** Security Analysts need to be part of the kickoff for EVERY SPRINT! Be part of the process, provide support, and point to solutions where you can.
- **Tiny Threat Models:** I'll unpack this in greater detail in a future post, but suffice to say now that our desire to create detailed, perfect, bullet-proof threat models is a throwback to the Waterfall method days gone by. If we're going to be effective at changing our mindset, we must look for ways to ask a simple series of questions at the outset of each sprint. Doing so reinforces the questions in the minds of developers who will get used to hearing:
  - Does this story involve the use of customer data?
  - How will the data be handled in use?
  - How will the data be stored at rest?
  - ...etc.

- **Make Champions:** By this point you might be yelling at me through your monitor saying something like *"Infosec can't possibly be part of every story!"*, and you're right, you can't be everywhere and there simply aren't enough practitioners to go around. But, what if you trained one or two of the software developers on each team as an *"Application Security Mentor"* of sorts? Get them trained on not just what to look for during code reviews (another vital part of Agile processes), but also how to fix them. I've found that these folks become extensions of our team, often volunteering for the job as a way to extend their skillset. Options for training abound for key vulnerabilities and limiting the scope to mentor volunteers also enables us to limit the spend on training. All must take the basics, mentors get extra.

#### 2) Think Small

The next thing we can do to think Agile is *STOP THROWING THE ENTIRE SET OF DISCOVERED VULNERABILITIES OVER THE WALL AND EXPECTING THEM TO GET FIXED! DAMMIT!!!*

Okay, rant over.

No, but seriously. One of the next greatest parts of the Agile mindset is breaking the problem down into small "stories" that can be completed in a single sprint. So how can we do this in terms of security?

First, I would suggest we start by paring down the ***OWASP Top Ten*** to what I like to refer to as the ***OWASP Top 2***, namely *Cross Site Scripting (XSS)*, and *[SQL Injection (SQLi)](http://codecurmudgeon.com/wp/sql-injection-hall-of-shame/)*. This benefits us in two ways. First, by setting a filtering policy on our vulnerability result set such that we limit the number of vulnerabilities requiring immediate action we take advantage of the *Principle of Psychological Psychological Acceptability*, playing to the mindset of developers that we are a trusted advisor, helping THEM secure the software their company needs to compete. By and large XSS and SQLi are in my experience the most frequently found and easiest flaws to remediate. By starting with these we drastically reduce risk, quickly, without creating a scenario where developer simply ignore us in favor of creating the next innovate shiny widget.

Once we eliminate the top flaws, then we open the policy valve to include the next item in the list like Carriage Return Line Feed (CRLF) and so on.

#### 3) Iterate
Finally, the last way we can adopt an Agile mindset is similar to the last point. We've all heard the concept of *"crawl, walk run"* but this is probably one of the most important points in this post:

*"Perfect is the enemy of good... or good enough"*

In our zeal to secure.all.the.things... we sometimes become our worst enemy. If we're going to think Agile, we have to learn to iterate. Do a little now, do a little more, and eventually we'll be done. Or maybe almost done, as new flaws will be introduced and new exploits will be found.


## Going forward, never back
Wrapping up I'd definitely stress, to adapt to and ever changing threat landscape we have to learn not adapt our methods as well. Our adversaries tirelessly poke, prod, and adapt their tactics, we have to as well. Thinking Agile-like means sharing information, being part of the solution not the problem, and being willing to change.

I wish you the best of luck in your quest. Stay tuned for future updates and expanded ideas on the topic of Securing the SDLC.
