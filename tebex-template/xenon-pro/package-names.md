# Package Names

Xenon PRO does not use a traditional category or tag system for displaying packages. Instead, it reads directly from the **package name** to extract and display all relevant information on the storefront.

This means the way you name your packages in Tebex **directly controls** how they appear to customers.

***

### How the Package Name Works

A package name is made up of three parts, each wrapped in a different type of bracket:

```
[Script Name] TAG1 TAG2 {SPECIAL TAG}
```

| Part         | Bracket Type          | What It Does                                            |
| ------------ | --------------------- | ------------------------------------------------------- |
| Script Name  | `[ ]` Square brackets | The actual name of the script/resource                  |
| Tags         | No brackets (middle)  | Framework tags, shown as labels on the package          |
| Special Tags | `{ }` Curly brackets  | Highlighted tags, shown in **bold** on the package card |

***

### Part 1 - Script Name `[ ]`

The content inside square brackets is the **script name** — the name of the resource or product being sold.

This can be anything:

```
[Fishing Job]
[Spawn Menu]
[Police MDT]
[Advanced Garage]
```

<figure><img src="../../.gitbook/assets/image (17).png" alt="" width="253"><figcaption></figcaption></figure>

***

### Part 2 - Tags (middle, no brackets)

Tags sit between the script name and the special tags. They appear as **labels** on the package card and tell customers which frameworks or platforms the script supports.

Common examples:

```
ESX
QBCore
QBox
Standalone
OneSync
```

You can add as many tags as needed, separated by spaces:

```
[Fishing Job] ESX QBCore Standalone
```

There are no restrictions on what a tag can be - use any label that makes sense for your product.

<figure><img src="../../.gitbook/assets/image (18).png" alt="" width="253"><figcaption></figcaption></figure>

***

### Part 3 - Special Tags `{ }`

Content inside curly brackets is a **special tag**. These are displayed in **bold** on the package card to draw attention to important information.

Common uses:

```
{ESCROW}
{OPEN SOURCE}
{LIFETIME}
{NEW}
{SALE}
```

<figure><img src="../../.gitbook/assets/image (19).png" alt="" width="253"><figcaption></figcaption></figure>

***

### Full Name Examples

Here are some complete package name examples and what they produce:

| Package Name                             | Script          | Tags              | Special Tag     |
| ---------------------------------------- | --------------- | ----------------- | --------------- |
| `[Fishing Job] ESX QBCore QBox {ESCROW}` | Fishing Job     | ESX, QBCore, QBox | **ESCROW**      |
| `[Spawn Menu] Standalone {OPEN SOURCE}`  | Spawn Menu      | Standalone        | **OPEN SOURCE** |
| `[Police MDT] QBCore ESX {ESCROW}`       | Police MDT      | QBCore, ESX       | **ESCROW**      |
| `[Advanced Garage] QBox {NEW}`           | Advanced Garage | QBox              | **NEW**         |

***

### Rules & Notes

{% hint style="info" %}
&#x20;**Order matters.** The name must follow this exact structure:

```
[Script Name] TAGS {SPECIAL TAG}
```

Putting tags before the script name or after the special tag may cause display issues.&#x20;
{% endhint %}

{% hint style="info" %}
&#x20;**Multiple special tags** can be added by using multiple `{ }` blocks:

```
[Fishing Job] ESX QBCore {ESCROW} {NEW}
```
{% endhint %}

{% hint style="info" %}
**Tags are completely flexible.** There is no fixed list. You can use any text as a tag - framework names, version info, compatibility labels, or anything else relevant to your customers.
{% endhint %}

***

### Where to Set the Package Name

Package names are set inside your **Tebex Dashboard**:

1. Go to **Webstore → Packages**
2. Open the package you want to configure
3. Edit the **Name** field using the format above
4. Save

The storefront will automatically parse the name and display each part correctly.
