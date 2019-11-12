# JSON Ruleset Format for SQL Assessment API

This specification defines the JSON format which is used to describe rulesets for SQL Assessment API. One of those, the default ruleset, is shipped within the API. Users can additionally create their own rulesets, also called configuration files, and use them to override rules of the default ruleset or create their own ones. 

????? Read more about SQL Assessment API !!!HERE and find some simple examples of custom rulesets !!!HERE and !!!HERE.

## Mandatory filling of configuration file

```JSONC
{ 
	"schemaVersion": "1.0",
	"version": "0.1",
	"name": "Custom Ruleset", 
	"rules":[]
}
```
