### 0.3.2 (January XX, 2013):
* FEATURE [#42025921](https://www.pivotaltracker.com/story/show/42025921), [#41570081](https://www.pivotaltracker.com/story/show/41570081): Refactor and enhance workflow and user interface for spawning Resources from Accessions
* FEATURE [#38629259](https://www.pivotaltracker.com/story/show/38629259): Deletion of accessions
* FEATURE [#40547867](https://www.pivotaltracker.com/story/show/40547867): Support storage of legacy record IDs in backend API requests to assist with migration
* FEATURE [#40662927](https://www.pivotaltracker.com/story/show/40662927): Add API-based support for parameters to add users to groups automatically on creation
* ENHANCEMENT [#41505445](https://www.pivotaltracker.com/story/show/41505445): Support automatic generation of Resource Component titles from Date statements
* BUG FIX [#42368327](https://www.pivotaltracker.com/story/show/42368327): Title should support text longer than 255 characters

### 0.3.1-1 (January 8, 2013):
* SECURITY FIX: Fix parameter parsing issue with Rails ([more info](https://groups.google.com/forum/#!topic/rubyonrails-security/61bkgvnSGTQ/discussion))
* FEATURE [#35869301](https://www.pivotaltracker.com/story/show/35869301): Add navigation between Resources and Accessions when linked
* FEATURE [#40160989](https://www.pivotaltracker.com/story/show/40160989): Control order of access points by dragging and dropping (0.3.0)
* FEATURE [#35063647](https://www.pivotaltracker.com/story/show/35063647): Accessions can be linked to Resources (0.3.0)
* FEATURE [#40160673](https://www.pivotaltracker.com/story/show/40160673): User management by application administrators (0.3.0)
* FEATURE [#36860209](https://www.pivotaltracker.com/story/show/36860209): Add "Publish?" boolean to external document (0.2.3-2)
* FEATURE [#40972827](https://www.pivotaltracker.com/story/show/40972827): Add rights statements to digital objects and their components (0.2.3-2)
* FEATURE [#35779245](https://www.pivotaltracker.com/story/show/35779245): Add standard identifier string to subject headings
* ENHANCEMENT [#40160785](https://www.pivotaltracker.com/story/show/40160785): Dates and Extents appear before Subjects in view and edit screens
* ENHANCEMENT [#39416499](https://www.pivotaltracker.com/story/show/39416499), [#39414337](https://www.pivotaltracker.com/story/show/39414337), [#39414051](https://www.pivotaltracker.com/story/show/39414051), [#39414695](https://www.pivotaltracker.com/story/show/39414695): Improve rights UI workflow
* BUG FIX [#41937667](https://www.pivotaltracker.com/story/show/41937667): Localized labels not appearing for agents that are corporate bodies
* BUG FIX [#41930209](https://www.pivotaltracker.com/story/show/41930209): Agent edit view displays only primary name in header
* BUG FIX [#41929859](https://www.pivotaltracker.com/story/show/41929859): Localized labels not loading in agent show view
* BUG FIX [#41430143](https://www.pivotaltracker.com/story/show/41430143): Fix validation requirements for source, rules, and authority identifiers in Agent records
* BUG FIX [#41484569](https://www.pivotaltracker.com/story/show/41484569): Make Location validation requirements clearer from a user perspective
* BUG FIX [#41485673](https://www.pivotaltracker.com/story/show/41485673): When assigning an Instance to a Location, browsing Locations shows an empty list 
* BUG FIX [#41438793](https://www.pivotaltracker.com/story/show/41438793): Description note field should be visually larger
* BUG FIX [#41429187](https://www.pivotaltracker.com/story/show/41429187): Change values/labels related to name order
* BUG FIX [#41493775](https://www.pivotaltracker.com/story/show/41493775): Change deaccession whole/part selection from boolean to drop down
* BUG FIX [#41439033](https://www.pivotaltracker.com/story/show/41439033): When linking a Subject to another record, the Browse popup does not display the available options
* BUG FIX [#41428105](https://www.pivotaltracker.com/story/show/41428105): Subject terms not appearing in correct order in headings
* BUG FIX [#41424139](https://www.pivotaltracker.com/story/show/41424139): Add edit button for existing subjects
* BUG FIX [#41426027](https://www.pivotaltracker.com/story/show/41426027): Trying to edit a previously created subject throws an application error
* BUG FIX [#41429359](https://www.pivotaltracker.com/story/show/41429359): Localized labels for Source and Rules in Agent Name Forms not displaying in edit view
* BUG FIX [#41440591](https://www.pivotaltracker.com/story/show/41440591): Dropdowns for creating Agents in a linking context (e.g. from an Accession) appear off the edge of the viewport
* BUG FIX [#41504625](https://www.pivotaltracker.com/story/show/41504625): Rights: Permissions and Restrictions should be TextFields, not Strings
* BUG FIX [#41439467](https://www.pivotaltracker.com/story/show/41439467): Accession browse list "identifier" column should display user-entered identifier instead of primary key
* BUG FIX [#41505151](https://www.pivotaltracker.com/story/show/41505151): Notes: labels should be optional 
* BUG FIX [#41505501](https://www.pivotaltracker.com/story/show/41505501): Barcode is optional for containers
* BUG FIX [#41527633](https://www.pivotaltracker.com/story/show/41527633): Dates: Show view should display date expression when collapsed 
* BUG FIX [#41509281](https://www.pivotaltracker.com/story/show/41509281): Digital Object save button reads "Save Resource" (0.3.0)
* BUG FIX [#41056439](https://www.pivotaltracker.com/story/show/41056439): Control jurisdiction values in rights records against ISO 3166 (0.2.3-2)
* BUG FIX [#41057509](https://www.pivotaltracker.com/story/show/41057509): Remove constraints on data values for accession/resource identifiers (0.2.3-2)
* BUG FIX [#41255933](https://www.pivotaltracker.com/story/show/41255933): Addition of "other_unmapped" value to controlled lists for migration testing (0.2.3-2)
* BUG FIX [#40823763](https://www.pivotaltracker.com/story/show/40823763): Remove constraints on data values for location coordinates (0.2.3-1)
* BUG FIX [#40979409](https://www.pivotaltracker.com/story/show/40979409): Resource component view not loading (0.2.3-1)
* BUG FIX [#40848483](https://www.pivotaltracker.com/story/show/40848483): Component level notes not appearing in menu or in view (0.2.3-1)

### 0.2.3 (December 7, 2012):
* FEATURE: Spawn new resource records from accession records
* FEATURE: Support for date expressions containing both date expressions and structured date information
* FEATURE: Select language of material for resources, digital objects, and their components from a controlled list
* FEATURE: Select a level of description for resources and resource components from a controlled list or specify "other level" with a user-specified level type
* FEATURE: Support for administrative and finding aid-related data on a top-level resource
* FEATURE: Support for notes on resource components, digital objects, and digital object components
* FEATURE: Basic support for import of EAD exported from Archon
* FEATURE: LDAP authentication
* FEATURE: Specify a custom configuration file or custom configuration options when starting the application 
* FEATURE: Allow administrators to create new users while logged in
* BUG FIX: Level should display for components in read only view
* KNOWN ISSUE: Containers and instances not importing properly from EAD

### 0.2.2 (November 26, 2012):
* FEATURE: Drag and drop hierarchy manipulation for resources and digital objects
* FEATURE: Keyboard-based hierarchy manipulation for resources and digital objects
* FEATURE: Support for mixed content/XML in notes fields
* FEATURE: Creation/editing of collection management subrecords (minimal implementation)
* FEATURE: Search support for resource, accession, and digital object records
* FEATURE: Support for custom locations of embedded database
* FEATURE: Basic support for import of EAD exported Archivists' Toolkit
* BUG FIX: Non-ASCII Unicode in Agent names not being saved/rendered correctly
* BUG FIX: Users should not need to enter a rights statement identifier

### 0.2.1 (November 13, 2012):

* FEATURE: Link agents to accessions, resources, digital objects, and their components as creators, sources, or subjects
* FEATURE: Suppression of accessions
* BUG FIX: Users should not enter a ref_id manually for a Resource Component
* BUG FIX: Users with appropriate permissions should be able to create a sibling  record to the Resource Component directly below a top level Resource
* BUG FIX: Top-level resource should not show extent records of subordinate component records

### 0.2.0-1 (October 29, 2012):
* FEATURE: Assignment of physical instances, containers, and locations to resources and resource components
* FEATURE: Creation/editing of deaccession records (minimal implementation)
* FEATURE: Creation/editing of digital objects (minimal implementation)
* FEATURE: Creation/editing of event records, including linking to agents and accessions, resources, and resource components
* FEATURE: Creation/editing of note subrecords linked to resources
* FEATURE: EAD export (basic implementation)
* FEATURE: Creation/editing of rights records in accessions, resources, and resource components
* BUG FIX: Resource component edit view link to External Documents section of form was broken
* BUG FIX: Table or column name too long for MySQL

### 0.1.3 (October 15, 2012):
* FEATURE: Create/edit rights management statements (linking to agents not yet implemented)
* FEATURE: Prevention of accidental overwriting of changes in progress in another session; fully implemented inc. UI in accessions; backend will prevent this in resources but will throw a fatal error
* FEATURE: EAD Import from within User Interface (basic implementation)
* FEATURE: EAD Import from command line (basic implementation)
* BUG FIX: Extent statements are optional for Accessions
* BUG FIX: When editing an existing Agent, saving an invalid record leads to an unhandled application error
* BUG FIX: Create subject view popup does not display input controls for term and type subdivisions when in Accessions
* BUG FIX: Only users that are in a member of a group with the “manage this repository” setting enabled should be able to access the groups controller and edit groups
* BUG FIX: Users with Repository Manager permissions cannot access groups configuration
* BUG FIX: Read only users should not be able to directly access views to create new or edit existing groups

### 0.1.2 (October 1, 2012):
* FEATURE: Declare source information for Agents (adding sources to list not yet implemented)
* FEATURE: Extent statements (including multiple extent statements) for accessions, resources, and resource components
* FEATURE: External documents
* FEATURE: Authorization: roles for repository manager, “archivist” (data entry), “viewer” (read only user); ability to define new roles
* FEATURE: Ability to develop custom importers
* BUG FIX: In Accessions, content description and condition description needs support field values of &gt; 255 characters
* BUG FIX: Title should be an optional property for Person Agent
* BUG FIX: Empty Contact Description property in an Agent record leads to error
* BUG FIX: Authority ID is an optional property for all Agents, and if used, then there must be a Name Source set for that name form

### 0.1.1 (September 17, 2012):
* FEATURE: Creation/editing of agents

### 0.1.0 (September 3, 2012):
* FEATURE: Creation/editing of resource records and resource component records
* FEATURE: Creation/editing of accessions
* FEATURE: Creation/editing of subjects
* FEATURE: Local authentication