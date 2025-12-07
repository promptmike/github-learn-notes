# License Usage Stats in Machine and Peripheral Devices

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

Machine accounts and peripheral services can impact license usage and security
> GitHub allows use through machine and peripheral devices, which can incur costs

Machine accounts are used for automation and peripheral services include CI/CD, API use and integrations
> Automations, CI/CD, API use and integrations can consume licenses

## Understanding Machine Accounts and Peripheral Services

### Machine Accounts

A machine account is a GitHub account used for automation, running scripts or using third-party tools
> GitHub allows machine accounts to act on behalf of users, but this consumes licenses

Machine accounts act independently of human users, and each one consumes a GitHub license just like a standard user
> GitHub licenses can be used by humans directly, or by machine accounts acting on behalf of humans

### Peripheral Services

Peripheral services are external integrations that interact with GitHub through API requests
> GitHub licenses can be consumed directly, or by deploying a machine account, while peripherals act through API requests

Peripheral services include CI/CD integrations like Actions, automated security like Dependabot and even self-hosted runners
> GitHub allows integration of peripherals through APIs and consumption of licenses by machine accounts for automation

You should track peripherals use to identify unused or redundant accounts and improve cost efficiency and security
> GitHub will bill you for overage of peripherals and licenses used by machine accounts, but also helps you track your spend and accounts

## Finding License Usage Statistics for Machine Accounts

### Method 1: GitHub Enterprise Admin Console

1. *Enterprise Settings*
2. *Billing & License Management*
3. Find *Machine Accounts* section
4. Review details

> Machine accounts consume licenses and integrations can incur billing, but GitHub helps you track your spend through the GUI

### Method 2: GraphQL API Query for Machine Accounts

```
{
  enterprise(slug: "enterprise-name") {
    organizations(first: 50) {
      nodes {
        name
        machineAccounts {
          totalCount
          nodes {
            login
            createdAt
            lastActiveAt
          }
        }
      }
    }
  }
}
```

> Machine accounts consume licenses and integrations can incur billing, but GitHub helps you track your spend through either GUI or GraphQL API

We should track machine accounts to identify inactive accounts and avoid unnecessary license consumption
> Machine accounts consume licenses to automate tasks and integrations overage can incur costs, so we should track usage through the GUI or GraphQL API

## Finding License Usage for Peripheral Services

### Method 1: GitHub Actions & Runners Usage Metrics

1. *Enterprise Settings* > *Actions*
2. Review Details

> Machine accounts use licenses, while integrations and runners incur billing, so we should track them through GUI or API

### Method 2: REST API for Self-Hosted Runners

**Track self-hosted runners**
```
curl -H "Authorization: token YOUR-TOKEN" \
"https://api.github.com/enterprises/YOUR-ENTERPRISE/actions/runners"
```

> Machine accounts, integrations and runners consume resources and increase bills, so we should track the through GUI or API

Runners consume licenses and idle runners waste resources, so we should track their usage carefully
> Machine accounts, integrations and runners can all waste resources if idle, so we should track their usage through GUI or API

### Method 3: Peripheral Services API Usage Tracking

**Monitor API integrations**
```
curl -H "Authorization: token YOUR-TOKEN" \
"https://api.github.com/enterprises/YOUR-ENTERPRISE/audit-log"
```

> Machine accounts, runners and peripherals can waste resources, so we should track their usage

Monitoring usage helps us identify waste and check that third-party services are configured properly
> Machine accounts, runners and peripherals require resource management and proper configuration

## Best Practices for Managing Machine Accounts & Peripheral Services Licenses

Unused machine accounts may still have privileged access, so they present a security risk if compromised
> Machine accounts, runners and peripherals can waste resources and present security risks if idle or improperly configured

Unused or unauthorised API use can lead to rate limits and present a security risk
> Machine accounts, runners and peripherals can waste resources, incur rate limits and produce security risks if idle or improperly configured

GitHub hosted runners are PAYG and incur billing while idle self-hosted runners waste computing resources and present a security risk
> Machine accounts, runners and peripherals can waste resources and present security risks if not properly configured, used and managed

Machine accounts can be a vector for privilege escalation, so they should never be given more permissions than necessary
> Machine accounts, runners and peripherals can waste resources or be compromised, so they should be properly managed, configured and kept in use or retired

Tracking license usage is critical for cost management, security and compliance
> Admins should track machine accounts, runners and peripherals with GitHub UI, GraphQL or REST, shut down idle accounts and enforce proper configuration
