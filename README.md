# Orca

Internal tooling and utilities for the webbexpert tenant.

## Tools

### Graph API File Explorer

`graph-explorer/index.html`

A zero-install, single-file React app for browsing OneDrive files via the Microsoft Graph API. Opens directly in any browser — no build step needed.

**Features**
- OAuth 2.0 popup login with your Microsoft 365 account
- OneDrive folder navigation with breadcrumbs
- Live search across your entire drive
- File open links (opens in Microsoft 365 online)
- Configurable app registration (Client ID / Tenant ID)

**Usage**

1. Open `graph-explorer/index.html` in a browser
2. Click **Sign in with Microsoft** and authenticate with your webbexpert credentials
3. Browse, navigate folders, or search files

The app uses Microsoft's [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer) public client ID by default, so no app registration is required to get started.

**Custom App Registration**

To use your own Azure AD app registration, expand the **App Registration Settings** panel and enter your:
- **Client ID** — found in Azure AD → App registrations → your app → Application (client) ID
- **Tenant ID** — your tenant ID or domain, or `common` for multi-tenant

Add the redirect URI shown in the panel to your app registration under **Authentication → Single-page application**.

Required delegated permissions: `Files.Read`, `Files.ReadWrite`, `Sites.Read.All`, `User.Read`
