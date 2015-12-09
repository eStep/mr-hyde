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
- One page per software repository. It does not matter what is the github organisation or user that the repository is loated in.
Page code should be located in gh-pages of software repository. If github is `minion` and software is `evil-contraption` the
URL of the page will be `minion.github.io/evil-contraption`.
