* 0.2.1 ()

* 0.2.0 (October 29, 2012):
    * FEATURE: Assignment of physical instances, containers, and locations to resources and resource components
    * FEATURE: Creation/editing of deaccession records (minimal implementation)
    * FEATURE: Creation/editing of digital objects (minimal implementation)
    * FEATURE: Creation/editing of event records, including linking to agents and accessions, resources, and resource components
    * FEATURE: Creation/editing of note subrecorts linked to resources
    * FEATURE: EAD export (basic implementation)
    * FEATURE: Creation/editing of rights records in accessions, resources, and resource components
    * BUG FIX: Resource component edit view link to External Documents section of form was broken

* 0.1.3 (October 15, 2012):
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

* 0.1.2 (October 1, 2012):
    * FEATURE: Declare source information for Agents (adding sources to list not yet implemented)
    * FEATURE: Extent statements (including multiple extent statements) for accessions, resources, and resource components
    * FEATURE: External documents
    * FEATURE: Authorization: roles for repository manager, “archivist” (data entry), “viewer” (read only user); ability to define new roles
    * FEATURE: Ability to develop custom importers
    * BUG FIX: In Accessions, content description and condition description needs support field values of &gt; 255 characters
    * BUG FIX: Title should be an optional property for Person Agent
    * BUG FIX: Empty Contact Description property in an Agent record leads to error
    * BUG FIX: Authority ID is an optional property for all Agents, and if used, then there must be a Name Source set for that name form

* 0.1.1 (September 17, 2012):
    * FEATURE: Creation/editing of agents

* 0.1.0 (September 3, 2012):
    * FEATURE: Creation/editing of resource records and resource component records
    * FEATURE: Creation/editing of accessions
    * FEATURE: Creation/editing of subjects
    * FEATURE: Local authentication