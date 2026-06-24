

<p align="center">
  <img src="images/ad-image.png" alt="Active Directory Banner" width="700">
</p>

<p align="center">
Windows Server 2022 | Active Directory | DNS | Group Policy | Identity & Access Management | RBAC | SMB File Sharing | Windows 11
</p>

---







# Enterprise Active Directory Administration & Identity Management Lab

## Project Overview

This project simulates a real-world enterprise Active Directory environment using Windows Server 2022 and Windows 11.

The lab demonstrates how organizations manage users, computers, security groups, organizational units, Group Policy, DNS, authentication, access control, and secure file sharing within a centralized domain environment.

The environment was designed to replicate common responsibilities performed by IT Support Engineers, System Administrators, and Identity & Access Management teams.

---

## Environment

| Component | Technology |
|------------|------------|
| Domain Controller | Windows Server 2022 |
| Client Device | Windows 11 |
| Directory Service | Active Directory Domain Services |
| DNS | Microsoft DNS |
| Identity Management | Active Directory |
| Group Management | Security Groups |
| Policy Management | Group Policy |
| File Services | SMB File Sharing |

---

## Skills Demonstrated

- Active Directory Administration
- User Account Management
- Organizational Unit Management
- Security Group Administration
- Domain Join Operations
- DNS Configuration
- Group Policy Management
- Identity & Access Management
- Authentication Troubleshooting
- Windows Server Administration
- Network Drive Mapping
- File Share Permissions
- Access Control Management

---

## Project Implementation

The project was completed in the following phases:

1. Windows Server Installation
2. Active Directory Deployment
3. DNS Configuration
4. Domain Creation
5. Windows 11 Domain Join
6. User & Group Management
7. Organizational Unit Administration
8. Secure File Sharing
9. Access Control Testing
10. Group Policy Configuration

---

## Verification & Evidence

The screenshots contained within the Images folder provide evidence of:

- Active Directory deployment
- Domain controller configuration
- DNS configuration
- Domain join operations
- User creation
- Group creation
- Organizational Units
- File share permissions
- Network drive mapping
- Group Policy implementation
- Authentication and access control testing

---


## Active Directory Deployment

### Objective

The objective of this phase was to deploy Active Directory Domain Services (AD DS), create a new enterprise domain, and establish the foundation for centralized identity and access management.

### Active Directory Installation

Active Directory Domain Services (AD DS) was installed on Windows Server 2022 using Server Manager. This role enables the server to function as a Domain Controller and provides centralized management of users, computers, groups, and authentication.

![AD DS Installation](images/01-server-installation-setup.png)

![AD DS Role Installation](images/02-adds-role-installation.png)

### Domain Controller Promotion

After the AD DS role was installed, the server was promoted to a Domain Controller. A new Active Directory forest was created and configured as the primary identity management platform for the environment.

![Domain Controller Promotion](images/03-domain-controller-promotion-ready.png)

### Active Directory Administrative Tools

Following promotion, Active Directory Users and Computers became available, providing a central location for managing domain objects including users, groups, and organizational units.

![Active Directory Users and Computers](images/04-open-active-directory-users-and-computers.png)

### Domain Structure Creation

A structured Active Directory environment was created to reflect a typical enterprise deployment. Organizational Units (OUs) were used to separate departments and simplify administration.

![Initial Domain Structure](images/05-initial-domain-structure.png)

### Organizational Unit Administration

Dedicated Organizational Units were created to represent business departments and provide logical separation of users, computers, and policies.

![Create Organizational Unit](images/06-create-organizational-unit.png)

### Security Group Management

Security groups were created to simplify permission assignment and access management. This approach follows enterprise best practices by assigning permissions to groups rather than individual users.

![Security Group Creation](images/07-groups-ou-creation.png)

### User Account Administration

User accounts were created within Active Directory and organized into the appropriate departments.

![Organized User Accounts](images/08-organize-default-accounts.png)

![Create User Account](images/09-create-user-account.png)

![User Account Details](images/10-user-account-details.png)

![User Accounts Created](images/11-user-accounts-created.png)

### Outcome

At the completion of this phase, the environment contained:

- Operational Active Directory Domain Services
- Functional Domain Controller
- Enterprise domain structure
- Organizational Units
- Security Groups
- Managed User Accounts

This provided the foundation for DNS configuration, domain joining, access control, Group Policy deployment, and file sharing.









## DNS Configuration & Windows 11 Domain Join

### Objective

The objective of this phase was to configure network connectivity, verify DNS functionality, and join a Windows 11 workstation to the Active Directory domain.

