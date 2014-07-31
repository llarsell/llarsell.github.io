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
 * ?category_id=[String]: Only traps belonging to the category with that ID will be returned.
 * ?pretty=[Boolean]: If true, results will be returned formatted.  
 
**Call**

    curl -L https://example.trap.it/api/{org_slug}/public-traps/?type=bundle&pretty=true -X GET

**Response:**

    {
      "records": [
        {
         "active": true, 
         "categories": [
           {
            "id": "[category_id]", 
            "name": "Science" 
            }
          ], 
         "created": 1403895387.098887, 
         "featured": false, 
         "id": "[trap_id]", 
         "last_updated": null, 
         "name": "Microsoft", 
         "public": true, 
         "type": "bundle", 
         "url": "https://st1.staging.trap.it/api/{org_slug}/traps/{trap_id}/"
        },
    ... 
    ...
     "prev": "https://example.trap.it/api/{org_slug}/public-traps/?before=1378812046.945051&size=12", 
     "next": "https://example.trap.it/api/{org_slug}/public-traps/?after=1381245869.187704&size=12"
    }


