
Microsoft Graph PowerShell wouldn't exist without Microsoft Graph. Microsoft Graph is a gateway to data and intelligence in Microsoft 365. It offers a single endpoint, `https://graph.microsoft.com`, to access rich, people-centric data and insights in the Microsoft cloud. The data and insights include Microsoft 365, Windows, and Enterprise Mobility + Security through REST APIs.
  
Microsoft Graph PowerShell is a Software Development Kit (SDK) that acts as an API wrapper for the Microsoft Graph APIs, exposing the entire API set for use in PowerShell. It contains cmdlets for all the Microsoft Graph APIs. Microsoft Graph PowerShell cmdlets and the reference documentation are autogenerated from the Microsoft Graph REST APIs.

## Packaging

Microsoft Graph PowerShell is packaged as the **Microsoft.Graph** and **Microsoft.Graph.Beta** modules in PowerShell gallery as the GA and beta root modules, respectively, with multiple child modules. Microsoft.Graph acts as a container for the other modules.

**Microsoft.Graph.Authentication** is the core module, which contains the following components:

- `Connect-MgGraph`: to sign in to Microsoft Graph
- `Invoke-MgGraphRequest`: to issue REST API requests for the Microsoft Graph API
- Commands to discover permissions and API-specific Graph commands in other modules

Other modules are made up of thousands of commands.

Commands are named like **{Verb}**-Mg **{Resource}** (a Graph API resource) for example, user,group, and application. For example, in the command `Get-MgUser`, **get** is the verb and **user** the resource.

To differentiate between v1.0 cmdlets and those in beta, the beta cmdlets are prefixed with **Beta**. For example, `Get-MgUser` is the v1.0 cmdlet and `Get-MgBetaUser` is the beta cmdlet.