### Connectivity Verification

Before joining the domain, communication between the Domain Controller and Windows 11 client was verified to ensure both systems could communicate successfully across the network.

![Domain Connectivity Verification](images/12-domain-connectivity-verification.png)

![Client Server Ping Test](images/13-client-server-ping-test.png)

### Domain Controller Network Configuration

A static IP address was configured on the Domain Controller to provide a reliable DNS and authentication service for domain clients.

![Domain Controller Static IP](images/14-domain-controller-static-ip.png)

![Domain Controller Network Verification](images/15-domain-controller-network-verification.png)

### DNS Configuration

The Windows 11 client was configured to use the Domain Controller as its primary DNS server. This is a critical requirement for successful Active Directory domain joins.

![Client DNS Configuration](images/16-client-dns-domain-controller.png)

### Client Network Verification

Additional testing was performed to verify that the client device could successfully communicate with the Domain Controller and resolve domain resources.

![Client Network Verification](images/17-client-network-verification.png)

### Domain Join Process

The Windows 11 workstation was joined to the Active Directory domain through System Properties.

![Domain Join Wizard](images/18-domain-join-wizard.png)

![Domain Name Entry](images/19-domain-name-entry.png)

### Domain Join Verification

The domain join was authenticated using domain administrator credentials and verified successfully.

![Domain Join Verification](images/20-domain-join-verification.png)

![Domain Join Credentials](images/21-domain-join-credentials.png)

### Active Directory Computer Object

Following the successful domain join, the Windows 11 workstation automatically appeared within Active Directory as a managed computer object.

![Computer Object Created](images/24-computer-object-created.png)

### Authentication Testing

User authentication was tested to confirm successful communication between the client device and the Domain Controller.

![User Account Properties](images/22-user-account-properties.png)

![Domain User Sign In](images/23-domain-user-sign-in.png)

![Domain User Verification](images/25-domain-user-verification.png)

### Outcome

At the completion of this phase:

- DNS resolution was functioning correctly
- The Windows 11 workstation successfully joined the domain
- Authentication between client and Domain Controller was verified
- Active Directory automatically created and managed the computer account
- The environment was ready for organizational unit administration, access control, and file sharing







## Identity & Access Management

### Objective

The objective of this phase was to implement a structured identity management model using Organizational Units (OUs), user administration, and security groups.

This approach reflects how enterprise organizations separate departments, manage identities, and control access through centralized Active Directory administration.

### Organizational Unit Administration

To improve management and scalability, dedicated Organizational Units (OUs) were created for different business departments.

This structure allows administrators to organize users, apply Group Policies, and delegate administration more effectively.

![Create Organizational Unit](images/26-create-organizational-unit.png)

![Organizational Units Created](images/27-organizational-units-created.png)

### User Organization

Users were moved from the default containers into their respective departmental OUs.

This creates a cleaner directory structure and aligns user accounts with business functions.

![Move User to OU](images/28-move-user-to-ou.png)

### Departmental Structure

Separate OUs were maintained for Engineering, Management, and IT departments.

This structure provides a foundation for applying department-specific permissions and policies.

#### Engineering Department

![Engineering OU Users](images/29-engineering-ou-users.png)

#### Management Department

![Management OU Users](images/30-management-ou-users.png)

#### IT Department

![IT OU Users](images/31-it-ou-users.png)

### Security Group Administration

Security Groups were created to simplify access management and support Role-Based Access Control (RBAC).

Instead of assigning permissions directly to users, permissions are assigned to groups and users inherit access through membership.

![Create Security Group](images/32-create-security-group.png)

![Engineering Security Group Created](images/33-engineering-share-group-created.png)

### Group Membership Management

Users were assigned to the appropriate departmental security groups to control access to shared resources.

This follows enterprise best practices and simplifies future administration.

![Engineering Group Membership](images/34-engineering-group-membership.png)

### Access Control Validation

Testing was performed to verify that users received the correct permissions through their assigned groups.

This confirmed that the security model was functioning as intended before file-sharing resources were deployed.

![Cross Department Access Test](images/35-cross-department-access-test.png)

### Outcome

At the completion of this phase:

- Departmental Organizational Units were created
- Users were organized by business function
- Security Groups were implemented
- Group membership was assigned and validated
- Role-Based Access Control principles were established
- The environment was prepared for secure file sharing and permission management






## Secure File Sharing & Access Control

### Objective

The objective of this phase was to implement secure file sharing within the domain environment and control access using Active Directory Security Groups.

