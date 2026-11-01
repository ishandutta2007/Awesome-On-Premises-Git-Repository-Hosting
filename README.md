# Awesome-On-Premises-Git-Repository-Hosting

## Top On-Premises Git Repository Hosting Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Self-Managed Git Forges, Code Review & Source Control Infrastructure*  

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **On-Premises Git Repository Hosting**. These tools enable organizations to run their own Git servers—keeping source code, CI/CD pipelines, and collaboration data on infrastructure they control, preserving data residency, avoiding per-seat cloud pricing, and maintaining full control over security and customization.



**Examples** include Bitbucket Server, GitHub Enterprise Server, GitLab Enterprise Edition, Gitea, Gogs, Gitolite, Gerrit Code Review, RhodeCode, Apache Allura, and Kallithea (the category leaders).



**Open-source emphasis**: On-Premises Git Hosting is a domain where open-source tooling is **genuinely mature and production-proven**, but the landscape carries critical licensing and maintenance caveats. **Gitea** is the lightweight champion—a single Go binary with a built-in web UI, issue tracking, pull requests, and Actions, requiring minimal resources (~100MB RAM) . **Forgejo** is the community-governed fork of Gitea under Codeberg e.V., with v14 (January 2026) replacing Monaco with CodeMirror for the file editor, adding Actions concurrency groups, and improving accessibility . **GitLab** consolidated its CE/EE distributions into a single codebase in 2020—the free tier is now "Free" (open-source features only), with Premium adding enterprise workflow controls and Ultimate adding the full security suite (SAST, DAST, compliance frameworks) . **RhodeCode** provides an enterprise-grade alternative with v5.15.0 (October 2026) adding pull request dependencies, draft PRs, and a collapsible file-tree sidebar . **Gerrit** remains the standard for rigorous code review workflows. The critical caveat: **Kallithea and Apache Allura appear to have limited recent activity**—verify maintenance status before adoption. **Gogs** is the original lightweight Go git server from which Gitea forked, but it has slower development.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Bitbucket Server (Data Center)](https://www.atlassian.com/software/bitbucket/enterprise)**  

  Atlassian's self-managed Git platform. **Bitbucket Data Center 10.2 is a Long Term Support release** (March 2026) with two-year support through March 2028 . Features: **merge queues** for keeping branches green during busy merge periods; responsive pull requests on mobile (480px+); OAuth 2.0 for app links; service accounts; Basic auth disabled by default for new instances; and instance health checks . **Note**: OpenSearch is no longer bundled—you provide your own search infrastructure . **Best for Atlassian-centric organizations** already using Jira and Confluence—but it is a commercial enterprise product with significant licensing costs.



- **[GitHub Enterprise Server](https://github.com/enterprise)**  

  Self-hosted GitHub for organizations requiring on-premises source control; includes repositories, pull requests, Actions, and security features. **Best for organizations wanting GitHub's ecosystem** with data residency—but it is a commercial product with per-seat pricing.



- **[GitLab Enterprise Edition (Self-Managed)](https://about.gitlab.com/)**  

  GitLab's single distribution (CE and EE merged since v12.3) . **Free tier** includes open-source features (source code management, basic CI/CD); **Premium** adds merge approval rules, code owners, epics, roadmaps, and audit events; **Ultimate** adds SAST, DAST, dependency/container scanning, secret detection, compliance frameworks, and value stream analytics . **Pricing**: Ultimate list at **$99/user/year**; Duo Enterprise AI at **$39/user/month** . **Best for organizations wanting an integrated DevOps platform**—but Ultimate's security suite is the primary TCO justification, and self-managed carries infrastructure and upgrade overhead .



## Open-Source GitHub Projects

*Sorted by GitHub Star count in descending order.*

- **[Gitea](https://github.com/go-gitea/gitea)** [![GitHub stars](https://img.shields.io/github/stars/go-gitea/gitea?style=social&color=white)](https://github.com/go-gitea/gitea/stargazers)  
  The leading lightweight open-source Git forge (MIT). Single Go binary with a built-in web UI, issue tracking, pull requests, wikis, package registry, and Gitea Actions (GitHub Actions-compatible CI). Idles at ~100MB RAM—the lightest full-featured option with minimal operational overhead.

- **[Gogs](https://github.com/gogs/gogs)** [![GitHub stars](https://img.shields.io/github/stars/gogs/gogs?style=social&color=white)](https://github.com/gogs/gogs/stargazers)  
  A painless, self-hosted Git service written in Go (MIT). Extremely lightweight and cross-platform with minimal resource consumption, providing core repository management, issue tracking, and web interface.

- **[GitLab (Self-Managed Free)](https://github.com/gitlabhq/gitlabhq)** [![GitHub stars](https://img.shields.io/github/stars/gitlabhq/gitlabhq?style=social&color=white)](https://github.com/gitlabhq/gitlabhq/stargazers)  
  The open-source core of GitLab (MIT for community edition code). Provides comprehensive source code management, code reviews, merge requests, issue tracking, and integrated CI/CD pipelines in a complete DevOps lifecycle platform.

- **[OneDev](https://github.com/theonedev/onedev)** [![GitHub stars](https://img.shields.io/github/stars/theonedev/onedev?style=social&color=white)](https://github.com/theonedev/onedev/stargazers)  
  An all-in-one open-source DevOps platform and Git server (MIT). Features GUI-friendly CI/CD build pipelines with Kubernetes/Docker support, deep code intelligence (symbol search and outline navigation), pull requests, and custom issue boards.

- **[GitBucket](https://github.com/gitbucket/gitbucket)** [![GitHub stars](https://img.shields.io/github/stars/gitbucket/gitbucket?style=social&color=white)](https://github.com/gitbucket/gitbucket/stargazers)  
  A GitHub clone powered by Scala and JVM (Apache 2.0). Provides a highly compatible GitHub-like UI and API, repository viewer, issues, pull requests, wiki, and plugin architecture, easily distributable as a single runnable WAR/Java file.

- **[Gitolite](https://github.com/sitaramc/gitolite)** [![GitHub stars](https://img.shields.io/github/stars/sitaramc/gitolite?style=social&color=white)](https://github.com/sitaramc/gitolite/stargazers)  
  An extremely mature, lightweight access control layer on top of bare Git (GPL-2.0). Provides fine-grained access control down to branch and tag level over SSH without the overhead of a web server or database.

- **[Soft Serve](https://github.com/charmbracelet/soft-serve)** [![GitHub stars](https://img.shields.io/github/stars/charmbracelet/soft-serve?style=social&color=white)](https://github.com/charmbracelet/soft-serve/stargazers)  
  A mighty, self-hostable Git server designed for the command line (MIT). Built by Charmbracelet with SSH-based interactive TUI menus, access control via SSH keys, web UI/TUI browsing, and Git LFS support.

- **[GitList](https://github.com/klaussilveira/gitlist)** [![GitHub stars](https://img.shields.io/github/stars/klaussilveira/gitlist?style=social&color=white)](https://github.com/klaussilveira/gitlist/stargazers)  
  An elegant, modern Git repository viewer written in PHP (BSD-3-Clause). Allows browsing repositories, commit logs, file history, diffs, and trees with zero database requirements.

- **[CodeFever Community Edition](https://github.com/PGYER/codefever)** [![GitHub stars](https://img.shields.io/github/stars/PGYER/codefever?style=social&color=white)](https://github.com/PGYER/codefever/stargazers)  
  A complete open-source self-hosted Git service platform (MIT). Features high performance, code hosting, code review, branch protection, and single-command deployment with Docker.

- **[Gitblit](https://github.com/gitblit-org/gitblit)** [![GitHub stars](https://img.shields.io/github/stars/gitblit-org/gitblit?style=social&color=white)](https://github.com/gitblit-org/gitblit/stargazers)  
  An open-source, pure Java stack for managing, viewing, and serving Git repositories (Apache 2.0). Operates as a standalone server or WAR file with integrated user management, access control, tickets, and federation.

- **[Bonobo Git Server](https://github.com/jakubgarfield/Bonobo-Git-Server)** [![GitHub stars](https://img.shields.io/github/stars/jakubgarfield/Bonobo-Git-Server?style=social&color=white)](https://github.com/jakubgarfield/Bonobo-Git-Server/stargazers)  
  A dedicated self-hosted Git server for Windows environments (MIT). Built on ASP.NET MVC and IIS, offering web-based repository management, user/team permissions, and Active Directory integration.

- **[Gerrit Code Review](https://github.com/GerritCodeReview/gerrit)** [![GitHub stars](https://img.shields.io/github/stars/GerritCodeReview/gerrit?style=social&color=white)](https://github.com/GerritCodeReview/gerrit/stargazers)  
  The industry standard for rigorous, review-first Git workflows (Apache 2.0). Enforces formal change-based code review before merge with fine-grained ACL permissions and continuous integration verification.

- **[GitPrep](https://github.com/yuki-kimoto/gitprep)** [![GitHub stars](https://img.shields.io/github/stars/yuki-kimoto/gitprep?style=social&color=white)](https://github.com/yuki-kimoto/gitprep/stargazers)  
  A portable GitHub clone written in Perl (Artistic License 2.0). Features an easy zero-configuration setup, web interface, pull requests, issue tracking, and repository permissions without requiring separate database engines.

- **[klaus](https://github.com/jonashaag/klaus)** [![GitHub stars](https://img.shields.io/github/stars/jonashaag/klaus?style=social&color=white)](https://github.com/jonashaag/klaus/stargazers)  
  A zero-configuration, minimalist Git web viewer written in Python (Flask) under the ISC license. Offers syntax highlighting, commit history, blame views, and markdown rendering with simple WSGI/Docker deployment.

- **[Pagure](https://github.com/Pagure/pagure)** [![GitHub stars](https://img.shields.io/github/stars/Pagure/pagure?style=social&color=white)](https://github.com/Pagure/pagure/stargazers)  
  A lightweight, fully open-source Git-centric forge written in Python (GPLv2+), developed by the Fedora Community. Offers issue tracking, pull requests, docs, and git-backed metadata storage.

- **[Apache Allura](https://github.com/apache/allura)** [![GitHub stars](https://img.shields.io/github/stars/apache/allura?style=social&color=white)](https://github.com/apache/allura/stargazers)  
  An open-source software forge platform (Apache 2.0) managing Git repositories, SVN, Mercurial, issue tracking, markdown wikis, forums, and discussion spaces.

- **[RhodeCode Community Edition](https://github.com/rhodecode/rhodecode-enterprise-ce)** [![GitHub stars](https://img.shields.io/github/stars/rhodecode/rhodecode-enterprise-ce?style=social&color=white)](https://github.com/rhodecode/rhodecode-enterprise-ce/stargazers)  
  Enterprise-grade Git and Mercurial repository management platform. Features unified code review, pull request dependencies, and fine-grained repository access controls.

**Frameworks & Guidance**: For a **lightweight, self-contained Git server with minimal RAM**, Gitea or Gogs is the safe default. For an **all-in-one DevOps platform with built-in CI/CD**, OneDev or GitLab Self-Managed Free. For **pure command-line / TUI experience**, Soft Serve. For **bare Git with SSH-only access control**, Gitolite. For **formal code review workflows**, Gerrit Code Review.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- On-premises Git hosting platforms handling source code and credentials must comply with organizational security policies; **self-hosted solutions place full responsibility for security patches, backups, and uptime on the operator**. **Gitea 28.3.0 fixed nine CVEs** including a critical private-repository enumeration flaw—delayed patching leaves source code and secrets exposed .

- **GitLab's CE/EE naming is obsolete**—the single distribution uses Free/Premium/Ultimate tiers, and the Free tier includes only open-source features . **Bitbucket Data Center 10.2 is an LTS release** supported through March 2028, but it is a commercial product . **Kallithea and Apache Allura** show limited recent activity—verify maintenance before adoption.

- Verify license terms for commercial use; Gitea and Forgejo are open-source (check repositories), GitLab uses MIT for most code , RhodeCode Enterprise is commercial , and Gerrit uses Apache 2.0 .



---



**Made for platform engineers, DevOps teams, and organizations choosing their self-hosted source control stack.**  

Let's make on-premises Git hosting more open, but with clear eyes about the CVE patching burden and the maintenance gaps that separate viable options from abandoned ones.
