# Security Policy

## Supported Versions

Security updates are applied only to the most recent releases.

## Reporting a Vulnerability

To securely report a vulnerability, please open an advisory on the affected GitHub repository. All repositories allow reporting vulnerabilities by clicking on the "New Issue" button.

## Vulnerability Process

1. Your report will be acknowledged within two business days.
2. The team will investigate and update the issue with relevant information.
3. If the TSC does not confirm the report, no further action will be taken and the issue will be closed.
4. If there is consensus on the TSC that this is a security risk for users, the TSC will take action to fix it immediately:
    1. Commits will be handled in a private repository for review and testing.
    2. Release a new patch version from the private repository.
    3. Issue a security advistory through GitHub.
    4. Write a blog post about the vulnerability.
    5. Notify Tidelift about the vulnerability.

If you do not receive an acknowledgement of your report within six business days, or if you cannot find a private security contact for the project, you may escalate to the OpenJS Foundation CNA at `security@lists.openjsf.org`.

If the project acknowledges your report but does not provide any further response or engagement within 14 days, escalation is also appropriate.

## Security Advisories

Security advisories are only issued when a confirmed vulnerability can be exploited by a non-local actor. Because ESLint and its related packages are primarily used as development dependencies on local machines, there are no security concerns related to regular expression performance or other problems that could bring down a public-facing server. These issues should be filed as bug reports instead of advisories.
