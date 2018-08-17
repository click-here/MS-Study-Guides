Most of this is just direct quotes from documentation. Paraphrased some things.
Exam MB2-716

# Configure Microsoft Dynamics 365 (20% - 25%)

## Configure Microsoft Dynamics 365 settings

### Configure [Auditing](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/auditing-overview)

> ###### The following bullets identify some key auditing concepts:
> 
> * You can enable or disable auditing at the organization, entity, and attribute levels. If auditing is not enabled at the organization level, auditing of entities and attributes, even if it is enabled, does not occur. By default, auditing is enabled on all auditable entity attributes, but is disabled at the entity and organization level.
> 
> * For Dynamics 365 (on-premises) servers that use SQL Server Enterprise editions, auditing data is recorded over time (quarterly) in partitions. A partition is called an audit log in the Dynamics 365 web application. Partitions are not supported, and therefore, not used, on a Dynamics 365 (online) server that is running SQL Server, Standard edition.
> 
> * The ability to retrieve and display the audit history is restricted to users who have certain security privileges: View Audit History, and View Audit Summary. There are also privileges specific to partitions: View Audit Partitions, and Delete Audit Partitions. See the specific message request documentation for information about the required privileges for each message.
> 
> * Audited data changes are stored in records of the audit entity.
> 
> ###### Data that can be audited
> 1. Create, update, and delete operations on records.
> 
> 2. Changes to the shared privileges of a record.
> 
> 3. N:N association or disassociation of records.
> 
> 4. Changes to security roles.
> 
> 5. Audit changes at the entity, attribute, and organization level. For example, enabling audit on an entity.
> 
> 6. Deletion of audit logs.
> 
> 7. When (date/time) a user accesses Dynamics 365 data, for how long, and from what client.
> 
> 8. Enabling or disabling of field level security by setting the IsSecured attribute cannot be audited.
> 
### [Document management](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/configure-document-management), and collaboration

### Configure administration settings

### Perform data management tasks

#### [Duplicate Detection](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/detect-duplicate-data-for-developers)

#### [Bulk Delete Data](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/delete-data-bulk)

#### [Import data](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/import-data)

Beyond importing data via Excel upload you can do the following with Dynamics 365 web services
> Create data maps that include complex transformation mapping, such as concatenation, split, and replace.
> 
> * Define custom transformation mapping.
> 
> * View source data that is stored inside the temporary parse tables.
> 
> * Access error logs to build custom error reporting tools with improved error logging views.
> 
> * Run data import by using command-line scripts.
> 
> * Add LookupMapXML tags in the data map to indicate that the data lookup will be initiated and performed on a source file that is used in the import.
> 
> * Add custom OwnerMetadataXML tags in the data map to match the user records in the source file with the records of the user (system user) in Dynamics 365.
> 
> * Use optional validation checks.
> 

### Perform user management

### [Implement themes](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/customize-dev/query-and-edit-an-organization-theme)

Add a logo, change color pallette


## Manage Microsoft Dynamics 365 security

### Identify security roles

### Define permissions and privileges

### Configure access levels

### Configure security roles

### Assign security roles

### Implement multiple security roles, manage access,

### Implement the standard security model and hierarchy security,

### Configure business units,

### Manage teams

## Configure email services

### Identify integration options

### Configure email server profiles and default organization email settings

### Enable server-side email synchronization 

### Enable folder tracking 

### Map exchange folders 

### Set up and configure the CRM App for Outlook

## Integrate Microsoft Dynamics 365 with other Office 365 offerings

### Select the appropriate Office 365 group integration

### Create and configure Office 365 groups
 
### Integrate Microsoft Dynamics 365 and SharePoint

### Enable linking to OneNote files, set up and configure OneNote integration

### Configure OneDrive integration

# Implement Microsoft Dynamics 365 entities, entity relationships, and fields (20% - 25%)

## Manage Microsoft Dynamics 365 entities

### Manage [entity ownership](https://msdn.microsoft.com/en-us/library/gg309396.aspx#EntityOwnership)

>There are several types of entity ownership. Most entities, including custom entities, are owned by the organization, by a user, or a team. There are some business entities that do not have an owner, such as discount type (discount list), where the ownership is defined by its parent entity discount. The type of ownership defines some of the operations that can be performed on a record. Ownership for an entity is defined in the metadata property OwnershipType. The following table lists the ownership properties.

