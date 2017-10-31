Project using [minforks-mvp](https://github.com/MindorksOpenSource/android-mvp-architecture/tree/master/app/src/main/java/com/mindorks/framework/mvp/ui)

## Changes
**1**
1. refactor app name, package name,
2. new icon, new libraries
3. change orientation to P+L
4. remove splash

**2**
1. Remove all abstract methods from Base MvpView & place it inthier specific views
2. Remove *SchedulerProvider*, *CompositeDisposable*, *handleApiError* and *setUserAsLoggedOut*  from Base MvpPresenter & place it in thier specific presenters
3. Move *MainMvpView* and *MainMvpPresenter* inside MainContract and rename it to *View* and *Presenter* only
4. Change constructor from @Inject *MainPresenter(DataManager dataManager, SchedulerProvider schedulerProvider, CompositeDisposable compositeDisposable)* to *MainPresenter(DataManager dataManager)*
5. Remove all extra classes only *main activity* left

**3**
1. Remove rxutils
2. Remove all crap from *MainActivity* except Navigation View
3. add *Details Activity*
4. add *Feed Activity* that has View Pager

**4**
1. Use same recycle view items in blog and implement google places with data binding
1. Details Activity: Recycler View 
2. Details Activity: Proper usage of Network repository
3. Details Activity: Configuration changes handeled
4. Details Activity: Retrofit NewsAPI call

**BASE ACTIVITY**

1. [Ribot](https://github.com/ribot/ribot-app-android/blob/master/app/src/main/java/io/ribot/app/ui/base/BaseActivity.java) 

. MVP base like official android blueprints

. issues : not up to date

**UP TO DATE MVP**

1. [Mindorks-mvp](https://github.com/MindorksOpenSource/android-mvp-architecture) 
    
. perfect for dagger

. issues : base class implementations too abstract
