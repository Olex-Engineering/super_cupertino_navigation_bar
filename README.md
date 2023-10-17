![Static Badge](https://img.shields.io/badge/Author-KSPoyraz-blue)
[![Linkedin: Kspoyraz](https://img.shields.io/badge/Kspoyraz-blue?logo=Linkedin&logoColor=fff)][linkedin]
[![Github: Kspo](https://img.shields.io/badge/Kspo-white?logo=Github&logoColor=000)][github]
![GitHub Licence](https://img.shields.io/github/license/kspo/apple_stocks_app_clone?label=Licence)
![GitHub last commit](https://img.shields.io/github/last-commit/kspo/apple_stocks_app_clone?label=Last+Commit)

# Super Cupertino Navigation Bar

Customize your iOS-style navigation bar and elevate the user experience of your project.


As a developer who appreciates Cupertino's elegant design, wouldn't you want to add this custom package to your app in development? The Super Cupertino Navigation Bar helps you create an iOS-style navigation bar while allowing you to add a search field and customize avatars.

| Floated Large Title                                                                                                         | Pinned Large Title                                                                                                            | Only Large Title                                                                                                              | Normal Navbar Floated                                                                                                         | Normal Navbar Pinned                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <img src="https://raw.githubusercontent.com/kspo/super_cupertino_navigation_bar/main/screenshots/intro.gif" width="75px"/> | <img src="https://raw.githubusercontent.com/kspo/super_cupertino_navigation_bar/main/screenshots/intro_1.gif" width="75px"/> | <img src="https://raw.githubusercontent.com/kspo/super_cupertino_navigation_bar/main/screenshots/intro_2.gif" width="75px"/> | <img src="https://raw.githubusercontent.com/kspo/super_cupertino_navigation_bar/main/screenshots/intro_33.gif" width="75px"/> | <img src="https://raw.githubusercontent.com/kspo/super_cupertino_navigation_bar/main/screenshots/intro_4.gif" width="75px"/> |

**It's been necessary from the beginning, and I just did it.**

<img src="https://raw.githubusercontent.com/kspo/super_cupertino_navigation_bar/main/screenshots/cheers.gif" width="351px"/>

### Why Should You Use Super Cupertino Navigation Bar?

1. **iOS-Style Navigation Bar**: Offer a more familiar experience to your iOS users. The Super Cupertino Navigation Bar reflects the native look and feel of iOS devices.


2. **Search Field**: Help users find content in your app more quickly and easily. Provide users with the ability to search.


3. **Avatar Customization**: Empower users to personalize their profiles. Customizable avatar addition is a fantastic way to recognize and customize users.


4. **Perfect Compatibility**: Seamlessly integrates with the Cupertino library. It works harmoniously with other components of your Flutter app.


5. **Transition Animations**: With this extension, you can have all transition animation on page route.


## Okay! Let's dive deep!

#### Table of Content

- [Getting Started](#getting-started)
- [Attributes of SuperCupertinoNavigationBar](#attributes)
  - [AppBarType Enum](#asd)
- [Attributes of SearchFieldDecoration](#attributes-of-bottombartheme)
  - [Attributes of SearchResultHeader](#asd)
  - [SearchFieldBehaviour Enum](#asd)
- [Attributes of AvatarModel](#attributes-of-mainactionbuttontheme)

### Getting Started

#### Add dependency

```yaml
dependencies:
  super_cupertino_navigation_bar: ^1.0.0
```

#### Add import package

```dart
import 'package:super_cupertino_navigation_bar/super_cupertino_navigation_bar.dart';
```

#### Easy to use

<strong style="color:#F99417">SuperCupertinoNavigationBar</strong> widget has **CustomScrollView** widget in it so you should place your children in **slivers** key whose type List.

```dart
CupertinoPageScaffold(  //inside CupertinoPageScaffold
  child: SuperCupertinoNavigationBar(
      transitionBetweenRoutes: false, // if don't want transition animation set false / default is true
      largeTitleType: AppBarType.LargeTitleWithFloatedSearch, // Set desired AppBarType
      avatarModel: AvatarModel(
        avatarUrl: null,
        avatarIsVisible: true, // Avatar is hidden as default, if you want to set visible, simply set true
        onTap: () => print("some event"),
      ),
      largeTitle: const Text('Home'),
      searchFieldDecoration: SearchFieldDecoration(
          hideSearchBarOnInit: true,
          searchFieldBehaviour: SearchFieldBehaviour.ShowResultScreenAfterFieldInput,
      ),
      slivers: [
        // Any Sliver here
      ],
  ),
);
```

[linkedin]: https://www.linkedin.com/in/kaz%C4%B1m-selman-poyraz-0048b7143/
[github]: https://github.com/kspo