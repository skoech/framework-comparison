# Static Site Generators: A comparison

For the [Tremor](https://www.tremor.rs/) [Web Content Redesign](https://github.com/tremor-rs/tremor-www-docs/issues/121) project, it is clear that we need a framework that unifies all the content forms (www, docs, rfcs and courseware) under a single consolidated theme and design. This issue, together with a [subsequent issue](https://github.com/tremor-rs/tremor-www-main/issues/27), form the basis of the criteria we shall be using to compare different frameworks and finally settle on one that best addresses Tremor's web concerns.

## Relevant Criteria

It is highly unlikely that one framework will be able to address every single criteria, or to have every nice little thing we want. That's life. But we will be considering the most important criteria, keeping our users, community and overall team in mind. Ergo, we shall give precedence to the right choice over the best choice.

1. Markdown- We would like to preserve Markdown for data entry due to its lower learning curve.
2. Focus on Documentation- Since most of Tremor's web content is docs.
3. Navigation- An easy-to-navigate theme/framework would be great for enhanced user experience. A framework that comes with breadcrumbs would be most ideal.
4. Versioned Documentation- Should be able to support multiple, separate versions of our documentation.
5. Syntax Highlighting- Should 
6. Visual Appeal- For better user experience, a beautiful theme would be best.
8. Wide community- Huge following demonstrated by number of forks and stars on GitHub. Ensures longevity of support for the framework.
9. Following/popularity with CNCF and Tremor team and Community.
10. Lower Learning Curve- To minimise barriers to entry; enable community contribute with ease.
11. Free and Open-source- Also ensures longevity of  support for the framework.
12. Search Bar- Should support search integration.
13. Dark/Light Mode Integration.

## Selected Candidates

After a lot of research, with the above consideration in mind, we settled on a few candidates to test out before settling on a framework for our project:

+ Hugo
+ Docusaurus
+ MkDocs
+ VuePress
+ Gatsby
+ Sphinx
+ Zola

You can find the tests (and instructions on how to run these frameworks) on a [different repository](). Now, let's take a look on each framework and its properties to find out if it satisfies our criteria.

1. ### Hugo

[Hugo](https://gohugo.io/) is a very popular open-source static site generator with a myriad of themes, suitable for building various types of websites, from documentation to landing pages, to e-commerce, etc. We tested the [Ananke](https://themes.gohugo.io/themes/gohugo-theme-ananke/) and [Docsy](https://themes.gohugo.io/themes/docsy/) themes for their visual appeal and focus on documentation respectively.

Some relevant properties of Hugo:

+ Written in [Go](https://golang.org/) (Golang).
+ Multiple themes for various needs.
+ Supports Markdown.
+ Suitable for documentation (Docsy theme).
+ Comes with really fast syntax highlighting from [Chroma](https://github.com/alecthomas/chroma).
+ Multilingual (i18n).
+ Blazingly fast.
+ [Thriving community](https://github.com/gohugoio/hugo)- 53K stars, 6K forks. Very active forum, making it easy to get help.
+ Free & open-source.
+ Additional: Used by the [CNCF](https://www.cncf.io/). Hugo enjoys a really good following by the CNCF, which is Tremor's home, and Golang programmers.

A few negative aspects:

* Steep learning curve.
* Doesn't have plugin support- adding highly custom functionality is not possible.
* Enabling versioning for docs is quite difficult.

2. ### Docusaurus

[Docusaurus](https://docusaurus.io/) is a tool that facilitates easy building, deploying, and maintaining open-source project websites. It is built with React, and has gained a lot of popularity since its release only in 2017. This popularity can be largely attributed to its endorsement by Facebook (Docusaurus has been used by a large number of the Facebook open-source projects- and by over 100 external projects.). It stood out for us greatly, owing to its many attractive features that are line with our project's objectives:

+ Focus on documentation- Docusaurus makes it extremely easy to maintain open-source documentation websites owing to its efforts to "put (users') focus on writing good documentation instead of worrying about the infrastructure of a website." 
+ Sensitive to open-source project needs- Docusaurus provides features that many open-source websites need e.g. blog support, search and versioning.
+ Supports Markdown.
+ Supports documentation versioning- enables you to keep documentation in sync with project releases, and support users on all versions of your project.
+ Enables syntax highlighting that is customable- Code blocks within documentation are super-powered; by using the matching language meta string for your code blocks, you allow Docusaurus to pick up syntax highlighting automatically, powered by [Prism React Renderer](https://github.com/FormidableLabs/prism-react-renderer).
+ Visual appeal- Beautiful theme.
+ Easy navigation.
+ Blog support.
+ Supports a search integration using [Algolia documentation search](https://www.algolia.com/).
+ Free & open-source.
+ Enables translation to oer 70 languages using [Crowdin](https://crowdin.com/)- Localization comes pre-configured.
+ Comes with Light Mode/Dark Mode.
+ Plugin support.
+ [Large community](https://github.com/facebook/docusaurus)- 25.2K stars, 2K forks.
+ Low learning curve.

| Criteria            | Hugo        | Docusaurus | MkDocs| VuePress | Gatsby | Zola | Sphinx |
| :---                |    :----:   |          ---: |
| Markdown            |             |          |
| Syntax highlighting |             | 
| Versioning          |             |
