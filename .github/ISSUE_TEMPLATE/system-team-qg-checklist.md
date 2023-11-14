---
name: Quality Gate Checklist
about: 'product check for a upcoming Release'
title: 'QG X checks (Release x.x)'
labels: documentation
assignees: ''

---

## QG checks
Please keep this issue open until QG X is concluded and will be managed by the Issue Creator!
We will inform you about finding and proposals in separated issues, this issue here is for the Overview of the Checks!

### Please keep this issue open until QG X is concluded!

Product Name: <!-- Note: Please specify the official product name. -->  
Product Owner: <!-- Note: Please search for the Product Owner of this product. -->  
Dev SPOC: <!-- Note: Please search for the single point of contact of the product developers. -->  
Helm Chart Version: <!-- Note: Please note the current Helm Chart Version to check. -->  
App Version: <!-- Note: Please note the current App Version to check. -->  
QG5 Approval: yes/no <!-- Note: Please ask for the approval from Release Management. -->

### Check of Tractus-X Release Guidelines

This QG x Check is depending on the mandatory information from our current [Release Guidelines](https://eclipse-tractusx.github.io/docs/release).
Currently implemented automatic checks can be found under your product on our [Release Guidelines Checks Board](https://eclipse-tractusx.github.io/sig-release/).

#### TRG 1 Documentation

- [ ] [TRG 1.01](https://eclipse-tractusx.github.io/docs/release/trg-1/trg-1-1) appropriate `README.md` 
- [ ] [TRG 1.02](https://eclipse-tractusx.github.io/docs/release/trg-1/trg-1-2) appropriate `INSTALL.md`
- [ ] [TRG 1.03](https://eclipse-tractusx.github.io/docs/release/trg-1/trg-1-3) appropriate `CHANGELOG.md`

[back on top](#qg-checks) | [back to TRG 1](#trg-1-documentation)

#### TRG 2 Git

- [ ] [TRG 2.01](https://eclipse-tractusx.github.io/docs/release/trg-2/trg-2-1) default branch is named `main`
- [ ] [TRG 2.03](https://eclipse-tractusx.github.io/docs/release/trg-2/trg-2-3) repository structure
  - [ ] TRG 2.03 `/docs` directory contains detailed product related documentation for the Tractus-X product 
  - [ ] TRG 2.03 `/charts` directory contains the Helm chart for the Tractus-X product IF available
  - [ ] TRG 2.03 `AUTHORS.md` file (optional) (TRG 2.03)
  - [ ] TRG 2.03 `CODE_OF_CONDUCT.md` file (TRG 2.03)
  - [ ] TRG 2.03 `CONTRIBUTING.md` file (TRG 2.03)
  - [ ] TRG 2.03 `DEPENDENCIES` file(s) with up-to-date content (Dash tool generated) (TRG 2.03)
  - [ ] TRG 2.03 `LICENSE` file (TRG 2.03)
  - [ ] TRG 2.03 `NOTICE.md` file (TRG 2.03)
  - [ ] TRG 2.03 `SECURITY.md` file (TRG 2.03)
- [ ] [TRG 2.04](https://eclipse-tractusx.github.io/docs/release/trg-2/trg-2-4) Leading product repository
  - [ ] TRG 2.04 repository name must be _product-name_ without prefix or suffix
  - [ ] TRG 2.04 should contain the release
  - [ ] TRG 2.04 references/urls to the product's other repositories
  - [ ] TRG 2.04 might contain product helm chart(s)
  - [ ] TRG 2.04 README.md: contains the urls for the underlying applications
- [ ] [TRG 2.05](https://eclipse-tractusx.github.io/docs/release/trg-2/trg-2-5) `.tractusx` metafile in a proper format

[back on top](#qg-checks) | [back to TRG 2](#trg-2-git)

#### TRG 3 Kubernetes

- [ ] [TRG 3.02](https://eclipse-tractusx.github.io/docs/release/trg-3/trg-3-2) PersistentVolume and PersistentVolumeClaim is used when needed

[back on top](#qg-checks) | [back to TRG 3](#trg-3-kubernetes)

#### TRG 4 Container

- [ ] [TRG 4.01](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-1) [semantic versioning](https://semver.org/) and tagging <!-- container is tagged correctly additionally to the latest tag -->
- [ ] [TRG 4.02](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-2) top level `README.md` file, that contains information about the used base image <!-- Java, Kotlin, ... if JVM based language use base image from [Eclipse Temurin](https://hub.docker.com/_/eclipse-temurin) -->
- [ ] [TRG 4.03](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-3) Image has `USER` command and Non Root Container
  - [ ] TRG 4.03 `deployment.yaml` has `runAsUser` and `allowPrivilegeEscalation: false` properly set
- [ ] [TRG 4.05](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-05) released image must be place `DockerHub` as mandatory container registry; remove `GHCR` references 
- [ ] [TRG 4.06](https://eclipse-tractusx.github.io/docs/release/trg-4/trg-4-06) Notice File for `DockerHub` has all necessary information
  - [ ] TRG 4.06 Link to the source of your base image (Container registry and GitHub if available)
  - [ ] TRG 4.06 Link to your product image on `DockerHub`
  - [ ] TRG 4.06 Link to your repository on `GitHub`
  - [ ] TRG 4.06 Direct link to the Dockerfile used to build your image
  - [ ] TRG 4.06 Link to LICENCE file in your repo as `Project License` (make clear, that this is the PROJECT licence, not an image license

[back on top](#qg-checks) | [back to TRG 4](#trg-4-container)

#### TRG 5 Helm

- [ ] [TRG 5.01](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-01) Helm chart must be released
  - [ ] TRG 5.01 appropriate semantic versioning for `version` and `appVersion` has to be used in `Chart.yaml`
  - [ ] TRG 5.01 must not contain any environment specific `values-xyz.yaml`
  - [ ] TRG 5.01 `values.yaml` file must contain proper default values/placeholders
  - [ ] TRG 5.01 No hostname provided for ingress
  - [ ] TRG 5.01 Ingress is disabled
  - [ ] TRG 5.01 No references to any secret engine service (e.g.: Hashicorp Vault)
  - [ ] TRG 5.01 Dependencies should be prefixed with the nameOverride and/or fullnameOverride properties
  - [ ] TRG 5.01 Image tag is set to the `Chart.yaml` `appVersion` property
  - [ ] TRG 5.01 must be deployable to any environment without overwriting default values with a simple helm install command
  - [ ] TRG 5.01 dependencies have to be declared in Chart.yaml NOT requirements.yml
- [ ] [TRG 5.02](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-02) Helm chart location in `/charts` directory and correct structure
  - [ ] TRG 5.02 each file must contain the [Apache 2.0 Licence](https://github.com/catenax-ng/foss-example/blob/main/general/LICENSE)
  - [ ] TRG 5.02 latest tag is not used in helm chart be default
- [ ] [TRG 5.04](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-04) CPU and memory limits and requests are properly set
- [ ] [TRG 5.06](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-06) application must be configurable through the Helm chart <!-- every startup configuration aspect of your application must be configurable through the Helm chart (ingress class, tls, labels, annotations, database, secrets, persistence, env variables) -->
- [ ] [TRG 5.07](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-07) dependencies are present in the `Chart.yaml` they are properly configured
- [ ] [TRG 5.08](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-08) a product has a single deployable helm chart that contains all components <!--(backend, frontend, etc.) -->
  - [ ] TRG 5.08 name of the Chart should be just the product-name without prefix or suffix
  - [ ] TRG 5.08 values file should contain all available variables (even from sub-charts) with default values and comments about what they do
  - [ ] TRG 5.08 helm install command should successfully install the chart to any supported Kubernetes version cluster (without overwriting default values)
  - [ ] TRG 5.08 helm test runs without errors
- [ ] [TRG 5.09](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-09) Helm Test running properly
  - [ ] TRG 5.09 A GitHub action exist which builds or uses the helm chart which gets released
  - [ ] TRG 5.09 The GitHub action can be triggered manually through GitHub WebUI manually running a workflow
  - [ ] TRG 5.09 Helm test verifies that the application is up and running
- [ ] [TRG 5.10](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-10) Products need to support 3 versions at a time
  - [ ] TRG 5.10 latest (K8s version 1.28)
  - [ ] TRG 5.10 latest - 1 (K8s version 1.27)
  - [ ] TRG 5.10 latest - 2  (K8s version 1.26)
- [ ] [TRG 5.11](https://eclipse-tractusx.github.io/docs/release/trg-5/trg-5-11) Upgrade-ability PRERELEASE
  - [ ] TRG 5.11 Based on the Helm test workflow, you must provide a GitHub action which takes the latest released helm chart, does an installation of it and then execute the upgrade to the current / new version.

[back on top](#qg-checks) | [back to TRG 5](#trg-5-helm)
 
#### TRG 6 Released Helm Chart

- [ ] [TRG 6.01](https://eclipse-tractusx.github.io/docs/release/trg-6/trg-6-1) Released Helm Chart <!-- A released Helm chart for each Tractus-X sub-product is expected to be available in corresponding GitHub repository. -->

[back on top](#qg-checks) | [back to TRG 6](#trg-6-released-helm-chart)

#### TRG 7 Open Source Governance
- [ ] [TRG 7.01](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-01) Legal Documentation
- [ ] [TRG 7.02](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-02) License and copyright header <!-- must be present in every file if possible and update the year in the copyright section at the beginning of each new year. --> 
- [ ] [TRG 7.03](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-03) IP checks for project content <!-- for each PR containing more than 1000 relevant lines there **must** be an approved [IP review for Code Contributions](/docs/oss/issues#eclipse-gitlab-ip-issue-tracker) before the contribution can be pushed/merged -->
- [ ] [TRG 7.04](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-04) IP checks for 3rd party content
  - [ ] TRG 7.04 DEPENDENCIES file is up-to-date and reflects the current use of the 3rd party content
  - [ ] TRG 7.04 all libraries listed there should have the status "approved"
  - [ ] TRG 7.04 no libraries with status "rejected"
  - [ ] TRG 7.04 for libraries with status "restricted", the according IP issues must be present (issue number in the source column)
- [ ] [TRG 7.05](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-05) Legal information for distributions
- [ ] [TRG 7.06](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-06) Legal information for end user content
- [ ] [TRG 7.07](https://eclipse-tractusx.github.io/docs/release/trg-7/trg-7-07) Legal notice for documentation

[back on top](#qg-checks) | [back to TRG 7](#trg-7-open-source-governance)

#### Hints

#### Information Sharing
