---
description: Xenon PRO Installation Guide
---

# Installation

> **Before you begin:** Read this guide fully before starting. Skipping steps especially the Publish step is the most common cause of installation issues.

***

### Overview

Xenon PRO is a custom Tebex webstore theme built on the `Exo` base template. This guide covers everything from downloading the files to publishing your live store.

**Time to complete:** \~15–30 minutes

**What you'll need:**

* A purchased copy of Xenon PRO (from [BuiltByBit](https://builtbybit.com/resources/xenon-pro-tebex-theme.82310/))
* Access to your Tebex dashboard with **Plus Subscription**
* A text editor (VS Code, Notepad++, or similar)

***

### Table of Contents

1. Download the Theme
2. Create a New Template in Tebex
3. Clean the Default Assets
4. Upload Xenon PRO Assets
5. Replace HTML Files
6. Clear Module Files
7. Replace the Schema
8. Publish the Template
9. Final Checklist
10. Troubleshooting

***

### 1. Download the Theme

Purchase and download Xenon PRO from the official product page:

🔗 [Xenon PRO on BuiltByBit](https://builtbybit.com/resources/xenon-pro-tebex-theme.82310/)

Once on the product page, go to the **Download** section and save the ZIP file to your computer. Then extract it you should have a folder containing all the Xenon PRO template files.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

***

### 2. Create a New Template in Tebex

1. Go to your **Tebex Dashboard**
2. From the left menu, navigate to **Webstore → Appearance**
3. Click **Create Custom Template**
4. Fill in the details:
   * **Name:** Any name you like (e.g. `Xenon PRO`)
   * **Base Template:** `Exo` ← _This is required_
5. Click **Create**

Tebex will open the template editor.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

***

### 3. Clean the Default Assets

Inside the template editor, find the **Assets** section in the left menu.

You need to delete the default assets but **two files must be kept**:

{% hint style="danger" %}
**Do NOT delete these two files:**

* `quote.html`
* `category/tiered.html`

**If you delete them, they cannot be recreated manually inside the Tebex editor. You would need to start over with a brand new template.**
{% endhint %}

Delete everything else in the Assets section, then move on to uploading the Xenon PRO assets.

***

### 4. Upload Xenon PRO Assets

All assets must be uploaded with the correct asset type. Click **Add** in the Assets section to start each upload.

#### 4.1 - Twig Files

| Setting       | Value         |
| ------------- | ------------- |
| Asset Type    | `Twig`        |
| Source Folder | `assets/twig` |

Click **Add → Twig → Upload → Browse**, select all files in `assets/twig`, then click **Upload file**.

***

#### 4.2 - CSS Files

| Setting       | Value           |
| ------------- | --------------- |
| Asset Type    | `CSS`           |
| Source Folder | `assets/styles` |

Click **Add → CSS → Upload → Browse**, select all files in `assets/styles`, then click **Upload file**.

***

#### 4.3 - JavaScript Files

| Setting       | Value            |
| ------------- | ---------------- |
| Asset Type    | `JavaScript`     |
| Source Folder | `assets/scripts` |

Click **Add → JavaScript → Upload → Browse**, select all files in `assets/scripts`, then click **Upload file**.

***

#### 4.4 - Image Files

| Setting       | Value         |
| ------------- | ------------- |
| Asset Type    | `Image`       |
| Source Folder | `assets/imgs` |

Click **Add → Image → Upload → Browse**, select all files in `assets/imgs`, then click **Upload file**.

{% hint style="info" %}
**Tip:** Upload all four asset types before moving on. Missing assets are the most common cause of a broken or unstyled theme.
{% endhint %}

***

### 5. Replace HTML Files

Go back to the left menu in the template editor and find the **Webstore** group. You will see a list of HTML files.

For each file listed below:

1. Open the matching file from your Xenon PRO folder in a text editor
2. Copy the full contents
3. Open the same file inside the Tebex editor
4. Delete all existing code
5. Paste the Xenon PRO code
6. Save

**Files to replace:**

```
category.html
checkout.html
cms/page.html
index.html
layout.html
module.featuredpackage.html
module.payments.html
options.html
package.html
username.html
```

***

### 6. Clear Module Files

Some module files must be **completely empty** no code at all.

Open each file below in the Tebex editor, delete all content, and save as a blank file:

```
module.communitygoal.html
module.giftcardbalance.html
module.goal.html
module.serverstatus.html
module.textbox.html
module.topdonator.html
```

{% hint style="warning" %}
These files should contain zero content. Do not leave any whitespace, comments, or leftover code inside them.&#x20;
{% endhint %}

***

### 7. Replace the Schema

1. Open `Schema.json` from your Xenon PRO folder in a text editor
2. Copy the full contents
3. In the Tebex template editor, click **Change Schema**
4. Delete all existing content in the schema editor
5. Paste the Xenon PRO schema
6. Save

{% hint style="info" %}
Schema changes may not appear correctly in **Preview** mode. This is expected they will apply correctly after you publish.
{% endhint %}

***

### 8. Publish the Template

Once all steps above are complete, click **Publish**.

{% hint style="danger" %}
**This step is required.** Do not skip it.

Schema settings and some layout changes will not work correctly until the template is published. Preview mode alone is not enough.
{% endhint %}

After publishing, visit your live webstore and verify that all pages, buttons, images, and sections are displaying correctly.

***

### 9. Final Checklist

Use this checklist to confirm you haven't missed anything:

* \[ ] Downloaded Xenon PRO from BuiltByBit
* \[ ] Extracted the ZIP file
* \[ ] Created a new custom Tebex template with `Exo` as the base
* \[ ] Deleted default assets - **without** deleting `quote.html` or `category/tiered.html`
* \[ ] Uploaded all Twig files from `assets/twig`
* \[ ] Uploaded all CSS files from `assets/styles`
* \[ ] Uploaded all JavaScript files from `assets/scripts`
* \[ ] Uploaded all image files from `assets/imgs`
* \[ ] Replaced all 10 required HTML files in the Webstore group
* \[ ] Cleared the 6 module files (left completely empty)
* \[ ] Replaced the schema using `Schema.json`
* \[ ] Clicked **Publish**

***

{% hint style="success" %}
**Installation complete!** Your Xenon PRO theme is now live. If you run into any issues not covered here, double-check the [Final Checklist](https://app.gitbook.com/o/JSioyuXsq4OuvGIOXUMF/s/dOkeqI4F1tteDwk0IhKW/~/edit/~/changes/56/tebex-template/xenon-pro/installation#id-9.-final-checklist) and make sure **Publish** was clicked after every change.
{% endhint %}
