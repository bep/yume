# Yume

Yume is a minimalist blog theme for Hugo.

* Minimalist design
* Disqus
* Code highlighting
* Google Analytics
* Twitter card
* Android Chrome browser toolbar color

## Screenshot

![Screenshot](https://github.com/nrechn/yume/raw/master/images/screenshot.png)

## Installation & Usage

Clone this repository into `themes` directory of your Hugo site:

```
cd themes
git clone https://github.com/nrechn/yume
```

Serve your Hugo site with MTL Pure theme:

```
hugo server -t yume
```

## Configuration

The following is the example of [`config.toml`](https://github.com/nrechn/yume/blob/master/exampleSite/config.toml).

```
baseurl = "/"
languageCode = "en-CN"
title = "Yume"
disqusShortname = "foo"
Copyright = ""

[Params]
subtitle = "進み続けてさえいれば、遅くとも関係ない"
footerlinks = true
about = "/about"
twitter = "https://twitter.com"
github = "https://github.com"
telegram = "https://telegram.org"
showsRSS = true
analytics = "UA-XXXXXXXX-X"
twitterShortname = "foo"
themeColor = "#9b4dca"
```

Details of each parameter are as follows.

| Parameter | Required | Comment |
| :--- | :--- | :--- |
| baseurl | yes | Enter the base url of your site. |
| languageCode | yes | Enter the language code of HTML. Example: en, ja. |
| title | yes | Enter the title of your site. |
| disqusShortname | no | Enter the short name of your disqus account. If you do not enter, disqus section will be hidden. |
| Copyright | no | Enter copyright information for your site. It will be displayed in footer. |
| subtitle | yes | Enter the subtitle of your site. |
| footerlinks | yes | Enter true if you want to enable `Extra Info` in footer. It contains links of `About`, `Twitter`, `GitHub`, `Telegram`, `Subscribe`. If you enter false or nothing, `Extra Info` section will not appear in footer. |
| about | no | Enter the URL of your `about page`. If you enter nothing, `About link` will not appear in footer. |
| twitter | no | Enter the URL of your `Twitter page`. If you enter nothing, `Twitter link` will not appear in footer. |
| github | no | Enter the URL of your `GitHub page`. If you enter nothing, `GitHub link` will not appear in footer. |
| telegram | no | Enter the URL of your `Telegram.me page`. If you enter nothing, `Telegram link` will not appear in footer. |
| showsRSS | no | Enter true to enable RSS subscribe. If you enter false or nothing, `Subscribe link` will not appear in footer. |
| analytics | no | Enter the tracking ID of Google analytics. If you do not enter, the analysis will be skipped. |
| twitterShortname | no | Enter the Twitter @username. Twitter card feature requires this parameter. |
| themeColor | no | Enter the hex color code. It is used to change toolbar color (address bar and header color) on Android Chrome browser. |

## Twitter Card

In order to Use Twitter card, you need set following parameters:

| Parameter | Location | Comment |
| :--- | :--- | :--- |
| twitterShortname | `config.toml` | @username for the website used in the card footer. |
| twittercard | post front matter | The card type, which will be one of “summary”, “summary_large_image”, “app”, or “player”. More card types information can be viewed in [Twitter Developer Documentation](https://dev.twitter.com/cards/types). |
| twitterdescription | post front matter | A description that concisely summarizes the content as appropriate for presentation within a Tweet. |
| twitterimage | post front matter | A URL to a unique image representing the content of the page. |

Here is an example of TOML configuration for the post (post front matter):

```
+++
date               = "2015-12-08T21:49:41-00:00"
title              = "What is SELinux"
tags               = [ "SELinux" ]
twittercard        = "summary_large_image"
twitterdescription = "Security Enhanced Linux (SELinux) is a security feature in the Linux kernel. It is usually enabled by default in Red Hat related GNU/Linux distributions."
twitterimage       = "https://nrechn.de/images/2015/12/selinux.png"
+++
```

The preview can be checked via [Twitter validator](https://cards-dev.twitter.com/validator), and should be similar to this:

![Twitter card](https://github.com/nrechn/yume/raw/master/images/twitter-card.png)

## Contributing

If you have any suggestion, idea, or bug report; feel free to open an issue on this repository.

## License

This theme is released under [GPL-3.0](https://github.com/nrechn/yume/blob/master/LICENSE).
