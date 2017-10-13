# NLA-10a (my)

Databinding:
http://www.vogella.com/tutorials/AndroidDatabinding/article.html


1) Integrate Realm Database
2) Integrate Preference
3) Making repository work with all 3(network, database & pref)

MVP is the mix of these articles:
1) Official Google - Unit Testing : https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/
2) Official Google - Testing - Code Labs : https://codelabs.developers.google.com/codelabs/android-testing/index.html#0
3) Repository of 3(Network, DB, Prefs) : https://github.com/MindorksOpenSource/android-mvp-architecture
4) Simplicity : https://github.com/androidstarters/android-starter/

# Main Points learned from above articles
MVP
----
1. Insert Presenter from Dagger in Activity
2. Insert repository in Presenter (not in Activity)

# Issues with NLA-4b
1) Improper use of Dagger as Presenter is not injected
