Google Tag Manager Container code
============
Implementation guide for proper Google Tag Manager container code. In advance of implementing the Google Tag Manager code you should check if you have received the necessary container ID from you Orangevalley point of contact. When referred to Google Tag Manager container you should use the script within [GTM_standardScript.js](https://github.com/orangevalley/GTM_standard/blob/master/GTM_standardScript.js).

## Background
Google Tag Manager is a free tool that eliminates tedious code-editing tasks for your website. The easy-to-use web interface lets your marketing colleagues add and update their own website tags—including javascript code snippets for conversion tracking, site analytics, remarketing and more. They can do it all without bothering you, leaving you time to focus on other (more) important work.
The basic Google Tag Manager container looks like:

```javascript
<!-- Google Tag Manager -->
<noscript><iframe src="//www.googletagmanager.com/ns.html?id=GTM-XXXXXX"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'//www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-XXXXXX');</script>
<!-- End Google Tag Manager -->
```
## Benefits of Google Tag Manager
- IT-friendly – Google Tag Manager has lots features to set your mind at ease—like user permissions, automated error checking,the Debug Console, and asynchronous technology. So everything runs efficiently, with no unpleasant surprises.
- Quick	and	easy – Users add or change tags whenever they want, to 
keep sites running smoothly and quickly. Tags are managed with an easy-to-use web interface, so there’s no need to write or rewrite site code following implementation.
- Verified	tags	&	templates – Google Tag Manager makes it easy to verify that new tags are working properly, so users don’t need to call on IT to check the tags. Built-in tag templates and automatic error checking also prevent tags with improper formatting from even being deployed on your site. With support of the expert knowledge of OrangeValley (a Google Tag Manager certified partner) a fail safe system of managing and deploying tag will be setup.
- Swift	loading – Google Tag Manager can replaces all your measurement and marketing tags with a single, asynchronously loading tag—so your tags can fire faster without getting in each other’s way.
- Multi-platform – Google Tag Manager works for mobile sites, mobile apps and Google's building support for other platforms as well.

## Implementation
The Google Tag Manager container snippet is a small piece of JavaScript and non-JavaScript code that you paste into your pages. It enables Tag Manager to fire tags by inserting gtm.js into the page (or through the use of an iframe when JavaScript isn't available).

To implement Google Tag Manager, copy the code snippet provided within [GTM_standardScript.js](https://github.com/orangevalley/GTM_standard/blob/master/GTM_standardScript.js), **replacing both instances of GTM-XXXXXX** with your container ID (supplied separately by OrangeValley). Paste this snippet into your website template page so that it appears immediately after the opening < body > tag.

```javascript
<!-- Google Tag Manager -->
<noscript><iframe src="//www.googletagmanager.com/ns.html?id=GTM-XXXX"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'//www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-XXXX');</script>
<!-- End Google Tag Manager -->
```
You will find the first instance which has to be replaced by the proper container ID at the beginning of the Google Tag Manager code:

```javascript
src="//www.googletagmanager.com/ns.html?id=GTM-XXXX"
```

And the second instance which has to be replaced by the proper container ID at the end of the Google Tag Manager code:

```javascript
window,document,'script','dataLayer','GTM-XXXX')
```

_**Note:** The Google Tag Manager snippet must be placed directly in the page that you intend on tracking. Placing it in a hidden iframe or deploying it within another tag management system will prevent certain tags from accurately tracking the parent page. Placing the Google Tag Manager snippet in a <div> may result in the same issues._

## Verify your implementation
You can verify the (basic) implementation by using a specific Google Chrome plugin. This plugin, called Tag Assistant, will report if the implementation of the Google Tag Manager code is correct or any warnings/errors could interfere with the correct function of the Google Tag Manager.

[Tag Assistant - Google Chrome](https://chrome.google.com/webstore/detail/tag-assistant-by-google/kejbdjndbnbjgmefkgdddjlbokphdefk?hl=en)

### Troubleshooting
If you run in to any problems; for instance the Tag Assistant is reporting issues or errors. Please:

- Refer to the [Google Tag Manager Quick Start Guide](https://developers.google.com/tag-manager/troubleshooting)
- [Google Tag Manager Troubleshooting information](https://developers.google.com/tag-manager/troubleshooting)
- Get in touch with your [OrangeValley](http://orangevalley.nl/) Point of contact or send a message to support _at_ orangevalley _dot_ nl.

## Additional information
[Google Tag Manager support website](https://developers.google.com/tag-manager/quickstart)

# Version History
- 1 (October 1 - 2012): Initial release of the Google Tag Manager container code by Google
- 1.01 (September 23 - 2015): Update on implementation

