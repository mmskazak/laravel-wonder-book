# laravel-wonder-book

    1. Передача дополнительных параметров в политики Laravel

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
