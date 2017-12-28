This repository reproduce an issue found With Visual Studio 2017 15.5.2 
and Visual Studio 2017 15.6.0 Preview 1.1 where properties defined in project 
schema definitions do not show up in a solution with multiple projects.

[[custom.xml]] contains the definition for a simple ProjectSchemaDefinitions
[[custom.targets]] includes the custom schema definition 

[[Single]] A solution with a single project that imports the custom schema
definition

![Single project screenshot](https://github.com/pepone/projectschema/raw/master/screenshots/single-properties.png)

[[Multi]] A solution with a two projects one that imports the custom schema
definition and one that not

![Multi project screenshot](https://github.com/pepone/projectschema/raw/master/screenshots/multi-properties.png)

The ConsoleApplication1 project is the same in both cases and as show in the screenshoots
the custom properties only show up in the case that there is one project in the solution.

With older Visual Studio versions including 2013, 2015 the properties show up in both
solutions.
