# Daktary, a new CMS based on open distributed databases

## Summary

In this paper we present Daktary, a new technology to facilitate content transfer and remix by acting as a CMS that can retrieve content from open distributed databases and present it just similarly to traditional CMS do with closed centralized database. Just as wiki allowed anyone to contribute and revolutionized collaboration 20 years ago, we believe having open distributed databases can revolutionize collaboration and content remix by breaking up silos effect between various collaboration platform.

## The rise of open distributed databases

Today most web publishing platforms use databases to store content and serve it dynamically to users.

From the beginning of the internet, because of technical requirements and culture of ownership, databases have been mostly centralized and closed/private.

Centralized means the database and its content are located on one particular server or a particular network under the control of one single agent/entity that has power over it.

Closed/private means the content is locked and only accessible/usable under the control of the agent/entity owning it.

This architecture makes sense when the content is private (such as passwords or personal information) or when the entity wants to keep control of the way the content is used or shared (such as content that has to be kept scarce to be sold commercially).

However having private/closed centralized databases makes little sense when content producers do want to favor content copy and reuse.

## Social innovation wants to be remixed

If "information wants to be free" as technology activists invoked against limiting access to information, we believe social innovation wants to be remixed. 

Indeed, more and more social innovation practices, tutorial and other educational materials are shared by positive change agents who documents their best social, sustainable practices and share them under free licenses to make shareable.

