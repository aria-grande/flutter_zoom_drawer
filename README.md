# Flutter Zoom Drawer

[![pub package](https://img.shields.io/pub/v/flutter_zoom_drawer.svg)](https://pub.dev/packages/flutter_zoom_drawer) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  

A Flutter package with custom implementation of the Side Menu (Drawer)

## Getting Started

To start using this package, add `flutter_zoom_drawer` dependency to your `pubspec.yaml`

```yaml
dependencies:
  flutter_zoom_drawer: '<latest_release>'
```

## Features

* Simple sliding drawer
* Sliding drawer with rotation
* Sliding drawer with rotation and shadows
* Support for both LTR & RTL


## Documentation

```dart
    ZoomDrawer(
      controller: ZoomDrawerController,
      menuScreen: MENU_SCREEN,
      mainScreen: MAIN_SCREEN,
      borderRadius: 24.0,
      showShadow: true,
      angle: -12.0,
      backgroundColor: Colors.grey[300],
      slideWidth: MediaQuery.of(context).size.width*.65,
    )
```

| Parameters         | Value                  | Required  | Docs                                                                        |
| ------------------ |----------------------- | :-------: | --------------------------------------------------------------------------- |
| `controller`       | `ZoomDrawerController` |    No     | Controller to have access to the open/close/toggle function of the drawer   |
| `mainScreen`       | `Widget`               |   Yes     | Screen containing the menu/bottom screen                                    |
| `menuScreen`       | `Widget`               |   Yes     | Screen containing the main content to display                               |
| `slideWidth`       | `double`               |    No     | Sliding width of the drawer - defaults to 275.0                             |
| `borderRadius`     | `double`               |    No     | Border radius of the slided content - defaults to 16.0                      |
| `angle`            | `double`               |    No     | Rotation angle of the drawer - defaults to -12.0 - should be 0.0 to -30.0   |
| `backgroundColor`  | `Color`                |    No     | Background color of the drawer shadows - defaults to white                  |
| `showShadow`       | `bool`                 |    No     | Boolean, whether to show the drawer shadows - defaults to false             |


### Controlling the drawer

To get access to the drawer, and be able to control it, there are 2 ways:

* Using a `ZoomDrawerController` inside the main widget where ou have the `ZoomDrawer` widget and providing it to the widget, which will allow you to trigger the open/close/toggle methods.
```dart
    final _drawerController = ZoomDrawerController();

    _drawerController.open();
    _drawerController.close();
    _drawerController.toggle();
```

* Using the static method inside ancestor widgets to get access to the `ZoomDrawer`.
```dart
  ZoomDrawer.of(context).open();
  ZoomDrawer.of(context).close();
  ZoomDrawer.of(context).toggle();
```

## Screens

![Example app Demo](https://drive.google.com/uc?export=view&id=1xc6XwVVtpl0RK9IJEdheagM4d1ychQms)

* Drawer Sliding

![Drawer Sliding](https://drive.google.com/uc?export=view&id=1axuT4Geh08s_QjmED9VTZiwZ9dC_C17C)

* Drawer Sliding with rotation

![Drawer Sliding with rotation](https://drive.google.com/uc?export=view&id=1xVYoZHnS9BFi5KicZtP3DY1vEiwZ4FyH)

* Drawer Sliding with rotation and shadows

![Drawer Sliding with rotation and shadows](https://drive.google.com/uc?export=view&id=1b-U25tIY36ka75Ju2jQT9BIUVHv-oNe6)


## Issues

Please file any issues, bugs or feature request as an issue on our [GitHub](https://github.com/medyas/flutter_zoom_drawer/issues) page.

## Want to contribute

If you would like to contribute to the plugin (e.g. by improving the documentation, solving a bug or adding a cool new feature), please carefully review our [contribution guide](CONTRIBUTING.md) and send us your [pull request](https://github.com/medyas/flutter_zoom_drawer/pulls).

## Credits

Credits goes to [pedromassango](https://github.com/pedromassango/flutter_delivery) as most of this package comes from his implementation.