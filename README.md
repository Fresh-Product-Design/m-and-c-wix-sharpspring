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
* Ensure `Add Code to Pages` is set to `All Pages > Load code on each new page`. This will ensure that the correct form loads when the user navigates the website.
* Ensure `Place Code In:` is set to `Body - End`.