This approach reflects how enterprise organizations manage shared resources while enforcing the principle of least privilege.

### Shared Folder Creation

A dedicated departmental file share was created for the Engineering department using Windows Server file services.

The share was configured to provide centralized access to departmental resources.

![Open Share Wizard](images/36-open-share-wizard.png)

![Create Engineering Share](images/37-create-engineering-share.png)

![Configure Share Details](images/38-configure-share-details.png)

### Permission Configuration

Both Share Permissions and NTFS Permissions were configured to control access to the resource.

Security Groups were used instead of individual user permissions to simplify administration and improve scalability.

![Configure NTFS Permissions](images/39-configure-ntfs-permissions.png)

![Assign Security Permissions](images/40-assign-security-permissions.png)

### Share Deployment

After permissions were configured, the Engineering department share was successfully created and published.

![Engineering Share Created](images/41-engineering-share-created.png)

### Authentication Testing

User authentication was verified to ensure that access requests were being processed through Active Directory.

![Domain User Authentication Test](images/42-domain-user-authentication-test.png)

### Client Access Verification

The Engineering share was accessed from a domain-joined Windows 11 workstation to verify connectivity and permissions.

![Accessing Share From Client](images/43-accessing-share-from-client.png)

![Engineering Share Visible](images/44-engineering-share-visible.png)

### Network Drive Mapping

The shared folder was mapped as a network drive on the client workstation.

This provides users with persistent access to departmental resources through File Explorer.

![Map Network Drive](images/45-map-network-drive.png)

![Engineering Share Mapped Drive](images/46-engineering-share-mapped-drive.png)

### Access Control Validation

To validate the effectiveness of the access control model, a separate Active Directory user account (Anthony Prince) was used to test access to the Engineering department file share.

The account successfully authenticated to the domain but was not assigned membership within the EngineeringShare security group.

![Anthony Domain User Login](images/47-anthony-domain-user-login.png)

### Unauthorized Access Testing

An attempt was made to access the Engineering department file share using the Anthony Prince account.

Although the user was successfully authenticated by Active Directory, access to the shared resource was denied because the account was not a member of the EngineeringShare security group.

This confirmed that Role-Based Access Control (RBAC) and Identity & Access Management (IAM) controls were functioning correctly by enforcing permissions through group membership rather than individual user accounts.

![Unauthorized Access Denied](images/48-unauthorised-access-denied.png)

### Outcome

At the completion of this phase:

- Departmental file shares were deployed
- Share and NTFS permissions were configured
- Security Group-based access control was implemented
- Client access was successfully verified
- Network drive mapping was completed
- Unauthorized access attempts were blocked
- Enterprise access control principles were enforced





## Group Policy Administration

### Objective

The objective of this phase was to demonstrate centralized desktop management using Group Policy Objects (GPOs).

Group Policy enables administrators to apply standardized configurations and security settings across users and computers within an Active Directory environment.

### Group Policy Creation

A new Group Policy Object named **LockDesktop** was created to manage user desktop settings within the Engineering department.

The policy was linked to the Engineering Organizational Unit, ensuring that only users within that department would receive the configuration.

![Create LockDesktop GPO](images/49-create-lockdesktop-gpo.png)

### Group Policy Deployment

The newly created policy was linked to the Engineering Organizational Unit alongside existing departmental policies.

This demonstrates how administrators can target specific departments without affecting the entire domain.

![GPO Linked To Engineering OU](images/50-gpo-linked-to-engineering-ou.png)

### Desktop Configuration Management

A desktop restriction policy was configured to prevent Engineering users from changing their assigned desktop background.

This helps maintain a consistent user experience and supports organizational desktop standards.

![Prevent Wallpaper Changes Policy](images/51-prevent-wallpaper-changes-policy.png)

### Outcome

At the completion of this phase:

- Group Policy Objects were created and managed
- Policies were linked to Organizational Units
- Department-specific configurations were implemented
- Centralized desktop management was demonstrated
- Enterprise administration practices were applied


## Project Outcomes

This project demonstrates the deployment and administration of a centralized Active Directory environment using Windows Server 2022 and Windows 11.

The environment includes:

- Active Directory Domain Services (AD DS)
- DNS Configuration
- Organizational Unit (OU) Administration
- User and Group Management
- Role-Based Access Control (RBAC)
- SMB File Sharing
- NTFS Permissions
- Group Policy Management
- Domain Authentication
- Endpoint Integration

The completed lab demonstrates how enterprise organizations manage identities, control access to resources, enforce security policies, and administer Windows-based environments through centralized directory services.