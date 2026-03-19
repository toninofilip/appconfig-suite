# AppConfig² Suite

<div align="center">
  <img src="https://www.appconfig.eu/images/logo-nobackground-5000-orange-grad-wheel.png" alt="AppConfig² Logo" width="200"/>
  <p><strong>Complete Application Management Suite for Microsoft Entra™ ID</strong></p>
</div>

---

## 🚀 What is AppConfig² Suite?

AppConfig² is a specialized application management suite designed specifically for Microsoft Entra ID application configuration, testing, and troubleshooting. The suite features two specialized tools designed for different organizational needs and compliance requirements. Both tools provide powerful Microsoft Entra ID capabilities while serving distinct use cases.

### 🔧 AppConfig - Full Configuration Management
The complete solution for developers, IT administrators, and security professionals who need full control over application configurations with comprehensive backup and restore capabilities.

### 🔍 AppTesting - Read-Only Analysis & Testing
A specialized tool for organizations requiring configuration changes through official Entra portal only, while maintaining powerful troubleshooting and analysis capabilities.

---

## 🎯 Who Is This Suite For?

<table>
<tr>
<td align="center" width="25%">
<img src="https://img.icons8.com/fluency/48/technical-support.png" alt="Support"/>
<br/><strong>Level 3 Support</strong>
<br/>Comprehensive troubleshooting with both read-only and full management options
</td>
<td align="center" width="25%">
<img src="https://img.icons8.com/fluency/48/code.png" alt="Developers"/>
<br/><strong>Developers</strong>
<br/>Test authentication flows with appropriate tool based on environment permissions
</td>
<td align="center" width="25%">
<img src="https://img.icons8.com/fluency/48/administrator-male.png" alt="Admins"/>
<br/><strong>IT Administrators</strong>
<br/>Choose between full management or compliance-ready read-only analysis
</td>
<td align="center" width="25%">
<img src="https://img.icons8.com/fluency/48/security-shield-green.png" alt="Security"/>
<br/><strong>Security Engineers</strong>
<br/>Security analysis tools with appropriate access levels for your organization
</td>
</tr>
</table>

---

## ⭐ AppConfig² Suite Features

### 🌟 Core Capabilities (Both Tools)
- **🎫 Authentication Flow Testing** - Test various flows and inspect token responses
- **🔓 Advanced Token Analysis** - Decode and analyze OAuth/OIDC tokens with detailed claims
- **📊 Enhanced Dashboard** - Real-time application portfolio metrics and insights
- **🛡️ Security Analysis** - Comprehensive permission analysis and risk assessment
- **📈 Attack Surface Analysis** - Identify and evaluate potential security vulnerabilities
- **🔄 Application Lifecycle Tracking** - Monitor creation, ownership, and change history
- **🌐 Embedded Graph Explorer** - Deep dive analysis using Microsoft Graph API
- **📋 Conditional Access Analysis** - View applied policies and their authentication impact

#### 🧰 Built-in Suite Tools (Available in Both Apps)
- **Confidential Client Auth Debugger** - Test web applications (confidential clients) with Authorization Code Flow using minimal configuration (only redirect URI addition); supports PKCE, custom APIs, and full token inspection; automatic silent backup enables easy restoration
- **Token Scope Requester** - Request tokens for Graph or custom APIs with /.default, consent, and tenant authority controls; includes quick GET tester
- **Raw OAuth Tester** - Run implicit flow without MSAL, generate authorize URLs, validate state/nonce, and inspect tokens
- **OData Query Builder** - Build Graph OData queries visually, paginate, and export JSON
- **Secrets & Certificate Expiration Monitor** - Surface expiring/expired secrets and certs (apps/SPs), filter by risk level, and export CSV
- **Entra Endpoints Explorer** - Comprehensive reference of Microsoft Entra ID endpoints across clouds (public, government, China, Germany) with variable substitution
- **MSAL Trace Viewer** - Real-time visibility into MSAL.js authentication events with correlation tracking, test actions, and detailed event inspection
- **OIDC Metadata Inspector** - Inspect OpenID Connect discovery documents, JWKS, validate JWT signatures, and analyze token claims across different authorities

