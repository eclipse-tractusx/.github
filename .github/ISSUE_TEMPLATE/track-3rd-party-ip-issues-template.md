---
name: Track 3rd-party dependency IP issues
about: If you want to track intellectual property issues
---

## Content Usage and Explaination
We use the following 3rd-party content:
<!-- Please describe why you need this content and reference it -->

## IP Issue Link to Track
You can found our 3rd-party IP GitLab Issue here:
<!-- Please add your GitLab IP Issue Link -->

<!-- Info: The following parts are for knowledge sharing, please remove not needed sections -->
### Instructions
- Automatic [Dash Licence Check][sig-infra-licence-check] via GitHub Action from `sig-infra` repository
- Automatic IP Team Review Requests via the [Dash Tool][DASH Tool]
- Manual IP Team Review Requests via [IP Issue Creation][ip-issue-creation]
- [Docs to IP Issues][docs-ip-issues]

**Additional Info**
- [Example GitLab Issue][gitlab-example-ip-issue]
- [TRG 7.03][TRG-7-03]
- [TRG 7.04][TRG-7-04]
- only a committer can create a valid IP Ticket!

| Example                     | Information                                          | Advisory                                                                  |
|-----------------------------|------------------------------------------------------|---------------------------------------------------------------------------|
| `approved, #3435`           | :heavy_check_mark: ability to merge                  | looks good, was already approved                                          |
| `approved, clearlydefined`  | :heavy_check_mark: non rejected                      | also fine                                                                 |
| `restricted, #5922`         | :heavy_multiplication_x: restricted but issue number | ok, but please this **must** be tracked                                   |
| `restricted`                | :x: restricted                                       | you don can't use this library/content please create a IP Issue on GitLab |

<!-- Links -->
[sig-infra-licence-check]: https://github.com/eclipse-tractusx/sig-infra#check-dependencies-with-dash-licenses
[DASH Tool]: https://github.com/eclipse/dash-licenses
[ip-issue-creation]: https://gitlab.eclipse.org/eclipsefdn/emo-team/iplab/-/issues/new
[TRG-7-03]: https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-03
[TRG-7-04]: https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-04
[gitlab-example-ip-issue]: https://gitlab.eclipse.org/eclipsefdn/emo-team/iplab/-/issues/8097
[docs-ip-issues]: https://eclipse-tractusx.github.io/docs/oss/issues#eclipse-gitlab-ip-issue-tracker
[IP Issue Track Link]: https://gitlab.eclipse.org/eclipsefdn/emo-team/iplab/-/issues/?search=automotive.tractusx&sort=created_date&state=opened&first_page_size=20
