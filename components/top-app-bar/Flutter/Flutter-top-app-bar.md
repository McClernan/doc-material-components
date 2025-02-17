<!--docs:
title: "Material Top App Bar"
layout: detail
section: components
excerpt: "A customizable top app bar component with updated visual styles."
iconId: 
path: /catalog/material-top-app-bar/
-->

**Instructions to authors:**
* _Follow the instructions in each section &ndash; see the [accompanying examples](button-examples) for futher guidance._
* _Delete these instructions before submitting your document_

# Top app bar

The [top app bar](https://material.io/components/app-bars-top/#) displays information and actions relating to the current screen.

There are two types of top app bar:

1. [Regular top app bar](#regular-top-app-bar)
1. [Contextual action bar](#contextual-top-app-bar)
<br>

![Regular app bar: purple background, white text and icons](assets/Top-app-bars_types_side-by-side.png)

## Using the top app bar

The top app bar provides content and actions related to the current screen. It’s used for branding, screen titles, navigation, and actions.

A regular top app bar can transform into a contextual action bar.

Before you can use Material buttons, you need to import the Material Components package for Flutter: 
```dart
package:flutter/material.dart
```

You need to use [`MaterialApp`](https://api.flutter.dev/flutter/material/MaterialApp-class.html).

For more information on getting started with the Material for Flutter, go to the Flutter [Material library](https://api.flutter.dev/flutter/material/material-library.html) page.


### Making the top app bar accessible

_List any accessiblity setting or attributes (such as labels), describe how to use them and link to any guidelines on the m.io site (for example, [how to write a good accessibility label for your component](https://material.io/design/usability/accessibility.html#writing))_



## Regular top app bar

The top app bar provides content and actions related to the current screen. It’s used for branding, screen titles, navigation, and actions.

### Regular top app bar example

`AppBar`
* [Class definition](https://api.flutter.dev/flutter/material/AppBar-class.html)
* [GitHub source](https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/app_bar.dart)
* [Dartpad Demo](https://dartpad.dev/embed-flutter.html?gh_owner=material-components&gh_repo=material-components-flutter&gh_path=docs/components/dartpad/top-app-bar/regular&gh_ref=develop)

The following example shows a top app bar with a page title, a navigation icon, two action icons, and an overflow menu:

![Top app bar with nav icon, page title, favorite icon, and search icon](assets/top_app_bar_screenshot.png)

```dart
AppBar(
    leading: Icon(Icons.menu),
    title: Text('Page title'),
    actions: <Widget>[
        Icon(Icons.favorite),
        Padding(
            padding: EdgeInsets.symmetric(horizontal: 16),
            child: Icon(Icons.search),
        ),
        Icon(Icons.more_vert),
    ],
    backgroundColor: Colors.purple,
),

```

### Anatomy and Key properties

![Regular app bar anatomy diagram](assets/top_app_bar_anatomy.png)

1. Container
1. Navigation icon (optional)
1. Title (optional)
1. Action items (optional)
1. Overflow menu (optional)

<b>Container </b>

| &nbsp; | Property |
| --- | --- |
| **Color** | color parameter |
| **Stroke color** |  In leading parameter, use Icon widget. Set color|
| **Shape** | shape parameter |
| **Elevation** | elevation parameter|
| **Ripple color** |  |

<b>Navigation icon (optional)</b>

| &nbsp; | Property |
| --- | --- |
| **Icon** |  In leading parameter, use Icon Widget |
| **Color** | In leading parameter, use Icon Widget and set parameter color |
| **Size** | In leading parameter, use Icon Widget and set parameter size |
| **Gravity** | titleSpacing parameter |
| **Padding** | Wrap Icon wiget with Padding widget |

<b>Title (optional)</b>

| &nbsp; | Property |
| --- | --- |
| **Text label** | In title parameter, use Text widget |
| **Color** | In title parameter, use Text Widget and and set parameter style |
| **Typography** |  |

<b>Action item (optional)</b>

| &nbsp; | Property |
| --- | --- |
| **Icon** | | 
| **Color** | | 
| **Size** | | 
| **Gravity** (position relative to text label) | | 
| **Padding** (space between icon and text label) | |

<b>Overflow menu (optional)</b>

| &nbsp; | Property |
| --- | --- |
| **Icon** |  |
| **Color** | |
| **Size** | | 
| **Gravity** (position relative to text label) | | 
| **Padding** (space between icon and text label) | | 


## Contextual action bar

A top app bar can transform into a contextual action bar to provide contextual actions to selected items. For example, upon user selection of photos from a gallery, the top app bar transforms to a contextual app bar with actions related to the selected photos.

When a top app bar transforms into a contextual action bar, the following changes occur:

* The bar color changes
* Navigation icon is replaced with a close icon
* Top app bar title text converts to contextual action bar text
* Top app bar actions are replaced with contextual actions
* Upon closing, the contextual action bar transforms back into a top app bar.

### Contextual action bar example
`AppBar`
* [Class definition](https://api.flutter.dev/flutter/material/AppBar-class.html)
* [GitHub source](https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/app_bar.dart)
* [Dartpad Demo](https://dartpad.dev/embed-flutter.html?gh_owner=material-components&gh_repo=material-components-flutter&gh_path=docs/components/dartpad/top-app-bar/contextual&gh_ref=develop)

The following example shows a contextual action bar with a contextual title, a close icon, two contextual action icons, and an overflow menu:

![Contextual top app bar with close button, download, garbage, and overflow menu icons](assets/contextual_screenshot.png)

```dart
AppBar(
    leading: Icon(Icons.close),
    title: Text('1 selected'),
    actions: <Widget>[
        Icon(Icons.file_upload),
        Padding(
            padding: EdgeInsets.symmetric(horizontal: 16),
            child: Icon(Icons.delete),
        ),
        Icon(Icons.more_vert),
    ],
    backgroundColor: Colors.black87,
),

```

### Anatomy and Key properties

![Contextual action bar anatomy diagram](assets/contextual_action_bar_anatomy.png)

1. Close Button
1. Contextual title
1. Contextual action items (optional)
1. Overflow menu (optional)

<b>Close button</b>

| &nbsp; | Property |
| --- | --- |
| **Icon** |  |
| **Color** |  |
| **Size** | |
| **Gravity** (position relative to text label) |  |
| **Padding** (space between icon and text label) |  |

<b>Contextual title</b>

| &nbsp; | Property|
| --- | --- |
| **Text label** |  |
| **Color** |  | 
| **Typography** |  |

<b>Contextual action item (optional)</b>

| &nbsp; | Property |
| --- | --- |
| **Icon** |  |
| **Color** |  |
| **Size** |  |
| **Gravity** (position relative to text label) |  |
| **Padding** (space between icon and text label) |  |

<b>Overflow menu (optional)</b>

| &nbsp; | Property |
| --- | --- |
| **Icon** | | 
| **Color** | | 
| **Size** | | 
| **Gravity** (position relative to text label) | | 
| **Padding** (space between icon and text label) | | 


#### Styles

_If the component API implements multiple types, include any style information that differentiates the types in a table_


## Theming a top app bar

The top app bar supports [Material Theming](https://material.io/components/app-bars-top/#theming) and can be customized in terms of color, typography and shape.

### Top app bar theming example
* [Regular Top App Bar with Theme Dartpad Demo](https://dartpad.dev/embed-flutter.html?gh_owner=material-components&gh_repo=material-components-flutter&gh_path=docs/components/dartpad/top-app-bar/theme&gh_ref=develop)
* [Contextual Action Bar with Dartpad Demo](https://dartpad.dev/embed-flutter.html?gh_owner=material-components&gh_repo=material-components-flutter&gh_path=docs/components/dartpad/top-app-bar/contextual_theme&gh_ref=develop)

![Top app bar with Shrine theming](assets/shrine_theme.png)
![Contextual app bar with Shrine theming](assets/contextual_theming.png)

```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      home: MyHomePage(),
      theme: _buildShrineTheme(),
    );
  }
}

class MyHomePage extends StatelessWidget {
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        leading: Icon(Icons.menu),
        title: Text('Page title'),
        actions: [
          Icon(Icons.favorite),
          Padding(
            padding: EdgeInsets.symmetric(horizontal: 16),
            child: Icon(Icons.search),
          ),
          Icon(Icons.more_vert),
        ],
      ),
      body: Container(),
    );
  }
}

ThemeData _buildShrineTheme() {
  final ThemeData base = ThemeData.light();
  return base.copyWith(
    colorScheme: _shrineColorScheme,
    accentColor: shrineBrown900,
    primaryColor: shrinePink100,
    buttonColor: shrinePink100,
    scaffoldBackgroundColor: shrineBackgroundWhite,
    cardColor: shrineBackgroundWhite,
    textSelectionColor: shrinePink100,
    errorColor: shrineErrorRed,
    buttonTheme: const ButtonThemeData(
      colorScheme: _shrineColorScheme,
      textTheme: ButtonTextTheme.normal,
    ),
    primaryIconTheme: _customIconTheme(base.iconTheme),
    textTheme: _buildShrineTextTheme(base.textTheme),
    primaryTextTheme: _buildShrineTextTheme(base.primaryTextTheme),
    accentTextTheme: _buildShrineTextTheme(base.accentTextTheme),
    iconTheme: _customIconTheme(base.iconTheme),
  );
}

IconThemeData _customIconTheme(IconThemeData original) {
  return original.copyWith(color: shrineBrown900);
}

TextTheme _buildShrineTextTheme(TextTheme base) {
  return base
      .copyWith(
        caption: base.caption.copyWith(
          fontWeight: FontWeight.w400,
          fontSize: 14,
          letterSpacing: defaultLetterSpacing,
        ),
        button: base.button.copyWith(
          fontWeight: FontWeight.w500,
          fontSize: 14,
          letterSpacing: defaultLetterSpacing,
        ),
      )
      .apply(
        fontFamily: 'Rubik',
        displayColor: shrineBrown900,
        bodyColor: shrineBrown900,
      );
}

const ColorScheme _shrineColorScheme = ColorScheme(
  primary: shrinePink100,
  primaryVariant: shrineBrown900,
  secondary: shrinePink50,
  secondaryVariant: shrineBrown900,
  surface: shrineSurfaceWhite,
  background: shrineBackgroundWhite,
  error: shrineErrorRed,
  onPrimary: shrineBrown900,
  onSecondary: shrineBrown900,
  onSurface: shrineBrown900,
  onBackground: shrineBrown900,
  onError: shrineSurfaceWhite,
  brightness: Brightness.light,
);

const Color shrinePink50 = Color(0xFFFEEAE6);
const Color shrinePink100 = Color(0xFFFEDBD0);
const Color shrinePink300 = Color(0xFFFBB8AC);
const Color shrinePink400 = Color(0xFFEAA4A4);

const Color shrineBrown900 = Color(0xFF442B2D);
const Color shrineBrown600 = Color(0xFF7D4F52);

const Color shrineErrorRed = Color(0xFFC5032B);

const Color shrineSurfaceWhite = Color(0xFFFFFBFA);
const Color shrineBackgroundWhite = Colors.white;

const defaultLetterSpacing = 0.03;


```