[read here](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/use-managed-properties#apply-managed-properties)

Good explanation [here](https://community.dynamics.com/crm/b/crmbusiness/archive/2014/12/02/crm-entity-ownership-how-do-you-decide)

|  Ownership Type | Description  |
|------|---|
|Organization Owned   | Contains data involving something that belongs to or that can be viewed by the whole organization. Organization-owned entities cannot be assigned or shared. For example, products are owned by the organization. These entities have an attribute named organizationid.  |
|Business Owned   | Entities that belong to a business unit. These entities have an attribute named owningbusinessunit.  |
|User or Team Owned   | Assigned to a user or to a team. These entities contain data that relates to customers, such as accounts or contacts. Security can be defined according to the business unit for the user or team. These entities have attributes named owningteam and owninguser.  |
|None | These entities are not owned by another entity. |




### Manage entity properties

I'm guessing they are talking about [this](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/use-managed-properties#apply-managed-properties) (preview below)


|Component|Display Name|Property|
|---|---|
|Entity|Can be customized|IsCustomizable. |
|Entity|Display name can be modified|IsRenameable. |
|Entity|Can be related entity in relationship|CanBeRelatedEntityInRelationship. |
|Entity|Can be primary entity in relationship|CanBePrimaryEntityInRelationship. |
|Entity|Can be in many-to-many relationship|CanBeInManyToMany. |
|Entity|New forms can be created|CanCreateForms. |
|Entity|New charts can be created|CanCreateCharts. |
|Entity|New views can be created|CanCreateViews. |
|Entity|Can change any other entity properties not represented by a managed property|CanModifyAdditionalSettings. |



### Configure system entities

### Describe activity entities

### Configure entity ownership and entity properties

### Implement managed properties

### Configure custom entities and security roles, delete entities

## Implement entity relationships

### Define relationship types

### Create relationships

### Configure cascading rules

### Identify types of cascading behavior

### Work with hierarchical data

### Configure entity mapping, create connections and connection roles

## Define and configure Microsoft Dynamics 365 fields

### Identify field types

### Define field naming requirements

### Configure field properties and field display formats

### Implement option sets and two option fields

### Configure lookup fields and customer fields

## Configure field customizations

### Configure fields

### Configure field properties

### Use calculated fields

### Use rollup fields

### Configure global option sets

### Create alternate keys

### Configure field security and security roles

### Use status and status reasons

### Identify status reason transitions

# Create and manage Microsoft Dynamics 365 solutions, forms, views, and visualizations (25% - 30%)

## Create and manage Microsoft Dynamics 365 solutions

### Recommend usage patterns for Microsoft Dynamics 365 solutions

### Identify solution components

### Identify solution types

### Create managed and unmanaged solutions

### Configure publishers and versions

### Manage multiple solutions

### Import and export solutions

#### [Managed Solution Updates](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/maintain-managed-solutions#create-managed-solution-updates)

1. New version
"Using your original unmanaged source solution... increase the version number of the solution before packaging it as a managed solution. When [you] install the new version, their capabilities will be upgraded to include your changes. If you want to go back to the behavior in a previous version, simply re-install the previous version. This overwrites any solution components with the definitions from the previous version but does not remove solution components added in the newer version. Those newer solution components remain in the system but have no effect because the older solution component definitions will not use them"

2. Update

"When only a small subset of solution components urgently requires a change you can release an update to address the issue. To release an update, create a new unmanaged solution and add any components from the original unmanaged source solution that you want to update. You must associate the new unmanaged solution with the same publisher record as was used for the original solution. After you finish with your changes, package the new solution as a managed solution.

When the update solution is installed in an organization where the original solution was installed the changes included in the update will be applied to the organization. If an organization needs to ‘roll back’ to the original version they can simply uninstall the update.

Any customizations applied to the solution components in the update will be overridden. When you uninstall the update they will return."
  
  
- Customize Microsoft Dynamics 365 forms
  - Identify Microsoft Dynamics 365 form types, build a form, use specialized form components, implement access teams and subgrids, create editable grids, work with navigation, use multiple forms
- Implement Microsoft Dynamics 365 views and visualizations
  - Identify view types; create, modify, manage, and delete views; customize views; create system and personal charts; identify chart types that can be combined; use available series aggregation types; customize charts; import and export charts; create dashboards and dashboard components; customize dashboards; control access to dashboards
- Configure Microsoft Dynamics 365 for mobile devices
  - Deploy the mobile client, identify available entities for the mobile client, configure mobile navigation, design mobile form layout, create custom controls, hide mobile form content, create multiple forms, create mobile views and activity lists

# Implement business rules, workflows, and business process flows (20% - 25%)

## Implement and manage business rules

### Determine when to use business rules

When you want to have simple Javascript-like form behavior.  But it can also be applied at the server level if you set the scope to "Entity". Entity scope restricts operations like Excel upload and SSIS update/create etc.

### Describe business rule scopes

"Entity" scope means that it runs server side and does not need the form for it to work. It&#39;s similar to the functionality of a workflow in this case.

"All Forms" scope means that it runs for all forms

### Identify actions that trigger business rules

When the related entities fields meet any of the user set parameters using the following options:
* Equals
* Does not equal
* Contains
* Does not contain
* Begins with 
* Does not begin with 
* Ends with 
* Does not end with 
* Does not contain data
* Contains data

### Configure business rules, conditions, and actions
Actions available are:
* Recommendation
* Lock/Unlock
* Show Error Message
* Set Field Value
* Set Default Value
* Set Business Required
* Set Visibility

## Implement and manage workflows, [dialogs](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/use-dialogs-guided-processes), and custom actions



### Implement workflows

### Identify workflow types

### Implement dialogs and custom actions

#### Dialogs

### Identify when to use business process flows

### Workflow dialogs, and custom actions

## Implement and manage business process flows

### Identify business flow components

### Enable business process flows

### Implement steps, stages, and categories

### Implement flows that use multiple entities; use conditional branching

### Implement role-driven business process flows; run workflows