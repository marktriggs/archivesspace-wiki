### 0.5.3 (June 7, 2013):

* FEATURE [#49569691](https://www.pivotaltracker.com/story/show/49569691): Public interface: Display all components of Resources with ability to collapse and expand them 
* FEATURE [#47584019](https://www.pivotaltracker.com/story/show/47584019): Display additional information in Resource/Digital Object tree view (e.g. instance and container information)
* FEATURE [#43561173](https://www.pivotaltracker.com/story/show/43561173): Locations: add batch add functionality
* FEATURE [#45367639](https://www.pivotaltracker.com/story/show/45367639): Revised Digital Object CSV import mapping
* FEATURE [#48217179](https://www.pivotaltracker.com/story/show/48217179): Autocomplete "combobox" for long dropdown lists (e.g. language)
* FEATURE [#45076989](https://www.pivotaltracker.com/story/show/45076989): Add Date subrecords to Agents as "dates of existence" and add Date subrecords to Name subrecords as "use dates" (for EAC-CPF/ISAAR(CPF) compliance)
* FEATURE [#42024799](https://www.pivotaltracker.com/story/show/42024799): Capture and display audit information for all records (creation and modification date; user who created and last modified the record)
* FEATURE [#47182143](https://www.pivotaltracker.com/story/show/47182143), [#49084609](https://www.pivotaltracker.com/story/show/49084609): EAD import: improve handling of components that have `@level` set to `otherlevel`
* FEATURE [#50619287](https://www.pivotaltracker.com/story/show/50619287): Link a Classification or a Classification Term to an Accession 
* FEATURE [#45975387](https://www.pivotaltracker.com/story/show/45975387): Add warning/alert for users using a "bronze"-level browser (e.g. IE 7)
* FEATURE [#47583949](https://www.pivotaltracker.com/story/show/47583949): Display accession number in linked accessions section of resource record
* FEATURE [#43515659](https://www.pivotaltracker.com/story/show/43515659): When looking at a record, I want to see all linked records, regardless of the direction of the link
* FEATURE [#41427063](https://www.pivotaltracker.com/story/show/41427063): Display Agents and Subjects in browse view in alphabetical order
* ENHANCEMENT [#47583829](https://www.pivotaltracker.com/story/show/47583829): Subjects: re-label "Add" button (in the Terms section) to "Add Subject Heading"
* ENHANCEMENT [#47583925](https://www.pivotaltracker.com/story/show/47583925): Archival Objects: Remove the placeholder "New Archival Object" from the Title field
* ENHANCEMENT [#47583529](https://www.pivotaltracker.com/story/show/47583529): Disable automatic pop-up of date entry widget 
* BUG FIX [#49089827](https://www.pivotaltracker.com/story/show/49089827): Accessions: `title` not required
* BUG FIX [#49272069](https://www.pivotaltracker.com/story/show/49272069): Protect enumeration values needed by the application
* BUG FIX [#50617725](https://www.pivotaltracker.com/story/show/50617725): Show view for Digital Objects and Archival Objects not loading translations for enumerations  
* BUG FIX [#45450543](https://www.pivotaltracker.com/story/show/45450543): Fix Rights date validation issue for Restriction Begin/Restriction End
* BUG FIX [#49093799](https://www.pivotaltracker.com/story/show/49093799): Lock version-related errors aren't surfacing to alert box (only receiving "Internal Server Error")
* BUG FIX [#48960499](https://www.pivotaltracker.com/story/show/48960499): Incorrectly formatted Accession Date throws an exception
* BUG FIX [#50099927](https://www.pivotaltracker.com/story/show/50099927): Containers may only have one Location with a Location Status of "Current"


### 0.5.2-1 (May 28, 2013):

* FEATURE [#43821087](https://www.pivotaltracker.com/story/show/43821087), [#49814363](https://www.pivotaltracker.com/story/show/49814363): "Rapid data entry" for Resources with sticky values (0.5.2)
* FEATURE [#47974011](https://www.pivotaltracker.com/story/show/47974011): Progress feedback for imports (0.5.2-1)
* FEATURE [#34942605](https://www.pivotaltracker.com/story/show/34942605), [#34942671](https://www.pivotaltracker.com/story/show/34942671): Plugins: Add proof of concept that integrates with the backend and the staff frontend (0.5.2)
* FEATURE [#40401639](https://www.pivotaltracker.com/story/show/40401639), [#49879423](https://www.pivotaltracker.com/story/show/49879423), [#40401755](https://www.pivotaltracker.com/story/show/40401755): Classification/Classification Terms: create, edit, delete, and allow for linking to Resources (0.5.2)
* FEATURE [#48947175](https://www.pivotaltracker.com/story/show/48947175): Display all "public" data in the public user interface when records are published (0.5.2)
* FEATURE [#48956939](https://www.pivotaltracker.com/story/show/48956939): Add "publish" button that recursively publishes all components, notes, etc. within Resources or Digital Objects (0.5.2)
* FEATURE [#49067191](https://www.pivotaltracker.com/story/show/49067191): Allow creation of digital objects from "add instance" form for Resources and Resource Components (0.5.2)
* FEATURE [#49568977](https://www.pivotaltracker.com/story/show/49568977), [#50239605](https://www.pivotaltracker.com/story/show/50239605): Additional User Defined Fields (0.5.2)
* BUG FIX [#50562445](https://www.pivotaltracker.com/story/show/50562445), [#50565433](https://www.pivotaltracker.com/story/show/50565433): Rapid Data Entry CSS not getting precompiled (0.5.2-1)
* BUG FIX [#50356825](https://www.pivotaltracker.com/story/show/50356825): Buttons to add new subrecords (e.g. User Defined) still add a new subrecord when clicked in their "disabled" state (0.5.2)
* BUG FIX [#50492611](https://www.pivotaltracker.com/story/show/50492611): Fix indexing error for digital objects that broke display in the public UI (0.5.2)
* BUG FIX [#50357025](https://www.pivotaltracker.com/story/show/50357025): User defined field form displaying '" "' or 'nil' (0.5.2)
* BUG FIX [#49807895](https://www.pivotaltracker.com/story/show/49807895): Digital Objects: show view causes frontend error (undefined method `linked_instances') when an object has a File Version (0.5.2)

### 0.5.1 (May 10, 2013): 

* FEATURE [#41457465](https://www.pivotaltracker.com/story/show/41457465), [#43512493](https://www.pivotaltracker.com/story/show/43512493), [#41508763](https://www.pivotaltracker.com/story/show/41508763): Allow deletion of all record types
* FEATURE [#41457465](https://www.pivotaltracker.com/story/show/41457465): Add filtering/faceting to rest of search browse screens within staff UI
* FEATURE [#47583279](https://www.pivotaltracker.com/story/show/47583279): Improved UI guidance about required fields
* FEATURE [#47583233](https://www.pivotaltracker.com/story/show/47583233): Provide access to record actions (spawn, delete, etc.) from within edit forms
* FEATURE [#47209991](https://www.pivotaltracker.com/story/show/47209991): Configure a default value for non-editable enumerations  such as date type or language
* FEATURE [#47583811](https://www.pivotaltracker.com/story/show/47583811): Sort and filter the browse list in record linking popup 
* ENHANCEMENT [#49292329](https://www.pivotaltracker.com/story/show/49292329): Update tooltips to describe required/conditionally required fields
* ENHANCEMENT [#48600195](https://www.pivotaltracker.com/story/show/48600195): Remove internal_only property from Archival Objects and Notes
* ENHANCEMENT [#43559667](https://www.pivotaltracker.com/story/show/43559667): Rename Subject "ref_id" property "authority_id" to make consistent with Agents
* ENHANCEMENT [#46217967](https://www.pivotaltracker.com/story/show/46217967): Extents: container_summary and physical_details should be a TextField
* ENHANCEMENT [#43820677](https://www.pivotaltracker.com/story/show/43820677): Dates: expression field should be visually larger
* ENHANCEMENT [#46377505](https://www.pivotaltracker.com/story/show/46377505): Update METS export mappings to include properties from File Version objects
* ENHANCEMENT [#48702729](https://www.pivotaltracker.com/story/show/48702729): Rework date/title requirements for Resource Components
* ENHANCEMENT [#46557613](https://www.pivotaltracker.com/story/show/46557613): Collection Management: Add processing_funding_source property
* ENHANCEMENT [#47583857](https://www.pivotaltracker.com/story/show/47583857): Change “+1” and “Add Child Component” component pull-downs to buttons, and relabel the former to “Add Sibling”
* ENHANCEMENT [#43558175](https://www.pivotaltracker.com/story/show/43558175): Add Resource Description and Access to Agent rules enum
* BUG FIX [#49637103](https://www.pivotaltracker.com/story/show/49637103): Record linker popup for events: translation missing
* BUG FIX [#48602367](https://www.pivotaltracker.com/story/show/48602367): Public frontend: repositories needs pagination
* BUG FIX [#47748631](https://www.pivotaltracker.com/story/show/47748631): External document URIs are trying to be resolved
* BUG FIX [#43516657](https://www.pivotaltracker.com/story/show/43516657): Subjects: authority_id only has to be unique in combination with the source
* BUG FIX [#48694911](https://www.pivotaltracker.com/story/show/48694911): Indexer raises Timeout::Error when importing large EAD files
* BUG FIX [#48602071](https://www.pivotaltracker.com/story/show/48602071): NoMethodError on some MARCXML and EAD imports
* BUG FIX [#49079625](https://www.pivotaltracker.com/story/show/49079625): Digital objects: level should allow null

### 0.5.0 (April 29, 2013): 
* FEATURE [#35792983](https://www.pivotaltracker.com/story/show/35792983): Add subdivisions (e.g. subject or form) to Agents linked to Resources, Digital Objects, and Accessions
* FEATURE [#47583321](https://www.pivotaltracker.com/story/show/47583321): Eliminate unnecessary mouse clicks and improve UI workflow
* FEATURE [#48766865](https://www.pivotaltracker.com/story/show/48766865): Editing forms should follow DACS/ISAD(G) more closely
* FEATURE [#37382431](https://www.pivotaltracker.com/story/show/37382431): Create backup "packages" for easy redeployment
* FEATURE [#41428503](https://www.pivotaltracker.com/story/show/41428503): Browse users or use autocomplete to locate users when adding to a group
* FEATURE [#47583643](https://www.pivotaltracker.com/story/show/47583643): Better UI feedback when saving records
* FEATURE [#46516237](https://www.pivotaltracker.com/story/show/46516237): Make date data entry easier
* FEATURE [#48086081](https://www.pivotaltracker.com/story/show/48086081): Create an event when transferring components from one Resource to another
* FEATURE [#46512927](https://www.pivotaltracker.com/story/show/46512927): Agents: add contact persons note field
* FEATURE [#37382393](https://www.pivotaltracker.com/story/show/37382393), [#37382341](https://www.pivotaltracker.com/story/show/37382341): Clustered/multitenant deployment support and documentation
* ENHANCEMENT [#34076709](https://www.pivotaltracker.com/story/show/34076709): Repositories also represented as Agents in data model (allows linking in events)
* ENHANCEMENT [#48128063](https://www.pivotaltracker.com/story/show/48128063): Convert static enums to dynamic enums so they can be stored in backend database
* BUG FIX [#47675227](https://www.pivotaltracker.com/story/show/47675227): Pagination does not work in public UI
* BUG FIX [#47691817](https://www.pivotaltracker.com/story/show/47691817): Resources with "Publish?" set to false are displaying public UI
* BUG FIX [#47691151](https://www.pivotaltracker.com/story/show/47691151): Locations and ref IDs should not display in public UI
* BUG FIX [#47675799](https://www.pivotaltracker.com/story/show/47675799): Application error in public UI when trying to display a resource with only digital instances
* BUG FIX [#47692875](https://www.pivotaltracker.com/story/show/47692875): Pagination in staff UI for repositories doesn't work
* BUG FIX [#47677273](https://www.pivotaltracker.com/story/show/47677273): Subject term autocomplete fails with left parentheses
* BUG FIX [#46673841](https://www.pivotaltracker.com/story/show/46673841): File format name should be configurable enum

### 0.4.3 (April 15, 2013): 
* FEATURE [#44678161](https://www.pivotaltracker.com/story/show/44678161): Relationships between agents (associative, earlier/later, parent/child)
* FEATURE [#45552845](https://www.pivotaltracker.com/story/show/45552845), [#47244859](https://www.pivotaltracker.com/story/show/47244859): Transfer components between resources
* FEATURE [#43807701](https://www.pivotaltracker.com/story/show/43807701): Digital objects in the public frontend
* FEATURE [#35061477](https://www.pivotaltracker.com/story/show/35061477): User-defined fields for Accessions, Resources and Digital Objects
* FEATURE [#35065215](https://www.pivotaltracker.com/story/show/35065215): Unprocessed accessions report
* FEATURE [#44675539](https://www.pivotaltracker.com/story/show/44675539): Specify components as internal only
* FEATURE [#43512693](https://www.pivotaltracker.com/story/show/43512693): Add contact info to Users
* FEATURE [#41461107](https://www.pivotaltracker.com/story/show/41461107): Add scope note to Subjects
* FEATURE [#43799411](https://www.pivotaltracker.com/story/show/43799411): Associate Accessions with Instances and Locations
* FEATURE [#41456665](https://www.pivotaltracker.com/story/show/41456665), [#43514117](https://www.pivotaltracker.com/story/show/43514117): Improved group/user workflow
* BUG FIX [#47205979](https://www.pivotaltracker.com/story/show/47205979): Collapse bar for collection management should show processing_status with appropriate value

### 0.4.2 (April 1, 2013):
* FEATURE [#43812815](https://www.pivotaltracker.com/story/show/43812815): Refactor Collections Management UI (creation/editing now in context of linked record)
* FEATURE [#35065125](https://www.pivotaltracker.com/story/show/35065125): Basic reporting framework with PDF, HTML, Excel, CSV, and JSON output
* FEATURE [#41506217](https://www.pivotaltracker.com/story/show/41506217): Specify a default value for Enumerations
* FEATURE [#41192409](https://www.pivotaltracker.com/story/show/41192409): Rework application distribution and provide scripts to run ArchivesSpace as a service
* FEATURE [#41508431](https://www.pivotaltracker.com/story/show/41508431): Resources: Add Level of Description label to Resource "tree" UI
* FEATURE [#41509815](https://www.pivotaltracker.com/story/show/41509815): Add extent types for digital materials
* FEATURE [#45553651](https://www.pivotaltracker.com/story/show/45553651): Automatically add an Event when creating an Agent (needed for EAC-CPF export)
* FEATURE [#43559337](https://www.pivotaltracker.com/story/show/43559337), [#43559173](https://www.pivotaltracker.com/story/show/43559173): Improve Agent index views
* FEATURE [#43459655](https://www.pivotaltracker.com/story/show/43459655): Add additional Accession properties
* ENHANCEMENT [#46409585](https://www.pivotaltracker.com/story/show/46409585): Remove descriptive notes from name form records (EAC-CPF data model consistency)
* ENHANCEMENT [#43820805](https://www.pivotaltracker.com/story/show/43820805): Change labels and property names that start with "Uncertainty" to "Certainty" (EAD data model consistency)
* BUG FIX [#45461739](https://www.pivotaltracker.com/story/show/45461739): Agent link role should not allow for configurable values
* BUG FIX [#45446279](https://www.pivotaltracker.com/story/show/45446279): Indexer should handle notifications about updated Enumerations

### 0.4.1 (March 18, 2013):
* FEATURE [#44678103](https://www.pivotaltracker.com/story/show/44678103): Improved note handling for Agents
* FEATURE [#43492849](https://www.pivotaltracker.com/story/show/43492849): Improved workflow for Repository creation and management
* FEATURE [#43807809](https://www.pivotaltracker.com/story/show/43807809): Advanced search in the public discover interface
* FEATURE [#43113233](https://www.pivotaltracker.com/story/show/43113233): Digital Objects: support for File Version subrecords
* FEATURE [#42100221](https://www.pivotaltracker.com/story/show/42100221): Export container labels
* FEATURE [#35064329](https://www.pivotaltracker.com/story/show/35064329): Create Events from within Accessions
* FEATURE [#43824271](https://www.pivotaltracker.com/story/show/43824271): Make text fields within application larger
* FEATURE [#43559931](https://www.pivotaltracker.com/story/show/43559931): Agents: Add Note textarea field to Contact Details subrecords
* FEATURE [#41509221](https://www.pivotaltracker.com/story/show/41509221): Specify Notes as internal only
* ENHANCEMENT [#43971539](https://www.pivotaltracker.com/story/show/43971539): Abbreviated representation of note types in data model
* BUG FIX [#44771071](https://www.pivotaltracker.com/story/show/44771071): Resource Components: ref_id should allow "-", "_", ":", and "."


### 0.4.0 (March 4, 2013):
* FEATURE [#42604075](https://www.pivotaltracker.com/story/show/42604075): Export digital objects as Dublin Core XML
* FEATURE [#42604105](https://www.pivotaltracker.com/story/show/42604105): Export digital objects as METS
* FEATURE [#42604123](https://www.pivotaltracker.com/story/show/42604123): Export digital objects as MODS
* FEATURE [#41570795](https://www.pivotaltracker.com/story/show/41570795): Implement Basic Data Entry group
* FEATURE [#39233395](https://www.pivotaltracker.com/story/show/39233395), [#43807667](https://www.pivotaltracker.com/story/show/43807667): Filter browse lists and query results using facets
* FEATURE [#43810817](https://www.pivotaltracker.com/story/show/43810817), [#44678553](https://www.pivotaltracker.com/story/show/44678553): Allow import process to automatically populate configurable enumerations (lookup lists)
* FEATURE [#43971737](https://www.pivotaltracker.com/story/show/43971737): Allow multiple text parts in a given note
* FEATURE [#35791779](https://www.pivotaltracker.com/story/show/35791779): Add optional role property to Agents that are linked to Resources, Accessions, or Digital Objects
* FEATURE [#42604057](https://www.pivotaltracker.com/story/show/42604057): Export Resource records as MARCXML
* FEATURE [#43807197](https://www.pivotaltracker.com/story/show/43807197), [#43807295](https://www.pivotaltracker.com/story/show/43807295), [#43807317](https://www.pivotaltracker.com/story/show/43807317): Add facets in the public frontend and staff to browse by repository, creator, subject
* FEATURE [#44685985](https://www.pivotaltracker.com/story/show/44685985), [#43807667](https://www.pivotaltracker.com/story/show/43807667): Add sorting of browse lists and query results
* FEATURE [#42603991](https://www.pivotaltracker.com/story/show/42603991): Import Digital Objects from CSV data
* FEATURE [#43794125](https://www.pivotaltracker.com/story/show/43794125): Extent: Change "Leafs" to "Leaves"
* FEATURE [#42604153](https://www.pivotaltracker.com/story/show/42604153): Export Agents as EAC-CPF
* FEATURE [#42604019](https://www.pivotaltracker.com/story/show/42604019): Import only Agents and Subjects from MARCXML data
* BUG FIX [#44918277](https://www.pivotaltracker.com/story/show/44918277): Usernames should allow hyphens
* BUG FIX [#43800193](https://www.pivotaltracker.com/story/show/43800193): Disable warnings for empty condition and content descriptions for Accessions
* BUG FIX [#45368405](https://www.pivotaltracker.com/story/show/45368405): Browse linker not loading for Agents and Subjects
* BUG FIX [#43824713](https://www.pivotaltracker.com/story/show/43824713): Spawning an Accession with a linked Rights record fails
* BUG FIX [#43970189](https://www.pivotaltracker.com/story/show/43970189), [#43970861](https://www.pivotaltracker.com/story/show/43970861): Textual content for notes that are bibliographies or indexes should be optional
* BUG FIX [#43930977](https://www.pivotaltracker.com/story/show/43930977): Usernames should allow spaces

### 0.3.4 (February 18, 2013):
* SECURITY FIX: Address CVE-2013-0269: vulnerability in JSON parser ([more info](https://groups.google.com/d/topic/rubyonrails-security/4_YvCpLzL58/discussion)) (0.3.2-1)
* FEATURE [#43807355](https://www.pivotaltracker.com/story/show/43807355), [#43807055](https://www.pivotaltracker.com/story/show/43807055): Public discovery application, with display of descriptive information and searching by title and keyword
* FEATURE [#42604187](https://www.pivotaltracker.com/story/show/42604187): Basic support for importing EAC-CPF records as Agents
* FEATURE [#42603975](https://www.pivotaltracker.com/story/show/42603975): Basic support for importing MARCXML records as Resources
* FEATURE [#43810291](https://www.pivotaltracker.com/story/show/43810291): Add additional required properties for Repositories (organization code, contact info, etc.)
* FEATURE [#42928309](https://www.pivotaltracker.com/story/show/42928309): Improve error messages for problems during import
* FEATURE [#41505927](https://www.pivotaltracker.com/story/show/41505927): Add component unique identifier (e.g. for series information) to Resource Components
* FEATURE [#43535127](https://www.pivotaltracker.com/story/show/43535127), [#42931479](https://www.pivotaltracker.com/story/show/42931479), [#43535079](https://www.pivotaltracker.com/story/show/43535079): Support for external help links and related configuration (to support external web-based documentation)
* BUG FIX [#43514895](https://www.pivotaltracker.com/story/show/43514895): Group form allows adding a username that doesn't exist
* BUG FIX [#43798975](https://www.pivotaltracker.com/story/show/43798975), [#43517753](https://www.pivotaltracker.com/story/show/43517753): Bottom navigation in agent/subject popups doesn't work properly
* BUG FIX [#43562315](https://www.pivotaltracker.com/story/show/43562315): Linking a digital object to an event fails
* BUG FIX [#43799713](https://www.pivotaltracker.com/story/show/43799713): Accessions: "Dates" missing from nav bar; "Extents" shows up twice
* BUG FIX [#43798569](https://www.pivotaltracker.com/story/show/43798569): Issues with selecting and editing text in large text fields
* BUG FIX [#41438617](https://www.pivotaltracker.com/story/show/41438617), [#42635441](https://www.pivotaltracker.com/story/show/42635441), [#42635327](https://www.pivotaltracker.com/story/show/42635327), [#41438505](https://www.pivotaltracker.com/story/show/41438505): Agents: Issues with Sort/Display Name generation

### 0.3.3 (February 2, 2013):
* SECURITY FIX: Address CVE-2013-0333: vulnerability in JSON parser ([more info](https://groups.google.com/d/topic/rubyonrails-security/1h2DR63ViGo/discussion)) (0.3.2-1)
* FEATURE [#42603937](https://www.pivotaltracker.com/story/show/42603937): CSV import of accessions data (basic support)
* FEATURE [#35775219](https://www.pivotaltracker.com/story/show/35775219): Add tooltips (first for accessions) and administrator-editable tooltip content
* FEATURE [#41570797](https://www.pivotaltracker.com/story/show/41570797): Implement Advanced Data Entry user group
* FEATURE [#41572523](https://www.pivotaltracker.com/story/show/41572523): Implement Project Manager user group
* FEATURE [#41509633](https://www.pivotaltracker.com/story/show/41509633): Link Resources and Digital Objects
* FEATURE [#42441493](https://www.pivotaltracker.com/story/show/42441493), [#42441483](https://www.pivotaltracker.com/story/show/42441483), [#42441471](https://www.pivotaltracker.com/story/show/42441471), [#42523625](https://www.pivotaltracker.com/story/show/42523625): Add support for dynamic, configurable Enumerations (lookup lists for semi-controlled values)
* BUG FIX [#42268601](https://www.pivotaltracker.com/story/show/42268601): Require Resource identifier
* BUG FIX [#41440365](https://www.pivotaltracker.com/story/show/41440365): End dates can't come before begin dates and vice versa
* BUG FIX [#34168827](https://www.pivotaltracker.com/story/show/34168827): Uniqueness of ref_id should only be enforced within a Resource, not across resources


### 0.3.2 (January 18, 2013):
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