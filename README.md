# email-router-api

A high-performance, scalable API gateway designed to parse, filter, and route inbound and outbound emails to webhooks, database queues, or third-party email providers based on customizable rulesets.

## Architecture and Stack

* **Runtime**: Node.js (v18+)
* **Engine**: Express.js, MIME message parsers
* **Dispatch**: HTTP Webhooks, SMTP connectors, asynchronous queue processors

## Key Features

* **Dynamic Rule Engine**: Route emails conditionally based on sender domain, recipient, subject regex, or header tags.
* **MIME Payload Parsing**: Automatic extraction of body text, HTML markup, attachments, and metadata.
* **Webhook Forwarding**: Configurable webhook endpoints with exponential backoff retry mechanisms.
* **Zero Dependency Sprawl**: Clean architectural boundaries with minimal external dependencies.

## Getting Started

### Prerequisites
* Node.js v18+
* npm or pnpm

### Installation
```bash
git clone https://github.com/itsgoharrehman/email-router-api.git
cd email-router-api
npm install
```

### Configuration
Create a `.env` file in the root directory:
```env
PORT=4000
WEBHOOK_TARGET_URL=https://api.yourdomain.com/webhooks/email
API_KEY=your_secure_api_key
```

### Running
```bash
npm start
```

## Security Policy

Disclose vulnerabilities to `goharrehmanfsd260@gmail.com`.

## Maintainer

* **Gohar Rehman**
* GitHub: [@itsgoharrehman](https://github.com/itsgoharrehman)
* Email: `goharrehmanfsd260@gmail.com`
* Website: [itsgoharrehman.netlify.app](https://itsgoharrehman.netlify.app/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
