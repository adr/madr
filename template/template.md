# Agent Reporting and Viewing

* Status: proposed
* Deciders: 
* Date: 2019-11-15

Technical Story: https://jira.redventures.net/browse/FLEX-302

## Context and Problem Statement

Twilio provides valuable tools for collection and analysis of agent metrics.  Unfortunately, most of those are locked behind admin permissions through Flex and Ytica.  How can we allow anyone, project owners, performance coaches, and sales professionals, to be able to see their relevant analytics?

## Decision Drivers <!-- optional -->

* [driver 1, e.g., a force, facing concern, …]
* [driver 2, e.g., a force, facing concern, …]
* … <!-- numbers of drivers can vary -->

## Considered Options

* Extract Data through Flex Insights
* Work with Twilio to Add Permissions
* Scrub Page and Grab IFrame Elements

## Pros and Cons of the Options

### Extract Data through Flex Insights

Extract data in a csv through Flex Insights, then display the data using Chart.js.

* + Enactable now without giving more permissions/access
* + Maintains the same reports and display information
* + Allows us flexibility in displaying data
* 0 Uses chart.js, which looks a little different
* - More manual process; have to setup each chart

### Work with Twilio to Add Permissions

Collaborate with Twilio to add more nuanced permissions to individual reports.

* + Allows for using Twilio's generated reports
* + Twilio is moving toward more granular permissions
* + Allows us flexibility in displaying data
* - Not available to us for at least several months

### Scrub Page and Grab IFrame Elements

Use an AWS service or Lamdba to access the iframe that Twilio builds containing the report, grab the HTML elements displaying the chart, and make the iframe visible through the service's endpoint.

*  + Allows for exact same look and feel
* - Time-consuming to construct scrubber
* - Requires an additional ECS/Lamdba
* - Very rigid and subject to breakage on changes
* - Passes through login credentials in some form




## Decision Outcome

Chosen option: "[option 1]", because [justification. e.g., only option, which meets k.o. criterion decision driver | which resolves force force | … | comes out best (see below)].

### Positive Consequences <!-- optional -->

* [e.g., improvement of quality attribute satisfaction, follow-up decisions required, …]
* …

### Negative Consequences <!-- optional -->

* [e.g., compromising quality attribute, follow-up decisions required, …]
* …
