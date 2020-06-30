---
logo: "/assets/img/mock-booth1.png"
name: BMW
url: https://bmw.com
description: |-
  **Bayerische Motoren Werke AG**, commonly referred to as **BMW** (German pronunciation: [\[ˈbeːˈʔɛmˈveː\]](https://en.wikipedia.org/wiki/Help:IPA/Standard_German "Help:IPA/Standard German") ([![About this sound](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Loudspeaker.svg/11px-Loudspeaker.svg.png =11x11)](https://en.wikipedia.org/wiki/File:De-BMW.ogg "About this sound")[listen](https://upload.wikimedia.org/wikipedia/commons/8/86/De-BMW.ogg "De-BMW.ogg"))), is a German multinational company which produces [luxury vehicles](https://en.wikipedia.org/wiki/Luxury_vehicle "Luxury vehicle") and [motorcycles](https://en.wikipedia.org/wiki/Motorcycle "Motorcycle"). The company was founded in 1916 as a manufacturer of aircraft engines, which it produced from 1917 until 1918 and again from 1933 to 1945.

  Automobiles are marketed under the brands BMW, [Mini](https://en.wikipedia.org/wiki/Mini_(marque) "Mini (marque)") and [Rolls-Royce](https://en.wikipedia.org/wiki/Rolls-Royce_Motor_Cars "Rolls-Royce Motor Cars"), and motorcycles are marketed under the brand [BMW Motorrad](https://en.wikipedia.org/wiki/BMW_Motorrad "BMW Motorrad"). In 2015, BMW was the world's [twelfth-largest producer of motor vehicles](https://en.wikipedia.org/wiki/List_of_manufacturers_by_motor_vehicle_production "List of manufacturers by motor vehicle production"), with 2,279,503 vehicles produced.[\[2\]](https://en.wikipedia.org/wiki/BMW#cite_note-2) The company has significant motorsport history, especially in [touring cars](https://en.wikipedia.org/wiki/Touring_car_racing "Touring car racing"), [Formula 1](https://en.wikipedia.org/wiki/Formula_1 "Formula 1"), [sports cars](https://en.wikipedia.org/wiki/Sports_car_racing "Sports car racing") and the [Isle of Man TT](https://en.wikipedia.org/wiki/Isle_of_Man_TT).

  BMW is headquartered in [Munich](https://en.wikipedia.org/wiki/Munich "Munich") and produces motor vehicles in Germany, Brazil, China, India, South Africa, the United Kingdom, the United States and Mexico. The [Quandt family](https://en.wikipedia.org/wiki/Quandt_family "Quandt family") are long-term shareholders of the company, with the remaining shares owned by public float

---
Any markdown file that contains a YAML front matter block will be processed by [gray-matter](https://github.com/jonschlinkert/gray-matter). The front matter must be the first thing in the markdown file and must take the form of valid YAML set between triple-dashed lines. Here is a basic example:

    ---
    title: Blogging Like a Hacker
    lang: en-US
    ---

Between these triple-dashed lines, you can set predefined variables (see [below](#predefined-variables) for a reference), or even create custom ones of your own. These variables will then be available to you to access using <code>[$frontmatter](./global-computed.md#frontmatter)</code> at the rest of the page, plus all custom and theming components.

::: tip Front matter variables are **optional** in VuePress. :::

## Alternative Front Matter Formats

In addition, VuePress also supports JSON or [TOML](https://github.com/toml-lang/toml) front matter.

JSON front matter needs to start and end in curly braces:

    ---
    {
      "title": "Blogging Like a Hacker",
      "lang": "en-US"
    }
    ---

TOML front matter needs to be explicitly marked as TOML:

    ---toml
    title = "Blogging Like a Hacker"
    lang = "en-US"
    ---

## Predefined Variables

### title

* Type: `string`
* Default: `h1_title || siteConfig.title`

Title of current page.

### lang

* Type: `string`
* Default: `en-US`

Language of current page.

### description

* Type: `string`
* Default: `siteConfig.description`

Description of current page.

### layout

* Type: `string`
* Default: `Layout`

Set the layout component of the current page.

### permalink

* Type: `string`
* Default: `siteConfig.permalink`

Refer to: [Permalinks](./permalinks.md).

### metaTitle

* Type: `string`
* Default: <code>\`${page.title} | ${siteConfig.title}\`</code>

Override the default meta title.

### meta

* Type: `array`
* Default: `undefined`

Specify extra meta tags to be injected:

    ---
    meta:
      - name: description
        content: hello
      - name: keywords
        content: super duper SEO
    ---

## Predefined Variables Powered By Default Theme

### navbar

* Type: `boolean`
* Default: `undefined`

See: [Default Theme Config > Disable the Navbar](../theme/default-theme-config.md#disable-the-navbar).

### sidebar

* Type: `boolean|'auto'`
* Default: `undefined`

See: [Default Theme Config > Sidebar](../theme/default-theme-config.md#sidebar).