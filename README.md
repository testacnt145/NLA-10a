# Reddit
[Reddit -> Sample_App_Required_That_Uses_MVP_Dagger_Retrofit](https://www.reddit.com/r/androiddev/comments/76wqog/sample_app_required_that_uses_mvp_dagger_retrofit/)

# Articles

### COLLECTION OF [STARTERS](http://androidstarters.com/)
1) {a,b} Official Google - Architecture Blue Prints : https://github.com/googlesamples/android-architecture
2) Official Google - Code Labs : https://codelabs.developers.google.com/codelabs/android-testing/index.html#0
3) {a,b} 3rd Party - Quiz - App : https://github.com/MindorksOpenSource
4) 3rd Party - Pokemon API - App : https://github.com/androidstarters/android-starter/
5) 3rd Party - Ribot - App : https://github.com/ribot/ribot-app-android
6) 3rd Party - Dribble API - App : https://github.com/athkalia/Just-Another-Android-App
7) Marvel Comic API - Multiple Implementations : [Main](https://goo.gl/weZ471) | [1](https://github.com/segunfamisa/marvel-comics-android) | [Basic-NoDagger,RxJava](https://github.com/JoaquimLey/avenging) | [Realm](https://github.com/segunfamisa/marvel-comics-android) | [Databinding](https://github.com/andremion/Villains-and-Heroes) | [All](https://github.com/mirhoseini/marvel)
8) [My Reddit Question](https://www.reddit.com/r/androiddev/comments/76wqog/sample_app_required_that_uses_mvp_dagger_retrofit/)

----
### 1- Official Google -> [android-architecture](https://github.com/googlesamples/android-architecture)

#### 1a [android-architecture/tree/todo-mvp](https://github.com/googlesamples/android-architecture/tree/todo-mvp/todoapp/app/src/main/java/com/example/android/architecture/blueprints/todoapp) **3-Mar-16 | 22,437**

#### 1b [android-architecture/tree/todo-mvp-dagger](https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/todoapp/app/src/main/java/com/example/android/architecture/blueprints/todoapp) **3-Mar-16 | 22,437**

1) Dagger
2) Testing
3) P+L(Config-chages-sup => Recycler view retains its position)
4) Activities + Fragments
5) Repository (Fake Implementation)
6) UI(Navigation Drawer)

----
### 2- Official Google -> [Code Labs](https://github.com/googlecodelabs/android-testing/tree/master/app/src/main/java/com/example/android/testing/notes) **20-Mar-15 | 408**

[Reddit](https://www.reddit.com/r/androiddev/comments/75wgde/android_architecture_blueprints_todomvp_sample/do9lrs3/)

[Reddit](https://www.reddit.com/r/androiddev/comments/6po5ls/any_good_resources_on_mvp_step_by_step/)

1) Testing in detail
2) P+L(Config-chages-sup => Recycler view retains its position)
3) Activities + Fragments
4) Repository (Fake Network Api)
5) UI(Navigation Drawer, Recycler View)

----
### 3- 3rd Party -> [Mindorks](https://github.com/MindorksOpenSource)

[Reddit](https://www.reddit.com/r/androiddev/comments/6po5ls/any_good_resources_on_mvp_step_by_step/)

[My Github issue](https://github.com/MindorksOpenSource/android-mvp-architecture/issues/46)

#### 3a [android-mvp-architecture](https://github.com/MindorksOpenSource/android-mvp-architecture/tree/master/app/src/main/java/com/mindorks/framework/mvp) **27-Jan-17 | 1936**

#### 3b ~~[android-mvp-interactor-architecture](https://github.com/MindorksOpenSource/android-mvp-interactor-architecture/tree/master/app/src/main/java/com/mindorks/framework/mvp)~~ **27-Jan-17 | 141 | *Too broad***

1) Repository (Network, DB, Prefs)
2) P only
3) RxJava, ButterKnife
4) UI(Navigation Drawer, Recycler View)

----
### 4- ~~3rd Party -> [Starter](https://github.com/androidstarters/android-starter/tree/develop/app/src/main/java/io/mvpstarter/sample)~~ **4-Aug-16 | 428 | *Copied Ribot***


[Reddit](https://www.reddit.com/r/androiddev/comments/5s72bi/android_app_starter_based_on_android_mvp_dagger2/)

1) Simplicity
2) P+L(Config-chages-Not-sup => Network call every time) 
3) Retrofit, RxJava, ButterKnife
4) UI(Recycler View)

----
### 5- 3rd Party -> [Ribot](https://github.com/ribot/ribot-app-android/tree/master/app/src/main/java/io/ribot/app) **21-Sep-15 | 1164**

1) Repository (uses all 3)
2) P+L
2) Retrofit, SqlBright, RxJava, ButterKnife
3) UI(Recycler View)
4) Marshmallow [6] permission
5) Oauth2
6) [Android Architecture, Code Guidelines](https://github.com/ribot/android-guidelines) |[Code Quality, Code Analysis tool](https://github.com/ribot/ribot-app-android#code-quality)

----
### 6- 3rd Party -> [Dribble API](https://github.com/athkalia/Just-Another-Android-App/tree/develop/app/src/main/java/com/example) **12-Sep-17 | 1556**

1) Mosby MVP
2) P+L(Config-chages-sup-via-ViewState => Recycler view does Not retain its position)
3) UI(Recycler View)
4) Nougat [7.1] apps shortcut
5) [Code Audit | APK Versioning - Hockey App | Dex count | FInd Bugs](https://github.com/athkalia/Just-Another-Android-App/tree/develop/art)

----
### 7- 3rd Party -> [Marvel Comic API](https://github.com/andremion/Villains-and-Heroes/tree/master/app/src/main/java/com/andremion/heroes) **6-May-16 | 41**

1) P+L(Config-chages-sup => No Network call twice - Recycler view retain its position)
2) Databinding, Retrofit, Dagger, RxJava, Realm
3) UI(Recycler View)

----

# Issues with NLA-4b
1) Dagger: Improper use of Dagger as Presenter is not injected
2) Dagger: Scope, Component not used
3) Binding [best practice](https://github.com/andremion/Villains-and-Heroes/tree/master/app/src/main/java/com/andremion/heroes/ui/binding) not followed to display image from glide 

# SAMPLE APP
#### API 17
#### Android Studio 3.0
#### sourceCompatibility JavaVersion.VERSION_1_8 | targetCompatibility JavaVersion.VERSION_1_8
#### Gradle: 4.1 | Android-Plugin: 3.0.0 | Android-Plugin-Repo: jcenter | Default-Lib-Repo: jcenter,google()

This app uses
1) MVP + Configuration changes supported + Repository (Database, API, Preferences)
2) Retrofit + Dagger + Databining
3) Localization + RTL
4) Fragments + View Pager + Navigation Drawer + Recycler view with multiple items
5) Test Presenter
6) Marshmallow Permission + Nougat App Shortcut + Oreo Notification Dots + Adaptive Icons

Project 7 seems to be suitable as it contains Databinding, Retrofit, Dagger, Realm
TODO:
- add navigation drawer, viewpager
- remove rxjava
- proper rename attachView DetachView, remove abstract class
- proper packaging
- proper use of realm

TODO
1) MVVM (same)
