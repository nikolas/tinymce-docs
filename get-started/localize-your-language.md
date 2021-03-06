---
layout: default
title: 11. Localize TinyMCE
description: Localize TinyMCE with global language capabilities.
keywords: internationalization localization languages
---

As developers we all hope our projects reach a wide audience, and for many of us they do. Which is why it is important that TinyMCE is easy to localize.

In this section of the Get Started guide we will show you how to change TinyMCE's user interface to suit your users' preferred language. The settings discussed in this section change the language that toolbar and menubar items, along with tooltips, are rendered in.


> Pro tip: language settings can be controlled in these configuration options: [directionality]({{ site.baseurl }}/configure/localization/#directionality), [language]({{ site.baseurl }}/configure/localization/#language) and  [language_url]({{ site.baseurl }}/configure/localization/#language_url). There is also a [Directionality Plugin]({{ site.baseurl }}/plugins/directionality/) that adds a toolbar button to control ltr-rtl behavior.

### Step 1

Go to our [language download page](http://archive.tinymce.com/i18n/index.php) (i18n), where you'll see a list of language packs for TinyMCE 4.

If you want to use one language only, click the download link on the far right of the table and you're done. If however you want to download multiple language packs, first check the box beside each language you need and then click the download button at the bottom of the table.

> Important note: the language packs provided via our language download page are translated by the TinyMCE community. We greatly appreciate their contribution!

### Step 2

Unpack the language `js` file(s) into your `path/to/tinymce/js/langs/` folder. Important: if you don't put the language pack in `js/langs/` the language settings will not work, unless you use the [language_url]({{ site.baseurl }}/configure/localization/#language_url) configuration option.

### Step 3

Set the language option in your TinyMCE configuration to the language code in the list on [this page]({{ site.baseurl }}/configure/localization/#language).

### Step 4

Confirm that the language has been set successfully by loading TinyMCE.



## A working example

We have prepared a code snippet below that would set TinyMCE's language to Chinese and text directionality right-to-left.

If you want to try it for yourself, [click here to directly download](http://archive.tinymce.com/i18n/download.php?download=zh_CN) the Chinese language pack. You'll also need a *local instance* of TinyMCE, which you can grab from our [downloads page](http://beta.tinymce.com/download/). Follow the [SDK install instructions]({{ site.baseurl }}/get-started/advanced-install/#sdkinstall) if you're not familiar with setting up TinyMCE locally.

```html
<!DOCTYPE html>
<html>
<head>
  <script src="js/tinymce.min.js"></script>
  <script type="text/javascript">
  tinymce.init({
    selector: 'textarea',
    language: 'zh_CN',
    directionality: 'rtl'
  });
  </script>
</head>

<body>
  <form method="post">
    <textarea>你好，世界!</textarea>
  </form>
</body>
</html>
```

{% assign_page next_page = "/get-started/system-requirements/index.html" %}
{% include next-step.html next=next_page %}
