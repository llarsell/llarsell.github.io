###About this project page:

This API Documentation was built using [Carte](https://github.com/devo-ps/carte) a [Jekyll](http://jekyllrb.com/) based template. 

###Adding/Editing posts

All API methods and help articles live in the _posts file. They are md files with the naming convention YYYY-MM-DD-text-name and are sorted by date (recent first) (use imaginary dates to achieve the order you desire, it's a pain, yes). They begin with a YAML header like so:

---
category: 'Interactive Apps Endpoints'
path: '/shares/{share_id}/'
title: 'Sharing to Social Accounts: Sending a Share'
type: 'PUT'

---

|Header attribute|Description|
|----------------|-----------|
|category|Refers to the API the method or help article belongs to and determines how the method will be grouped in the navigation. Options are "Interactive Apps Endpoints", "Public Traps Endpoints", "Recommender Engine Endpoints", and "Getting Started"|
|path|The endpoint path (convention in this doc to only use the URL after the {org_slug}) for method posts. If not needed on help article posts use path:''|
|title|Title of the post (should describe the use case for method posts or the contents of a help article post).|
|type|The color coded method for method posts ('POST','PUT','GET','DELETE') or a free text "tag" for help articles (will show gray). Help articles can also omit a type.| 

###Formatting/Style Things that are Helpful

Linking from one post to another uses the format [text to link](#/text-part-of-file-name) where text-part-of-file-name is the post to be linked to's filename after the YYYY-MM-DD part.

Whitespace trailing rows in a table will seriously screw up formatting. Much pickier than most markdown editors are.

Navigation in the _includes folder and any new categories to be used in the YAML header must be accounted for there.