---
layout: minutes
date: 2018-03-16
title: Publishing WG — WAM Task Force Telco — 2018-03-16
---

# Publishing WG — WAM Task Force Telco — Minutes
{: .no_toc}



**Date:** 2018-03-16

See also the [Agenda](https://lists.w3.org/Archives/Public/public-publ-wg/2018Mar/0079.html) and the [IRC Log](https://www.w3.org/2018/03/16-pwg-manifest-irc.txt)

## Attendees
{: .no_toc}
**Present:** Ivan Herman, Zheng Xu, Franco Alvarado, Dave Cramer, Benjamin Young, Hadrien Gardeur, Romain Deltour, Tzviya Siegman, Tim Cole, Matt Garrish

**Regrets:**

**Guests:**

**Chair:** Benjamin Young

**Scribe(s):** Dave Cramer

## Content:
{: .no_toc}

* TOC
{:toc}
---


### 1. Work organization, high level issues
{: #section1}

> *Benjamin Young:* Our project space: [https://github.com/w3c/wpub/projects/3](https://github.com/w3c/wpub/projects/3)

**Benjamin Young:** how do we come at these problems as a group, and organize our project?  
… I've found everything with topic:manifest  
… we're focusing on what might go into WAM  
… they have an extension mechanism  
… we need to figure out what we need to talk to WAM task force about  
… feel free to fix any labeling issues  
… any questions?  
… we have an unknown column  
… the definitely column has to go to WAM  
… handled elsewhere means, 'this isn't us'  

**Ivan Herman:** there are two things  
… when we say to WAM, "we need these things" or adaptations  
… but sometimes what they have there we can use, even if the name is weird  
… these two things are not the same  

**Benjamin Young:** should we change column labels?  

**Ivan Herman:** a new column where we say we just use WAM  

> *Hadrien Gardeur:* [https://github.com/w3c/wpub/issues/127#issuecomment-363063172](https://github.com/w3c/wpub/issues/127#issuecomment-363063172)

**Ivan Herman:** Hadrien made a list of those  

**Benjamin Young:** some of these are large issues, which may be removed from this board  

**Romain Deltour:** some of these issues are buckets indeed, and we may split them into smaller issues  
… these columns are helpful for triage  
… we have to figure which features can be added with current WAM extension mechanism  
… and which features might need an additional layer on top of WAM, like an API  
… we can refine labels and issues  

> *Tzviya Siegman:* Hadrien's proposal for using WAM [https://github.com/w3c/wpub/issues/118](https://github.com/w3c/wpub/issues/118)

> *Tzviya Siegman:* and [https://github.com/w3c/wpub/issues/127](https://github.com/w3c/wpub/issues/127)

### 2. triage of specific issues
{: #section2}

**Benjamin Young:** let's work through this left-hand column  

#### 2.1. https://github.com/w3c/wpub/issues/32
{: #section2-1}

**Benjamin Young:** we should close #32 and take it off the board  

**Ivan Herman:** one of those horrendously long things...  

**Tzviya Siegman:** ivan, do you think we can close issues here?  

**Ivan Herman:** we should propose it, but let group decide.  

> **Proposed resolution: mark #32 as "propose to close" and remove from WAM TF project** *(Benjamin Young)*
{: .proposed_resolution}

**Romain Deltour:** we could leave open and continue to comment  

**Benjamin Young:** let's leave open and mention in other issues  

> *Romain Deltour:* +1

> *Ivan Herman:* +1

> *Tim Cole:* +1

**Benjamin Young:** new proposal is to leave open but remove from project  

> **Proposed resolution: leave #32 open but remove it from the project; mention it in other issues** *(Benjamin Young)*
{: .proposed_resolution}

**Benjamin Young:** issue #127 is next, it's a similar thing  
… with more actionable commentary, and links to other issues  

#### 2.2. https://github.com/w3c/wpub/issues/127
{: #section2-2}

> *Benjamin Young:* [https://github.com/w3c/wpub/issues/127#issuecomment-362548707](https://github.com/w3c/wpub/issues/127#issuecomment-362548707)

**Romain Deltour:** let's add another column for issues from which we want to extract smaller issues before closing  

> **Proposed resolution: move #127 into new Extract Smaller Issues column** *(Benjamin Young)*
{: .proposed_resolution}

> *Ivan Herman:* +1

> *Tim Cole:* +1

> *Benjamin Young:* +1

> *Romain Deltour:* +1

#### 2.3. https://github.com/w3c/wpub/issues/54
{: #section2-3}

**Benjamin Young:** this may be one of the more general things, and it might be mislabeled  

> *Benjamin Young:* "Obtaining language from http headers" is the title of #54

**Ivan Herman:** if I do an http request to the publication, I may get a language tag  
… the way the issue is formulated is not exact  
… the question is what do we do with that language tag?  
… that language tag is the language of the resource itself, and we can't change that  
… the language we use in the manifest is something else  
… it is the language of the terms in the manifest  
… whatever comes in from HTTP is irrelevant for the manifest itself  

**Hadrien Gardeur:** that's not entirely true  
… what you said is right for the resources of the publication  
… for the WAM, people do translate the manifest itself  
… based on accept-language header, they do negotiation, and return a translated manifest  
… so we need to separate language of resource from language of manifest  

**Ivan Herman:** I understand  
… I have impression that what they do is incorrect  

**Hadrien Gardeur:** on the web your browser requests a language, and server returns that language  

**Ivan Herman:** if I make an http request, I get an html file, and from the html file I link to the manifest  
… what I get from http is the language of the resource  

**Hadrien Gardeur:** you can do indirection  
… if I say accept-langage: fr I might get french manifest  

**Benjamin Young:** it's very nuanced and not related to our task with WAM  
… the WAM inbound language stuff defines only the content of the WAM  
… it does not dictate language of resources of the web app  
… I'm not sure this is a WAM issue, but it may be an issue of publication-wide...  

**Ivan Herman:** Hadrien is right when we look at the HTTP response for the manifest file itself  
… this is a "handled elsewhere" item  

**Hadrien Gardeur:** right now our infoset is consistent with WAM  
… and in our WebIDL  
… it provides default language for members of manifest  
… but we're consistent  

**Ivan Herman:** the http header does that  
… I would say that issue is subject to close  

**Hadrien Gardeur:** there could be lang negotiation on resources ourselves  

**Benjamin Young:** the way the web works is no one considers the WAM language a default  

**Hadrien Gardeur:** we're doing the same thing in the infoset  

**Ivan Herman:** it's only about the metadata  

> **Proposed resolution: move #54 to "handled elsewhere" column and possibly mark as "possibly close"** *(Benjamin Young)*
{: .proposed_resolution}

**Romain Deltour:** sounds good  

> *Benjamin Young:* +1

#### 2.4. https://github.com/w3c/wpub/issues/58
{: #section2-4}

**Benjamin Young:** next issue is #58  

**Hadrien Gardeur:** this is infoset related. shouldn't be here  

**Benjamin Young:** do we have an infoset label?  

**Ivan Herman:** no  

**Hadrien Gardeur:** there's a label for metadata  

> **Proposed resolution: remove topic:manifest label from #58 and move to "handled elsewhere" column** *(Benjamin Young)*
{: .proposed_resolution}

#### 2.5. https://github.com/w3c/wpub/issues/67
{: #section2-5}

**Benjamin Young:** #67  
… should linking from manifest support URI templates?  

**Ivan Herman:** guilty on that one  
… I would postpone to next version. Let's not go down that road now.  

**Tzviya Siegman:** we have a defer label  

> *Dave Cramer:* (musical interlude)

**Hadrien Gardeur:** your idea of using uri template was different from mine  
… and easy way of declaring a bunch of resources are part of default reading order etc  
… i think that use case is impossible  
… but for providing user search or api, we're going to need URI templates  
… the impact on webidl and spec is minimal  
… we just need a flag for a URL  
… it's fine to defer, but we need to separate this concept from using templates for declaring a list of resources  

**Ivan Herman:** as I said, postpone  

> **Proposed resolution: remove #67 from the WAM project board and mark as "postpone"** *(Benjamin Young)*
{: .proposed_resolution}

> *Romain Deltour:* +1

> *Ivan Herman:* +1

**Ivan Herman:** I don't think this is a part of a minimum viable project  

> *Tim Cole:* +1

> *Dave Cramer:* +1

#### 2.6. https://github.com/w3c/wpub/issues/59
{: #section2-6}

**Benjamin Young:** next is #59  
… avoiding resource declaration duplication  

**Hadrien Gardeur:** I think this is easy to solve  
… in RWPM what's in the reading order doesn't need to be in list of resources  
… EPUB has a lot of duplication, and the id/idref thing  

**Ivan Herman:** in a sense, this is a meta issue, this is how we should do all our thing  
… keep it as handled elsewhere  

**Hadrien Gardeur:** infoset and serialization  

> **Proposed resolution: move #59 to "handled elsewhere"** *(Benjamin Young)*
{: .proposed_resolution}

**Romain Deltour:** it's also infoset  

**Benjamin Young:** move to 'handled elsewhere'  

**Ivan Herman:** then I will also add topic:metadata  

#### 2.7. https://github.com/w3c/wpub/issues/63
{: #section2-7}

**Benjamin Young:** next is #63  

**Romain Deltour:** remove from project board  

**Benjamin Young:** this is not related to manifest  

> **Proposed resolution: remove #63 from the board; change labels** *(Benjamin Young)*
{: .proposed_resolution}

**Tzviya Siegman:** we'll call it "bikeshed" :)  

#### 2.8. https://github.com/w3c/wpub/issues/163
{: #section2-8}

**Benjamin Young:** next is #163  

**Ivan Herman:** this is indirectly with the WAM  
… we want from WAM we may want to link to other metadata  
… the privacy policy may have it's own vocab  
… just like linking to ONIX  

**Romain Deltour:** I agree there's a general issue  
… but there might be differences depending on the manifest  
… some handled in WAM, some externally  

> **Proposed resolution: move #163 to "possibly" column** *(Benjamin Young)*
{: .proposed_resolution}

**Ivan Herman:** now we say "possibly"  

**Hadrien Gardeur:** this one is mine along with linking to external metadata record and a third one... linking to alt rep  
… I think all three should be "possibly"  

> *Benjamin Young:* also [https://github.com/w3c/wpub/issues/162](https://github.com/w3c/wpub/issues/162)

**Hadrien Gardeur:** they could have a common tech solution  

> *Benjamin Young:* also [https://github.com/w3c/wpub/issues/159](https://github.com/w3c/wpub/issues/159)

> **Proposed resolution: move to #159, #162, #163 the "possibly" column** *(Benjamin Young)*
{: .proposed_resolution}

**Hadrien Gardeur:** WAM has links, they are just specialized  

**Ivan Herman:** they are link to specific resources, which is different than linking to metadata  

**Benjamin Young:** it's not the expectation of this task force to find a home for all things in WAM  
… we don't know if we'll go there with our entire infoset  
… depends on what they're willing to do, and what might be better elsewhere  

**Romain Deltour:** Marcos was lukewarm about generic metadata in WAM  
… the basic principle was that metadata in WAM should be directly beneficial to end user (agent)  
… if we think otherwise, then we need to document with use cases and build our case to present to wam editors (and TAG)  

**Hadrien Gardeur:** for  alt rep and privacy, these are actionable for end user  
… I think we need to make sure that whatever is publication specific should be at collection level, in WAM  
… most can go through generic extension mechanism  
… we should only worry about when we have conflicts  
… or things that are useful for the larger community  

**Benjamin Young:** I don't think we're looking at the WAM cohesively  
… it's just config settings for a runtime  
… and category data for app stores  
… the things that might make it into WAM are things that might help with creating a runtime, like a privacy policy  
… right now they say link to it  
… privacy settings might go in a manifest, but not a privacy policy  
… there's a conceptual difference between what WAM is and what they expect it to be  

**Romain Deltour:** when Hadrien said that we can solve things with extensions, we don't have to go to the group  

**Romain Deltour:** I think we should go to them, we would hope that some of our extensions are implemented by browsers  
… we should liaise with the editors even as we use their extension mechanism  

**Hadrien Gardeur:** we have to do that anyway  
… there's a big difference between using an extension, and changing the manifest itself  
… I disagree with Benjamin. If we're not using the wam for defining a collection, and we spread information around, I don't see the point of using the WAM  
… for an extension we would declare reading order, and if we don't what's the point?  

**Zheng Xu:** I get confused about who consumes the manifest? publisher? reading system vendor?  
… if we define affordance layer, it could be extension of WAM  
… but a web publication is different than web app, as the creator is not a developer  
… I want to focus more on infoset which is related to creator/publisher  
… might not to need extension or related to WAM  

#### 2.9. https://github.com/w3c/wpub/issues/73
{: #section2-9}

**Benjamin Young:** #73, modification date  

> **Proposed resolution: relabel 73 as info set; remove from project** *(Benjamin Young)*
{: .proposed_resolution}

**Benjamin Young:** relabel and remove, as it's an infoset question  

> *Romain Deltour:* +1

**Benjamin Young:** next is 118  

#### 2.10. https://github.com/w3c/wpub/issues/118
{: #section2-10}

**Benjamin Young:** break up into smaller things?  

**Hadrien Gardeur:** yes  

#### 2.11. https://github.com/w3c/wpub/issues/119
{: #section2-11}

**Benjamin Young:** #119, using RWPM  

**Hadrien Gardeur:** not related to WAM, but an alternate proposal  
… even if we go with WAM this can inspire extensions  

#### 2.12. https://github.com/w3c/wpub/issues/122
{: #section2-12}

**Ivan Herman:** JSON manifest as script element--we have to discuss this with WAM  
… we shouldn't spend time on it now  

#### 2.13. https://github.com/w3c/wpub/issues/148
{: #section2-13}

**Hadrien Gardeur:** this is mostly useful for single resource publication  

**Benjamin Young:** #148  
… limiting reading order to manifest  

**Hadrien Gardeur:** infoset-related  

> *Benjamin Young:* removed from the board

#### 2.14. https://github.com/w3c/wpub/issues/126
{: #section2-14}

**Benjamin Young:** 126, progression direction  
… probably remove or handled elsewhere?  

**Ivan Herman:** it's something that we would put in our extension, and they shouldn't fuss  

**Hadrien Gardeur:** this goes in possibly, because it's part of our extension  

#### 2.15. https://github.com/w3c/wpub/issues/167
{: #section2-15}

**Benjamin Young:** 167  
… roles for creators  

**Hadrien Gardeur:** how do we express creators in general in our serialization?  
… this is definitely possibly  
… we should discuss with WAM  
… as this is not publication specific  

> *Tzviya Siegman:* see ivan's comment [https://github.com/w3c/wpub/issues/167#issuecomment-373455166](https://github.com/w3c/wpub/issues/167#issuecomment-373455166)

**Zheng Xu:** there is a lot of duplication between creators and ONIX  
… can this information be related similar to ONIX?  

**Hadrien Gardeur:** handling ONIX is like spending your holiday in hell  
… and we shouldn't assume we'll get ONIX  
… and there is never ONIX for some kinds of publications  

**Benjamin Young:** the wam's way of doing metadata is scary, as they make a new top-level key for everything  

**Hadrien Gardeur:** you need creator/dev/company even in web apps  
… MS has been using manifest for their store  

> **Proposed resolution: move #167 to "possibly" and add refined use cases** *(Benjamin Young)*
{: .proposed_resolution}

**Ivan Herman:** we're at the top of the hour  

> *Romain Deltour:* +1

**Ivan Herman:** #150 is comments to Brady from Chrome team; 90% was for infoset rather than what we're discussing now  
… let's put in handle elsewhere column  

> *Romain Deltour:* Next call: March 28th (2 weeks from today) @ 14:00 UTC

> *Ivan Herman:* [https://github.com/w3c/scribejs](https://github.com/w3c/scribejs)

---
