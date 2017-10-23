# Purpose
### MVP
----
#### 1a) Base Presenter
1) 1

a- [todo-mvp](https://github.com/googlesamples/android-architecture/blob/todo-mvp/todoapp/app/src/main/java/com/example/android/architecture/blueprints/todoapp/BasePresenter.java)
```java
interface BasePresenter
    void start();
```
b- [todo-mvp-dagger](https://github.com/googlesamples/android-architecture/blob/todo-mvp-dagger/todoapp/app/src/main/java/com/example/android/architecture/blueprints/todoapp/BasePresenter.java)
```java
interface BasePresenter<T>
     void takeView(T view); 
     void dropView();
```
2) [2](https://github.com/googlecodelabs/android-testing/blob/master/app/src/main/java/com/example/android/testing/notes/notes/NotesPresenter.java)
```java
class NotesPresenter
```
3) 3

a- [android-mvp-architecture](https://github.com/MindorksOpenSource/android-mvp-architecture/blob/master/app/src/main/java/com/mindorks/framework/mvp/ui/base/BasePresenter.java)
```java
class BasePresenter<V extends MvpView> implements MvpPresenter<V> 
     @Override
     public void onAttach(V mvpView)  
     @Override
     public void onDetach()
```
b- [android-mvp-interactor-architecture](https://github.com/MindorksOpenSource/android-mvp-interactor-architecture/blob/master/app/src/main/java/com/mindorks/framework/mvp/ui/base/BasePresenter.java)
```java
class BasePresenter<V extends MvpView, I extends MvpInteractor> implements MvpPresenter<V, I>
     @Override
     public void onAttach(V mvpView)  
     @Override
     public void onDetach()
```

4) [4](https://github.com/androidstarters/android-starter/blob/develop/app/src/main/java/io/mvpstarter/sample/features/base/BasePresenter.java)
```java
class BasePresenter<T extends MvpView> implements Presenter<T>  
     @Override
     public void attachView(T mvpView) 
     @Override
     public void detachView()
```
5) [5](https://github.com/ribot/ribot-app-android/blob/master/app/src/main/java/io/ribot/app/ui/base/BasePresenter.java)
```java
class BasePresenter<T extends MvpView> implements Presenter<T>
     @Override
     public void attachView(T mvpView)  
     @Override
     public void detachView()
```
6) [6](https://github.com/athkalia/Just-Another-Android-App/blob/develop/app/src/main/java/com/example/features/dashboard/presenter/MainPresenter.java)
```java
class MainPresenter extends MvpNullObjectBasePresenter<MainView> 
     @Override
     public void detachView(boolean retainInstance)
```
7) [7](https://github.com/andremion/Villains-and-Heroes/blob/master/app/src/main/java/com/andremion/heroes/ui/AbsPresenter.java) 
```java
abstract class AbsPresenter<V>
     @CallSuper public void attachView(@NonNull V view)
     @CallSuper public void detachView()
```

#### 1b) Injection of Network Repository
1) [1](https://github.com/googlesamples/android-architecture/blob/todo-mvp/todoapp/app/src/main/java/com/example/android/architecture/blueprints/todoapp/addedittask/AddEditTaskActivity.java) 

a- todo-mvp (Repository is **injected** in **Activity** and pass to **Presenter** via constructor)
```java
//Activity.java
mAddEditTaskPresenter = new AddEditTaskPresenter(
                taskId,
                Injection.provideTasksRepository(getApplicationContext()),
                addEditTaskFragment,
                shouldLoadDataFromRepo);
```

b- todo-mvp-dagger (Presenter constructor is **injected** directly in **Presnter**)
```java
//Presenter.java
@Inject
AddEditTaskPresenter(@Nullable String taskId, @NonNull TasksRepository tasksRepository,
                         Lazy<Boolean> shouldLoadDataFromRepo) {
     mTaskId = taskId;
     mTasksRepository = tasksRepository;
     mIsDataMissingLazy = shouldLoadDataFromRepo;
}
```
2) [2](https://github.com/googlecodelabs/android-testing/blob/master/app/src/main/java/com/example/android/testing/notes/notes/NotesActivity.java)  (Repository is **injected** in **Fragment** and pass to **Presenter** via constructor)
```java
 mActionListener = new AddNotePresenter(Injection.provideNotesRepository(), this,
                Injection.provideImageFile());
```

#### Dagger injection
1) Insert Presenter from Dagger in Activity
2) Insert repository in Presenter (not in Activity)
### OTHERS
----
3) Integrate Realm Database
4) Integrate Preference
5) Making repository work with all 3(network, database & pref)
### UI
----
1) View Pager + Navigation Drawer + Recycler View
### CONFIGURATION CHANGES
----
1) RTL -> Languages change -> by saving presenter state

