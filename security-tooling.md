# Security Tooling

These developer-friendly workflows ensure all security findings are directly visible in the GitHub Security tab, keeping everything within the familiar GitHub environment. While using these actions is optional, their implementation is strongly recommended as they introduce a foundational level of security into the development process. This documentation will guide you through their benefits and setup.

## Emphasized Guidelines for Optimizing Security GitHub Actions

Following, here are specific guidelines and best practices for developers:

1. **Action Failures**: Actions should only fail if there is an error with the Action _"Engine"_ itself or if there is a misconfiguration in the workflow. Failures should not occur based solely on high-severity findings.

2. **Manual Execution**: Include the on: workflow_dispatch option in all workflows. This allows you to manually trigger workflows whenever necessary.

3. **Scheduling Workflows**: Workflows should run frequently. Ideally, they should be set to execute once nightly. At a minimum, they should run once per week. Configure the on: schedule option to achieve this frequency.

4. **Exclusions**: Do not exclude files or directories from scans. If false positives are detected, they can be simply ignored. However, when pushing documentation to the main branch, the workflows do not need to be executed. For such cases, configure the exclude option.

5. **Pull Requests (PRs)**: It's not mandatory for workflows to run with every PR. Nonetheless, the Secret Scan is strongly recommended and deemed sufficient.

6. **Target Scanning**: Avoid over-scanning. Focusing on scanning the releases and the main branch from which releases are made is adequate.

7. **Issue Reporting**: Should developers encounter issues during scanning or have questions regarding tool usage, they are encouraged to create an issue in our repository. An appropriate issue template has been provided to streamline this process.

By adhering to these guidelines, developers can efficiently integrate GitHub actions into their workflow, ensuring optimal security without compromising productivity. 

## Security Tool Workflows

Find example workflows with explanations of the tools [(CodeQL, Dependabot, KICS, Trivy, GitGuardian) in the Tractus-X Release Guidelines (TRGs)](https://eclipse-tractusx.github.io/docs/release).

All of these tools are free for public GitHub repositories, and no key is required.
