# TierZeroTable
Table of AD and Azure assets and whether they belong to Tier Zero.

View the table here: [https://specterops.github.io/TierZeroTable](https://specterops.github.io/TierZeroTable/)

Blog posts: 
  - [What is Tier Zero - Part 1](https://posts.specterops.io/what-is-tier-zero-part-1-e0da9b7cdfca)
  - [What is Tier Zero - Part 2](https://posts.specterops.io/what-is-tier-zero-part-2-6e1d14fddcaf)

Webinars:
  - [Defining the Undefined: What is Tier Zero](https://www.youtube.com/watch?v=5Ho83R9Jy68)
  - [Defining the Undefined: What is Tier Zero Part II](https://www.youtube.com/watch?v=SAI3mXQgy_I)

**DISCLAIMER: The table does not include all Tier Zero assets yet.** We will add assets to the table throughout the webinar series. So if you think we are missing something, then you are completely right. But feel free to make a pull request or open an issue with the asset you think we should add. All contributions are appreciated. Also if you disagree on something in the table :)

# Table columns

### Name
Common name of the asset.

### Type
Type of the asset.

Values:
- AD computer
- AD container
- AD domain
- AD GPO 
- AD group
- AD user
- Computer host
- DC group

### IdP
Identity Provider of the asset.

Values:
- Active Directory

### Identification
How the asset can be identified. E.g., SID of AD object.

### Description
Description of the asset, i.e., its purpose of existence. This will be copied from Microsoft documentation if available.

### Known Tier Zero compromise by default configuration
Whether a publicly known abuse technique exists that allows compromise of Tier Zero assets using this asset. The abuse technique must work in an environment with default configurations.

If a publicly known abuse technique exists it will be described in the _Reasoning_ column and links will be provided in the _External links_ column.

Values:
- YES - Takeover - A publicly known abuse technique to takeover one or more Tier Zero assets exists and works in environments with default configurations.
- YES - Disruption - A publicly known abuse technique to disrupt the operations of Tier Zero assets exists and works in environments with default configurations.
- NO - No publicly known abuse technique to compromise Tier Zero assets in an environment with default configurations exists.

### Known Tier Zero compromise by common (mis)configuration
Whether a publicly known abuse technique exists that allows compromise of Tier Zero assets using this asset, which is enabled do to a common non-default (mis)configuration.

If a publicly known abuse technique exists it will be described in the _Reasoning_ column and links will be provided in the _External links_ column.

Values:
- YES - Takeover - A publicly known abuse technique to takeover one or more Tier Zero assets exists and works in environments with a common non-default (mis)configuration.
- YES - Disruption - A publicly known abuse technique to disrupt the operations of Tier Zero assets exists and works in environments with a common non-default (mis)configuration.
- NO - No publicly known abuse technique to compromise Tier Zero assets in an environment with common non-default (mis)configurations exists.
- N/A - Compromise by default - A publicly known abuse technique to compromise Tier Zero assets exists and works in environments with default configurations, hence it does not require any special configuration.

### Is Tier Zero
If the asset should be considered Tier Zero based on our [Definition of Tier Zero](https://github.com/SpecterOps/TierZeroTable/tree/main#definition-of-tier-zero).

### Reasoning
The explanation of why the asset is/isn't Tier Zero, including an abuse summary and if the asset is a security dependency for Tier Zero.

### Microsoft: Privileged access security roles
Whether the asset is included in Microsoft's [Privileged access security roles](https://learn.microsoft.com/en-us/security/privileged-access-workstations/privileged-access-security-levels) list.

Values:
- YES
- NO

### AdminSDHolder protected
Whether the asset is part of the default [Protected Accounts and Groups in Active Directory](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/appendix-c--protected-accounts-and-groups-in-active-directory), which are protected with the AdminSDHolder security descriptor.

Values:
- YES
- NO
- Not applicable

### What is Tier Zero episode
In which episode of the _What is Tier Zero_ series was this asset discussed.

Values:
- 1
- 2
- Community contribution

### External links
Links to documentation for the asset, abuse information, etc.
