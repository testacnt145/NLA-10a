# Purpose
### MVP
1) Insert Presenter from Dagger in Activity
2) Insert repository in Presenter (not in Activity)
3) Integrate Realm Database
4) Integrate Preference
5) Making repository work with all 3(network, database & pref)
### UI
1) View Pager + Navigation Drawer + Recycler View
### Proper Configuration changes handeling
1) RTL -> Languages change -> by saving presenter state


# Articles
1) Official Google - Architecture Blue Prints : https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/
2) Official Google - Code Labs https://codelabs.developers.google.com/codelabs/android-testing/index.html#0
3) 3rd Party : https://github.com/MindorksOpenSource/android-mvp-architecture
4) 3rd Party : https://github.com/androidstarters/android-starter/

----
### 1- Official Google -> [android-architecture/tree/todo-mvp-dagger](https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/)

1) Dagger
2) Testing
3) Portrait + Landscape (Configuration change supported)
4) Activities + Fragments

----
### 2- Official Google -> [Code Labs](https://codelabs.developers.google.com/codelabs/android-testing/index.html#0)

Based on [Reddit](https://www.reddit.com/r/androiddev/comments/75wgde/android_architecture_blueprints_todomvp_sample/do9lrs3/)

1) Testing in detail
2) Portrait + Landscape (Configuration change supported)
3) Activities + Fragments
4) Repository (Fake Network Api)

----
### 3- 3rd Party -> [Mindorks](https://github.com/MindorksOpenSource/android-mvp-architecture)

1) Repository (Network, DB, Prefs)
2) Navigation Drawer
3) Only Portrait orientation supported

----
### 4- 3rd Party -> [Starter](https://github.com/androidstarters/android-starter/)

1) Simplicity

----

# Issues with NLA-4b
1) Improper use of Dagger as Presenter is not injected

# Useful Tutorial
Databinding:
http://www.vogella.com/tutorials/AndroidDatabinding/article.html
