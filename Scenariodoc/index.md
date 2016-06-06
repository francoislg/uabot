# Documentation for the usage analytics bot configuration file format

This is the documentation index file for all the possible options of the data generation bot.
This file should be kept up to date with the changes, otherwise contact the author.

## General parameters

Parameters that are necessary are in **bold**, otherwise there is a default value in defaults\defauls.go
Parameters that are optional without a default value are in *italics*

Parameter | Type | Usage | Default
------------ | ------------- | ---------------- | -----------------
*orgName* | string | The name of the cloud org | (none)
searchendpoint | string | Endpoint where to direct the search queries | https://cloudplatform.coveo.com/rest/search/
analyticsendpoint | string | Endpoint where to direct the usage analytics events | https://usageanalytics.coveo.com/rest/v15/analytics/
**randomGoodQueries** | []string | The dataset of random queries (good ones) | ""
**randomBadQueries** | []string | The dataset of random queries (bad ones) | ""
**scenarios** | []Scenarios | The dataset of scenarios to execute | (none) See below
timeBetweenVisits | number | The time to wait between each visits (between 0 and X seconds) | 120 seconds
timeBetweenActions | number | The time to wait between each actions (between 0 and X seconds) | 3 seconds
*pipeline* | string | The name of the pipeline the queries will use | (none)
*defaultOriginLevel1* | string | The name of the originLevel1 param by default | (none)
partialMatch | boolean | Enable partial match on the queries | false
partialMatchKeywords | number | Number of words after which to enable partial match | (none)
partialMatchTreshold | string | Number of words considered in a partial match (string because you can send "50%") | (none)
allowAnonymousVisits | boolean | If you allow some of the visits to be anonymous | false
anonymousTreshold | number | Number between 0 and 1 of the % of anonymous visits | 0
globalfilter | string | A filter to be applied to all queries | ""
languages | []string | A list of random languages for the visits | (none)