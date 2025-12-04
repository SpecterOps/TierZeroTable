# TierZeroTable
Table of AD and Azure assets and whether they belong to Tier Zero.

View the table here: [https://specterops.github.io/TierZeroTable](https://specterops.github.io/TierZeroTable/)

Blog posts: 
  - [What is Tier Zero - Part 1](https://posts.specterops.io/what-is-tier-zero-part-1-e0da9b7cdfca)
  - [What is Tier Zero - Part 2](https://posts.specterops.io/what-is-tier-zero-part-2-6e1d14fddcaf)

Webinars:
  - [Defining the Undefined: What is Tier Zero](https://www.youtube.com/watch?v=5Ho83R9Jy68)
  - [Defining the Undefined: What is Tier Zero Part II](https://www.youtube.com/watch?v=SAI3mXQgy_I)
  - [Defining the Undefined: What is Tier Zero Part III](https://www.youtube.com/watch?v=ykrse1rsvy4)
  - [Defining the Undefined: What is Tier Zero Part IV](https://ghst.ly/4eSssxL)

**DISCLAIMER: The table does not include all Tier Zero assets yet.** We will add assets to the table throughout the webinar series. So if you think we are missing something, then you are completely right. But feel free to make a pull request or open an issue with the asset you think we should add. All contributions are appreciated. Also if you disagree on something in the table :)

# Complementary Projects

While TierZeroTable aims to provide a comprehensive list of AD and Azure assets classified as Tier Zero, there are other community-driven projects focused on tiered administration with deeper coverage of Azure. These may complement or extend your use of this repository:

 - [AzTier](https://aztier.com/) by [Emilien Socchi](https://github.com/emiliensocchi) — A project to browse a tiered view of Azure/Entra/Microsoft Graph administrative assets based on known attack paths.
 - [EntraOps](https://www.cloud-architekt.net/entraops/) by [Thomas Naunheim](https://github.com/Cloud-Architekt) — A PowerShell-based solution for classifying and managing privileged identities in Entra ID using the Enterprise Access Model (EAM), with support for automation, historical tracking, and integration with logging / detection systems.

# Table columns

### Name
Common name of the asset.

### Type
Type of the asset.

Values:
- AD computer
- AD container
- AD group
- AD object
- AD OU
- AD user
- Computer host
- DC group
- Entra ID role

### IdP
Identity Provider of the asset.

Values:
- Active Directory
- Entra ID

### Identification
How the asset can be identified. E.g., SID of AD object.

### Description
Description of the asset, i.e., its purpose of existence. This will be copied from Microsoft documentation if available.

### Compromise by default
Whether a publicly known abuse technique exists that allows compromise of Tier Zero assets using this asset. The abuse technique must work in an environment with default configurations.

If a publicly known abuse technique exists it will be described in the _Reasoning_ column and links will be provided in the _External links_ column.

Values:
- YES - Takeover - A publicly known abuse technique to takeover one or more Tier Zero assets exists and works in environments with default configurations.
- YES - Disruption - A publicly known abuse technique to disrupt the operations of Tier Zero assets exists and works in environments with default configurations.
- NO - No publicly known abuse technique to compromise Tier Zero assets in an environment with default configurations exists.
- IT DEPENDS - A publicly known abuse technique to takeover or disrupt Tier Zero exists and works in some configurations.

### Compromise by configuration
Whether a publicly known abuse technique exists that allows compromise of Tier Zero assets using this asset, which is enabled do to a common non-default (mis)configuration.

If a publicly known abuse technique exists it will be described in the _Reasoning_ column and links will be provided in the _External links_ column.

Values:
- YES - Takeover - A publicly known abuse technique to takeover one or more Tier Zero assets exists and works in environments with a common non-default (mis)configuration.
- YES - Disruption - A publicly known abuse technique to disrupt the operations of Tier Zero assets exists and works in environments with a common non-default (mis)configuration.
- NO - No publicly known abuse technique to compromise Tier Zero assets in an environment with common non-default (mis)configurations exists.
- N/A - Compromise by default - A publicly known abuse technique to compromise Tier Zero assets exists and works in environments with default configurations, hence it does not require any special configuration.

### Is Tier Zero
If the asset should be considered Tier Zero based on our [Definition of Tier Zero](https://github.com/SpecterOps/TierZeroTable/tree/main#definition-of-tier-zero).

Values:
- YES
- NO
- IT DEPENDS - If the asset is Tier Zero in some legitimate configuration but not always.

### Reasoning
The explanation of why the asset is or is not Tier Zero, including an abuse summary and if the asset is a security dependency for Tier Zero.

### Cypher query
Cypher query to return the node representing the asset in [BloodHound](https://github.com/specterOps/BloodHound).

### Privileged access security role
Whether the asset is included in Microsoft's [Privileged access security roles](https://learn.microsoft.com/en-us/security/privileged-access-workstations/privileged-access-security-levels#privileged) list, or has a "PRIVILEGED" label if an Entra ID role. 

Values:
- YES
- NO

### AdminSDHolder protected
Whether the asset is part of the default [Protected Accounts and Groups in Active Directory](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/appendix-c--protected-accounts-and-groups-in-active-directory), which are protected with the AdminSDHolder security descriptor.

Values:
- YES
- NO
- N/A - The asset cannot be protected by AdminSDHolder.

### What is Tier Zero episode
In which episode of the _What is Tier Zero_ series was this asset discussed.

Values:
- 1
- 2
- 3
- 4
- Community contribution

### External links
Links to documentation for the asset, abuse information, etc.
