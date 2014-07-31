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
          "document": {
            "author": "Jennifer Zaino", 
            "content_type": "text", 
            "id": "3d44227f2e0145e7892bc770614e73ae", 
            "images": {
              "original_url": "http://semanticweb.com/wp-content/uploads/2014/07/synthimage.jpg", 
              "sizes": [
                {
                  "dimensions": "367x312", 
                  "url": "http://images.staging.trap.it/sizes/orig/3d44227f2e0145e7892bc770614e73ae.jpeg"
                }, 
                {
                  "dimensions": "320x272", 
                  "url": "http://images.staging.trap.it/sizes/320/3d44227f2e0145e7892bc770614e73ae.jpeg"
                }
              ]
            }, 
            "original": "http://semanticweb.com/digital-reasoning-takes-early-risk-detection-compliance-security-sensitive-sectors_b43808", 
            "published": 1406540225.0, 
            "summary": "Digital Reasoning\u2019s Synthesys machine learning platform (which The Semantic Web Blog initially covered here) this summer should\u00a0see its Version 3.9 release. The update will build on the 3.8...", 
            "title": "Digital Reasoning Takes On Early Risk Detection For Compliance- And Security-Sensitive Sectors"
      }, 
          "document_overlay_image_url": null, 
          "document_overlay_images": {
            "sizes": [
              {
                "dimensions": null, 
                "url": null
              }
            ]
          }, 
          "document_overlay_summary": null, 
          "document_overlay_title": null, 
          "id": "6e224516081e40c7a517fa68dd64869d-3d44227f2e0145e7892bc770614e73ae", 
          "trap": {
            "id": "[trap_id]", 
            "method": null, 
            "name": "semantic web", 
            "section": "", 
            "type": "topic", 
            "url": "https://example.trap.it/api/traps/{trap_id}/"
          }, 
          "trapped": 1406586819.992331, 
          "url": "https://example.trap.it/api/{org_slug}/traps/{trap_id}/queue/{doc_id}/"
        }, 
        …
        …
         ], 
      "prev": "https://example.trap.it/api/v4/{org_slug}/public-traps/queue/?before=1383833563.168672&size=100", 
      "next": "https://example.trap.it/api/v4/{org_slug}/public-traps/queue/?after=1383863087.285967&size=100"
    }
