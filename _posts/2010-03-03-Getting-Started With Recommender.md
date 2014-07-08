---
title: 'Recommender Engine API'
type: 'GETTING STARTED'
path: ''
layout: nil
---

##Getting Started with the Recommender Engine API

Interact programatically with Trapit’s recommendation engine and source library. Use this API to layer relevant recommendations (“more like what I’m reading!”) over content in your website or app, suggest recommended articles based on keywords or document URLs supplied by a user or program. 

The recommender engine API draws from Trapit's library of high quality Internet sources. Trapit combines technology with human expertise to identify, qualify, and catalogue the sources in its library. Trapit's sources produce original content, have honest presentation, are freely accessible, and cover an extremely wide variety of subject categories. Trapit is publisher friendly, driving traffic to the sources within our library.

Sources within our library have been evaluated for quality and authority. Trapit presently has two classes of content;  high quality or “a-list” content (comprising 20% of our sources) and less high quality (that meets our baseline) “b” content (comprising 80%). This metadata translates to a filtering option in the recommender API (for example, make a request that returns only allow "a-list" content). 

**Trapit’s a-list sources:**

* Account for who they are and/or where their information is coming from.
* Have reliable, subject matter expert authors.
* Contain original and in depth information and a consistent subject or theme.
* Often have a reputation; established publications or respected institutions.
* Are not trying to sell anything (idea or object).

##Authentication to the API

Access to the Trapit's API uses HTTP Basic Auth over SSL. Organizations will receive a custom, organization specific URL and org_slug (for the purposes of this documentation we will use the URL base "example.trap.it") as well as an "auth_id" and "auth_secret" to be used for authentication.

###/v4/{org_slug}/auth/basic/verify/

**POST credentials -> token**

Returns auth token.		

Attribute | Required | Description
------|-------|--------|
auth_id	|Yes | Email Address of registered User
auth_secret | Yes | Password


**Curl Example (Authentication)**

    curl --insecure -d '{"auth_id":"user@trapit.com","auth_secret":"myPassword"}' \
    https://example.trap.it/api/v4/{org_slug}/auth/basic/verify/

**JSON Response Example**

    {
    "session": “[session id],
    "user_id": “[user id]”
    }

All other calls to the recommender engine API can now take the format:

    curl -u ‘<user_id>:<session_id>’ -L "https://example.trap.it/api/v4/{org_slug}/foo/
 