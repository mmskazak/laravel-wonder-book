# laravel-wonder-book

### 1. Передача дополнительных параметров в политики Laravel ###

     /*
     *   В политики доплнительные данные могут передаваться в таком виде,
     *   например такой код может быть в Resource
     *   'permissions' => [
     *      'detachUser' => auth()->user()->can('detachUser', [$someModel, $plusData]),
     *      'attachUser' => auth()->user()->can('attachUser', [$someModel, $plusData]),
     *    ],
     */     
    public function attachUser(User $user, SomeModel $someModel, PlusData $plusData): bool
    {
      //do something
    }
    
### 2. Carbon работа со временем ###
    
    First, Eloquent automatically converts it's timestamps (created_at, updated_at) into carbon objects. You could just use updated_at to get that nice feature, or specify edited_at in your model in the $dates property:

    protected $dates = ['edited_at'];
    Now back to your actual question. Carbon has a bunch of comparison functions:

    eq() equals
    ne() not equals
    gt() greater than
    gte() greater than or equals
    lt() less than
    lte() less than or equals
    Usage:

    if($model->edited_at->gt($model->created_at)){
        // edited at is newer than created at
    }
    
### 3. Установка Vuetify в Laravel ###    
    https://stackoverflow.com/questions/48735602/how-to-implement-vuetify-in-laravel
    
    
### 4. Подключение к базе данных Laravel sail ###  
    
    https://tallpad.com/series/laravel-sail/lessons/creating-a-database-client-connection
    
### 5. Установка докер на Ubuntu ###  
    https://www.digitalocean.com/community/tutorials/docker-ubuntu-18-04-1-ru
    
### 6. Установка докер-компос на Ubuntu ###     
    https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-18-04-ru
    
### 7. Настройка гитлаб в облаке ### 
    
    https://mcs.mail.ru/help/ru_RU/cases-gitlab/case-gitlab
    
### 8. Установака gitlab из докера, проблема с перввой авторзацией ###

https://forum.gitlab.com/t/how-to-login-for-the-first-time-local-install-with-docker-image/55297/5
https://stackoverflow.com/questions/55747402/docker-gitlab-change-forgotten-root-password
