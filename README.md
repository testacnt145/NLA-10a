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

#### 1a [android-architecture/tree/todo-mvp](https://github.com/googlesamples/android-architecture/tree/todo-mvp/todoapp/app/src/main/java/com/example/android/architecture/blueprints/todoapp)

1) Dagger
2) Testing
3) Portrait + Landscape (Configuration change supported)
4) Activities + Fragments
5) Repository (Fake Implementation)
6) UI(Navigation Drawer)

#### 1b [android-architecture/tree/todo-mvp-dagger](https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/todoapp/app/src/main/java/com/example/android/architecture/blueprints/todoapp)

1) Dagger
2) Testing
3) Portrait + Landscape (Configuration change supported)
4) Activities + Fragments
5) Repository (Fake Implementation)
6) UI(Navigation Drawer)

----
### 2- Official Google -> [Code Labs](https://github.com/googlecodelabs/android-testing/tree/master/app/src/main/java/com/example/android/testing/notes)

[Reddit](https://www.reddit.com/r/androiddev/comments/75wgde/android_architecture_blueprints_todomvp_sample/do9lrs3/)

[Reddit](https://www.reddit.com/r/androiddev/comments/6po5ls/any_good_resources_on_mvp_step_by_step/)

1) Testing in detail
2) Portrait + Landscape (Configuration change supported)
3) Activities + Fragments
4) Repository (Fake Network Api)
5) UI(Navigation Drawer, Recycler View)

----
### 3- 3rd Party -> [Mindorks](https://github.com/MindorksOpenSource)

[Reddit](https://www.reddit.com/r/androiddev/comments/6po5ls/any_good_resources_on_mvp_step_by_step/)

#### 3a [android-mvp-architecture](https://github.com/MindorksOpenSource/android-mvp-architecture/tree/master/app/src/main/java/com/mindorks/framework/mvp)

1) Repository (Network, DB, Prefs)
2) Only Portrait orientation supported
3) RxJava, ButterKnife
4) UI(Navigation Drawer, Recycler View)

#### 3b [android-mvp-interactor-architecture](https://github.com/MindorksOpenSource/android-mvp-interactor-architecture/tree/master/app/src/main/java/com/mindorks/framework/mvp)

1) Repository (Network, DB, Prefs)
2) Only Portrait orientation supported
3) RxJava, ButterKnife
4) UI(Navigation Drawer, Recycler View)

----
### 4- 3rd Party -> [Starter](https://github.com/androidstarters/android-starter/tree/develop/app/src/main/java/io/mvpstarter/sample)

[Reddit](https://www.reddit.com/r/androiddev/comments/5s72bi/android_app_starter_based_on_android_mvp_dagger2/)

1) Simplicity
2) Retrofit, RxJava, ButterKnife
3) Portrait + Landscape (Configuration change not supported) 
4) UI(Recycler View)

----
### 5- 3rd Party -> [Ribot](https://github.com/ribot/ribot-app-android/tree/master/app/src/main/java/io/ribot/app)

1) Repository (uses all 3)
2) Retrofit, SqlBright, RxJava, ButterKnife
3) UI(Recycler View)
4) Marshmallow [6] permission

----
### 6- 3rd Party -> [Dribble API](https://github.com/athkalia/Just-Another-Android-App/tree/develop/app/src/main/java/com/example)

1) Mosby MVP
2) Screen orientation changes supported (via ViewState)
3) UI(Recycler View)
4) Nougat [7.1] apps shortcut
5) [Code Audit | APK Versioning - Hockey App | Dex count | FInd Bugs](https://github.com/athkalia/Just-Another-Android-App/tree/develop/art)

----
### 7- 3rd Party -> [Marvel Comic API](https://github.com/andremion/Villains-and-Heroes/tree/master/app/src/main/java/com/andremion/heroes)

1) Screen orientation changes supported
2) Databinding, Retrofit, Dagger, RxJava, Realm
3) UI(Recycler View)

----

# Issues with NLA-4b
1) Dagger: Improper use of Dagger as Presenter is not injected
2) Dagger: Scope, Component not used
3) Binding [best practice](https://github.com/andremion/Villains-and-Heroes/tree/master/app/src/main/java/com/andremion/heroes/ui/binding) not followed to display image from glide 


# Useful Tutorial
Databinding:
http://www.vogella.com/tutorials/AndroidDatabinding/article.html

# SAMPLE APP - API 17
This app uses
1) MVP + Configuration changes supported + Repository (Database, API, Preferences)
2) Retrofit + Dagger + Databining
3) Localization + RTL
4) Fragments + View Pager + Navigation Drawer + Recycler view with multiple items
5) Test Presenter
6) Marshmallow Permission + Nougat App Shortcut + Oreo Notification Dots + Adaptive Icons

TODO
1) MVVM (same)
