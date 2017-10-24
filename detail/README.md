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
#### 1b) Where to call onAttach, onDetach [Activity, Fragment]
1) [1]

#### 1c) Injection of Network Repository
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
1) How to avoid network call on configuration changes
3) Integrate Realm Database
4) Integrate Preference
5) Making repository work with all 3(network, database & pref)
### UI
----
1) View Pager + Navigation Drawer + Recycler View
### CONFIGURATION CHANGES
----
1) RTL -> Languages change -> by saving presenter state

