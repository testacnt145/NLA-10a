# Purpose
### MVP
#### Base Presenter
1) [1](https://github.com/googlesamples/android-architecture/blob/todo-mvp-dagger/todoapp/app/src/main/java/com/example/android/architecture/blueprints/todoapp/BasePresenter.java) | [2](https://github.com/googlecodelabs/android-testing/blob/master/app/src/main/java/com/example/android/testing/notes/notes/NotesPresenter.java) | [3](https://github.com/MindorksOpenSource/android-mvp-architecture/blob/master/app/src/main/java/com/mindorks/framework/mvp/ui/base/BasePresenter.java) | [4](https://github.com/androidstarters/android-starter/blob/develop/app/src/main/java/io/mvpstarter/sample/features/base/BasePresenter.java) | [5](https://github.com/ribot/ribot-app-android/blob/master/app/src/main/java/io/ribot/app/ui/base/BasePresenter.java) | [6](https://github.com/andremion/Villains-and-Heroes/blob/master/app/src/main/java/com/andremion/heroes/ui/AbsPresenter.java)
2) 1 has BasePresnter(interface) | 3,4,5,6 hasBasePresenter(class) that implements Presenter(interface)
#### Dagger injection
1) Insert Presenter from Dagger in Activity
2) Insert repository in Presenter (not in Activity)
### OTHERS
3) Integrate Realm Database
4) Integrate Preference
5) Making repository work with all 3(network, database & pref)
### UI
1) View Pager + Navigation Drawer + Recycler View
### CONFIGURATION CHANGES
1) RTL -> Languages change -> by saving presenter state


# Articles
1) Official Google - Architecture Blue Prints : https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/
2) Official Google - Code Labs https://codelabs.developers.google.com/codelabs/android-testing/index.html#0
3) 3rd Party - Quiz - App : https://github.com/MindorksOpenSource/android-mvp-architecture
4) 3rd Party - Pokemon API - App: https://github.com/androidstarters/android-starter/
5) 3rd Party - Ribot - App : https://github.com/ribot/ribot-app-android
6) 3rd Party - Dribble API - App : https://github.com/athkalia/Just-Another-Android-App
7) Marvel Comic API - Multiple Implementations [Main](https://goo.gl/weZ471) | [1](https://github.com/segunfamisa/marvel-comics-android) | [Basic-NoDagger,RxJava](https://github.com/JoaquimLey/avenging) | [Realm](https://github.com/segunfamisa/marvel-comics-android) | [Databinding](https://github.com/andremion/Villains-and-Heroes) | [All](https://github.com/mirhoseini/marvel)

----
### 1- Official Google -> [android-architecture/tree/todo-mvp-dagger](https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/)

1) Dagger
2) Testing
3) Portrait + Landscape (Configuration change supported)
4) Activities + Fragments
5) Repository (Fake Implementation)

----
### 2- Official Google -> [Code Labs](https://codelabs.developers.google.com/codelabs/android-testing/index.html#0)

[Reddit](https://www.reddit.com/r/androiddev/comments/75wgde/android_architecture_blueprints_todomvp_sample/do9lrs3/)

[Reddit](https://www.reddit.com/r/androiddev/comments/6po5ls/any_good_resources_on_mvp_step_by_step/)

1) Testing in detail
2) Portrait + Landscape (Configuration change supported)
3) Activities + Fragments
4) Repository (Fake Network Api)

----
### 3- 3rd Party -> [Mindorks](https://github.com/MindorksOpenSource/android-mvp-architecture)

[Reddit](https://www.reddit.com/r/androiddev/comments/6po5ls/any_good_resources_on_mvp_step_by_step/)

1) Repository (Network, DB, Prefs)
2) Navigation Drawer
3) Only Portrait orientation supported
4) RxJava, ButterKnife

----
### 4- 3rd Party -> [Starter](https://github.com/androidstarters/android-starter/)

[Reddit](https://www.reddit.com/r/androiddev/comments/5s72bi/android_app_starter_based_on_android_mvp_dagger2/)

1) Simplicity
2) Retrofit, RxJava, ButterKnife

----
### 5- 3rd Party -> [Ribot](https://github.com/ribot/ribot-app-android )

1) Repository (uses all 3)
2) Retrofit, SqlBright, RxJava, ButterKnife

----

# Issues with NLA-4b
1) Dagger: Improper use of Dagger as Presenter is not injected
2) Dagger: Scope, Component not used
3) Binding [best practice](https://github.com/andremion/Villains-and-Heroes/tree/master/app/src/main/java/com/andremion/heroes/ui/binding) not followed to display image from glide 


# Useful Tutorial
Databinding:
http://www.vogella.com/tutorials/AndroidDatabinding/article.html
