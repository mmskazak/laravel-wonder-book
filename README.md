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
    https://stackoverflow.com/questions/50985783/vuetify-css-not-working-taking-effect-inside-component
    https://codersdiaries.com/blog/laravel-vuetify
    
    
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
https://docs.gitlab.com/ee/security/reset_user_password.html

### 9. Хороший пример использования интерцептора axios.js
https://medium.com/@ruslan201010/%D1%81%D0%B8%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5-%D1%81%D1%82%D0%BE%D1%80%D0%BE%D0%BD%D1%8B-axios-7eb96df40900

### 10. Пример испльзования middleware Vue.js ###
https://webdevblog.ru/ispolzovanie-middleware-vo-vue/

### 11. Настройка локализации Inertia.js
https://www.nicolaskempf.fr/en/translate-laravel-jetstream-and-inertia-with-vue-i18n-matice/

### 12. Инициализация и Boot в трейтах Eloquent для Laravel 
https://medium.com/swlh/laravel-booting-and-initializing-models-with-traits-2f77059b1915


### 13. Загрука файла из потока

     $filename = 'signer';
        $contents = $response->getBody()->getContents();

        return response()->streamDownload(function () use ($contents) {
            echo $contents;
        }, $filename);
### 14. Laravel создание собственных функций
https://laravel.demiart.ru/laravel-sozdayom-svoi-sobstvennye-funktsii/

### 15.  Возвращает название таблицы 
в модели необходимо добавить метод
public function getTable() {
    return $this->getConnection()->getDatabaseName().".$table";
}
