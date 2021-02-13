<!--docs:
title: "Text field"
layout: detail
section: components
excerpt: "<Platform name> Text field"
ide_version: "<cIDE name> <compatible IDE version and build number>"
material_package_version: "<compatible Material platform package version number>"
iconId:
path: /
api_doc_root:
-->

_**Instructions**_
* [Using text field](#using-text-field)
    * Add a link under [Using text field](#using-text-field) to your getting started page if you have one
    * Insert [installation](#installation) and [theming](#theming) as appropriate for your platform
    * Insert any additional instructions that apply to your platform with a separte level 3 header
    * If you have no getting started links or instructions, delete the [Using text field](#using-text-field) sections
* [Filled text](#filled-text) ane [Outlined-text](#outlined-text) sections
    * Add links to your platform 


# Text field

[Text fields](https://material.io/components/text-fields) let users enter and edit text.

The text field class consists of the following types:

* [Filled text](#filled-text)
* [Outlined text](#outlined-text)

<img src="assets/text-field-generic.png" alt="Text field examples of both filled and outlined types, and each type showing both inactive and focused states. The filled text fields show a gray background and a darker gray activation indicator that is purple when focused. The outlined text fields show a clear background and an outline that is purple when focused">

## Using text fields

Text fields allow users to enter text into a UI. They typically appear in forms and dialogs.

### Install `TextFields`


Before using the `TextFields` API to implement its types you must install `TextFields`. In you source files import the component and then apply your theme:

1. Install `TextFields`
  * Use CocoaPods to install `TextFields`
    1. Add the following line to your `Podfile`:
      ```pod
      pod 'MaterialComponents/TextFields'
      ```
    1. Run the installer:
      ```bash
      pod install
      ```
1. Import `TextFields` and text field theming and initialize `TextFields` using `alloc` / `init`. Initialize your theme before applying it to your text field.
  **Note** For more information about themes, go to the [Theming page](https://material.io/develop/ios/components/theming/) for iOS.
<!--<div class="material-code-render" markdown="1">-->
  **Swift**
    ```swift
    import MaterialComponents.MaterialTextFields
    ```

    ```Objc
    #import "MaterialTextFields.h"
    ```
<!--</div>-->
1. Apply accessibility settings
  To help make your text fields usable to as many users as possible, set an appropriate [accessibilityLabel](https://developer.apple.com/documentation/uikit/uiaccessibilityelement/1619577-accessibilitylabel) if you choose not to use a text label or if you need to include additional descriptions of visual cues, or [accessibilityHint](https://developer.apple.com/documentation/uikit/uiaccessibilityelement/1619585-accessibilityhint) if you choose not to include helper text, or error text:

## Filled text

[Filled text fields](https://material.io/components/text-fields/#filled-text-field) have more visual emphasis than outlined text fields, making them stand out when surrounded by other content and components.

### Filled text example

Source code API:

* `TextInputLayout` 
  * [Class definition]()
  * [GitHub source](https://github.com/material-components/)

The following examples shows a filled text field.


_**Copy the image to your platform's assets folder. Use a screenshot of your render.**_


<img src="assets/.png" alt="filled text field for Android">

```
* The label text should read "Label text"
* The input text should read "Input text"
* The helper text should read "Helper text"
* The text field should have a character counter of up to 20 characters
* The text field should have a "favorite" leading icon
```

### Anatomy and key properties

![Filled text field anatomy](assets/textfields_filled_anatomy.png)

1. Container
1. Leading icon (optional)
1. Label text
1. Input text
1. Trailing icon (optional)
1. Activation indicator
1. Helper text (optional)

<b>Container</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Color** | | | |
| **Stroke color** | | | |
| **Stroke width** | | | |
| **Shape** | | | |
| **Elevation** | | | |
| **Ripple color** | | | |

<b>Leading icon (optional) </b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Icon** | | | |
| **Color** | | | |
| **Size** | | | |
| **Gravity** | | | |
| **Padding** | | | |

<b>Label text</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Label text** |  | | |
| **Typography** | | | |
| **Color** | | | |

<b>Input text</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Label text** |  | | |
| **Typography** | | | |
| **Color** | | | |

<b>Trailing icon (optional)</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Icon** | | | |
| **Color** | | | |
| **Size** | | | |
| **Gravity** | | | |
| **Padding** | | | |

<b>Activation indicator</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Stroke color** | | | |
| **Stroke width** | | | |
| **Ripple color** | | | |

<b>Helper text (optional)</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Label text** |  | | |
| **Typography** | | | |
| **Color** | | | |

<b>Styles</b>

|  | Style|
| --- | --- |
| **Default style** | |
| **Icon style** | |


## Outlined text

[Outlined text fields](https://material.io/components/text-fields/#outlined-text-field) have less visual emphasis than filled text fields. When they appear in places like forms, where many text fields are placed together, their reduced emphasis helps simplify the layout.

### Outlined text example

Source code API:

* `TextInputLayout` 
  * [Class definition]()
  * [GitHub source]()

The following examples shows an outlined text field.

_**Copy the image to your platform's assets folder. Use a screenshot of your render.**_
<img src="assets/.png" alt="outlined text field for Android.">

```
* The label text should read "Label text"
* The input text should read "Input text"
* The error message text should read "Error message" and display the error message
* The text field should have a trailing error icon
```
### Anatomy and key properties

![Outlined text field anatomy](assets/textfields_outlined_anatomy.png)

1. Container
1. Leading icon (optional)
1. Label text
1. Input text
1. Trailing icon (optional)
1. Activation indicator
1. Helper text (optional)

<b>Container</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Color** | | | |
| **Stroke color** | | | |
| **Stroke width** | | | |
| **Shape** | | | |
| **Elevation** | | | |
| **Ripple color** | | | |

<b>Leading icon (optional)</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Icon** | | | |
| **Color** | | | |
| **Size** | | | |
| **Gravity** | | | |
| **Padding** | | | |

<b>Label text</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Label text** |  | | |
| **Typography** | | | |
| **Color** | | | |

<b>Input text</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Label text** |  | | |
| **Typography** | | | |
| **Color** | | | |

<b>Trailing icon (optional)</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Icon** | | | |
| **Color** | | | |
| **Size** | | | |
| **Gravity** | | | |
| **Padding** | | | |

<b>Activation indicator</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Stroke color** | | | |
| **Stroke width** | | | |
| **Ripple color** | | | |

<b>Helper text (optional)</b>

|  | Attribute | Related method(s) | Default value |
| --- | --- | --- | --- |
| **Label text** |  | | |
| **Typography** | | | |
| **Color** | | | |

<b>Styles</b>

|  | Style|
| --- | --- |
| **Default style** | |
| **Icon style** | |

## Theming text fields

Text fields support [Material Theming](https://material.io/components/text-fields/#theming) and can be customized in terms of color, typography and shape.

### Text field theming example

API and source code:

* `\<Component platform API name\>`
    * [Class description](https://)
    * [GitHub source](https://github.com/material-components/)
    
The following example shows filled and outlined text fields with Material Theming.

!["Two text fields, one filled, one outlined, with green/black color theming and cut corners."](assets/button-theming.svg)

_Use the [Shrine theme](https://material.io/design/material-studies/shrine.html) for this example_

```

* Include one filled text field with the following:
    * The label text should read "Label text"
    * The input text should read "Input text"
    * The helper text should read "Helper text"
    * The text field should have a character counter of up to 20 characters
    * The text field should have a "favorite" leading icon
    * The container should have cut corners instead of rounded
* Include one outlined text field with the following:
    * The label text should read "Label text"
    * The input text should read "Input text"
    * The error message text should read "Error message" and display the error message
    * The text field should have a trailing error icon
    * The container should have cut corners instead of rounded
```
</details>
