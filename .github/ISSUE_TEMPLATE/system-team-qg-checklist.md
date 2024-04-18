---
name: Quality Gate Checklist
about: 'product check for a upcoming Release'
title: 'QG X checks (Release x.x)'
labels: documentation
assignees: ''

---

## QG checks
Please keep this issue open until QG is concluded and will be managed by the Issue Creator!
We will inform you about finding and proposals in separated issues, this issue here is for the Overview of the Checks!

### Please keep this issue open until QG is concluded!

Product Owner: <!-- Note: Please search for the Product Owner of this product. -->  
Dev SPOC: <!-- Note: Please add every contributor to this product -->  
Helm Chart Version: <!-- Note: Please note the current Helm Chart Version to check. -->  
App Version: <!-- Note: Please note the current App Version to check. -->  

Release Managemnet Reference Issue: <!-- Note: Add the related product RM issue -->  

### Check of Tractus-X Release Guidelines

- Currently implemented automatic checks can be found under your product on our [Release Guidelines Checks Board](https://eclipse-tractusx.github.io/sig-release/) 
- This QG Check is depending on the mandatory information from our current [Release Guidelines](https://eclipse-tractusx.github.io/docs/release)

#### TRG 1 Documentation

- [ ] [TRG 1.01](https://eclipse-tractusx.github.io/docs/release/trg-1/trg-1-1) appropriate `README.md` 
- [ ] [TRG 1.02](https://eclipse-tractusx.github.io/docs/release/trg-1/trg-1-2) appropriate install instructions either `INSTALL.md` or in `README.md`
- [ ] [TRG 1.03](https://eclipse-tractusx.github.io/docs/release/trg-1/trg-1-3) appropriate `CHANGELOG.md`
- [ ] [TRG 1.04](https://eclipse-tractusx.github.io/docs/release/trg-1/trg-1-4) editable static files

#### TRG 2 Git

- [ ] [TRG 2.01](https://eclipse-tractusx.github.io/docs/release/trg-2/trg-2-1) default branch is named `main`
- [ ] [TRG 2.03](https://eclipse-tractusx.github.io/docs/release/trg-2/trg-2-3) repository structure
- [ ] [TRG 2.04](https://eclipse-tractusx.github.io/docs/release/trg-2/trg-2-4) leading product repository
- [ ] [TRG 2.05](https://eclipse-tractusx.github.io/docs/release/trg-2/trg-2-5) `.tractusx` metafile in a proper format

#### TRG 3 Kubernetes

- [ ] [TRG 3.02](https://eclipse-tractusx.github.io/docs/release/trg-3/trg-3-2) persistent volume and persistent volume claim is used when needed

#### TRG 4 Container

- [ ] [TRG 4.01](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-01) [semantic versioning](https://semver.org/) and tagging <!-- container is tagged correctly additionally to the latest tag -->
- [ ] [TRG 4.02](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-02) base image is agreed  <!-- Java, Kotlin, ... if JVM based language use base image from [Eclipse Temurin](https://hub.docker.com/_/eclipse-temurin) -->
- [ ] [TRG 4.03](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-03) image has `USER` command and Non Root Container
- [ ] [TRG 4.05](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-05) released image must be placed in `DockerHub`, remove `GHCR` references 
- [ ] [TRG 4.06](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-06) separate notice file for `DockerHub` has all necessary information

#### TRG 5 Helm

- [ ] [TRG 5.01](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-01) Helm chart requirements
- [ ] [TRG 5.02](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-02) Helm chart location in `/charts` directory and correct structure
- [ ] [TRG 5.03](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-03) proper version strategy 
- [ ] [TRG 5.04](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-04) CPU / MEM resource requests and limits and are properly set
- [ ] [TRG 5.06](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-06) Application must be configurable through the Helm chart <!-- every startup configuration aspect of your application must be configurable through the Helm chart (ingress class, tls, labels, annotations, database, secrets, persistence, env variables) -->
- [ ] [TRG 5.07](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-07) Dependencies are present and properly configured in the Chart.yaml
- [ ] [TRG 5.08](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-08) Product has a single deployable helm chart that contains all components <!--(backend, frontend, etc.) -->
- [ ] [TRG 5.09](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-09) Helm Test running properly
- [ ] [TRG 5.10](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-10) Products need to support 3 versions at a time
- [ ] [TRG 5.11](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-11) Upgradeability
 
#### TRG 6 Released Helm Chart

- [ ] [TRG 6.01](https://eclipse-tractusx.github.io/docs/release/trg-6/trg-6-1) Released Helm Chart <!-- A released Helm chart for each Tractus-X sub-product is expected to be available in corresponding GitHub repository. -->

#### TRG 7 Open Source Governance
- [ ] [TRG 7.01](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-01) Legal Documentation
- [ ] [TRG 7.02](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-02) License and copyright header <!-- must be present in every file if possible and update the year in the copyright section at the beginning of each new year. --> 
- [ ] [TRG 7.03](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-03) IP checks for project content <!-- for each PR containing more than 1000 relevant lines there **must** be an approved [IP review for Code Contributions](/docs/oss/issues#eclipse-gitlab-ip-issue-tracker) before the contribution can be pushed/merged -->
- [ ] [TRG 7.04](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-04) IP checks for 3rd party content
- [ ] [TRG 7.05](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-05) Legal information for distributions
- [ ] [TRG 7.06](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-06) Legal information for end user content
- [ ] [TRG 7.07](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-07) Legal notice for documentation
- [ ] [TRG 7.08](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-08) Legal notice for KIT documentation

#### TRG 8 Security
- [ ] [TRG 8.01](https://eclipse-tractusx.github.io/docs/release/trg-8/trg-8-01) Mitigate high and above findings in CodeQL
- [ ] [TRG 8.02](https://eclipse-tractusx.github.io/docs/release/trg-8/trg-8-02) Mitigate high and above findings in KICS
- [ ] [TRG 8.03](https://eclipse-tractusx.github.io/docs/release/trg-8/trg-8-03) Mitigate high and above findings in GitGuardian
- [ ] [TRG 8.04](https://eclipse-tractusx.github.io/docs/release/trg-8/trg-8-04) Mitigate high and above findings in Trivy

#### Hints

#### Information Sharing
