This is an overview of the development process for ArchivesSpace, based upon the process used during the grant-funded development period. This documentation is written from the perspective of the Product Owner, and is designed to complement the documentation about the [[Release process]].

### Sprints, Cycles and Versioning

ArchivesSpace uses the Scrum development methodology to prioritize features for a given sprint and cycle. During our initial implementation phase, we used two week sprints, with four sprints to a cycle. A cycle was intended to be equivalent to a "minor" release; for example, we released the first cycle as ArchivesSpace 0.1.0. Subsequent sprints were equivalent to a pre-release "build", so for example the first sprint of the second cycle concluded with the release of ArchivesSpace 0.1.1. At the end of the second cycle, we released ArchivesSpace 0.2.0, and so forth.

### Prioritizing features and bugs

ArchivesSpace has used [Pivotal Tracker](https://www.pivotaltracker.com/s/projects/386247) to document, prioritize, and manage assignment and acceptance for user stories, bugs, chores, and releases. Before the sprint planning meeting, the Product Owner creates any necessary user stories and provisionally prioritizes them in order of importance.

### Sprint planning: assigning, estimating, and clarifying stories

The Team and Scrum Master meet with the Product Owner in a Sprint Planning Meeting to estimate prioritized stories by giving them a specific number of "points." The estimation determines the potential upper limit of what the Team is expected to deliver during a given sprint based on their velocity. As part of the estimation process, a Team Member  volunteers to be assigned a given story. The Sprint Planning Meeting also gives the Team the opportunity to ask the Product Owner for additional information about any of the stories.

### Acceptance 

Once the Team implements a story, a Team Member marks it as "finished." Any changes should be made in a branch and merged in using a pull request when possible. Once the change is merged into the master branch, it is marked as "delivered," and is reviewed by the Product Owner. If the Product Owner believes that the feature or bug is adequately addressed, the Product Owner marks the story as "accepted." If not, the Product owner can "reject" the story, and provides additional information in comments on the story to describe why the story was not satisfied.