# Reddit
[Reddit -> Sample_App_Required_That_Uses_MVP_Dagger_Retrofit](https://www.reddit.com/r/androiddev/comments/76wqog/sample_app_required_that_uses_mvp_dagger_retrofit/)

# Articles

### COLLECTION OF [STARTERS](http://androidstarters.com/)
1) {a,b} Official Google - Architecture Blue Prints : https://github.com/googlesamples/android-architecture
2) Official Google - Code Labs https://codelabs.developers.google.com/codelabs/android-testing/index.html#0
3) {a,b} 3rd Party - Quiz - App : https://github.com/MindorksOpenSource
4) 3rd Party - Pokemon API - App: https://github.com/androidstarters/android-starter/
5) 3rd Party - Ribot - App : https://github.com/ribot/ribot-app-android
6) 3rd Party - Dribble API - App : https://github.com/athkalia/Just-Another-Android-App
7) Marvel Comic API - Multiple Implementations [Main](https://goo.gl/weZ471) | [1](https://github.com/segunfamisa/marvel-comics-android) | [Basic-NoDagger,RxJava](https://github.com/JoaquimLey/avenging) | [Realm](https://github.com/segunfamisa/marvel-comics-android) | [Databinding](https://github.com/andremion/Villains-and-Heroes) | [All](https://github.com/mirhoseini/marvel)
8) [My Reddit Question](https://www.reddit.com/r/androiddev/comments/76wqog/sample_app_required_that_uses_mvp_dagger_retrofit/)

----
### 1- Official Google -> [android-architecture](https://github.com/googlesamples/android-architecture)

#### 1a [android-architecture/tree/todo-mvp](https://github.com/googlesamples/android-architecture/tree/todo-mvp/)

1) Dagger
2) Testing
3) Portrait + Landscape (Configuration change supported)
4) Activities + Fragments
5) Repository (Fake Implementation)

#### 1b [android-architecture/tree/todo-mvp-dagger](https://github.com/googlesamples/android-architecture/tree/todo-mvp-dagger/)

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
### 3- 3rd Party -> [Mindorks](https://github.com/MindorksOpenSource)

[Reddit](https://www.reddit.com/r/androiddev/comments/6po5ls/any_good_resources_on_mvp_step_by_step/)

#### 3a [android-mvp-architecture](https://github.com/MindorksOpenSource/android-mvp-architecture)

1) Repository (Network, DB, Prefs)
2) Navigation Drawer
3) Only Portrait orientation supported
4) RxJava, ButterKnife

#### 3b [android-mvp-interactor-architecture](https://github.com/MindorksOpenSource/android-mvp-interactor-architecture)

1) Repository (Network, DB, Prefs)
2) Navigation Drawer
3) Only Portrait orientation supported
4) RxJava, ButterKnife

----
### 4- 3rd Party -> [Starter](https://github.com/androidstarters/android-starter/)

[Reddit](https://www.reddit.com/r/androiddev/comments/5s72bi/android_app_starter_based_on_android_mvp_dagger2/)

1) Simplicity
2) Retrofit, RxJava, ButterKnife
3) Portrait + Landscape (Configuration change not supported) 

----
### 5- 3rd Party -> [Ribot](https://github.com/ribot/ribot-app-android )

1) Repository (uses all 3)
2) Retrofit, SqlBright, RxJava, ButterKnife
3) Marshmallow [6] permission

----
### 6- 3rd Party -> [Dribble API](https://github.com/athkalia/Just-Another-Android-App)

1) Mosby MVP
2) Screen orientation changes supported (via ViewState)
3) Nougat [7.1] apps shortcut

----
### 7- 3rd Party -> [Dribble API](https://github.com/segunfamisa/marvel-comics-android)

1) Screen orientation changes supported
2) Databinding, Retrofit, Dagger, RxJava, Realm

----

# Issues with NLA-4b
1) Dagger: Improper use of Dagger as Presenter is not injected
2) Dagger: Scope, Component not used
3) Binding [best practice](https://github.com/andremion/Villains-and-Heroes/tree/master/app/src/main/java/com/andremion/heroes/ui/binding) not followed to display image from glide 


# Useful Tutorial
Databinding:
http://www.vogella.com/tutorials/AndroidDatabinding/article.html
