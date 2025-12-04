# License Usage Stats

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We will learn to manage GitHub Enterprise licenses for accounts and server instances
GitHub Enterprise licenses can be tracked and managed by admins

There are several ways to track seat usage
GitHub Enterprise is billed by seat usage which you can track

**==Note==**
For prepaid (subscription-based) plans, you see a set number of available licenses. For Pay-As-You-Go (PAYG) plans—the default for new Enterprise customers—there’s no concept of “available licenses.” Billing is based on actual usage (active seats), and you’re charged each month according to that usage.

## Method 1: Find license usage for a specific organization

1. Navigate to GHEC Admin Panel
2. *Settings* > *Billing & plans*
3. *License usage* section
4. Review details

**GraphQL API alternative**
```
{
  organization(login: "org-name") {
    billingInfo {
      totalSeats
      seatsUsed
      seatsAvailable
    }
  }
}
```

You can track license usage using the Admin Panel or the GraphQL API

## Method 2: Find license usage across multiple organizations

1. Navigate to GHEC > *Enterprise settings*
2. *Billing* > *License Usage*
3. Review details for each organization

**GraphQL API alternative**
```
{
  enterprise(slug: "enterprise-name") {
    organizations(first: 50) {
      nodes {
        name
        billingInfo {
          totalSeats
          seatsUsed
          seatsAvailable
        }
      }
    }
  }
}
```

You can track license usage for a specific organization or multiple organizations from the GUI or GraphQL API

## Method 3: Find license usage for enterprise accounts

1. Navigate to GHES Admin Console
2. *Settings* > *License Usage*
3. Review details

**REST API alternative**
```
curl -H "Authorization: token YOUR-TOKEN" \
"https://api.github.com/enterprises/YOUR-ENTERPRISE/license"
```

You can track license usage for Enterprise Cloud using the GUI or GraphQL API, and Enterprise Server using the GUI or REST API

## Method 4: Find license usage across multiple GitHub instances

1. Access GHES Admin Settings
2. Use Metrics API:
    ```
    curl -H "Authorization: token YOUR-TOKEN" \
    "https://api.github.com/enterprise/settings/licenses"
    ```
3. Review details

You can track license usage for GHEC using the GUI or GraphQL API, for GHES using the GUI or REST API and multiple server instances using Metrics API

## Best practices for license usage management

Automate monitoring with APIs, reclaim unused seats, enable usage-based billing and audit regularly
GitHub Enterprise admins should monitor usage with GraphQL, REST and Metrics APIs, enable usage-based billing, audit monthly, reclaim unused seats and allocate resources effectively
