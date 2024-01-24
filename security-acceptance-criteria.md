---
name: FOSS Security Release XX.XX
about: Use this template to track all Security-relevant topics for your component with regards to the upcoming Milestone.
title: "[FOSS NAME] Release Security XX.XX"
labels: foss, "security analysis"
team: SIG-Security
---

<!-- 
Thanks for your contribution! Please fill out this template as good as possible. 
Important: Contributing Guidelines can be found here: https://eclipse-tractusx.github.io/docs/oss/how-to-contribute
Checkout the repository README for process description. 
-->

# Release Security XX.XX

Source in Catena-X Confluence and Expert Contacts [here](https://confluence.catena-x.net/display/PL/Consortia+Quality+Gates)<br>
(Source only accessible for Catena-X Consortia members in current transition phase).

- [ ] **Threat Modelling Analysis results**
  Analysis completed (operations excluded):
  
    - List of risks generated or updated, rated & actions defined
    - Risks accepted or mitigation actions implemented and tested
    - no high threats acceptable

  _Artifact Repository:_
  
    - risk register (decentral on Catena-X confluence)

  _Prime Contacts:_
  
    - SIG-Security

- [ ] **Static Application Security Testing (SAST)**
  - code must be scanned weekly with Veracode tool
  - medium risks require mitigation statement
  - high and above not accepted

  _Best Practice:_
  
    - Confirm relevant repository as early as possible to SEC team to enable regular, automated scans. Evidence required for Gate approval.

  _Artifact Repository:_
  
    - Veracode UI
    - (+ GitHub Action)

  _Prime Contacts:_
  
    - SIG-Security

- [ ] **Dynamic Application Security Testing (DAST)**
  incl API testing (if applicable)
  - all findings assessed
  - high & very high findings mitigated
  - evidence by re-scan

  _Best Practice:_
  
    - Confirm relevant repository as early as possible to SEC team to enable regular, automated scans. Evidence required for Gate approval.

  _Artifact Repository:_
  
    - INVICTI tool

  _Prime Contacts:_
  
    - SIG-Security

- [ ] **Secret scanning**
  Scan executed centrally by SEC team and ZERO valid findings
  
  _Artifact Repository:_
  
    - Veracode or alternative tool
    - GitHub Secret Scanning
    - GitGuardian

  _Best Practice:_
  
    - Confirm relevant repository as early as possible to SEC team to enable regular, automated scans. Evidence required for Gate approval.

   _Prime Contact:_
  
     - SIG-Security

- [ ] **Software Composition Analysis (SCA)**
  Dependencies must be scanned with Veracode tool with regards to vulnerability
    - high and above not accepted
    - FOSS whitelist policy has to be passed

  _Best Practice:_
  
    - Confirm relevant repository as early as possible to SEC team to enable regular, automated scans. Evidence required for Gate approval.

  _Artifact Repository:_
  
    - Veracode UI
    - (& GitHub Action)

  _Prime Contacts:_
  
    - SIG-Security

- [ ] **Container Scan conducted**
  All containers in GitHub Packages must be scanned
  
    - High / Critical findings not accepted

  _Best Practice:_
  
    - Confirm relevant repository as early as possible to SEC team to enable regular, automated scans. Evidence required for Gate approval.

  _Artifact Repository:_
  
    - Trivy
    - via nightly GitHub Action

  _Prime Contacts:_
  
    - SIG-Security

- [ ] **Infrastructure as Code**
  IaC code must be scanned. 
    - Error findings not accepted

   _Best Practice:_
  
    - Confirm relevant repository as early as possible to SEC team to enable regular, automated scans. Evidence required for Gate approval.

  _Artifact Repository:_
  
    - KICS or alternative tool
    - via nightly GitHub Action

  _Prime Contacts:_
  
    - SIG-Security
