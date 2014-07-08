---
category: 'Public Traps Endpoints'
path: '/public-traps/queue/'
title: 'Get all Public Content Items'
type: 'GET'

layout: nil
---

**GET -> Collection of Queue Items**

Returns a collection of the combined documents from all public traps. Use this endpoint to display content at the document level (create a wall of content on mixed subjects view). Each record has a `trap` attribute which contains information on each document's originating public trap including it’s resource URL. 

**Call**

    curl -L https://example.trap.it/api/v3/{org_slug}/public-traps/queue/ -X GET

**Response:**

    {
    "records": [
        {
         queue item representation
        },
        {
         queue item representation
        },
        …
        …
         ], 
      "prev": "https://example.trap.it/api/v4/{org_slug}/public-traps/queue/?before=1383833563.168672&size=100", 
      "next": "https://example.trap.it/api/v4/{org_slug}/public-traps/queue/?after=1383863087.285967&size=100"
    }
