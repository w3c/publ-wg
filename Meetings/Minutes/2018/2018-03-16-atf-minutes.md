---
layout: minutes
date: 2018-03-16
title: Publishing WG — Affordances’ Task Force Telco — 2018-03-16
---

# Publishing WG — Affordances’ Task Force Telco — Minutes
{: .no_toc}



**Date:** 2018-03-16

See also the [Agenda](https://goo.gl/mTxMDL) and the [IRC Log](https://www.w3.org/2018/03/16-pwgatf-irc.txt)

## Attendees
{: .no_toc}
**Present:** Mateus Teixeira, Avneesh Singh, Ivan Herman, jasmine, George Kerscher, Wolfgang Schindler, Katie Haritos-Shea, Tzviya Siegman, Franco Alvarado, Romain Deltour, Matt Garrish, Matt Garrish, Jasmine, Benjamin Young, Hadrien Gardeur, Zheng Xu

**Regrets:**

**Guests:**

**Chair:** Mateus Teixeira, Jasmine Mulliken

**Scribe(s):** Tzviya Siegman, Benjamin Young

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Mateus Teixeira:* [https://goo.gl/mTxMDL](https://goo.gl/mTxMDL)

> *Tzviya Siegman:* [https://docs.google.com/document/d/1BEiBAB-RU2FK2_3XZKUERfFi-nGwwFrMFvKe08e0-QQ/edit?usp=sharing](https://docs.google.com/document/d/1BEiBAB-RU2FK2_3XZKUERfFi-nGwwFrMFvKe08e0-QQ/edit?usp=sharing)

### 1. overview of our work, identify goals
{: #section1}

**Mateus Teixeira:** overview of our work, identify goals  
… Affordances apply to UX that is surfaced to a user in any context  
… our goal is to identify the experiences and formalize the requirements and frame them in a technical way  

> *Tzviya Siegman:* It is possible that we will kick some work back to the WG to integrate into the spec.

**Mateus Teixeira:** We hope to have something for F2F in May.  

**Mateus Teixeira:** We need participation from all communities (UAs, users, authors, publishers)  
… participation from non-technical people who are familiar with user needs is very helpful  

**Katie Haritos-Shea:** It sounds like we are talking about use cases  

**Mateus Teixeira:** We are talking the WPUB UCR as a starting point, but also the expectations of the user  

**Katie Haritos-Shea:** We are taking the existing use cases?  

**Mateus Teixeira:** We are also looking at how Packaged use cases might differ  
… the use cases might not be comprehensive, and we are not sure which can be speced  

> *Tzviya Siegman:* DPUB IG published [https://www.w3.org/TR/pwp-ucr/](https://www.w3.org/TR/pwp-ucr/)

**Avneesh Singh:** do we need to decide which issues should be provided by UA and which should be provided by WP?  

**Mateus Teixeira:** we discussed this months ago, and we had to wait until manifests and metadata to settle  
… for the purpose of this group, I think we should focus on use cases and then make the decision with the whole WG in the context of metadata/manifest  

> *Jasmine Mulliken:* Use case document: [https://www.w3.org/TR/pwp-ucr/](https://www.w3.org/TR/pwp-ucr/)

**Ivan Herman:** We have to be careful to separate use cases from what is in WP document, which will include a technical description of what we would like to see happen  
… example -I would like to be able to search through the whole publication, which can be bound back to several use cases  

> *Mateus Teixeira:* Related to ivan's comment: [https://github.com/w3c/wpub/issues/143](https://github.com/w3c/wpub/issues/143)

**Ivan Herman:** the question is what do we have to do for each affordance and what are normative requirements  

> *Avneesh Singh:* It would be good to have a template with one or two examples

**George Kerscher:** so we are specifying UA behavior?  

**Mateus Teixeira:** yes, but we also need to identify what a WP needs to provide in order for that behavior to happen  

> *Ivan Herman:* +1 to George

**Katie Haritos-Shea:** We are talking about the capabilities that have to be available to the publication and the UA has to support?  

**Mateus Teixeira:** Yes  
… and we need to identify what we can actually write as a spec. Some of these might be more along the lines of guidelines and best practices.  

**Benjamin Young:** example of affordances: HTML affords hypermedia (links & forms) and the browser provides the features needed to interact with them  

**Mateus Teixeira:** thank you for the affordance summary Benjamin. the distinction between features and affordances is helpful  
… and the fact that UA's use the affordance to enable features is useful  
… Going back to the google doc https://goo.gl/mTxMDL  
… I'd like to be clear about the scope of our  
… so that we don't have to deal with scope creep  
… we're only focused on affordances that have a pathway to features in the UA via the specification track  
… we shouldn't take on affordance related issues that might be enabled by other standards or other WGs  
… that's something we'll have to take into account on a case by case basis  
… accessibility and personalization are both things that may have affordance needs  
… but they will also need to have related features in UAs to enable them as accessible features, etc.  
… does that sound relatively straight forward?  

**Wolfgang Schindler:** as George mentioned there is a data aspect on the part of the publication  
… but you need some hooks in your data for the UA to offer some feature  
… do we see those as data requirements?  
… we need to express that these affordances have a pathway to the features we want in the UA  

**Mateus Teixeira:** yes. we need to define and clarify these pathways  
… I'm going to need help from the wider group who have more of a technical background than I do  
… certainly we need to clarify that these are spec-able and not just recommendations  

**Zheng Xu:** are we looking toward testing?  

**Mateus Teixeira:** yes. that sounds useful  

**Ivan Herman:** it's useful, but we have to be careful that we only test normative things from a spec perspective  
… and that some of these things will be expressed as non-normative things  

**Zheng Xu:** I wonder should we also work with some other WGs such as CSS  
… about some of these issues we may have?  

**Mateus Teixeira:** I don't think that item is about limiting what we can do  
… so much as proactively looking for the things that are in some other WG's domain  
… but we'd still want to monitor the progress, etc, if we need those things done  
… we need to filter out what we can do vs. what we can't  

**Zheng Xu:** my second question about personalization  
… it's a pretty wide space  
… I hope we can define what we want to do here  

**Jasmine Mulliken:** is that one of the bigger issues we discuss on Monday? tzviya?  
… it's #138  

> *Jasmine Mulliken:* [https://github.com/w3c/wpub/issues/138](https://github.com/w3c/wpub/issues/138)

**Mateus Teixeira:** it is more complicated than it seems  
… and we need to be very focused on the accessibility issues  
… and it's great that we have people who can help us navigate that as part of this group  

**Zheng Xu:** we need to both enable vendor options as well as work for interoperable personalization across vendors  

### 2. Work Items
{: #section2}

**Mateus Teixeira:** looks like the queue is empty  
… so let's move on to work items  

> *Mateus Teixeira:* [https://github.com/w3c/wpub/labels/topic%3Aaffordances](https://github.com/w3c/wpub/labels/topic%3Aaffordances)

**Mateus Teixeira:** let's look at this list as a starting point  
… this will take you to all the `topic:affordances` labeled issues  
… we need to go through this list and put them through our filtering  
… to find an implementation pathway  
… and what things we might need to let go of  
… or pass on to some other WG to do  
… and ivan made a "propose closing" label to help move things along the process  
… so let's start there  

**Katie Haritos-Shea:** there are a few of these like reading order which I'd be happy to take  

**Mateus Teixeira:** if you're able and ready to take on some of these, by all means!  

> *Mateus Teixeira:* [https://www.w3.org/TR/pwp-ucr/](https://www.w3.org/TR/pwp-ucr/)

**Mateus Teixeira:** the next item is really reviewing the use cases  
… and matching the against our issues  
… this document really outlines what we hope to enable with a Web Publication  
… it is very helpful to find our list of requirements or expectations  

> *Tzviya Siegman:* Josh Pyle and Laurent Le Meur are responsible for keeping the UCR up to date

**Mateus Teixeira:** so besides our GitHub issues list, may we also reconsider this use case document  
… additionally we may also need to make some of these part of PWP  
… or that are better done there than within just WP  
… again, our primary focus is on affordances for WP  
… so I'd suggest we focus there first  

**Ivan Herman:** so. first of all, yes for your last comment  
… for those who look over the use case doc to make links to whichever affordances we are considering  
… at the end of the day it would be great that for each affordance we make explicit reference to each of the requirements  
… and explain how it's backed up by these use cases  
… the more we keep that as part of our process, the easier it will be at the end  
… for the time being, just make not somewhere—in the issue or somewhere—then later Matt and I can work out getting it into the text  

**Jasmine Mulliken:** yeah. I think that's a great idea.  

**Mateus Teixeira:** great. that will definitely help use clarify these affordances  

> *Mateus Teixeira:* [https://github.com/w3c/wpub/issues/143](https://github.com/w3c/wpub/issues/143)

**Mateus Teixeira:** let's go after issue #143  
… we should also correspond this one to the use case requirements (UCRs)  
… it seems we should get on with this one sooner rather than later  

> *Tzviya Siegman:* +1

**Mateus Teixeira:** and then we can use that template going forward  
… I'd ask that all of us take a look at this #143  
… as it will greatly help our progress on the other issues  
… once we start clarifying some of the issues on GitHub, then we'll start forming them into this template  
… and run it through some other filters such as data requirements and making sure there's a pathway to implementation  

**Benjamin Young:** I'd not slow down on serialization discussions, but do define what the general data needs are to get to the end-goal feature (via the affordance)  
… for instance treating a WP as a collection of documents is part of affording search and progression  

**Mateus Teixeira:** I do think we may need to add parts into the template about that  

**Ivan Herman:** one more sort of warning to ourselves  
… we should not solve all the miseries of the world in the coming 2 months  
… we need to have a first viable product soon  
… so 80% of the needs perhaps  
… there will always be a 20% who will be unhappy  
… at the present time, we should live with that  
… we really don't want to get carried away by discussions—and it's very easy to do that  
… for all of us  

**Mateus Teixeira:** agreed we do need to avoid scope creep  
… for the template discussion, I can send a follow-up email  

**Ivan Herman:** email or issues comments?  

**Mateus Teixeira:** I'll do issue comments to keep things together  
… can anyone take that item?  

**Zheng Xu:** yes. I think I can do that  

**Mateus Teixeira:** thank you. let's aim for the end of March for that  
… we don't have anyone looking at the UCR doc atm  

**Katie Haritos-Shea:** I can do it, but I'm not sure what you want out of it  

**Mateus Teixeira:** yeah. it doesn't have to be done before the template is ready  
… but if we can get some discussion done while that's being ready  
… then we can do some writing after March  

**Tzviya Siegman:** I did much of the UCR to issue mapping already  

> *Tzviya Siegman:* Laurent and Josh Pyle

**Tzviya Siegman:** Josh Pyle and Laurent are keeping UCR things up to date  

**Tzviya Siegman:** it also looks like David Wood is back to active  
… and he can probably help here  

**Mateus Teixeira:** those are all the work items we've identified so far  
… if anyone thinks of anything else, we can set something up for a future call as well  
… for the meantime, let's keep things on GitHub and use email for side discussions  

**Jasmine Mulliken:** don't wait on the template to be done before you comment on the issues  

**Katie Haritos-Shea:** so find categories to help describe the issues?  

**Jasmine Mulliken:** yes. so find categories like "normative" and "non-normative" etc.  
… we don't have to wait on the template to have our discussions and organize things  

### 3. Meetings
{: #section3}

**Ivan Herman:** in my practice it's very helpful to have a fixed day/time for these meetings  
… it's early for Jasmine  
… and if we move it though, then Avneesh runs into time issues  
… Friday a bit later than now is still doable for both ends so to say  

**Mateus Teixeira:** one of the problems for this month is loads of conferences this month and next  
… I'll be sure to get something on the calendar and get it out with plenty of advance notice  

**Ivan Herman:** I'll get these minutes up to our website  
… you can try and do it on the github  

**Tzviya Siegman:** yeah. it's not that magical  
… ivan is the only one who can clean up the minutes  

**Ivan Herman:** it's my job  

**Mateus Teixeira:** bye all!  

---
