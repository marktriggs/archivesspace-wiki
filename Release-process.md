This is an overview of the development process for ArchivesSpace, based upon the process used during the grant-funded development period. This documentation is written from the perspective of the Product Owner, and is designed to complement the documentation about the [[Development process]].

This presumes that the `master` branch in `archivesspace/archivesspace` is maintained as stable, deployable code, and that a separate branch or repository is used to commit changes prior to release.

### Development 

For a release to occur, the Team must implement a set of features, bugs, or chores as expressed in user stories in Pivotal Tracker. See the [[Development process]] page for more information. 

### Acceptance of features

The Product Owner should ensure that all features that have been delivered are marked as accepted or rejected. The Product Owner and the Scrum Master should establish if any rejected stories will block a release or will be deferred until the next sprint before proceeding. All automated tests should pass before proceeding, and code coverage should be maintained **at least** to be 89%.

### Update developer documentation

The Scrum Master should ensure that the `gh-pages` branch contains the most up-to-date version of the developer documentation (e.g. API docs, models, etc.) generated using `yard`. 

**BH: INSERT STEPS HERE**

### Tag release

Once the feature acceptance process is complete, the Scrum Master should create a new tag based on the appropriate commit in the development branch with the the version number prefixed with the letter `v`. For example, for version 1.0.0, the version should be tagged as `v1.0.0`:

    $ git tag v1.0.0

A "patch release" to address security issues should be specified by adding a hyphenated, incremental patch number (e.g. `v1.0.0-1` for the first patch release). 

### Push changes to stable branch

Once tagged, the Product Owner pushes the commits for the codebase, the new tag, and the updated development documentation to the `master` branch in the `archivesspace/archivesspace` repository:

    $ git pull # or git fetch --tags ; git merge [branch]
    $ git push --tags git@github.com:archivesspace/archivesspace.git v1.0.0~0:master
    $ git checkout gh-pages
    $ git push git@github.com:archivesspace/archivesspace.git gh-pages

### Verify status of build 

The automated test suite will run on the [Travis-CI continuous integration environment](https://travis-ci.org/archivesspace/archivesspace). Ensure that the build does not fail, and investigate any failures before proceeding.

### Build a new release

**JVM VERSION REQUIREMENTS?**

If the test suite passes in Travis-CI, build the new version using the `build_release` script:

    $ scripts/build_release v1.0.0

Once the new release is built, rename the file so it includes the version name:

    $ mv archivesspace.zip archivesspace-v1.0.0.zip

### Create and post release notes

Create the release notes based on the format used in the [[Changelog]]:

```markdown
### version (release date)

* SECURITY FIX: Describe resolved security issue, provide CVE ID if applicable, and link to more info
* FEATURE [#PT story ID](PT story URL): Description of feature. Features are used for user-facing functionality.
* ENHANCEMENT: [#PT story ID](PT story URL): Description of enhancement; most often "chores" in PT
* BUG FIX: [#PT story ID](PT story URL): Description of bug fix
* KNOWN ISSUE: Description of existing issue; may help mitigate reports
```

For example:

```markdown
### 1.0.0 (July 99, 2301)

* SECURITY FIX: Address CVE-2013-0269: vulnerability in JSON parser ([more info](https://groups.google.com/d/topic/rubyonrails-security/4_YvCpLzL58/discussion))
* FEATURE [#43561173](https://www.pivotaltracker.com/story/show/43561173): Locations: add batch add functionality.
* ENHANCEMENT [#46377505](https://www.pivotaltracker.com/story/show/46377505): Update METS export mappings to include properties from File Version objects
* BUG FIX [#43930977](https://www.pivotaltracker.com/story/show/43930977): Usernames should allow spaces
* KNOWN ISSUE: Containers and instances not importing properly from EAD
```

Once finished, edit the [[Changelog]] page and add the release notes for the new version to the top.

### Upload release

Upload the release to the [Releases](http://github.com/archivesspace/archivesspace/releases) page and add notes for the the latest version.

Update the [[Downloads]] page to the link with to the compiled version.

### Announce release

Announce the new release to the following locations: ArchivesSpace website, ArchivesSpace Google Group, etc.