---
name: Track 3rd-party dependency IP issues
about: If you want to track intellectual property issues
title: ''
labels: 
assignees: ''

---

**Description**  
We use the following 3rd-party content:  
<!-- Please describe why you need this content and reference it -->

**Link to our Eclipse Foundation Issue**  
You can found our 3rd-party IP GitLab Issue here:  
<!-- Please add your GitLab IP Issue Link -->

**Differences**  

| Information                 | Advisory                                | Example                    |
|-----------------------------|-----------------------------------------|----------------------------|
| ability to merge            | looks good, was already approved        | `approved, #3435`          |
| non rejected                | also fine                               | `approved, clearlydefined` |
| restricted but issue number | ok, but please this **must** be tracked | `restricted, #5922`        |
| :x: restricted              | you don can't use this library/content  | `restricted`               |

**Instructions**
- Automatic IP Team Review Requests via the [Dash Tool](https://github.com/eclipse/dash-licenses)
- IP issue for [Code Contributions](https://gitlab.eclipse.org/eclipsefdn/emo-team/iplab/-/issues/new), choose template "vet-project"
  - title pattern: project/<project id>/-/<name>/0.0
  - [more information](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-03)
  - [Example](https://gitlab.eclipse.org/eclipsefdn/emo-team/iplab/-/issues/8097)
- For PRs: use the link to the PR as source reference!  
- IP issue for [3rd party content](https://gitlab.eclipse.org/eclipsefdn/emo-team/iplab/-/issues/new)
  - choose template "vet-third party":

**Additional Info**  
- [Docs to IP Issues](https://eclipse-tractusx.github.io/docs/oss/issues#eclipse-gitlab-ip-issue-tracker)

- [Eclipse GitLab IP Issue Tracker](https://gitlab.eclipse.org/eclipsefdn/emo-team/iplab/-/issues/?search=automotive.tractusx&sort=created_date&state=opened&first_page_size=20)  
**IMPORTANT**: only a committer can create a valid IP Ticket!

- [Example GitLab Issue](https://gitlab.eclipse.org/eclipsefdn/emo-team/iplab/-/issues/5875)
- [TRG 7.04 Checking other content (fonts, images, ...)](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-04#checking-other-content-fonts-images-)
- [Dash tool information](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-04#checking-libraries-using-the-eclipse-dash-license-tool)
