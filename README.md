# Awesome-On-Premises-Git-Repository-Hosting

# Top On-Premises Git Repository Hosting Ecosystem

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

### Lightweight Git Forges (Gitea, Forgejo)

- **[Gitea](https://github.com/go-gitea/gitea)**  
  The **leading lightweight open-source Git forge** (MIT). Single Go binary with a built-in web UI, issue tracking, pull requests, wikis, package registry, and **Gitea Actions** (GitHub Actions-compatible CI). **Idles at ~100MB RAM**—the lightest full-featured option. **Critical security note**: **Gitea 28.3.0** (October 2026) fixed **nine CVEs**, including a critical flaw where Actions task tokens could list every private repository on the instance, and a public-only token with `write:organization` could create runner registration tokens that received jobs and secrets from private repositories . **Best for teams wanting a lightweight, self-contained Git server** with minimal operational overhead—but security patches must be applied promptly given the CVE history.

- **[Forgejo](https://github.com/forgejo/forgejo)**  
  The **community-governed fork of Gitea** under Codeberg e.V. (GPLv3). **Forgejo v14** (January 2026) replaced the Monaco file editor with **CodeMirror** (lighter, better mobile/accessibility), added **Actions concurrency groups** and dynamic matrices, pull request trust management, and a CLI tool to clean up redundant commit status records (97% of records on code.forgejo.org were redundant) . **Forgejo v17.0** adds repository funding links and Bitbucket Data Center migration support . **Best for organizations wanting Gitea's lightweight footprint with community governance** and no single-vendor control—the CodeMirror swap and cleanup tooling show active investment.

### Enterprise-Grade Git Platforms (GitLab, RhodeCode)

- **[GitLab (Self-Managed Free)](https://github.com/gitlabhq/gitlabhq)**  
  The open-source core of GitLab (MIT for most code). **Free tier** provides source code management, merge requests, basic CI/CD, and issue tracking. **Heavier footprint** than Gitea/Forgejo (~8GB RAM recommended for full stack including PostgreSQL, Redis, Gitaly, Sidekiq). **Best for organizations wanting an integrated DevOps platform** with a clear upgrade path to Premium/Ultimate—but resource requirements are significantly higher than lightweight forges.

- **[RhodeCode Enterprise](https://github.com/rhodecode/rhodecode-enterprise-ce)**  
  Enterprise-grade **Git and Mercurial hosting platform** with code review, pull requests, and full-text search (Elasticsearch). **v5.15.0** (October 2026) adds **pull request dependencies** (blocking merges until dependencies resolve), draft PRs, collapsible file-tree sidebar, and security fixes for draft comment visibility . **Requires Python 3.11+** and pygit2 1.20.1/libgit2 1.9.7 . **Best for organizations needing Mercurial support alongside Git** or wanting an enterprise-grade commercial platform with support—but it is a heavier deployment than lightweight forges.

### Code Review Specialists (Gerrit)

- **[Gerrit Code Review](https://github.com/GerritCodeReview/gerrit)**  
  The **standard for rigorous, review-first Git workflows** (Apache 2.0). Used by the Android Open Source Project and Chromium. Enforces code review before merge, with fine-grained permissions, change-based review, and integration with CI. **Best for projects requiring formal code review gates** and large-scale contribution workflows—but the workflow is opinionated and can feel heavy for small teams.

### Additional Strong Open-Source Options

- **Gogs** — The original lightweight Go git server from which Gitea forked; **slower development** than Gitea/Forgejo. **Best for minimal deployments** where Gitea/Forgejo features are not needed—but verify security patch cadence.
- **Gitolite** — Git hosting **without a web UI**; pure SSH-based access control and repository management. **Best for teams wanting bare Git with fine-grained permissions** and no web overhead—but no issue tracking, pull requests, or UI.
- **Kallithea** — Open-source Git/Mercurial hosting with web UI; **verify maintenance status** as recent activity appears limited based on available search results .
- **Apache Allura** — Open-source forge with Git, SVN, Mercurial, tickets, wikis, and discussion forums; **Apache-governed** but development pace should be verified.

**Frameworks for building custom systems**: For a **lightweight, self-contained Git server with minimal RAM**, Gitea (applying security patches promptly) or Forgejo (community-governed) . For an **integrated DevOps platform with a clear upgrade path**, GitLab Self-Managed Free . For **Mercurial support alongside Git**, RhodeCode Enterprise . For **formal code review workflows**, Gerrit . For **bare Git with SSH-only access**, Gitolite . **Avoid Kallithea and Allura** unless you verify active maintenance—the search results suggest limited recent activity. **Bitbucket Data Center 10.2 LTS** is the commercial option for Atlassian-centric organizations (supported through March 2028) .

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
