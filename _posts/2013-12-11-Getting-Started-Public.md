---
title: 'Public Traps API'
type: 'GETTING STARTED'
path: ''


---
##Getting Started with the Public Traps API

The Public Traps API accesses public traps and their content. This REST API is for clients using Trapit to create public traps, dynamic, curated collections of content. Content can be displayed in a trap view (as topically grouped collections that mirror curator selections) or as a document queue (a single view of all content from all public traps mixed together). 

No authentication is needed to use the Public Traps API. All Trapit clients using public traps will receive a custom, organization specific URL base and org_slug (for the purposes of this documentation we will use the URL base "example.trap.it"). 

    -curl https://example.trap.it/api/v4/{org_slug}/public-traps/ -X GET

This documentation uses [cURL](http://curl.haxx.se/docs/manpage.html) to demonstrate content requests. Translating these examples into any other programming language is trivial. The key elements are, the URL, HTTP method, request body and response body. 



