---
category: new stuff
path: '/new/post/'
title: 'Adding a post'
type: 'POST'

layout: nil
---

    curl -u "<user_id>:<session_id>" -L https://new/post/
    
**Example Response:** 

	{
      "short_host": "https://example.it/s/", 
      "integrated_directory": false, 
      "name": "Example", 
      "allow_public_traps": true, 
      "timezone": "US/Pacific", 
      "refresh_queues_on_feedback": null, 
      "slug": "[orgID]", 
      "host_name": "example.trap.it"
    }