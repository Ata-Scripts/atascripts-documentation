# Tiered Category

Packages inside a **Tiered** category work differently from standard packages. They have a special naming format and require a structured HTML description that the template uses to automatically extract and display content.

***

### Overview

Tiered categories are used for **subscription or rank-based packages** (e.g. Bronze, Silver, Gold tiers). The template reads two things from each package to render it correctly:

1. **The package name** - parsed to extract the tier name, duration, and icon
2. **The package description** - an HTML table that holds the description text, popular flag, and feature list

***

### Package Name Format

```
[Tier Name] Duration {unicode}
```

| Part      | Bracket Type          | What It Contains                                                  |
| --------- | --------------------- | ----------------------------------------------------------------- |
| Tier Name | `[ ]` Square brackets | The name of the tier (e.g. `Bronze`, `Silver`, `Gold`)            |
| Duration  | No brackets (middle)  | The subscription period (e.g. `1 Months`, `3 Months`, `Lifetime`) |
| Icon Code | `{ }` Curly brackets  | A FontAwesome Unicode code that renders as the tier icon          |

#### Examples

| Package Name                | Tier    | Duration | Icon   |
| --------------------------- | ------- | -------- | ------ |
| `[Bronze] 1 Months {f240}`  | Bronze  | 1 Month  | `f240` |
| `[Silver] 3 Months {f241}`  | Silver  | 3 Months | `f241` |
| `[Gold] 6 Months {f242}`    | Gold    | 6 Months | `f242` |
| `[Diamond] Lifetime {f3a5}` | Diamond | Lifetime | `f3a5` |

{% hint style="info" %}
FontAwesome Unicode codes can be found at [fontawesome.com/icons](https://fontawesome.com/icons). Use the code shown after the `\` - for example `\f240` becomes `f240`.&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

***

### Package Description (HTML Table)

Each tiered package must have a structured HTML description. The template reads this table automatically on page load to extract:

* The **description** shown below the package name
* Whether the package is marked as **popular** (applies a visual highlight)
* The **feature list** displayed on the package card, each with an icon

{% hint style="warning" %}
**Do not use plain text in the description field.** The template will not be able to parse it. You must use the HTML table format described below.
{% endhint %}

***

#### How to Add the Description

1. In your **Tebex Dashboard**, open the package
2. Scroll to the **Description** field
3. Enable **HTML mode** (toggle in the editor toolbar)
4. Click **Insert Table** and create a table with:
   * **2 columns** (required - the template reads exactly 2 columns)
   * **Minimum 2 rows** (for `description` and `popular`) plus one row per feature
5. Paste or write your HTML following the structure below

{% hint style="danger" %}
**The first 2 rows are required and must always be present:**

* Row 1: `description`
* Row 2: `popular`

Without these two rows, the template cannot parse the package correctly.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

***

#### Table Structure

```html
<table style="width:100%;">
  <tbody>

    <!-- Row 1: Short description shown below the package name -->
    <tr>
      <td style="width:50%;">description</td>
      <td style="width:50%;">Your description text here</td>
    </tr>

    <!-- Row 2: Mark this package as popular (yes / no) -->
    <tr>
      <td style="width:50%;">popular</td>
      <td style="width:50%;">no</td>
    </tr>

    <!-- Rows 3+: Features — FontAwesome unicode on left, label on right -->
    <tr>
      <td style="width:50%;">f576</td>
      <td style="width:50%;">Feature label here</td>
    </tr>

  </tbody>
</table>
```

***

#### Row Reference

| Row | Left Column                       | Right Column               | Notes                                    |
| --- | --------------------------------- | -------------------------- | ---------------------------------------- |
| 1   | `description`                     | The short description text | **Required**                             |
| 2   | `popular`                         | `yes` or `no`              | **Required** - `yes` highlights the card |
| 3+  | FontAwesome unicode (e.g. `f576`) | Feature label              | One row per feature                      |

<figure><img src="../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

***

#### Full Example

This is a complete description table for a Bronze tier package with 7 features:

```html
<table style="width:100%;">
  <tbody>
    <tr>
      <td style="width:50%;">description</td>
      <td style="width:50%;">Perfect for newcomers looking to get started.</td>
    </tr>
    <tr>
      <td style="width:50%;">popular</td>
      <td style="width:50%;">no</td>
    </tr>
    <tr>
      <td style="width:50%;">f576</td>
      <td style="width:50%;">Access to VIP Lounge</td>
    </tr>
    <tr>
      <td style="width:50%;">f5aa</td>
      <td style="width:50%;">Custom Name Color</td>
    </tr>
    <tr>
      <td style="width:50%;">f547</td>
      <td style="width:50%;">Priority Queue</td>
    </tr>
    <tr>
      <td style="width:50%;">f5bf</td>
      <td style="width:50%;">Discord Role</td>
    </tr>
    <tr>
      <td style="width:50%;">f1e5</td>
      <td style="width:50%;">Weekly In-Game Currency</td>
    </tr>
    <tr>
      <td style="width:50%;">f7bf</td>
      <td style="width:50%;">Exclusive Vehicle Skin</td>
    </tr>
    <tr>
      <td style="width:50%;">f197</td>
      <td style="width:50%;">Bonus XP Multiplier</td>
    </tr>
  </tbody>
</table>
```

<figure><img src="../../.gitbook/assets/image (24).png" alt="" width="264"><figcaption></figcaption></figure>

***

### Package Image

Tiered packages **do not require an image**. The template renders correctly without one.

However, adding an image is supported and will:

* Display as a thumbnail on the package card
* Improve the visual appearance of the storefront
* Help with **SEO** (search engine indexing of your store page)

If you add an image, use a consistent size and aspect ratio across all packages in the same category for a clean, uniform look.

***

### Full Setup Checklist (Per Package)

* \[ ] Package name follows the format: `[Tier Name] Duration {unicode}`
* \[ ] Tier name is inside square brackets `[ ]`
* \[ ] Duration is in the middle with no brackets
* \[ ] FontAwesome icon code is inside curly brackets `{ }`
* \[ ] Description field is in **HTML mode**
* \[ ] Table has exactly **2 columns**
* \[ ] **Row 1** is `description` with your text
* \[ ] **Row 2** is `popular` set to `yes` or `no`
* \[ ] Each feature has its own row with a unicode code and a label
* \[ ] (Optional) Package image uploaded for better UI and SEO

***

### How the Template Uses This Data

When a customer visits the Tiered category page, the template:

1. Reads each package name → extracts the tier, duration, and icon code
2. Reads the HTML description table → finds the `description` row and the `popular` row
3. If `popular` is `yes` → applies a visual highlight style to that package card
4. Reads every remaining row as a feature → renders the FontAwesome icon and the label side by side

This all happens automatically on page load - no manual configuration is needed beyond setting up the name and description correctly.
