```
 post '/repositories/:repo_id/accessions/:accession_id':
   Description: Update an Accession
   Parameters: 
     Integer accession_id -- The accession ID to update
     JSONModel(:accession) <request body> -- The accession data to update
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
 
 post '/repositories/:repo_id/accessions':
   Description: Create an Accession
   Parameters: 
     JSONModel(:accession) <request body> -- The accession to create
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
 
 get '/repositories/:repo_id/accessions':
   Description: Get a list of Accessions for a Repository
   Parameters: 
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- [(:accession)]
 
 get '/repositories/:repo_id/accessions/:accession_id':
   Description: Get an Accession by ID
   Parameters: 
     Integer accession_id -- The accession ID
     Integer repo_id -- The Repository ID -- The Repository must exist
     [String] resolve -- A list of references to resolve and embed in the response
   Returns:
     200 -- (:accession)
 
 get '/agents':
   Description: Get all agent records
   Parameters: 
   Returns:
     200 -- [(:agent)]
 
 get '/agents/by-name':
   Description: Get all agent records by their sort name
   Parameters: 
     (?-mix:[\w0-9 -.]) q -- The name prefix to match
   Returns:
     200 -- [(:agent)]
 
 post '/agents/corporate_entities':
   Description: Create a corporate entity agent
   Parameters: 
     JSONModel(:agent_corporate_entity) <request body> -- The corporate entity to create
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
 
 post '/agents/corporate_entities/:agent_id':
   Description: Update a corporate entity agent
   Parameters: 
     Integer agent_id -- The ID of the agent to update
     JSONModel(:agent_corporate_entity) <request body> -- The corporate entity to create
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
     400 -- {:error => (description of error)}
 
 get '/agents/corporate_entities/:id':
   Description: Get a corporate entity by ID
   Parameters: 
     Integer id -- ID of the corporate entity agent
   Returns:
     200 -- (:agent)
     404 -- {"error":"Agent not found"}
 
 post '/agents/families':
   Description: Create a family agent
   Parameters: 
     JSONModel(:agent_family) <request body> -- The family to create
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
 
 post '/agents/families/:agent_id':
   Description: Update a family agent
   Parameters: 
     Integer agent_id -- The ID of the agent to update
     JSONModel(:agent_family) <request body> -- The family to create
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
     400 -- {:error => (description of error)}
 
 get '/agents/families/:id':
   Description: Get a family by ID
   Parameters: 
     Integer id -- ID of the family agent
   Returns:
     200 -- (:agent)
     404 -- {"error":"Agent not found"}
 
 post '/agents/people':
   Description: Create a person agent
   Parameters: 
     JSONModel(:agent_person) <request body> -- The person to create
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
 
 post '/agents/people/:agent_id':
   Description: Update a person agent
   Parameters: 
     Integer agent_id -- The ID of the agent to update
     JSONModel(:agent_person) <request body> -- The person to create
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
     400 -- {:error => (description of error)}
 
 get '/agents/people/:id':
   Description: Get a person by ID
   Parameters: 
     Integer id -- ID of the person agent
   Returns:
     200 -- (:agent)
     404 -- {"error":"Agent not found"}
 
 post '/agents/software':
   Description: Create a software agent
   Parameters: 
     JSONModel(:agent_software) <request body> -- The software to create
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
 
 post '/agents/software/:agent_id':
   Description: Update a software agent
   Parameters: 
     Integer agent_id -- The ID of the software to update
     JSONModel(:agent_software) <request body> -- The software to create
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
     400 -- {:error => (description of error)}
 
 get '/agents/software/:id':
   Description: Get a software by ID
   Parameters: 
     Integer id -- ID of the software agent
   Returns:
     200 -- (:agent)
     404 -- {"error":"Agent not found"}
 
 post '/repositories/:repo_id/archival_objects':
   Description: Create an Archival Object
   Parameters: 
     JSONModel(:archival_object) <request body> -- The Archival Object to create
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
     409 -- {"error":{"[:resource_id, :ref_id]":["An Archival Object Ref ID must be unique to its resource"]}}
 
 post '/repositories/:repo_id/archival_objects/:archival_object_id':
   Description: Update an Archival Object
   Parameters: 
     Integer archival_object_id -- The Archival Object ID to update
     JSONModel(:archival_object) <request body> -- The Archival Object data to update
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
     400 -- {:error => (description of error)}
     409 -- {"error":{"[:resource_id, :ref_id]":["An Archival Object Ref ID must be unique to its resource"]}}
 
 get '/repositories/:repo_id/archival_objects/:archival_object_id':
   Description: Get an Archival Object by ID
   Parameters: 
     Integer archival_object_id -- The Archival Object ID
     Integer repo_id -- The Repository ID -- The Repository must exist
     [String] resolve -- A list of references to resolve and embed in the response
   Returns:
     200 -- (:archival_object)
     404 -- {"error":"ArchivalObject not found"}
 
 get '/repositories/:repo_id/archival_objects/:archival_object_id/children':
   Description: Get the children of an Archival Object
   Parameters: 
     Integer archival_object_id -- The Archival Object ID
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- [(:archival_object)]
     404 -- {"error":"ArchivalObject not found"}
 
 get '/repositories/:repo_id/archival_objects':
   Description: Get a list of Archival Objects for a Repository
   Parameters: 
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- [(:archival_object)]
 
 get '/repositories/:repo_id/digital_objects/:digital_object_id':
   Description: Get a Digital Object
   Parameters: 
     Integer digital_object_id -- The ID of the digital object to retrieve
     Integer repo_id -- The Repository ID -- The Repository must exist
     [String] resolve -- A list of references to resolve and embed in the response
   Returns:
     200 -- (:digital_object)
 
 post '/repositories/:repo_id/digital_objects':
   Description: Create a Digital Object
   Parameters: 
     JSONModel(:digital_object) <request body> -- The digital object to create
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
 
 post '/repositories/:repo_id/digital_objects/:digital_object_id':
   Description: Update a Digital Object
   Parameters: 
     Integer digital_object_id -- The ID of the digital object to retrieve
     JSONModel(:digital_object) <request body> -- The digital object to update
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
     400 -- {:error => (description of error)}
 
 get '/repositories/:repo_id/digital_objects':
   Description: Get a list of Digital Objects for a Repository
   Parameters: 
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- [(:digital_object)]
 
 get '/repositories/:repo_id/digital_objects/:digital_object_id/tree':
   Description: Get a Digital Object tree
   Parameters: 
     Integer digital_object_id -- The ID of the digital object to retrieve
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- OK
 
 post '/repositories/:repo_id/digital_objects/:digital_object_id/tree':
   Description: Update a Digital Object tree
   Parameters: 
     Integer digital_object_id -- The ID of the digital object to retrieve
     JSONModel(:digital_object_tree) <request body> -- A JSON tree representing the modified hierarchy
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
 
 post '/repositories/:repo_id/digital_object_components':
   Description: Create an Digital Object Component
   Parameters: 
     JSONModel(:digital_object_component) <request body> -- The Digital Object Component to create
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
 
 post '/repositories/:repo_id/digital_object_components/:digital_object_component_id':
   Description: Update an Digital Object Component
   Parameters: 
     Integer digital_object_component_id -- The Digital Object Component ID to update
     JSONModel(:digital_object_component) <request body> -- The Digital Object Component data to update
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
     400 -- {:error => (description of error)}
 
 get '/repositories/:repo_id/digital_object_components/:digital_object_component_id':
   Description: Get an Digital Object Component by ID
   Parameters: 
     Integer digital_object_component_id -- The Digital Object Component ID
     Integer repo_id -- The Repository ID -- The Repository must exist
     [String] resolve -- A list of references to resolve and embed in the response
   Returns:
     200 -- (:digital_object_component)
     404 -- {"error":"DigitalObjectComponent not found"}
 
 get '/repositories/:repo_id/digital_object_components/:digital_object_component_id/children':
   Description: Get the children of an Digital Object Component
   Parameters: 
     Integer digital_object_component_id -- The Digital Object Component ID
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- [(:digital_object_component)]
     404 -- {"error":"DigitalObjectComponent not found"}
 
 get '/repositories/:repo_id/digital_object_components':
   Description: Get a list of Digital Object Components for a Repository
   Parameters: 
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- [(:digital_object_component)]
 
 post '/repositories/:repo_id/events':
   Description: Create an Event
   Parameters: 
     JSONModel(:event) <request body> -- The Event to create
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
 
 post '/repositories/:repo_id/events/:event_id':
   Description: Update an Event
   Parameters: 
     Integer event_id -- The event ID to update
     JSONModel(:event) <request body> -- The event data to update
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
 
 get '/repositories/:repo_id/events':
   Description: Get a list of Events for a Repository
   Parameters: 
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- [(:event)]
 
 get '/repositories/:repo_id/events/:event_id':
   Description: Get an Event by ID
   Parameters: 
     Integer event_id -- The Event ID
     Integer repo_id -- The Repository ID -- The Repository must exist
     [String] resolve -- A list of references to resolve and embed in the response
   Returns:
     200 -- (:event)
     404 -- {"error":"Event not found"}
 
 get '/repositories/:repo_id/events/linkable-records/list':
   Description: Get a list of records matching some search criteria that can be linked to an event
   Parameters: 
     (?-mix:[\w0-9 -.]) q -- The record title prefix to match
   Returns:
     200 -- A list of matching records
 
 get '/repositories/:repo_id/resource_descriptions/:resource_id.xml':
   Description: Get an EAD representation of a Resource 
   Parameters: 
     Integer resource_id -- The ID of the resource to retrieve
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- (:resource)
 
 post '/repositories/:repo_id/groups':
   Description: Create a group within a repository
   Parameters: 
     JSONModel(:group) <request body> -- The group to create
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
     409 -- conflict
 
 post '/repositories/:repo_id/groups/:group_id':
   Description: Update a group
   Parameters: 
     Integer group_id -- The Group ID to update
     JSONModel(:group) <request body> -- The Group data to update
     Integer repo_id -- The Repository ID -- The Repository must exist
     RESTHelpers::BooleanParam with_members -- If 'true' (the default) replace the membership list with the list provided
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
     400 -- {:error => (description of error)}
     409 -- conflict
 
 get '/repositories/:repo_id/groups/:group_id':
   Description: Get a group by ID
   Parameters: 
     Integer group_id -- The group ID
     Integer repo_id -- The Repository ID -- The Repository must exist
     RESTHelpers::BooleanParam with_members -- If 'true' (the default) return the list of members with the group
   Returns:
     200 -- (:group)
     404 -- {"error":"Group not found"}
 
 get '/repositories/:repo_id/groups':
   Description: Get a list of groups for a repository
   Parameters: 
     Integer repo_id -- The Repository ID -- The Repository must exist
     String group_code -- Get groups by group code
   Returns:
     200 -- [(:resource)]
 
 post '/repositories/:repo_id/locations/:location_id':
   Description: Update a Location
   Parameters: 
     Integer location_id -- The ID of the location to update
     JSONModel(:location) <request body> -- The location data to update
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
 
 post '/repositories/:repo_id/locations':
   Description: Create a Location
   Parameters: 
     JSONModel(:location) <request body> -- The location data to create
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
 
 get '/repositories/:repo_id/locations':
   Description: Get a list of locations
   Parameters: 
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- [(:location)]
 
 get '/repositories/:repo_id/locations/:location_id':
   Description: Get a Location by ID
   Parameters: 
     Integer location_id -- The Location ID
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- (:location)
 
 get '/permissions':
   Description: Get a list of Permissions
   Parameters: 
     String level -- The permission level to get (one of: repository, global, all) -- Must be one of repository, global, all
   Returns:
     200 -- [(:permission)]
 
 post '/repositories':
   Description: Create a Repository
   Parameters: 
     JSONModel(:repository) <request body> -- The repository to create
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
     403 -- access_denied
 
 get '/repositories/:id':
   Description: Get a Repository by ID
   Parameters: 
     Integer id -- ID of the repository
   Returns:
     200 -- (:repository)
     404 -- {"error":"Repository not found"}
 
 get '/repositories':
   Description: Get a list of Repositories
   Parameters: 
   Returns:
     200 -- [(:repository)]
 
 post '/repositories/:repo_id/resources':
   Description: Create a Resource
   Parameters: 
     JSONModel(:resource) <request body> -- The resource to create
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
 
 get '/repositories/:repo_id/resources/:resource_id':
   Description: Get a Resource
   Parameters: 
     Integer resource_id -- The ID of the resource to retrieve
     Integer repo_id -- The Repository ID -- The Repository must exist
     [String] resolve -- A list of references to resolve and embed in the response
   Returns:
     200 -- (:resource)
 
 get '/repositories/:repo_id/resources/:resource_id/tree':
   Description: Get a Resource tree
   Parameters: 
     Integer resource_id -- The ID of the resource to retrieve
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- OK
 
 post '/repositories/:repo_id/resources/:resource_id':
   Description: Update a Resource
   Parameters: 
     Integer resource_id -- The ID of the resource to retrieve
     JSONModel(:resource) <request body> -- The resource to update
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
     400 -- {:error => (description of error)}
 
 post '/repositories/:repo_id/resources/:resource_id/tree':
   Description: Update a Resource tree
   Parameters: 
     Integer resource_id -- The ID of the resource to retrieve
     JSONModel(:resource_tree) <request body> -- A JSON tree representing the modified hierarchy
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
 
 get '/repositories/:repo_id/resources':
   Description: Get a list of Resources for a Repository
   Parameters: 
     Integer repo_id -- The Repository ID -- The Repository must exist
   Returns:
     200 -- [(:resource)]
 
 post '/subjects':
   Description: Create a Subject
   Parameters: 
     JSONModel(:subject) <request body> -- The subject data to create
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
 
 get '/subjects':
   Description: Get a list of Subjects
   Parameters: 
   Returns:
     200 -- [(:subject)]
 
 get '/subjects/:subject_id':
   Description: Get a Subject by ID
   Parameters: 
     Integer subject_id -- The subject ID
   Returns:
     200 -- (:subject)
 
 post '/users':
   Description: Create a local user
   Parameters: 
     String password -- The user's password
     JSONModel(:user) <request body> -- The user to create
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
     400 -- {:error => (description of error)}
 
 get '/users/:username':
   Description: Get a user's details (including their current permissions)
   Parameters: 
      username -- The username of interest
   Returns:
     200 -- (:user)
 
 post '/users/:username/login':
   Description: Log in
   Parameters: 
      username -- Your username
      password -- Your password
   Returns:
     200 -- Login accepted
     403 -- Login failed
 
 post '/vocabularies/:vocab_id':
   Description: Update a Vocabulary
   Parameters: 
     Integer vocab_id -- The vocabulary ID to update
     JSONModel(:vocabulary) <request body> -- The vocabulary data to update
   Returns:
     200 -- {:status => "Updated", :id => (id of updated object)}
 
 post '/vocabularies':
   Description: Create a Vocabulary
   Parameters: 
     JSONModel(:vocabulary) <request body> -- The vocabulary data to create
   Returns:
     200 -- {:status => "Created", :id => (id of created object), :warnings => {(warnings)}}
 
 get '/vocabularies':
   Description: Get a list of Vocabularies
   Parameters: 
     String ref_id -- An alternate, externally-created ID for the vocabulary
   Returns:
     200 -- [(:vocabulary)]
 
 get '/vocabularies/:vocab_id/terms':
   Description: Get a list of Terms for a Vocabulary
   Parameters: 
     Integer vocab_id -- The vocabulary ID
   Returns:
     200 -- [(:term)]
 
 get '/vocabularies/:vocab_id':
   Description: Get a Vocabulary by ID
   Parameters: 
     Integer vocab_id -- The vocabulary ID
   Returns:
     200 -- OK
 
 post '/webhooks/register':
   Description: -- No description provided --
   Parameters: 
     String url -- The URL to receive POST notifications
   Returns:
     200 -- OK
 
 get '/webhooks/test':
   Description: -- No description provided --
   Parameters: 
   Returns:
     200 -- OK
```

This was generated by running
```sh
./build/run backend:doc | colrm 1 11
```
on tag `v0.2.0-1`