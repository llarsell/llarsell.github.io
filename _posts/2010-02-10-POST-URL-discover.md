---
category: 'Recommender Engine Endpoints'
path: '/url-discover/'
title: 'Recommendations Based on an Example Document'
type: 'POST'

layout: nil
---

**POST -> Collection of Documents**

Returns a selection of documents based on analysis of an example document. The URL to an example document is included in the request body. Good example document URLs will point to a single post or article. Top domain URLs will result in unfocused or no results.

**Request Body Accepts:**

|Attribute|Description|Type|
|-------|---------|--------|
|url|URL to an example document from which results are based off of. Required|String|
|num_docs|Indicated the number of documents to be returned. Optional|Int|
|quality|Quality score from 1-100. 100 indicates "a-list" sources. Optional Optional.|Int|
|images_only|If true, requires that returned documents have images. Optional|Boolean|

**Example:**

    curl -u "<user_id>:<session_id>" -L https://example.trap.it/api/v4/{org_slug}/url-discover/ \
    -X POST -d '{"url":"http://www.nytimes.com/2013/10/31/us/politics/ban-on-discrimination-against-gays-gains-ground-in-senate.html", "num_docs":3}'

**Example Response:**

    {
      "records": [
        {
          "original": "http://www.nytimes.com/2013/10/31/us/politics/ban-on-discrimination-against-gays-gains-ground-in-senate.html?partner=rss&emc=rss", 
          "display_image": true, 
          "author": "By JEREMY W. PETERS", 
          "images": {
            "sizes": [], 
            "original_url": null
          }, 
          "title": "Ban on Discrimination Against Gays Gains Ground in Senate", 
          "published": 1383148478.0, 
          "custom_metadata": null, 
          "id": "[trap_id]", 
          "summary": "Senator Joe Manchin III\u2019s for the Employment Nondiscrimination Act puts it within one vote of gaining the support it needs to overcome a filibuster.\u00a0\u00a0\u00a0\u00a0"
        }, 
     {
          "original": "http://www.nytimes.com/2013/11/05/us/politics/bill-on-workplace-bias-appears-set-to-clear-senate-hurdle.html?partner=rss&emc=rss", 
          "display_image": true, 
          "author": "By JEREMY W. PETERS", 
          "images": {
            "sizes": [], 
            "original_url": null
          }, 
          "title": "Bill on Workplace Bias Appears Set to Clear Senate Hurdle", 
          "published": 1383580741.0, 
          "custom_metadata": null, 
          "id": "[trap_id]", 
          "summary": "A measure that would add sexual orientation and gender identity to federal nondiscrimination law has gained its 60th supporter in the Senate.\u00a0\u00a0\u00a0\u00a0"
        }, 
        {
          "original": "http://www.latimes.com/nation/politics/politicsnow/la-pn-republican-support-enda-senate-20131104,0,7022384.story?track=rss", 
          "display_image": true, 
          "author": "By Michael A. Memoli", 
          "images": {
            "sizes": [
              {
                "url": "http://images.higgs.trap.it/sizes/orig/681116bfa88c4c54bc258f195adc4d7e.jpeg", 
                "dimensions": "599x384"
              }, 
              {
                "url": "http://images.higgs.trap.it/sizes/320/681116bfa88c4c54bc258f195adc4d7e.jpeg", 
                "dimensions": "320x205"
              }
            ], 
            "original_url": "http://www.trbimg.com/img-5277d06e/turbine/la-pn-republican-support-enda-senate-20131104-001/599"
          }, 
          "title": "Republican support pushes gay rights bill closer to Senate passage", 
          "published": 1383583860.0, 
          "custom_metadata": null, 
          "id": "[trap_id]", 
          "summary": "WASHINGTON -- A gay rights bill appears set to overcome a key Senate hurdle Monday, after a fifth Republican expressed support for the measure to prohibit workplace discrimination on the basis of..."
        }
      ]
    }
