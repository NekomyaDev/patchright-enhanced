# Security policy

## Supported code

Security fixes target the current default branch. There is no separate maintenance
policy for older releases yet; reproduce reports against the latest code when possible.

## Reporting a vulnerability

Do not disclose vulnerabilities, exploit details, or credentials in public issues
or pull requests.

If GitHub private vulnerability reporting is enabled for this repository, use
**Security → Report a vulnerability**. Otherwise, use a private contact method
published by a repository maintainer on their GitHub profile. If neither is
available, open an issue asking only for a private security contact, without
technical details or sensitive information.

Include the affected revision and environment, impact, minimal reproduction using
synthetic data, and any suggested mitigation. Coordinate public disclosure with
maintainers after a fix is available. No response-time commitment is currently defined.

## Areas requiring particular care

- Proxy credentials, API tokens, cookies, browser profiles, logs, and traces.
- URL handling and future automation endpoints: SSRF, authentication bypass,
  unauthorized profile access, and command injection.
- Session isolation, concurrent access, and temporary-profile cleanup.

Use authorized test environments and redact secrets from all shared artifacts.
If a credential has been exposed, revoke or rotate it; deleting it from a report
or commit alone is insufficient.
