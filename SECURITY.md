# Security Policy

## Supported Versions

| Version | Supported | Description |
| :--- | :--- | :--- |
| `1.0.x` | Yes | Current stable release branch (`main`) |
| `< 1.0.0` | No | Legacy versions |

## Security Scope and Invariants

email-router-api executes at the Cloudflare Workers edge and handles inbound mail routing. Security invariants include:
* **CRLF Header Injection Defense**: Inbound values rendered into email headers must be strictly sanitized to prevent carriage return / line feed (`\r`, `\n`) header injection attacks.
* **Credential Isolation**: Cloudflare API tokens and email bindings must never be hardcoded into source files or serialized in API responses.
* **CORS Policy**: Cross-origin requests must be restricted to authorized domains in production environments.

## Reporting a Vulnerability

If you discover an email relay vulnerability, header injection vector, or authentication flaw, report it privately:

* **Security Contact**: Gohar Rehman
* **Email**: `goharrehmanfsd260@gmail.com`
* **Response SLA**: Initial acknowledgement within 48 hours; resolution timeline provided within 7 days.

Please do not open public GitHub issues or discussions regarding undisclosed vulnerabilities.