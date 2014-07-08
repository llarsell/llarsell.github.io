---
category: 'Public Traps Endpoints'
path: '/public-traps/'
title: 'Get all Public Traps'
type: 'GET'

layout: nil
---

**GET -> Collection of Public Traps**

Returns a collection of all public traps. Use this endpoint to display content at the trap level. Use attributes `prev` and `next` to page through results. Each trap returned will contain a `url` containing the resource URL for that individual trap. 

**Optional Query Parameters:**

 * ?size=[Integer]: Specify the number of trap records to return per page.
 * ?orphaned-only=[Boolean]: If true, only traps that haven’t been assigned to a section/category will be returned.
 * ?type=[String]: Use “bundle” to ensure only bundle type traps are returned.
 * ?pretty=[Boolean]: If true, results will be returned formatted.  
 
**Call**

    curl -L https://example.trap.it/api/v4/{org_slug}/public-traps/?type=bundle&pretty=true -X GET

**Response:**

    {
      "records": [
        {
          trap representation
        },
        {
          trap representation
        },  
    ... 
    ...
     "prev": "https://example.trap.it/api/v4/{org_slug}/public-traps/?before=1378812046.945051&size=12", 
     "next": "https://example.trap.it/api/v4/{org_slug}/public-traps/?after=1381245869.187704&size=12"
    }


