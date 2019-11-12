# JSON Ruleset Format for SQL Assessment API

This specification defines the JSON format which is used to describe rulesets for SQL Assessment API. One of those, the default ruleset, is shipped within the API. Users can additionally create their own rulesets, also called configuration files, and use them to override rules of the default ruleset or create their own ones. 

????? Read more about SQL Assessment API !!!HERE and find some simple examples of custom rulesets and how to run them with SQL Assessment !!!HERE and !!!HERE.

## Mandatory filling of configuration file

This snippet shows the least filling of a configuration file. Such a file will be just processed by SQL Assessment API but its application won't change anything.

```JSONC
{ 						// Absence of any key below will lead to a parsing error
	"schemaVersion": "1.0",			// Schema version is not verified in the current version of SQL Assessment. It's a string
	"version": "0.1",			// Ruleset version and name are properties to indetify a ruleset. It's a string
	"name": "Custom Ruleset",
	"rules":[]				// Array of rule objects
}
```

The snippet doesn't contain another very important property—`probes`—because it's not mandatory. Here's a snippet with it. 

```JSONC
{
	"schemaVersion": "1.0",			// Schema version is not verified in the current version of SQL Assessment. It's a string
	"version": "0.1",			// Ruleset version and name are properties to indetify a ruleset. It's a string
	"name": "Custom Ruleset",
	"rules":[],				// Array of rule objects
	"probes":{}				// Object to define implementations of probes
}
```

`rules` and `probes` are described in detail in further sections.

## `rules`

Rule is a unit of assessment that represents a best practice, policy, or 
