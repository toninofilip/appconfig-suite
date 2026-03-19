# AppConfig² Suite Features Guide

This guide covers features available in the AppConfig² Suite, organized by tool and functionality.

## 🌟 Core Capabilities (AppConfig & AppTesting)

### Enhanced Portfolio Dashboard
- Application Portfolio Overview - Comprehensive view of all applications with key metrics
- Security Dashboard - Real-time security posture analysis across all applications
- Interactive Metrics - Clickable cards that filter and navigate to specific applications
- Export Capabilities - CSV exports for compliance and reporting needs

### Testing & Authentication
- Multi-Flow Support - Authorization Code, Implicit, Client Credentials, and hybrid flows
- Real-Time Token Analysis - Live token decoding with syntax highlighting
- Claims Inspector - Detailed token claims analysis and validation
- User Context Testing - Test authentication flows as different users

### Advanced Security Analysis
- Attack Surface Analysis - Comprehensive vulnerability assessment and attack vector identification
- Permission Analysis - Detailed API permission review with risk scoring
- Security Scorecard - Overall security posture with actionable recommendations

### Application Lifecycle Tracking
- Creation Tracking - Monitor when and how applications were created
- Ownership Management - Track application owners and management responsibilities
- Quick Statistics - View number of owners, API Permissions, Redirect URIs and App Roles

### Graph Integration & Tools
- Embedded Graph Explorer - Full Microsoft Graph API console integration
- Request Templates - Pre-built queries for common scenarios
- Batch Operations - Execute Graph API calls efficiently (limited to GET method in AppTesting)

### Suite Tools (AppConfig & AppTesting)
- **Confidential Client Auth Debugger** - Test web applications (confidential clients) using Authorization Code Flow with PKCE support, custom API integration, and comprehensive token inspection. Requires only adding AppConfig² redirect URI (easily restored via automatic silent backup). Provides step-by-step flow visualization, automatic state/nonce validation, and detailed comparison with SPA flows
- **Token Scope Requester** - Request tokens for Graph or custom APIs with /.default, consent, and tenant authority controls; includes quick GET tester
- **Raw OAuth Tester** - Run implicit flow without MSAL, generate authorize URLs, validate state/nonce, and inspect tokens
- **OData Query Builder** - Build Graph OData queries visually, paginate, and export JSON
- **Secrets & Certificate Expiration Monitor** - Surface expiring/expired secrets and certs (apps/SPs), filter by risk level, and export CSV
- **Entra Endpoints Explorer** - Comprehensive reference guide for Microsoft Entra ID endpoints across all Azure clouds with multi-cloud support, variable substitution, categorized endpoints (OAuth 2.0/OIDC, Graph, Azure Management, B2C, SAML), one-click copying, and direct links to Microsoft documentation
- **MSAL Trace Viewer** - Real-time MSAL.js authentication event monitoring and debugging with live event capture grouped by correlation ID, built-in test actions, interaction type filtering, PII redaction toggle, JSON export, and detailed event payload inspection
- **OIDC Metadata Inspector** - OpenID Connect discovery and JWT validation tool with support for fetching and analyzing OIDC discovery documents, JWKS inspection, JWT decoding with automatic token type detection, signature verification, and key matching.


## 🔧 AppConfig - Full Management Tool

### Complete Application Lifecycle Management
- New Application Registration - Guided creation wizard with template-based setup
- Configuration Management - Comprehensive settings management with backup protection
- User Provisioning - Bulk and individual user provisioning with role assignment
- Credential Management - Client secret and certificate generation with expiration tracking
- Backup & Restore - Automatic configuration backups with one-click restoration
- Delete Application - Securely delete applications when no longer needed
- Restore Deleted Application - Recover deleted applications to minimize accidental loss

### Advanced Configuration Features
- App Roles Management - Dynamic role creation with permission mapping
- API Permissions - Interactive Microsoft Graph permission picker
- API Exposure Management - Configure and manage exposed APIs, scopes, and permissions for your applications
- Optional Claims Management - Add and manage optional claims for tokens to customize app authentication and authorization
- Claims Mapping Policies - Visual policy editor with template library
- Directory Extensions - Custom attribute creation and schema management
- Manifest Editor - Direct application manifest editing with validation

## 🔍 AppTesting - Read-Only Analysis Tool

