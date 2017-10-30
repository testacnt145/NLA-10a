Project using [minforks-mvp](https://github.com/MindorksOpenSource/android-mvp-architecture/tree/master/app/src/main/java/com/mindorks/framework/mvp/ui)

**Changes**
1. Remove all abstract methods from Base MvpView & place it inthier specific views
2. Remove *handleApiError* and *setUserAsLoggedOut* from Base MvpPresenter & place it inthier specific presenters
3. Move *MainMvpView* and *MainMvpPresenter* inside MainContract and rename it to *View* and *Presenter* only


**BASE ACTIVITY**

1. [Ribot](https://github.com/ribot/ribot-app-android/blob/master/app/src/main/java/io/ribot/app/ui/base/BaseActivity.java) 

. MVP base like official android blueprints

. issues : not up to date

**UP TO DATE MVP**

1. [Mindorks-mvp](https://github.com/MindorksOpenSource/android-mvp-architecture) 
    
. perfect for dagger

. issues : base class implementations too abstract
