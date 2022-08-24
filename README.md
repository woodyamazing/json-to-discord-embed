# json-to-discord-embed
Documentation for converting json to discord embed for woody bots™️

Bot slash command takes one argument - gist ID. The gist must be a json file.

# json Syntax

Example json file can be found [here](https://github.com/woodyamazing/json-to-discord-embed/blob/main/example-embed.json). 


You can include up to 10 embeds in a message, but don't forget to change their key value (e.g. "embed1", "embed2"...)

`{
    "embed1": [
        {"title": "EMBED TITLE [REQUIRED]", "description": "EMBED DESCRIPTION", "color": "COLOR"}
    ],
    "embed2": [
        {"title": "EMBED TITLE [REQUIRED]", "description": "EMBED DESCRIPTION", "color": "COLOR"}
    ]
}`

## The first dictionary is required and must be first

`{"title": "EMBED TITLE [REQUIRED]", "description": "EMBED DESCRIPTION", "color": "COLOR"}`

* **Title** required, must be 256 characters or fewer. 
* **Description** must be 4096 characters or fewer.
* **Color** side color of the embed. Gray is default.

> Available colors:
default, teal, dark_teal, green, dark_green, blue, dark_blue, purple, dark_purple, magenta, dark_magenta, gold, dark_gold, orange, dark_orange, red, dark_red, lighter_grey, dark_grey, light_grey, darker_grey, blurple, greyple

## Author
`{"type": "author", "name": "AUTHOR NAME [REQUIRED]", "url": "LINK TO AUTHOR", "icon url": "URL TO IMAGE OF AUTHOR"}`
* **name** required, must be 256 characters or fewer.
* **url** URL of the author
* **icon url** URL of author icon. Must be HTTP(S)

## Field
1 embed supports up to 25 fields.

`{"type": "field", "name": "FIELD NAME [REQUIRED]", "value": "FIELD VALUE", "inline": true}`

* **name** required, must be 256 characters or fewer.
* **value** required, must be 1024 characters or fewer.
* **inline** true/false choose if field should be inline or not.

## Image
`{"type": "image", "url": "URL TO IMAGE [REQUIRED]"}`

* **url** required, URL of the image. Must be HTTP(S)

## Thumbnail
`{"type": "thumbnail", "url": "URL TO THUMBNAIL [REQUIRED]"}`

* **url** required, URL of the image. Must be HTTP(S)

## Footer
`{"type": "footer", "text":"FOOTER TEXT [REQUIRED]"}`

# Formatting
## Adding links to text
`[This text will contain a link](https://buildtheearth.net/buildteams/251)`
## New line
To go to a new line, use `\n` `example text\nthis text will be on a new line`

example text

this text will be on a new line
