---
layout: default
---

# The practicalities of the self-publishing process
{: .no_toc}

Publishing the group’s Working Drafts is done via a combination of GitHub and a W3C tool called [Echidna](https://github.com/w3c/echidna/wiki). The high-level points to remember:

- a separate branch is defined for all the group’s GitHub repositories, called `publishd_wd`;
- every time the `master` branch is merged **_into_** `publish_wd` (and pushed to the repository) the document is automatically published on the W3C site as the "latest version" of the official Working Draft.

What this means in practice is that the group can publish a Working Draft as often as its desires without any human intervention from the W3C staff.

Some more details for the technically inclined/interested are below. (All the examples use the `wpub` repository as an example, the other repositories are set up in a similar fashion.)

* TOC
{:toc}


## More detailed steps for editors

The goal of these steps is that the editor does not have to significantly change the editor’s draft, which is in using `respec`.

### Preparation of the `respec` source

There are some rules to remember, all of them related to the `respecConfig` content. These are to be set once.

1. The data of each editor _must_ include the `w3cid` field, identifying the person in the W3C database. This number appears on the page of the person’s profile page at W3C; alternatively, the staff contact can find it.
2. Do not add a `publishDate` field in `respecConfig`; this means that the day of the publication will be  automatically used.

### Check the document with the pubrules' checker

It is _required_ to check the document using the [W3C pubrules’ checker](https://www.w3.org/pubrules/) when publishing W3C drafts. The problem is that, by default, the pubrules’ checker operates on final HTML documents, not on sources in `respec`. There are, however, some tricks (worth remembering anyway) that can be used in combination.

- It is possible to force `respec` to generate, on-the-fly, a slightly different version of the document than what is in the source by providing some `respecConfig` values in the URL. For example:
    - [`https://w3c.github.io/wpub/?specStatus=WD`](https://w3c.github.io/wpub/?specStatus=WD) produces a `WD`, regardless on whether the document itself refers to `ED`. One can use this to generate a specific version of the document _without_ modifying the original `respec` source.
- There is a [`spec generator`](https://labs.w3.org/spec-generator/) service at W3C that can run `respec` via a server process generating the right document. Using the previous URL, this:
    - [`https://labs.w3.org/spec-generator/?type=respec&url=https://w3c.github.io/wpub/?specStatus=WD`](https://labs.w3.org/spec-generator/?type=respec&url=https://w3c.github.io/wpub/?specStatus=WD)

    generates the right version of the document.
- Use this URL in the pubrule’ checker input field.

One error _is_ reported: it refers to a the missing `common.css` file. This is related to the way the spec generator works; we can safely ignore this error.

(Note that, at this moment, there is a small bug in the pubrules’ checker, and it reports a bunch of errors if the `§` is used in the TOC header. Adding the `;includePermalinks=false` to the URL takes care of this, ie, [`https://labs.w3.org/spec-generator/?type=respec&url=https://w3c.github.io/wpub/?specStatus=WD;includePermalinks=false`](https://labs.w3.org/spec-generator/?type=respec&url=https://w3c.github.io/wpub/?specStatus=WD;includePermalinks=false) does the trick.)

### What files are to be published?

(This group would refer to this problem as the list of constituent resources:-)

The repository contains a file called `ECHIDNA`, which contains a list of files to be included in the final publication (i.e., not if a file is used by `respec` only like the `biblio.js` file). This list is used as an expansion of the `github.io` URL.

Your friendly staff contact sets up the initial version of ECHIDNA; adding additional files should be a matter of cut-and-paste. 

## Behind the scenes

The process is based on [Travis](https://en.wikipedia.org/wiki/Travis_CI), which is one of the powerful GitHub tools. By setting up a special file (called `.travis.yml`) in a repository, whenever that branch is updated, GitHub can start some specific process(es) to do various things on the repository content. This includes, for example, checking the validity of a software, checking (in our case) whether the submitter of a Pull Request is part of the WG (thereby his/her IPR status if fine), etc.

Echidna is one of those processes: it takes the relevant respec content, runs the aforementioned spec generator, pulls all the files together and creates a "proper" publication on the W3C Technical Report’s site. 

