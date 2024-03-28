## Security Tooling

These developer-friendly workflows ensure all security findings are directly visible in the GitHub Security tab, keeping everything within the familiar GitHub environment. While using these actions is optional, their implementation is strongly recommended as they introduce a foundational level of security into the development process. This documentation will guide you through their benefits and setup.

### Emphasized Guidelines for Optimizing Security GitHub Actions

Following, here are specific guidelines and best practices for developers:

1.**Action Failures:** Actions should only fail if there is an error with the Action "Engine" itself or if there is a misconfiguration in the workflow. Failures should not occur based solely on high-severity findings.

2.**Manual Execution:** Include the on: workflow_dispatch option in all workflows. This allows you to manually trigger workflows whenever necessary.

3.**Scheduling Workflows:** Workflows should run frequently. Ideally, they should be set to execute once nightly. At a minimum, they should run once per week. Configure the on: schedule option to achieve this frequency.

4.**Exclusions:** Do not exclude files or directories from scans. If false positives are detected, they can be simply ignored. However, when pushing documentation to the main branch, the workflows do not need to be executed. For such cases, configure the exclude option.

5.**Target Scanning:** Avoid over-scanning. Focusing on scanning the releases and the main branch from which releases are made is adequate.

6.**Issue Reporting:** Should developers encounter issues during scanning or have questions regarding tool usage, they are encouraged to create an issue in our repository. An appropriate issue template has been provided to streamline this process.

By adhering to these guidelines, developers can efficiently integrate GitHub actions into their workflow, ensuring optimal security without compromising productivity.

## Security Tool Workflows

Find example workflows with explanations of the tools [(CodeQL, Dependabot, KICS, Trivy, GitGuardian) in the Tractus-X Release Guidelines (TRGs)](https://eclipse-tractusx.github.io/docs/release/).

All of these tools are free for public GitHub repositories, and no key is required.

### Additional Security Measures

While the above tools are integral to our TRGs, we also recommend **SNYK** as an additional layer of security. **SNYK** specializes in providing actionable insights and guidance to remediate vulnerabilities, thereby enhancing the security posture of your projects.

Please note that **SNYK** setup is managed exclusively by the Security Team. To incorporate **SNYK** into your workflow, developers should contact the Security Team by creating an issue on GitHub.

**SNYK's** integration with GitHub repositories allows for continuous scanning and monitoring, offering security reports, automated fix pull requests, and timely alerts.

To integrate **SNYK** with your GitHub repository, you need to follow these steps:

- Login to **SNYK** using your GitHub account
- Go to the Integrations page in your **SNYK** account and click **Connect to GitHub**
- Grant permissions to SNYK to access your GitHub repositories and authorize the **SNYK** application
- Choose which repositories you want to test and monitor with **SNYK** and click **Add selected repositories to SNYK**
- **Snyk** will scan your repositories for vulnerabilities and provide you with security reports, fix pull requests, and alerts
