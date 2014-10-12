ToastedBits Gradle Scripts
=============

##Downstream Plugin
Easily detect which projects are depending on old/deprecated libraries
Keep projects more in sync
Most useful on large teams

Prerequisites
* Setup a neo4j server
* Edit the buildscript dependencies section to use your dependency manager (e.g. Artifactory, Nexus, Archiva, etc)
* Edit the default neo4j host to point to your team's neo4j server
* Ensure all projects have a version set
* Use Gradle for all projects' builds, apply the downstream.gradle plugin to each root project (can be applied via url or filesystem)

Usage
* Run "gradle reportUpstream" in all of your projects, preferably as part of a continous integration solution (e.g. Jenkins)
* Run "gradle showDownstream" to view downstream projects
* Access the neo4j database directly for complicated queries, or build your own UI using the neo4j REST API!