(see What is Open Social Innovation and why we need free/libre recipes: http://www.lilianricaud.com/web-strategy/open-research/open-social-innovation-open-sourcing-social-innovation-to-promote-sharing-sustainable-social-practices/)

Most often this is done using wikis or other similar softwares, yet because each of them use a centralized closed database, this creates a silos effect preventing easy exchange of content between the various platforms.

Effectively there's no direct interoperability and this leads to duplication of efforts, duplication of content, …

## Towards open distributed databases

To prevents this and facilitate large scale content reuse and remix we propose the concept of open distributed database. We define an open distributed database as this:
* open: the content the database is open for everyone to read without any conditions or restriction. There is no obligation to use a particular API to access the content. Raw database content is just freely accessible.
* distributed: the content is not under control of a single person or entity, this means various parts of the data and the database are under control of various persons/entities and not and single one. this implies the use of some sort of standard for easy content interoperability.
* use of free license: for both content and code to be reusable without any legal hassle it implies they are shared under free licenses. This allow any kind of modification and reuse both for the code and the content.

Note that what we propose is different from the BitCoin Blockchain, that can also be seen as kind of open distributed database.  The Blockchain, although it is distributed over all the computers belonging to the network, effectively works as a giant centralized database owned collectively by the network. Writing in this database is done by the network using a consensus based mechanism.

What we envision in our definition of open distributed database is more like a network of interoperable open databases that co-exist in parallel and can constantly exchange content and feed from each other.

## Daktary technology as a proof of concept

As a proof of concept we chose to use github as a tool to demonstrate what open distributed database could look like. Github is a tool to manage version control in software development but it is more and more used by non-developers to store and collaborate on content, taking advantage of github robust versioning system.

We use github to store content in the same way a traditional database stores content, ie webpage content is stored to be able to be retrieved and displayed in various location and formats.

In order to separate the content from the formatting we chose to use markdown. Although not an established standard, Markdown is widely used, simple to understand for non-developers, yet allow developers to use it to format the text content.

To "read" the content and display it on the web, we developed a special CMS that can use markdown content stored in github repositories and display it in the same way a traditional CMS retrieved content from a closed centralized database and display dynamically as a web page.

## Presentation of Daktary technology and features

This technology called Daktary is still a prototype. Yet, because it has been developed thoughtfully using agile methodologies, it already has several great working functionality's:
* at its core daktary is a reader that can interpret markdown content stored in github and displayed in a simple elegant interface.
* any markdown content stored on github can be read via daktary using smart URLs
* integrated with the existing prose.io content editor for github, daktary allows direct content edition for content owners while users who don't own content can still make edit proposals and submit them to the content owner (via pull request). Content owners can then decide to include the proposed edit or parts of it.
* to redistribute content in various forms and formats, daktary offers and embed code that can inject the github stored data in any webpage. Unlike an iframe where the content called remains external to the webpage, daktary injects the markdown content directly in the webpage using the website default stylesheet to format the content and diplay it using the website graphic identity.

Working in a API way of thinking, Daktary calls up external services when it's available instead of redeveloping yet another redundant functionality. For example Daktary use prose.io as wysiwyg content editor for github and uses github pages has a web host for dakatary.com

In this way both the code of the application are open and accessible to anyone on github.

Daktary was initially developed roughly using Meteor to build a proof of concept. Since then, the code was redeveloped cleanly in javascript ES2015 and documented to allow other open source developers to contribute.

To facilitate development and accept contributions from other developers, several mechanisms have been put into place using state of the art best practices:
* automated acceptance tests
* documentation of code
* ...

More information on Daktary's technical aspects can be found here: http://dev.daktary.com/#daktary-team/

## MultiBAO: a working prototype using Daktary technology

Daktary technology was initially used to power MultiBAO, a toolbox that seek to aggregate participatory methods from various contributors and where previously hosted on different siloed-CMS.

MultiBAO currently aggregates over hundred of participatory methods from 10 contributing persons or networks. Although the graphic design is frugal it already attracted tens of contributors and hundreds of visitors.

http://www.multibao.org

## OpenPatternPedia: a proof of concept for pattern sharing/improvement

The Daktary technology was used to buld a proof oc oncept for pattern sharing. although on the outside it might look and feel like a wiki, the technology behind it allow contributors
- to read patterns and explore whole language
- to submit changes to the author
- to clone and customize their own version of the pattern. Thanks to git/github powerful versionning technology, patterns can be compared and shared back between various branches.

See OpenPatternPedia: https://lilianricaud.github.io/PatternPedia/

An example of pattern from Christopher Alexander that can easily be cloned and customized:
https://lilianricaud.github.io/PatternPedia/#lilianricaud/Christopher_Alexander_Pattern_Language/blob/master/A_Pattern_Language/147_Communal_eating.md

## Perspectives

We imagine Daktary could help power hundreds of specialized Multibao-like resources for sustainable agriculture, open source hardware documentation, civil code tracking, … all retaining their individuality and identity while remaining interoperable without silo-effect.

It may seem contradictory to talk about open distributed database while using github, which is itself a centralized database owned by non-open source commercial entity.

Yet this allowed us to quickly deploy a working app. Github offers several advantages:
- it has large community of early adopters and a lot non-code content is already available there
- it has a great versioning system, pull requests and all the git functionalities hosted within a nice user friendly graphic interface
- it allows each contributor to remain the owner of his own content, therefore although the content is all hosted on github it is distributed between various owners. 
- it natively reads markdown
- there are several useful services built around it that we can take advantage of (prose.io, github pages).

As of now, Daktary can only use Github as an open distributed database, but in the future we envision Daktary could read content from any Git-like repositories (GitLab, Bitbucket, …)

Furthermore Daktary so far only display web pages, but we imagine it could be coupled to technology like reveal.js to create powerpoint and prezi like presentations from markdown content.

As of now content producers still have to make the effort of converting their content to markdown and publish it onto github but we envision to develop tools that allow them to automatically convert to markdown content from most popular CMS such as MediaWiki or WordPress and push it to github. Making content pushing to github painless is seen as essential to convince more content producers to join and make their content available.

Another option could be to develop automated scraping tools that could do the same for content available under free licenses. The previous option is more desirable since it implies active involvement of the content creator in the process.

Having possibilities to copy and remix content so easily might lead to a lot of duplicate on the web, so it's important to think about the impact it might have for content creators in term of search engine optimization, but also more widely on signal/noise ratio for end users.

## A glimpse of the future 

The use of open databases allow more than one app to use content. If Daktary is the first reader, it is possible that other custom Daktary-like CMS will appear to provide customized functions, interfaces, just like the web content can be read by various browsers.

We plan to remain focus on developing only the features we deem essential but looking in the longer term, we imagine that others could also apply the same principles to develop collaborations tools for multimedia content. 

Imagine what a youtube with github functionalities could look like. It would make remixing of video content extremely easy and efficient.

On the future web, there might be a "remix me" function embedded in every piece of content that would allow the users to immediately be able to work on the content itself and start personalize it just like developers do today on code hosted on github.

In short we believe the use of open-distributed database and Dakatary-like CMS tools could unleash an unprecedent wave of large scale collaboration and creativity.
