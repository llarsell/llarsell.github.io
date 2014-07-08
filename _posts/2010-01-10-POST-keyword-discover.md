---
category: 'Recommender Engine Endpoints'
path: '/keyword-discover/'
title: 'Recommendations Based on a Keyword'
type: 'POST'

layout: nil
---

**POST -> Collection of Documents**

Returns a selection of documents based off of keyword(s). 

**Request Body Accepts:**

Attribute|Description|Type|
|-------|---------|--------|
|keywords|keywords used to discover documents. Required|String|
|num_docs|Indicated the number of documents to be returned. Optional|Int|
|quality|Quality score from 1-100. 100 indicates "a-list" sources. Optional Optional.|Int|
|images_only|If true, requires that returned documents have images. Optional|Boolean|

**Example**:

    curl -u "<user_id>:<session_id>" -L https://example.trap.it/api/v4/{org_slug}/keyword-discover/ \
    -X POST -d '{"keywords":"basketball", "quality":100, "num_docs":3}'

**Example Response:**

    {
      "records": [
        {
          "original": "http://rushthecourt.net/2013/04/08/acc-m5-04-08-13-edition/", 
          "display_image": true, 
          "author": "mpatton", 
          "images": {
            "sizes": [], 
            "original_url": null
          }, 
          "title": "ACC M5: 04.08.13 Edition", 
          "published": 1365424298.0, 
          "custom_metadata": null, 
          "id": "[trap_id]", 
          "summary": "Great selection and low prices on quality Basketball Backboards from Robbins Sports.\n\nAt Sports Unlimited Inc we carry more basketball equipment than anyone. Browse more then 100 basketball hoops!..."
        }, 
        {
          "original": "http://feedproxy.google.com/~r/Hoopsfix/~3/8ZpGdNuAxBY/", 
          "display_image": true, 
          "author": "Sam Neter", 
          "images": {
            "sizes": [
              {
                "url": "http://images.higgs.trap.it/sizes/orig/c11a42f0e9504faea02461b544c7adc4.png", 
                "dimensions": "234x130"
              }, 
              {
                "url": "http://images.higgs.trap.it/sizes/320/c11a42f0e9504faea02461b544c7adc4.png", 
                "dimensions": "320x177"
              }
            ], 
            "original_url": "http://www.hoopsfix.com/wp-content/uploads/2013/10/John-Amaechi-234x130.png"
          }, 
          "title": "John Amaechi Talks British Basketball at NBA Manchester", 
          "published": 1381262051.0, 
          "custom_metadata": null, 
          "id": "[trap_id]", 
          "summary": "John Amaechi talks at the NBA Global Games 2013 in Manchester about British Basketball \u2013 his relationship with England Basketball and Great Britain Basketball, the current state of affairs,..."
        }, 
        {
          "original": "http://www.hoopsworld.com/college-basketball-coaches-salary-database?utm_source=rss&utm_medium=rss&utm_campaign=college-basketball-coaches-salary-database", 
          "display_image": true, 
          "author": "HOOPSWORLD", 
          "images": {
            "sizes": [
              {
                "url": "http://images.higgs.trap.it/sizes/orig/8a282b423b354108b341a3f138ac25fc.jpg", 
                "dimensions": "600x50"
              }
            ], 
            "original_url": null
          }, 
          "title": "College basketball coaches salary database", 
          "published": 1365008408.0, 
          "custom_metadata": null, 
          "id": "[trap_id]", 
          "summary": "Which team will win the 2013 Final Four?"
        }
      ]
    }
