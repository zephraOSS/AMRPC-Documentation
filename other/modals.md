# Modals

```json
{
    "id": "my_modal_title"
    "title": "My Modal Title",
    "description": "This Modal is my Modal. Don't take it away from me!",
    "priority": true,
    "i18n": {
        "de_DE": i18n
    },
    "buttons": Button[]
}
```

<table><thead><tr><th>Key</th><th>Type</th><th data-type="checkbox">Required</th><th>Description</th></tr></thead><tbody><tr><td>title</td><td>string</td><td>true</td><td>Title of the modal</td></tr><tr><td>description</td><td>string</td><td>true</td><td>Description of the modal</td></tr><tr><td>priority</td><td>boolean</td><td>false</td><td>Whether a window should be created if none is open</td></tr><tr><td>i18n</td><td><a href="modals.md#undefined">i18n</a></td><td>false</td><td>Localization for title and description</td></tr><tr><td>buttons</td><td><a href="modals.md#undefined">Button</a>[]</td><td>false</td><td>Buttons</td></tr></tbody></table>

### Button data

```json
{
    "label": "Close",
    "style": "btn-red",
    "events": [
        {
            "name": "click",
            "type": "close"
        }
    ]
}
```

<table><thead><tr><th>Key</th><th>Type</th><th data-type="checkbox">Required</th><th>Description</th></tr></thead><tbody><tr><td>label</td><td>string</td><td>true</td><td>Label of the button</td></tr><tr><td>style</td><td>string</td><td>true</td><td>CSS class of the button</td></tr><tr><td>events</td><td><a href="modals.md#undefined">ButtonEvent</a>[]</td><td>false</td><td>Buttons</td></tr></tbody></table>

### ButtonEvent data

```json
{
    "name": "click",
    "type": "close"
}
```

<table><thead><tr><th>Key</th><th>Type</th><th data-type="checkbox">Required</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>string</td><td>true</td><td>Name of the <a href="https://www.w3schools.com/jsref/dom_obj_event.asp">event listener</a></td></tr><tr><td>type</td><td>string</td><td>false</td><td>Which <a href="modals.md#undefined">action </a>to trigger at (e.g.) "click"</td></tr><tr><td>value</td><td>string</td><td>false</td><td>JS code as string</td></tr></tbody></table>

{% hint style="danger" %}
Use **type** OR **value** - **not** both!
{% endhint %}

#### ButtonEvent types

* close
* delete

### i18n data

```json
{
    "title": "...",
    "description": "...",
    "buttons": {
        "Close": "..."
    }
}
```

<table><thead><tr><th>Key</th><th>Type</th><th data-type="checkbox">Required</th><th>Description</th></tr></thead><tbody><tr><td>title</td><td>string</td><td>true</td><td>Title of the modal</td></tr><tr><td>description</td><td>string</td><td>true</td><td>Description of the modal</td></tr><tr><td>buttons</td><td>Object</td><td>false</td><td>The original label as key and the translated label as value</td></tr></tbody></table>
