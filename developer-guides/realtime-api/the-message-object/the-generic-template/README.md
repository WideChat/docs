# The Generic Template

The generic template specifies the information to expect in the payload object when the attachment.template_type is set to "generic".

The payload object can contain several fields:
- `elements`: A collection of element objects
- `image_aspect_ratio`: _(Optional)_ The aspect ratio used to render images specified by element.image_url. Must be horizontal (1.91:1) or square (1:1). Defaults to horizontal.

An element object can contain several fields:
- `title`: The title to display in the template. 80 character limit.
- `subtitle`: _(Optional)_ The subtitle to display in the template. 80 character limit.
- `image_url`: _(Optional)_ The URL of the image to display in the template.
- `default_action`: _(Optional)_ The default action executed when the template is tapped. Accepts the same properties as URL button, except title.
- `buttons`: _(Optional)_ An array of [buttons][1] to append to the template. A maximum of 3 buttons per element is supported.

[1]:../buttons
