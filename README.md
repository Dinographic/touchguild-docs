---
description: This page is deprecated.
---

# 🌟 Get started

<figure><img src=".gitbook/assets/touchguild-cradius.png" alt=""><figcaption></figcaption></figure>

## This page is an archive and features legacy versions of TouchGuild

## Installation

NodeJS **16.16.0** or higher is required.

{% tabs %}
{% tab title="npm" %}
```bash
npm install touchguild@latest
```
{% endtab %}

{% tab title="yarn" %}
```bash
yarn add touchguild@latest
```
{% endtab %}

{% tab title="ppm" %}
```bash
pnpm add touchguild@latest
```
{% endtab %}
{% endtabs %}

## Get started

```javascript
const TouchGuild = require('touchguild'); // import for CommonJS
// import * as TouchGuild from 'touchguild' // import for ESM & TS

const client = new TouchGuild.Client({token: 'insert token here'});

client.on('ready', ()=> {
   console.log(`Logged as ${client.user.username}`);
});

client.on('error', (err)=> {
   console.error("Whoops, somethin' went wrong..", err);
});

client.connect();
```

{% hint style="info" %}
Note: CommonJS, ESM & Typescript are supported.
{% endhint %}

## Development builds (Nightly)

Nightly builds are pre-release builds, they're having new features in real time. Once there's enough features, we're releasing them as a brand new 'stable build'.

<figure><img src=".gitbook/assets/touchguild nightly.png" alt=""><figcaption></figcaption></figure>

## Install Nightly builds

You can get new features before the stable release.

### Install the latest Nightly build automatically:

{% tabs %}
{% tab title="npm" %}
```bash
npm install touchguild@nightly
```
{% endtab %}

{% tab title="yarn" %}
```bash
yarn add touchguild@nightly
```
{% endtab %}

{% tab title="ppm" %}
```bash
pnpm add touchguild@nightly
```
{% endtab %}
{% endtabs %}

### Install the latest Nightly build manually:

```bash
npm install dinographicpixels/touchguild#nightly
```

1. Run the command
2. Go to `node_modules/touchguild`
3. Run: `npm run build` inside the touchguild folder
4. &#x20;Now, it's ready.

You need to reproduce those steps everytime you update to a newer nightly build.

{% hint style="warning" %}
Be aware that Nightly builds aren't stable and can have still have major bugs. If you face issues, feel free to report it by creating an issue on TouchGuild's GitHub, please specify that you're using a Nightly build.
{% endhint %}

{% hint style="info" %}
You can check [Nightly Features here.](broken-reference)
{% endhint %}

## Additional links:

#### Repository & NPM

* [NPM Package](https://www.npmjs.com/package/touchguild)
* [GitHub](https://github.com/DinographicPixels/TouchGuild)

#### Guide & documentation

* [Guide](https://guide.touchguild.dinographicpixels.com)
* [Documentation](documentation/select-version/)

#### Additional links

* [Our vision of the project](https://docs.touchguild.dinographicpixels.com/misc/our-vision)
* [FAQ](https://docs.touchguild.dinographicpixels.com/misc/faq)
* [Get started, youtube video](https://www.youtube.com/watch?v=AUaiQRMjJZo)

#### Our servers

* [Our Discord server](https://discord.gg/UgPRaGRkrQ)
* [Our Guilded server](https://www.guilded.gg/i/ExPXPrwE)
