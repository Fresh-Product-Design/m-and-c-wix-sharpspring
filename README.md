# M & C Communications Wix + Sharpspring

Custom code and instructions for how the Wix + SharpSpring integration works

To support the SharpSpring forms in the Wix website, the custom scripts need to be loaded in the website document's
body, at the end.

# Installation Instructions

To add this custom code:

* Navigate to the [Site Settings](https://manage.wix.com/dashboard/aa482a64-f245-4add-9f72-20be722a1e05/settings/)
* Scroll down and choose Advanced > Custom Code
* Scroll down to find the `Body - End` section. You should see an existing `SharpSpring Universal Contact Form Code`
  configuration.
* To make changes, click the "more menu" button and paste in your updated code
  from `/lib/sharpspring-custom-code-body.html`. Ensure both `<script>` tags are copied and pasted (the custom code a
  well as the external SharpSpring script).
* Ensure `Add Code to Pages` is set to `All Pages > Load code on each new page`. This will ensure that the correct form
  loads when the user navigates the website.
* Ensure `Place Code In:` is set to `Body - End`.

# Alternative Installation:

Create your own iFrame in Wix! This is what SharpSpring is doing behind the scenes, so we can just grab the URL and use
it directly in Wix, which is something Wix is good at handling.

Using this approach, you can actually see your form in the UI, rather than a placeholder paragraph tag.

Example URL

```
https://app-3qnnp6zq9u.marketingautomation.services/forms-proxy/MzawMLEwMTA1BAA/MzEwNU0xTk7RtTQzStE1MTew0E00tjDVNUkxsUi2TDFNMU0zAQA?_tk=202101|5fff2c42ea83c164515ac9e9&instance=eiyvz9
```

where the URL is in the format of:

`[domain]/forms-proxy/[accountId]/[formId]?instanceId=[instanceId]&_tk=[trackingCookie]`

and the values are:
`domain = app-3QNNP6ZQ9U.marketingautomation.services`
`accountId = MzawMLEwMTA1BAA`
`instanceId = Math.random().toString(36).substring(7)`
`trackingCooke = the tracking cookie, if present`

`formId = (one of the following form IDs)`

* GENERAL_CONTACT_ID = `S7JINEy0tEzTTTOwNNM1MTJL0U1MNjIBco0NjA3NDdIsUxIB`
* CBD_CONTACT_ID = `MzEwNU0xTk7RtTQzStE1MTew0E00tjDVNUkxsUi2TDFNMU0zAQA`
* CRISIS_CONTACT_ID = `S0q2TDYwSTPVtTAxMtM1sTBN1k0yMDLQTQXyUw0sEhONU1MA`
* MEDIA_CONTACT_ID = `M0sxMkk0SzPTNTBONtE1STGw0LU0ME7VTTUzSjQ2MzUxMDYyBQA`
* LIVE_EVENT_ID = `MzM2TjQ1TErStUxMMtQ1MQUSFhZJJromScaJ5onGximWRgYA`