### 🔧 AppConfig - Full Management Capabilities
- **📝 Complete App Lifecycle** - Create, configure, and manage applications end-to-end
- **🔄 Automatic Backups & Restore** - Tested application silently backed up with one-click restoration
- **👥 User Provisioning** - Provision and deprovision users with role assignments
- **🏷️ Dynamic App Roles** - Create and manage application roles with permissions
- **🗺️ Claims Mapping Policies** - Create, edit, and assign claims mapping policies
- **📦 Directory Extensions** - Manage custom directory extensions and attributes
- **🔑 Credential Management** - Generate and manage client secrets and certificates

### 🔍 AppTesting - Read-Only Analysis
- **✅ All Testing Capabilities** - Complete authentication flow testing without modifications
- **🛡️ Compliance Ready** - Meets strict organizational change control policies
- **📊 Comprehensive Analysis** - Full permission and security analysis capabilities
- **🔒 Safe Operation** - Zero risk of accidental configuration changes
- **👀 Deep Insights** - All troubleshooting features with read-only access

---

## 📸 Suite Screenshots

<div align="center">

### Application Dashboard
<img src="https://www.configsquared.com/images/Home.png" alt="Application Dashboard" width="600"/>

### Application Filtering
<img src="https://www.configsquared.com/images/AppsContent.png" alt="Application Filtering" width="600"/>

### Application Management
<img src="https://www.configsquared.com/images/AppTester.png" alt="Application Management" width="600"/>

</div>

<details>
<summary>📱 <strong>View More Screenshots</strong></summary>

### Troubleshooting Authentication as Different User
<img src="https://www.configsquared.com/images/AuthenticateAs-2.png" alt="Troubleshooting Authentication" width="500"/>

### Advanced Tools Suite
<img src="https://www.configsquared.com/images/ToolsContent.png" alt="Advanced Tools" width="500"/>

### Integrated Graph Explorer
<img src="https://www.configsquared.com/images/GraphExplorer.png" alt="Graph Explorer" width="500"/>

</details>

---

## 🚦 How The Suite Works

```mermaid
flowchart LR
    A[🔐 Sign in with Entra ID] --> B{Choose Your Tool}

    %% Vertically stack tool choices (AppTesting above AppConfig)
    subgraph S[ ]
      direction TB
      D[🔍 AppTesting - Read-Only]
      C[🔧 AppConfig - Full Manage]
    end
    style S fill:transparent,stroke:transparent

    B --> D
    B --> C

    %% Paths
    D --> F[📊 Analyze & Test]
    C --> E[📊 Configure & Test]
    E --> G[⏪ Restore]
    F --> H[📈 Monitor & Report]
    G --> H

    %% Styling
    style A fill:#e1f5fe
    style B fill:#f3e5f5
    style C fill:#e8f5e8
    style D fill:#fff3e0
    style E fill:#f1f8e9
    style F fill:#fce4ec
    style G fill:#f3e5f5
    style H fill:#e0f2f1
```

### AppConfig Workflow
1. **🔐 Sign in** with your Microsoft Entra ID account
2. **🎯 Select** applications from your portfolio dashboard
3. **🔧 Configure** settings with automatic backup protection
4. **📊 Test** authentication flows and analyze results
5. **⏪ Restore** configurations using one-click restoration

### AppTesting Workflow
1. **🔐 Sign in** with your Microsoft Entra ID account
2. **🎯 Select** applications for analysis
3. **📊 Test** authentication flows without modification risks
4. **🔍 Analyze** configurations and identify issues
5. **📈 Report** findings while maintaining compliance

---

## 🏁 Getting Started

### Choose Your Tool

**Need full configuration management?** → **AppConfig**
- Modify application settings
- Create and manage app roles
- Generate client secrets
- User provisioning capabilities
- Complete backup and restore

**Need read-only analysis only?** → **AppTesting**
- Comprehensive testing without changes
- Compliance with strict change control
- All troubleshooting capabilities
- Risk-free operation
- Security and permission analysis

