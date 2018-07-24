## Endpoints to add or tweak

- `detectFileProperties` - this is part-specified but only thinking about the happy path given a single file type. Think about scenarios where the file can't be read or isn't recognised. Other filetypes can be considered longer term? 
- `supplementaryDataSources` GET- e.g. uniprot, pubmed, GO, etc.
- `supplementaryDataSources` POST - save if defaults aren't correct and user changes them.
- `dataTools` GET - list tools appropriate to the user's data types
- `dataTools` POST - save if defaults aren't correct and user changes them.
- `mineConfig` POST - set url of new mine, privacy settings, licence
- `mineConfig` GET - list details known (if any) - this may initially seem like a set-only property in the wizard, but the getter is important too. Relevant if the user is going back and forth through the wizard or leaves and comes back, OR if potentially this is the second, third, fourth mine etc. and some info is already known, e.g. if their first mine was `MyFirstDatabase.AliceLab.intermine.org`, we can pre-populate the `.AliceLab.intermine.org`

## Questions / thoughts to ponder

- Authentication. We'll need to think about this some more (where in the process, does it use existing intermine mechanisms?)