### Comprehensive Testing Without Changes
- Authentication Flow Testing - Complete OAuth2/OIDC flow validation
- Token Analysis - Advanced JWT decoding and claims inspection
- Permission Analysis - Detailed API permission and risk assessment
- Configuration Review - Read-only access to all application settings
- Security Analysis - Comprehensive security posture evaluation

### Compliance-Ready Operation
- Zero Modification Risk - All configuration change functions disabled
- Policy Compliance - Designed for organizations requiring change control
- Safe Exploration - Explore configurations without modification capabilities

### Advanced Analysis Capabilities
- Conditional Access Insights - View applied policies and their impact
- Service Principal Analysis - Comprehensive service principal information
- Permission Risk Scoring - Automated risk assessment of application permissions

## 📊 AppDashboard - Tenant Analytics Tool

AppDashboard is a 100% read-only, client-side analytics tool that provides a single pane of glass into every app registration across the Entra ID tenant. No backend, no data storage, no write permissions required. All analysis runs in the browser using delegated Graph API access.

### Six Analytical Dashboards

#### 🏠 1. Tenant Overview
- **Health Scorecard** — At-risk apps, expired credentials, expiring ≤ 30 days, multi-tenant exposure, apps without owners
- **9 Metric Cards** — Total, SPA, Web Apps, API/Daemon, SAML, Single-Tenant, Multi-Tenant, With Secrets, With Certificates
- Searchable paginated app table with display name, App ID, type, audience, and credential counts
- Click any metric card to instantly filter the app list below
- One-click CSV export of the filtered app list

#### 🛡️ 2. Security Posture
- **Scoring Engine** — 0–100 score per app evaluating redirect URI hygiene, implicit flow, sign-in audience, and permission risk
- **Risk Tiers** — Critical, High, Medium, Low/Healthy
- 7 metric cards including No Owners and Implicit Grant detection
- Top 5 Critical Apps panel for immediate attention
- Per-app security report with every check as pass/fail, impact description, and recommendation
- CSV export of risk, score, issue count, and failed checks

#### 🎯 3. Attack Surface
- **Authentication** vectors — Insecure HTTP redirects, wildcard URIs, implicit flow, localhost in production
- **Credential** vectors — Broad sign-in audience, expired secrets, missing credentials on confidential apps
- **Privilege** vectors — Excessive permissions (> 20), SPA apps with application-level roles
- **Exposure** vectors — APIs without Identifier URI, preauthorized apps bypassing consent
- Severity levels: Critical, High, Medium, Low — with per-app vector detail dialog and CSV export

#### ⏱️ 4. Secrets & Expiry
- **Expiry Buckets** — Expired, ≤ 7 days, ≤ 30 days, ≤ 90 days, Healthy
- Smart filters — at-risk only (default), group by app, include service principal credentials
- Detailed table: Application, Source (App vs. SP), Type (Secret vs. Certificate), Status chip, Days Left, Expiry date
- Direct Azure Portal link per credential for quick remediation
- CSV export of all credential records

#### 📈 5. App Lifecycle
- **11 Metric Cards** — Total Apps, Avg Age, No Owners, Expired Secrets, Expiring ≤ 30d, Multi-Platform, API Integrations, API Providers, Healthy Secrets, Created (7d), Created (30d)
- **4 Visual Charts** — Age distribution, monthly creation trend, credential health bars, sign-in audience breakdown
- Per-app detail dialog with created date, age, type, owners, credentials, and redirect URIs
- CSV export

#### 🔑 6. Permission Inventory
- **Two View Modes** — By Permission (unique permissions across tenant) and By App (per-app permission profile)
- **Risk Classification** — Critical, High, Medium, Low per permission, powered by a built-in known-permissions catalog
- 6 summary metrics: Unique Permissions, Critical + High Risk, Application Perms, Delegated Perms, Apps With Permissions, Apps With High Risk
- Drill-down dialogs: per-permission description, risk chip, resource, and consuming apps
- Per-app: every permission as a color-coded chip
- Custom API grouping with Entra portal links for unknown resources
- CSV export adapts to current view mode

### Required Permissions

