## Endpoints to add


- `dataTools` POST - save if defaults aren't correct and user changes them.
- `mineConfigs` GET - list of all partial or complete mine build configs associated with a given user/lab.

## Questions / thoughts to ponder

- Authentication. We'll need to think about this some more (where in the process, does it use existing InterMine mechanisms?)
- can a browser take the first n lines of a file to send away for type detection? Y to investigate.
- `supplementaryDataSources` GET- Do we have this data annotated in such a way that we know what it is, programmatically? e.g. if a user uploads a set of mouse genes, do we know not to apply a worm disease expression data set if there are no worm homologues? (probably possibly genome assembly versions matter here too + other stuff?). We also need to add versions of the data in question, especially for part baked mines.
- `File/Properties/detect` - this is part-specified but only thinking about the happy path given a single file type. Think about scenarios where the file can't be read or isn't recognised. Other filetypes can be considered longer term?
- sometimes will be able to parse first n lines, other times (i.e. gff) w will need to upload the whole file to get all possible column mappings. Need to prototype performance. 
- should we indicate to the user that there is a certain level of certainty when detecting fields? ie.e very sure, best guess mapping, etc. 
