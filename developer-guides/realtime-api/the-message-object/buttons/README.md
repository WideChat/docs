# Buttons

Buttons can invoke different types of actions. These buttons allow you to easily offer the message recipient actions they can take in response to the template, such as opening a webview, starting a payment flow, sending a postback message to your webhook, and more. *

The button object contains these fields:

- `type`: One of these "url", "webview", or "postback"
- `title`: Button title. (String)
- `url`: _(Required with url type)_ This URL is opened in a mobile browser when the button is tapped.  (String)
- `webUrl`: _(Required with webview type)_ This URL is opened in an integrated webview. The page view is in front of the chat window and it can be a configurably sized in conjunction with the `webviewHeightRatio` field.  (String)
- `webviewHeightRatio`: _(Optional with webview type)_ Height of the webview. Valid values: "compact", "tall", "full". Defaults to full.
- `payload`: _(Required with the postback type) This data will be sent back to your webhook. (String)
- `image`: _(Optional)_ Url to an image to be displayed in a button.

## url button type

The URL Button opens a web page in a mobile browser. This allows you to enrich the conversation with a web-based experience, where you have the full development flexibility of the web.

```json
"buttons":[
    {
      "type": "url",
      "url": "<URL_TO_OPEN_IN_MOBILE_BROWSER>",
      "title": "<BUTTON_TEXT>",
    },
]
```

## webUrl button type

The webview button opens an integrated webview where the page in the view is in front of the chat window and it's size can be configured.

```json
"buttons":[
    {
      "type": "webUrl",
      "webUrl": "<URL_TO_OPEN_IN_INTEGRATED_WEBVIEW>",
      "webviewHeightRatio": "<COMPACT | TALL | FULL>",
      "title": "<BUTTON_TEXT>",
      "image": "<URL_TO_IMAGE_DISPLAYED_IN_BUTTON"
    },
]
```

## postback button type

The postback button sends a message event to your webhook with the string set in the payload property. This allows you to take an arbitrary actions when the button is tapped.

```json
"buttons":[
    {
      "type": "postback",
      "title": "<BUTTON_TEXT>",
      "payload": "<STRING_SENT_TO_WEBHOOK>",
      "image": "<URL_TO_IMAGE_DISPLAYED_IN_BUTTON"
    },
]
```

`*` Buttons can be included within a '''buttons''' object inside the generic template or in a '''buttons template''' of it's own. 

## Resources

- [A Survey of Rich Messaging in Chatbots (buttons)](https://github.com/WideChat/Rocket.Chat.Android/wiki/A-Survey-of-Rich-Messaging-in-Chatbots#buttons)
