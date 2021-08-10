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
