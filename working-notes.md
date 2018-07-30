## Endpoints to add or tweak

- `detectFileProperties` - this is part-specified but only thinking about the happy path given a single file type. Think about scenarios where the file can't be read or isn't recognised. Other filetypes can be considered longer term?
- `saveFile` - important to upload / save file if only a preview of the file was uploaded initially.
- `supplementaryData` - need to add versions of the data in question, especially for part baked mines.  
- `dataTools` GET - list tools appropriate to the user's data types
- `dataTools` POST - save if defaults aren't correct and user changes them.
 `MyFirstDatabase.AliceLab.intermine.org`, we can pre-populate the `.AliceLab.intermine.org`
- `mineConfigs` GET - list of all partial or complete mine build configs associated with a given user/lab.
- `startBuild` POST - trigger the data build to start in the background, possibly while user is configuring other things. Required mine config id.
- `buildStatus` GET - return if still building or not. Useful for UI to know if it's time to show the full mine or a holding screen.
- `checkNameAvailability` POST - check this lab/mine name combination is available

## Questions / thoughts to ponder

- Authentication. We'll need to think about this some more (where in the process, does it use existing InterMine mechanisms?)
- can a browser take the first n lines of a file to send away for type detection? Y to investigate.
- `supplementaryDataSources` GET- Do we have this data annotated in such a way that we know what it is, programmatically? e.g. if a user uploads a set of mouse genes, do we know not to apply a worm disease expression data set if there are no worm homologues? (probably possibly genome assembly versions matter here too + other stuff?)
- how do we determine when a mine build is done? Maybe go to the url and present a loader if it's not live but is building. probably needs a service?
