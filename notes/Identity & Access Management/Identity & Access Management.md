# Cloud IAM

Defines **who**(<span class="green">identity</span>) and **what** (<span class="orange">role</span>) for **which** ***resource***

Based on **least privilege principle**: meaning default deny

IAM policy: binds identity to roles which contains permissions. Member is assocated to a role and inherits all the privileges

## Identity

Associated with users or members accessing to resources. Is based on:
- Google account
- service account
- google group
- Gsuite domain
- Cloud Identity domain

Has implicit aliases:
- allAuthenticatedUsers
- allUsers

## Permissions
Determine the operations performed on a resource.
Corresponds to REST api: the're a **mapping** to REST APIs exposed by GCP resources
Can't be assigned directly to members/users, instead are grouped to a role

## Roles
### Primitives
1. Owner
2. Editor
3. Viewer

### Predefined
related to GCP services
They're assigned to every resource or service

### Custom roles
Collection of assorted set of permissions
Provides very fine-grades access to resources

## Service Accounts
Special Google account that belongs to an application or VM
ex the app programmatically creates resources: it needs permissions to do that

Identified by unique email address + a **token** that associates the resource with the rest of GPC services

There are 2 types:
- User managed
- Google managed

Each one is associated with one or more roles

## Where you use IAM?
When sharing GCP resources with fine-grained control
Selectively allow/deny permissions to individual resources
Define custom reoles specific to a team 
Enable authentication of applications trough service accounts