### Quick Start
1. Get the AppConfig² Suite on Azure Marketplace: <a href="https://azuremarketplace.microsoft.com/en-us/marketplace/apps?search=AppConfig%C2%B2&page=1" target="_blank" rel="noopener noreferrer">Open Azure Marketplace</a>
2. Choose your tool based on organizational requirements
3. Sign in with your Entra ID credentials
4. Explore the enhanced dashboard and portfolio insights
5. Start testing with comprehensive toolkit

---

## 🏗️ Technical Architecture

The AppConfig² Suite is built using modern web technologies optimized for enterprise identity management:

- **Frontend**: React 18+ with TypeScript and Material-UI
- **Authentication**: Microsoft Authentication Library (MSAL) 2.0
- **API Integration**: Microsoft Graph SDK with enhanced caching
- **State Management**: React Context with custom hooks and optimized caching
- **Security**: OAuth 2.0 / OpenID Connect compliant with zero-trust architecture

### Enhanced Features
- **Portfolio Dashboard**: Real-time application metrics and insights
- **Advanced Caching**: Optimized performance with intelligent data caching
- **Export Capabilities**: CSV exports for security and lifecycle analysis
- **Attack Surface Analysis**: Comprehensive security vulnerability assessment
- **Lifecycle Tracking**: Complete application creation and change history

---

## 🔒 Security & Compliance

The AppConfig² Suite follows enterprise security best practices:

- **🔐 Zero Secrets Storage** - No application secrets or credentials stored
- **🎫 Token-Based Access** - All operations use delegated permissions
- **🛡️ Principle of Least Privilege** - Minimal required permissions only
- **🔄 Automatic Backups** - Safety nets for all modifications (AppConfig)
- **📊 Compliance Ready** - Read-only option for strict change control (AppTesting)
- **🛡️ Zero Trust Architecture** - Never trust, always verify approach

---

## 📚 Suite Documentation

- **[AppConfig² Features Guide](./Features%20Guide.md)** - Comprehensive suite feature documentation
- **[Architecture Overview](./Architecture%20Overview.md)** - Technical architecture and design decisions

---

## 🤝 Contributing

We welcome contributions from the community! Whether you're reporting bugs, suggesting features, or contributing code, please read our [Contributing Guidelines](./CONTRIBUTING.md).

### Ways to Contribute
- 🐛 **Report Issues** - Help us identify and fix bugs across both tools
- 💡 **Suggest Features** - Share ideas for new functionality in either tool
- 📖 **Improve Documentation** - Help make our comprehensive docs better
- 🧪 **Beta Testing** - Join our early access program for the complete suite

---

## 🛒 Azure Marketplace Availability

Now available on Azure Marketplace:
- 1-month free trial of the full AppConfig² Suite
- Azure-native billing and subscription management
- Enterprise-ready security and compliance
- Professional technical support

Get it on Azure Marketplace:
<a href="https://azuremarketplace.microsoft.com/en-us/marketplace/apps?search=AppConfig%C2%B2&page=1" target="_blank" rel="noopener noreferrer">Open Azure Marketplace</a>

---

## 📞 Support & Community

- **🌐 Website**: [www.appconfig.eu](https://www.appconfig.eu/)
- **💼 LinkedIn**: [AppConfig² Company Page](https://www.linkedin.com/company/appconfig-square/)
- **📧 Email**: [support@appconfig.app](mailto:support@appconfig.app)

---

## 📄 License

This project is proprietary software. All rights reserved. See [LICENSE](./LICENSE.md) for details.

---

## 🙏 Acknowledgments

- **Microsoft** for the comprehensive Entra ID and Graph API ecosystem
- **Early Access Users** for valuable feedback and testing across both tools
- **Enterprise Partners** for guidance on compliance and organizational requirements

---

<div align="center">
  <h3>🚀 Get it on Azure Marketplace</h3>
  <p>Deploy AppConfig² Suite with Azure-native billing and compliance.</p>
  <a href="https://azuremarketplace.microsoft.com/en-us/marketplace/apps?search=AppConfig%C2%B2&page=1" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/Get%20it%20on-Azure%20Marketplace-0078D4?style=for-the-badge&logo=microsoft-azure" alt="Get it on Azure Marketplace"/>
  </a>
</div>

---

<div align="center">
  <sub>Built with ❤️ for the Microsoft Entra ID community</sub>
</div>