# NLA-10a (my)

Databinding:
http://www.vogella.com/tutorials/AndroidDatabinding/article.html


1) Integrate Realm Database
2) Integrate Preference
3) Making repository work with all 3(network, database & pref)

MVP is the mix of these 3
1) Googleness + Unit Testing : https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/
2) Repository of 3: https://github.com/MindorksOpenSource/android-mvp-architecture
3) Simplicity : https://github.com/androidstarters/android-starter/

# Main Points learned from 3 articles
MVP
----
1. Insert Presenter from Dagger in Activity
2. Insert repository in Presenter (not in Activity)

# Issues with NLA-4b
1) Improper use of Dagger as Presenter is not injected
