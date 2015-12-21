Using github.io pages, jekyll static site generation and liquid templates to build consistent
Netherlands eScience Center Project and software pages.
This architecture has been largely inspired by Software Carpentry workshop templates.

Ideas:
- Three layer, distributed architecture.
- One NLeSC page that keeps track of all the projects run by NLeSC.
URL should be `nlesc.github.io`.
- One page for each project. This should be separate organisation.
If the organisation name is `moriarty-corp`, the page URL will be `moriarty-corp.github.io`.
Page should be in repository `github.com/moriarty-corp/moriarty-corp.github.io`.
- One page per software repository. It does not matter what is the github organisation or user that the repository is located in.
Page code should be located in `gh-pages` branch of software repository. If github user is `minion` and software is `evil-contraption` the
URL of the page will be `minion.github.io/evil-contraption`.
- Project page should have and index of its software tools. This list should be extended via pull requests from tools developer.
- Organisations should be added to NLeSc page via pull request from project *administrator*.
- It should be possible to validate software page, checking if the minimum information is provided.
Some of the things that can be checked are:
    * is repository is public?
    * is repository versioned with semver?
    * does repostiory contain LICENSE file?
    * does repository contain REDME.md?
    * does repository contain editorconfig file?
    * does software have DOI?
- Project and software pages should be created from templates that can be imported with github import tool.
- There should be validation of pages and maybe some github hooks.
- Everything should be automated as much as possible.
- Checks could be done during build with Travis continuous integration.
  * when commit in master branch update gh-pages, validate and rebuild
