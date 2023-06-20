
![W3C Logo](https://www.w3.org/Icons/w3c_home)

> **This Working Group has been closed on the 20th of June 2023. The maintenance of the WG documents have been taken over by the
 [Publishing Maintenance Working Group](https://www.w3.org/groups/wg/pm).**

# W3C Audiobooks (formerly Publishing) Working Group

This is the repository for the home page of the W3C Publishing Working Group:

https://www.w3.org/publishing/groups/publ-wg/

(That URL is redirected to the `w3c.github.io` view of this repository.)

## Specifications

GitHub repositories are linked from each specification.

## Contributing to the Publishing Working Group Repositories

Use the standard fork, branch, and pull request workflow to propose changes to the specification. Please make branch names informative—by including the issue or bug number for example.

Editorial changes that improve the readability of the spec or correct spelling or grammatical mistakes are welcome.

Please read [CONTRIBUTING.md](CONTRIBUTING.md), about licensing contributions.

## Tools

Generating weekly minutes is done via the
[scribejs](https://github.com/w3c/scribejs) script and some additional
configuration settings provided in this repo (see `.scribejs.json`).

To use this repository's scribejs setup first install the tools...

```bash
$ npm install
```

Then run the following (with date
information changed to match your scenario):

```bash
$ npm run scribejs -- -d 2018-07-09 -o Meetings/Minutes/2018/2018-07-09-pwg.md
```

This will request the IRC logs for the correct channel and convert them into
the Kramdown (a more feature rich form of Markdown) with settings to match this
repositories other documents.

If you need to make edits to the IRC log before generating the output (due to
incorrect scribenick or similar), you can download the W3C logs from URLs such
as `https://www.w3.org/2018/07/09-pwg-irc.txt`. Once downloaded, you can
reference that input document directly (rather than using the automagic
date-based retrieval).

For example:

```bash
$ curl https://www.w3.org/2018/07/09-pwg-irc.txt > 2018-07-09-pwg-irc.txt
$ npm run scribejs -- 2018-07-09-pwg-irc.txt -d 2018-07-09 -o Meetings/Minutes/2018/2018-07-09-pwg.md
```
Edit the .txt file and repeat the `npm run scribejs` line as necessary. Once
finished, you can commit the `.md` file and delete the `.txt` file (or keep it
for your records).
