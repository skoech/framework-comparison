# Static Site Generators: A comparison

For the [Tremor](https://www.tremor.rs/) [Web Content Redesign](https://github.com/tremor-rs/tremor-www-docs/issues/121) project, it is clear that we need a framework that unifies all the content forms (www, docs, rfcs and courseware) under a single consolidated theme and design. This issue, together with a [subsequent issue](https://github.com/tremor-rs/tremor-www-main/issues/27), form the basis of the criteria we shall be using to compare different frameworks and finally settle on one what best addresses Tremor's web concerns.

## Relevant Criteria

It is highly unlikely that one framework will be able to address every single criteria, or to have every nice little thing we want. That's life. But we will be considering the most important criteria, keeping our users, community and overall team in mind. Ergo, we shall give precedence to the right choice over the best choice.

1. Markdown- We would like to preserve [Markdown](https://www.markdownguide.org/) for data entry due to its lower learning curve.
2. Focus on Documentation- Since most of Tremor's web content is docs, we would prefer a framework that does documentation well.
3. Navigation- An easy-to-navigate theme/framework would be great for enhanced user experience. A framework that comes with breadcrumbs would be most ideal.
4. Versioned Documentation- Should be able to support multiple, separate versions of our documentation.
5. Syntax Highlighting- Should support code block and even individual line highlighting.
6. Visual Appeal- For better user experience, a beautiful theme would be best.
7. Wide community- Huge following demonstrated by number of forks and stars on GitHub. Ensures longevity of support for the framework.
8. Following/popularity with the CNCF as well as the Tremor team and Community.
9. Lower Learning Curve- To minimise barriers to entry; enable community contribute with ease.
10. Free and Open-source- Also ensures longevity of  support for the framework.
11. Search Bar- Should support search integration.
12. Dark/Light Mode Integration.

## Selected Candidates

After a lot of research, with the above considerations in mind, we settled on a few candidates to test out before choosing a framework for our project:

+ Hugo
+ Docusaurus
+ MkDocs
+ VuePress
+ Gatsby
+ Sphinx
+ Zola

You can find the tests (and instructions on how to run these frameworks) on a [different repository](). Now, let's take a look at each framework and its properties to find out if it satisfies our criteria.

1. ### Hugo

[Hugo](https://gohugo.io/) is a very popular open-source static site generator with a myriad of themes, suitable for building various types of websites, from documentation to landing pages, to e-commerce, etc. We tested the [Ananke](https://themes.gohugo.io/themes/gohugo-theme-ananke/) and [Docsy](https://themes.gohugo.io/themes/docsy/) themes for their visual appeal and focus on documentation respectively.

Some relevant properties of Hugo:

+ Written in [Go](https://golang.org/) (Golang).
+ Multiple themes for various needs.
+ Supports Markdown.
+ Suitable for documentation (Docsy theme).
+ Comes with really fast syntax highlighting from [Chroma](https://github.com/alecthomas/chroma).
+ Multilingual ([i18n](https://en.wikipedia.org/wiki/Internationalization_and_localization))- Hugo supports the creation of websites with multiple languages side by side. Uses [go-i18n](https://github.com/nicksnyder/go-i18n) to support string translations.
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

+ Focus on documentation- Docusaurus makes it extremely easy to maintain open-source documentation websites, owing to its efforts to "put (users') focus on writing good documentation instead of worrying about the infrastructure of a website." 
+ Sensitive to open-source project needs- Docusaurus provides features that many open-source websites need e.g. blog support, search and versioning.
+ Supports Markdown.
+ Supports documentation versioning- enables you to keep documentation in sync with project releases, and support users on all versions of your project.
+ Enables syntax highlighting that is customisable- Code blocks within documentation are super-powered; by using the matching language meta string for your code blocks, you allow Docusaurus to pick up syntax highlighting automatically, powered by [Prism React Renderer](https://github.com/FormidableLabs/prism-react-renderer).
+ Visual appeal- Beautiful theme.
+ Easy navigation.
+ Blog support.
+ Supports a search integration using [Algolia documentation search](https://www.algolia.com/).
+ Free & open-source.
+ Enables translation to over 70 languages using [Crowdin](https://crowdin.com/)- Localisation comes pre-configured.
+ Comes with Light Mode/Dark Mode.
+ Plugin support.
+ [Large community](https://github.com/facebook/docusaurus)- 25.2K stars, 2K forks.
+ Low learning curve.

A few negative aspects:

* It's built with React- hard to compile with Go.
* Not endorsed by the CNCF- we will miss out on their support.

3. ### MkDocs

[MkDocs](https://www.mkdocs.org/) is a fast and simple site generator, also geared towards building project documentation. It's written in Python, and is what we currently use at Tremor. However, it lacks some of our desired features, hence the need for this redesign and/or migration. Its features:

+ Supports Markdown- documentation source files are written in Markdown, and configured with a single YAML configuration file.
+ Variety of themes- MkDocs includes two built-in themes: [mkdocs](https://www.mkdocs.org/user-guide/choosing-your-theme/#mkdocs) and [readthedocs](https://www.mkdocs.org/user-guide/choosing-your-theme/#readthedocs). Also available are many [third party themes](https://www.mkdocs.org/user-guide/choosing-your-theme/#third-party-themes) to choose from.
+ Low learning curve- It’s quite easy to configure and deploy.
+ Easy customisation- lets you modify your site to look however you want by customising your theme, installing plugins or even modifying Markdown's behaviour with [Markdown extensions](https://www.mkdocs.org/user-guide/configuration/#markdown_extensions).
+ [Plugin](https://www.mkdocs.org/user-guide/configuration/#plugins) support.
+ [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) is a beautiful theme.
+ [Average community following](https://github.com/mkdocs/mkdocs)- 12.5K stars, 1.8 forks on GitHub.
+ Free & open-source.

A few negative aspects we have encountered: 

* Documentation versioning isn't built-in- requires `mkdocs versioning` plugin.
* No syntax highligting.
* Current theme (mkdocs) isn't very visually appealling. 

4. ### VuePress

[VuePress](https://vuepress.vuejs.org/) is a minimalistic static site generator powered by Vue, with a [default theme](https://vuepress.vuejs.org/theme/default-theme-config.html#homepage) optimised for writing technical documentation. It was created to support the documentation needs of Vue’s own sub projects. VuePress is quite similar to Docusaurus given its heavy focus on content-centric websites and tailored documentation features out of the box, except that  VuePress is powered by Vue, unlike its counterpart which is powered by React. Features:

+ Built-in [Markdown extensions](https://vuepress.vuejs.org/guide/markdown.html#header-anchors).
+ Documentation versioning support.
+ Syntax highlighting- in code blocks as well as line highlighting.
+ Line numbers and code snippet import- You can enable line numbers for each code block, and also import code snippets from existing files.

Input:

``` js{4}
export default {
  data () {
    return {
      msg: 'Highlighted!'
    }
  }
}
```

Output: 

![Line Numbers](file:///home/shaysenberg/Desktop/highlight.png)

In addition to a single line, you can also specify multiple single lines, ranges, or both.

+ Vue in Markdown- you can use Vue-style interpolation in text, as well as Vue components.
+ Vue-powered custom theme system- default theme and blog theme.
+ Built-in search- you can disable the built-in search box with `themeConfig.search: false`, and customise how many suggestions will be shown with `themeConfig.searchMaxSuggestions`. Moreover, the `themeConfig.algolia` option allows you to use [Algolia DocSearch](https://docsearch.algolia.com/) (opens new window) to replace the simple built-in search.
+ Plugin support- Powerful Plugin API, Blog Plugin, Search Plugin, PWA Plugin, Google Analytics Plugin.
+ Multi-language support (internationalisation)- the default theme has built-in i18n support.
+ Free & open-source.
+ [Relatively wide community](https://github.com/vuejs/vuepress)- 19.2K stars, 4.1K forks on Github.

Negative aspects:

* Heavily Vue-powered, which might present a barrier to entry for contributors, and not very suitable for community members who are not well versed with Vue.
* Requires a lot of customisation.

You can find set-up and installation instructions on this [test site repository](https://github.com/skoech/vuepress-test-website).

5. ### Gatsby

[Gatsby](https://www.gatsbyjs.com/) is a dynamic site generator that provides development teams an open-source frontend framework for creating dynamic, optimized websites and a cloud platform. for delivering them on a blazing fast edge network. It's a React-based framework that enables building of fast, secure, performant, scalable and accessible websites of different kinds (from marketing sites, to eCommerce stores, to documentation), which are then hosted on [Gatsby Cloud](https://www.gatsbyjs.com/products/cloud/).

+ Supports versioned documentation.
+ Supports syntax highlighting.
+ Rich ecosystem of [plugins](https://www.gatsbyjs.com/plugins), [themes](https://www.gatsbyjs.com/docs/themes/) and [starters](https://www.gatsbyjs.com/starters/?)- "Go from idea to production in less time with starters, themes, and over 2500 plugins that can help connect nearly any CMS, eCommerce platform, analytics tool, or other web service and get your website up and running in just minutes."
+ Blog support- you can leverage themes and starters to build blogs in your site, for example the [Gatsby Blog Starter](https://www.gatsbyjs.com/starters/gatsbyjs/gatsby-starter-blog/).
+ Free & open-source.
+ Can unify multiple content forms and data from different sources while maintaining consistency- Gatsby has an innovative data layer built on GraphQL that allows developers to easily combine data from different sources and render them alongside each other. You can add content to your site, from a Shopify store, a WordPress blog, and some JSON from a payment processor all in a consistent manner.
+ Unparalleled speed and responsiveness- combines static-site generation and intelligent page rendering to selectively preload only the content that matters - give you a blazing fast website that feels incredibly smooth.
+ [Docz](https://github.com/doczjs/docz) theme for building documentation is beautiful and easily configurable and customisable, and fully plugable.
+ [Huge community](https://www.gatsbyjs.com/starters/gatsbyjs/gatsby-starter-blog/)- 50.9K stars, 9.8 forks.
+ Screenshots enabled in documentation.

Some observed negative aspects:

* High learning curve- Gatsby is packed with a myriad of features, capabilities and plugins, which, naturally, comes at a cost of a higher learning curve. It also leverages GraphQL (not necessarily, though), whichmay present a barrier to entry for contributors not versed with the tool.
* Not focused on documentation- suitable for building different types of dynamic wesites, from e-commerce to marketing, to documentation sites).

6. ### Sphinx

[Sphinx](https://www.sphinx-doc.org/en/master/) is a powerful Python documentation generator with excellent facilities for the documentation of software projects in a range of languages. It has many great features for writing technical documentation. Sphinx was originally created for [the Python documentation](https://docs.python.org/3/). Sphinx uses [reStructuredText](https://docutils.sourceforge.io/rst.html) as its markup language, and many of its strengths come from the power and straightforwardness of reStructuredText and its parsing and translating suite, [Docutils](https://docutils.sourceforge.io/). 
Relevant features to highlight:

+ Supports Markdown- you can use reStructuredText (default markup format) or Markdown to write documentation.
+ Syntax highlighted code samples- automatic highlighting using the [Pygments](https://pygments.org/) highlighter.
+ Supports versioned documentation- https://holzhaus.github.io/sphinx-multiversion/master/index.html.
+ A vibrant ecosystem of first and third-party [extensions](https://www.sphinx-doc.org/en/master/usage/extensions/index.html).
+ Hierarchical structure- easy definition of a document tree, with automatic links to siblings, parents and children (enables the activation of breadcrumbs).
+ Extensive cross-references: semantic markup and automatic links for functions, classes, citations, glossary terms and similar pieces of information.
+ Focus on documentation- Sphinx focuses on documentation, in particular handwritten documentation However, Sphinx can also be used to generate blogs, homepages and even books. Much of Sphinx’s power comes from the richness of its default plain-text markup format, reStructuredText, along with its [significant extensibility capabilities](https://www.sphinx-doc.org/en/master/development/index.html).
+ Search bar.
+ Blog support.
+ Free & open-source- in fact, there are dozens of extensions contributed by users, most of them installable from PyPI.
+ Multiple themes- some of which are beautiful e.g. the [Read the Docs](https://sphinx-themes.org/sample-sites/sphinx-rtd-theme/), [Material](https://sphinx-themes.org/sample-sites/sphinx-material/) and [PDJ](https://sphinx-themes.org/sample-sites/sphinx-pdj-theme/) themes.

A number of negative aspects that stood out:

* Steep learning curve- using reStructuredText, which is not as simple as Markdown to master, as its default markup language would present a barrier to entry for contributors of an open-source project such as Tremor.
* Default theme design not very visually appealling.
* Not very popular: quite a [small community](https://github.com/sphinx-doc/sphinx)- 4K stars, 1.5K forks on GitHub.

7. ### Zola

[Zola](https://www.getzola.org/) is a static site generator (SSG), similar to Hugo. It is written in [Rust](https://www.rust-lang.org/), and its content written in [CommonMark](https://commonmark.org/), a strongly defined, highly compatible specification of Markdown.

+ Written in Rust- huge advantage for Tremor which is also written in Rust; support from the Tremor team and community will be easy- low barrier to entry.
+ No dependencies- Zola comes as a single executable with Sass compilation, syntax highlighting, table of contents and many other features that traditionally require setting up a dev environment or adding some JavaScript libraries to your site. 
+ Augmented Markdown- Zola comes with [shortcodes](https://www.getzola.org/documentation/content/shortcodes/) and [internal links](https://www.getzola.org/documentation/content/linking/) to make it easier to write your content. 
+ Comes with breadcrumbs- enables easy navigation.
+ Syntax highligted code samples.
+ Blog support.
+ Search bar.
+ Ease of use (lower learning curve)- From the CLI to the template engine, everything is designed to be intuitive.
+ Flexible- Zola gets out of your way so you can focus on your content, be it a blog, a knowledge base, a landing page or a combination of them. 
+ Variety of themes- enable building blogs, landing pages, documentation sites, etc.

Negative aspects:

* [Very small community](https://github.com/getzola/zola) following- 7.2K stars, 530 forks on GitHub- support for it in the long run is not guaranteed; smaller forums.
* The default design isn't particularly visually appealing, athough there are beautiful themes to choose from.

## Final Tally


| Criteria                | Hugo        | Docusaurus  | MkDocs  | VuePress | Gatsby | Sphinx |  Zola  |
| :-------:               |:----------: | :------:    |:-------:| :------: |:-----: | :------|:-------|
| Markdown                |  1          |  1          |1        | 1        |1       | 1/2    | 1      |
| Syntax Highlighting     |   1         |   1         | 0       |    1     | 1      | 1      | 1      |
| Versioning              |   0         |    1        |  0      |     1    |  1     | 1      | 0      |
| Focus on Documentation  |  1/2        |     1       |   1     |      1   |   0    | 1      | 1      |        
| Breadcrumbs             |     0       |      0      |    0    |       0  |  0     | 0      | 1      |
| Visual Appeal           |      1      |       1     |   1/2   |     1    |   1    | 1/2    | 1/2    |
| Dark/Light Mode         |       0     |        1    |    0    |      0   |    0   | 0      | 0      |
| Search Bar              |        1    |         1   |     1   |       1  |     1  | 1      | 1      |  
| Wide Community          |         1   |          1  |    1/2  |      1/2 | 1      | 0      | 0      |
| Free & Open-source      |          1  |           1 |   1     |    1     |  1     | 1      | 1      |
| Low Learning Curve      |           0 |            1|    0    |     0    |   0    | 0      | 1      |
| Popularity with CNCF    |            1|            0|     0   |      0   |    0   |0       | 0      |
| TOTAL                   |   **7.5**   |    **10**   |  **5**  |  **7.5** |  **7** | **6**  | **7.5**|

The defence rests. 

## Verdict

After carefully analysing the frameworks we considered, weighing their pros and cons with respect to our project's objectives, we have a clear winner: DOCUSAURUS! Yay! 

We shall, therefore, be using Docusaurus to implement the web redesign project for Tremor.
