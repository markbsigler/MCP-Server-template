# MCP-Server-template

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)
![Last Updated](https://img.shields.io/badge/last%20updated-2025--06--30-orange.svg)

A comprehensive template for creating production-ready MCP (Model Context Protocol) servers from AI prompts. This template generates fully-featured TypeScript/Node.js projects with OpenAPI-to-MCP tool mapping, security best practices, and enterprise-grade architecture.

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- Docker (optional, for containerized deployment)
- Git
- AI model access (Claude, GPT-4, etc.) for prompt usage

### 5-Minute Setup

1. **Use the template to create a new project:**
   ```bash
   git clone https://github.com/markbsigler/MCP-Server-template.git
   cd MCP-Server-template
   ```

2. **Generate your MCP server** using the `PROMPT.md` with your preferred AI model

3. **Install and run:**
   ```bash
   npm install
   npm run dev
   ```

4. **Test your MCP server:**
   ```bash
   curl http://localhost:3000/healthz
   ```

## ✨ Features Overview

### 🔧 Generated Project Includes

- **🛠️ OpenAPI-to-MCP Tools**: Automatic conversion of OpenAPI specs to MCP tools
- **🔐 Enterprise Security**: JWT authentication, input validation, rate limiting
- **🏗️ Production Architecture**: Modular structure with handlers, middleware, and types
- **🧪 Comprehensive Testing**: Jest-based unit and integration tests with coverage
- **🐳 Container Ready**: Multi-stage Docker builds with docker-compose
- **🚀 CI/CD Pipeline**: GitHub Actions with security scanning and multi-platform builds
- **📊 Monitoring**: Health checks, structured logging, and metrics collection
- **🔌 Extensible**: Plugin architecture and middleware system
- **📚 Documentation**: Auto-generated API docs and comprehensive examples

### 🏛️ Architecture Highlights

- **MCP Protocol Compliance**: Full `tools/list`, `tools/call`, and notifications support
- **Streamable HTTP Transport**: JSON-RPC 2.0 over HTTP with SSE support
- **Security First**: No token passthrough, secure session management
- **Performance Optimized**: Streaming responses and efficient resource usage

## 📁 Generated Project Structure

```
your-mcp-server/
├── src/
│   ├── handlers/          # MCP protocol handlers
│   ├── middleware/        # Authentication, validation, CORS
│   ├── types/            # TypeScript type definitions
│   ├── utils/            # Helper functions and utilities
│   └── index.ts          # Main server entry point
├── tests/
│   ├── unit/             # Unit tests
│   ├── integration/      # Integration tests
│   └── __mocks__/        # Test mocks
├── config/
│   ├── openapi.json      # OpenAPI specification
│   └── environments/     # Environment configurations
├── docs/
│   ├── api/              # Generated API documentation
│   └── architecture/     # Architecture diagrams
├── .github/
│   └── workflows/        # GitHub Actions CI/CD
├── docker/
│   ├── Dockerfile        # Multi-stage Docker build
│   └── docker-compose.yml
├── package.json
├── tsconfig.json
└── README.md
```

## 📖 PROMPT.md Usage Guide

### Using with AI Models

1. **Copy the entire `PROMPT.md` content**
2. **Customize for your use case:**
   ```
   Generate an MCP server for [YOUR_USE_CASE] with the following additional requirements:
   - [Custom requirement 1]
   - [Custom requirement 2]
   
   [Paste PROMPT.md content here]
   ```

3. **Submit to your AI model** (Claude, GPT-4, etc.)

### Customization Options

The prompt supports several customization variables:

- **Project Name**: Modify the generated project name and structure
- **OpenAPI Specification**: Provide your own OpenAPI spec for custom tools
- **Security Requirements**: Add specific authentication or authorization needs
- **Deployment Target**: Specify cloud platform or container orchestration
- **Integration Requirements**: Add specific third-party service integrations

### Best Practices

- **Be Specific**: Add detailed requirements for your use case
- **Include Examples**: Provide sample OpenAPI operations you want to support
- **Specify Security**: Define your authentication and authorization requirements
- **Mention Integrations**: List any third-party services you need to integrate

## 🛠️ How to Setup a New Project

If you want to use this template to create a completely new MCP server project (without the original history and disconnected from this template), follow these steps:

### Step 1: Clone and Remove Git History

```bash
git clone https://github.com/markbsigler/MCP-Server-template.git
cd MCP-Server-template
rm -rf .git
```

### Step 2: Initialize as New Git Repository

```bash
git init
git add .
git commit -m "Initial commit"
```

### Step 3: Create New Repository on GitHub

1. Go to GitHub.com and click the **+** icon
2. Select **New repository** 
3. Enter **&lt;newMCPrepo&gt;** as the repository name
4. Choose public/private
5. **Don't** check any initialization options (README, .gitignore, license)
6. Click **Create repository**

### Step 4: Connect to Your New Repository

```bash
git branch -M main
git remote add origin https://github.com/&lt;username&gt;/&lt;newMCPrepo&gt;.git
git push -u origin main
```

### Step 5: Rename the Local Folder

```bash
cd ..
mv MCP-Server-template &lt;newMCPrepo&gt;
cd &lt;newMCPrepo&gt;
```

Now you have your new MCP project ready to go - completely independent from the original template with a fresh git history!

## 📝 Examples

### Generated Project Examples

1. **REST API to MCP Tools**
   - OpenAPI spec with CRUD operations
   - Automatic MCP tool generation
   - JWT authentication with rate limiting

2. **File Processing Service**
   - File upload/download operations
   - Binary content handling
   - Streaming responses

3. **Data Analytics Platform**
   - Complex query operations
   - Paginated responses
   - Real-time data streaming

### Usage Scenarios

- **API Gateway**: Convert existing REST APIs to MCP tools
- **Microservice Integration**: Bridge microservices with MCP protocol
- **AI Assistant Backend**: Provide tools for AI assistants and agents
- **Workflow Automation**: Create tools for business process automation

## 🤝 How to Contribute

We welcome contributions to improve this MCP Server template! Here's how you can help:

### Getting Started

1. **Fork the repository** to your GitHub account
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/&lt;your-username&gt;/MCP-Server-template.git
   cd MCP-Server-template
   ```
3. **Create a feature branch** for your contribution:
   ```bash
   git checkout -b feature/your-feature-name
   ```

### Types of Contributions

We're looking for help with improving the **PROMPT.md** file:

- **Additional MCP features**: Expand the prompt to include more MCP protocol capabilities
- **Security enhancements**: Add more security best practices and implementation details
- **Architecture improvements**: Better project structure and organization patterns
- **Tool implementation patterns**: More comprehensive OpenAPI-to-MCP tool mapping examples
- **Performance optimizations**: Add performance considerations and monitoring requirements
- **Testing strategies**: Expand testing requirements and methodologies
- **Documentation standards**: Improve documentation generation and maintenance requirements
- **Deployment scenarios**: Add more container and cloud deployment patterns
- **Integration examples**: More comprehensive client and integration examples
- **Error handling**: Enhanced error handling and recovery patterns

### Submitting Changes

1. **Commit your changes** with clear, descriptive messages:
   ```bash
   git add .
   git commit -m "feat: add new MCP tool for file processing"
   ```
2. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```
3. **Create a Pull Request** on GitHub:
   - Provide a clear description of your changes
   - Reference any related issues
   - Include screenshots or examples if applicable

### Pull Request Guidelines

- **Keep PRs focused**: One feature or fix per PR
- **Write clear descriptions**: Explain what changes you made and why
- **Include tests**: All new code should have corresponding tests
- **Update documentation**: Ensure README and other docs reflect your changes
- **Follow conventional commits**: Use clear, descriptive commit messages

### Code Standards

- **TypeScript**: Use strict typing and follow existing patterns
- **ESLint/Prettier**: Code must pass linting and formatting checks
- **Testing**: Maintain or improve test coverage
- **Security**: Follow security best practices, especially for MCP tools
- **Performance**: Consider performance implications of changes

### Reporting Issues

If you find a bug or have a feature request:

1. **Search existing issues** to avoid duplicates
2. **Use issue templates** when available
3. **Provide detailed information**:
   - Steps to reproduce (for bugs)
   - Expected vs. actual behavior
   - Environment details (Node.js version, OS, etc.)
   - Relevant code snippets or logs

### Community Guidelines

- **Be respectful** and constructive in all interactions
- **Help others** by answering questions and reviewing PRs
- **Follow the code of conduct** (if applicable)
- **Stay focused** on improving the template for everyone

### Questions?

If you have questions about contributing:
- Open a **Discussion** on GitHub
- Check existing **Issues** and **Pull Requests**
- Review the **PROMPT.md** file for technical details

Thank you for helping make this MCP Server template better for everyone!

## 🐛 Troubleshooting

### Common Issues

**Q: AI model generates incomplete code**
- A: The prompt is comprehensive - try breaking it into smaller sections or use a model with larger context window

**Q: Generated project won't start**
- A: Check Node.js version (18+ required) and run `npm install` to install dependencies

**Q: OpenAPI tools not generating**
- A: Verify your `config/openapi.json` file is valid JSON and follows OpenAPI 3.0+ specification

**Q: Authentication issues**
- A: Check JWT token configuration and ensure proper Bearer token format

**Q: Docker build fails**
- A: Ensure Docker is installed and running, check Dockerfile syntax

### Getting Help

- Check the generated project's README for specific setup instructions
- Review the PROMPT.md for implementation details
- Open an issue with detailed error messages and environment info

## 📋 Changelog

### Version 1.0.0 (2025-06-30)
- Initial release of MCP Server template
- Comprehensive PROMPT.md for AI code generation
- OpenAPI-to-MCP tools mapping
- Security best practices implementation
- Docker and CI/CD support
- Extensive documentation and examples

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Attribution

When using this template:
- Retain the original LICENSE file
- Modify the copyright notice in generated projects
- Credit this template in your project documentation (optional but appreciated)

### Third-Party Licenses

Generated projects may include:
- Express.js (MIT License)
- Jest (MIT License)
- TypeScript (Apache 2.0 License)
- Other npm packages with their respective licenses

## 🔗 Related Resources

### MCP Protocol
- [MCP Specification](https://spec.modelcontextprotocol.io/)
- [MCP Tools Documentation](https://spec.modelcontextprotocol.io/specification/basic/tools/)
- [MCP Security Best Practices](https://spec.modelcontextprotocol.io/specification/basic/security/)

### OpenAPI
- [OpenAPI Specification](https://swagger.io/specification/)
- [OpenAPI Generator](https://openapi-generator.tech/)
- [Swagger Editor](https://editor.swagger.io/)

### TypeScript & Node.js
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Node.js Best Practices](https://github.com/goldbergyoni/nodebestpractices)
- [Jest Testing Framework](https://jestjs.io/docs/getting-started)

### Related MCP Tools
- [MCP Servers Collection](https://github.com/modelcontextprotocol/servers)
- [MCP Client Libraries](https://github.com/modelcontextprotocol/typescript-sdk)
- [MCP Protocol Implementations](https://github.com/modelcontextprotocol)

---

**Ready to build your MCP server?** Use the PROMPT.md with your favorite AI model and create production-ready MCP servers in minutes! 🚀