| Permission | Type | Purpose |
|---|---|---|
| `User.Read` | Delegated | Read signed-in user profile |
| `Application.Read.All` | Delegated | Read all app registrations (read-only) |
| `openid` | Delegated | OpenID Connect sign-in |
| `profile` | Delegated | User profile claims |
| `offline_access` | Delegated | Refresh tokens |

> No write permissions are requested or needed. AppDashboard is strictly read-only with all analysis running client-side in the browser.

## 📊 Reporting

### Reporting Capabilities
- Export Capabilities - CSV exports for security analysis, lifecycle tracking, and compliance
- Dashboard Integration - Embed metrics and reports in custom dashboards

### Security Reporting
- Attack Surface Reports - Detailed vulnerability assessment reports
- Permission Analysis Reports - Comprehensive API permission and risk reports

## 🎯 Specialized Use Cases

### Development Teams
- Development Environment Setup - Quick setup for dev/test environments
- Authentication Testing - Comprehensive flow testing and validation
- Integration Validation - Test API integrations without production impact
- Token Debugging - Advanced token analysis and troubleshooting

### IT Operations
- Application Portfolio Management - Centralized view and management of all applications
- Lifecycle Management - Track application creation, changes, and ownership
- Security Monitoring - Continuous security posture assessment

### Security Teams
- Security Assessment - Comprehensive security review of application configurations
- Attack Surface Analysis - Identify and evaluate potential security vulnerabilities
- Compliance Verification - Verify applications against security policies and standards
- Incident Response - Quick identification and analysis of security issues

### IT Managers & Tenant Administrators
- Tenant-Wide Security Visibility - AppDashboard provides full-tenant security posture at a glance
- Governance Reporting - Exportable CSV reports for compliance reviews and executive briefings
- Registration Inventory - Complete picture of every app registration, ownership status, and multi-tenant exposure
- Risk Prioritization - Top critical apps and risk-tiered summaries for actionable triage

### Support Teams
- Advanced Troubleshooting - Comprehensive tools for diagnosing authentication issues
- Configuration Analysis - Deep dive into application configurations
- Issue Resolution - Quick identification and resolution of common issues

## 📈 Performance & Scalability

### Optimized Performance
- Intelligent Caching - Smart caching strategies for improved performance
- Lazy Loading - On-demand loading of components and data
- Batch Operations - Efficient bulk operations for better performance

### Scalability Features
- Large Tenant Support - Optimized for organizations with hundreds of applications
- Efficient Data Loading - Optimized queries and data loading strategies
- Progressive Enhancement - Features load based on user permissions and needs
- Resource Management - Efficient resource utilization and memory management

---

## 🆕 Recent Enhancements

### AppDashboard - New Tenant Analytics Tool
- **Six Analytical Dashboards** — Tenant Overview, Security Posture, Attack Surface, Secrets & Expiry, App Lifecycle, and Permission Inventory
- **Security Scoring Engine** — 0–100 per-app scores with Critical/High/Medium/Low risk tiers
- **Attack Surface Mapping** — Authentication, Credential, Privilege, and Exposure vector categories
- **Credential Lifecycle Tracking** — Expiry buckets with direct Azure Portal remediation links
- **Permission Risk Catalog** — Built-in known-permissions database with risk classification
- **100% Read-Only & Client-Side** — Zero infrastructure, zero write permissions

### New Testing Capabilities
- **Confidential Client Auth Debugger** - Simplified web application testing with full Authorization Code Flow support, PKCE, custom API integration, and comprehensive token inspection; requires only redirect URI addition with automatic silent backup for easy restoration

### Dashboard Improvements
- Enhanced Portfolio View - Comprehensive application portfolio management
- Interactive Security Dashboard - Real-time security metrics with drill-down capabilities
- Advanced Filtering - Multi-criteria filtering with saved filter states
- Export Functions - Enhanced CSV export capabilities for reporting

### New Analysis Tools
- Attack Surface Analyzer - Comprehensive security vulnerability assessment
- Application Lifecycle Tracker - Application history and ownership tracking
- Permission Risk Analyzer - Advanced permission analysis with risk scoring

---

> 💡 Need Help? Contact our support team at support@AppConfig.app for assistance with any feature across the AppConfig² Suite.

> 🔄 Feature Updates This guide reflects the latest features in the AppConfig² Suite. New capabilities are added regularly based on user feedback and industry requirements.