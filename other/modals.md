# Modals

```json
{
    "title": "My Modal Title",
    "description": "This Modal is my Modal. Don't take it away from me!",
    "buttons": Button[]
}
```

<table><thead><tr><th>Key</th><th>Type</th><th data-type="checkbox">Required</th><th>Description</th></tr></thead><tbody><tr><td>title</td><td>string</td><td>true</td><td>Title of the modal</td></tr><tr><td>description</td><td>string</td><td>true</td><td>Description of the modal</td></tr><tr><td>buttons</td><td>null | <a href="modals.md#undefined">Button</a>[]</td><td>false</td><td>Buttons</td></tr></tbody></table>

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

<table><thead><tr><th>Key</th><th>Type</th><th data-type="checkbox">Required</th><th>Description</th></tr></thead><tbody><tr><td>label</td><td>string</td><td>true</td><td>Label of the button</td></tr><tr><td>style</td><td>string</td><td>true</td><td>CSS class of the button</td></tr><tr><td>events</td><td>null | <a href="modals.md#undefined">ButtonEvent</a>[]</td><td>false</td><td>Buttons</td></tr></tbody></table>

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
