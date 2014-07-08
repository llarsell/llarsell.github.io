---
category: 'Public Traps Endpoints'
path: '/traps/{trap_id}/queue/'
title: "Accessing a Trap's Documents"
type: 'GET'

layout: nil
---

**GET -> Collection of Queue Items**

Returns a collection of all documents in a trap by trap_id. This endpoint returns just the documents from the trap (a trap's queue) and no trap representation. Use "next" and "prev" to page through content. When there are no more documents to be served (i.e. the end of the queue has been reached), status code 204 will be returned. 

**Call**:

    curl -u "<user_id>:<session_id>" \
    -L https://example.trap.it/api/v4/{org_slug}/traps/{trap_id}/queue/
  
**Response:**
  
    {
      "records": [
        {
          "origin": {
            "url": "https://example.trap.it/api/v4/{org_slug}/traps/{trap_id}/", 
            "section": null, 
            "id": "[trap_id]", 
            "name": "Adobe"
          }, 
          "liked": false, 
          "document": {
            "original": "http://feeds.mediapost.com/~r/online-media-daily/~3/HVzgVheQAIQ/hewlett-packard-enters-digital-analytics-space-for.html", 
            "display_image": true, 
            "author": null, 
            "images": {
              "sizes": [], 
              "original_url": null
            }, 
            "title": "Hewlett-Packard Enters Digital Analytics Space For Enterprise Market", 
            "published": 1381950725.0, 
            "custom_metadata": null, 
            "id": "[doc_id]", 
            "summary": "Hewlett-Packard entered the digital analytics space Wednesday to support marketing across platforms, media and content. The HP Digital Marketing Hub services offered through HP Autonomy..."
          }, 
          "relevancy": null, 
          "blacklisted": false, 
          "trapped": 1381956721.073197, 
          "url": "https://example.trap.it/api/v4/{org_slug}/traps/{trap_id}/queue/{doc_id}/", 
          "visible": true, 
          "read_later": false, 
          "document_overlay_title": null, 
          "read": false, 
          "featured": false, 
          "vector": "slings", 
          "source": {
            "url": "https://example.trap.it/api/v4/{org_slug}/traps/{trap_id}/", 
            "section": "Online Media Daily", 
            "id": "{trap_id}", 
            "name": "Media Post"
          }, 
          "document_overlay_images": {
            "sizes": [
              {
                "url": null, 
                "dimensions": "0x0"
              }
            ]
          }, 
          "disliked": false, 
          "document_overlay_summary": null, 
          "id": "[doc_id]", 
          "trap": {
            "url": "https://example.trap.it/api/v4/{org_slug}/traps/{trap_id}/", 
            "section": null, 
            "id": "[trap_id]", 
            "name": "Marketing Cloud"
          }
        },
	    ...
	    ...
      ], 
      "prev": "https://example.trap.it/api/v4/{org_slug}/traps/{trap_id}/queue/?before=1381782795.626091", 
      "next": "https://example.trap.it/api/v4/{org_slug}/traps/{trap_id}/queue/?after=1381956721.073197"
    }