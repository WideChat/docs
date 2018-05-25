# Complex Types

The complex types offer a more rich in-conversation experience than standard text messages by integrating buttons, images, links, and more, into an "element" alongside text in a single message. These types can be used for many purposes, such as displaying product information, asking the message recipient to choose from a pre-determined set of options, and showing search results.

## The Generic Type

The generic type is a simple structured message that combines various message components like title, subtitle, image, link, text body and up to three [buttons](../buttons) into an "element". You may also specify a defaultAction object that sets a URL that will be opened in a webview when the template is tapped. Multiple elements can be described in the `elements` array and displayed vertically.

The generic type contains these fields:

- `type`: must be "generic" (String)
- `elements`: An array of element objects that describe instances of the generic template to be sent.

The Elements array contains these fields:

- `title`: The title to display in the template. (String)
- `subtitle`: _(Optional)_  The subtitle to display in the template. (String)
- `imageUrl`: _(Optional)_ The URL of the image to display in the template. (String)
- `defaultAction`: _(Optional)_ The default action executed when the template is tapped. accepts the same properties as URL button, except title. (Object)
- `buttons`: _(Optional)_ An array of buttons to append to the template. A maximum of 3 buttons per element is supported.

```json
"payload": {
  "type": "generic",
  "elements":[
     {
        "title":"<TITLE_TEXT>",
        "imageUrl":"<imageUrl_TO_DISPLAY>",
        "subtitle":"<SUBTITLE_TEXT>",
        "defaultAction": {
            "type": "web_url",
            "url": "<DEFAULT_URL_TO_OPEN>",
            "webviewHeightRatio": "<COMPACT | TALL | FULL>"
        },
      "buttons":["<BUTTON_OBJECT>", 
                 "<BUTTON_OBJECT>", 
                 "<BUTTON_OBJECT>" ]      
    },
  ]
}
```

## The Carousel Type

Like the generic type, the carousel type combines various message components like title, text body, image, link, or buttons into an element in an elements array. **When there are multiple elements, the carousel displays them left to right with a slider.**


