# code_test
I've seen this code is following repository pattern for model, It is good. but it will slow the code, because whenever the controller calls, then repository __constructor automatically calls and it will use memory + time,

We can make repository code more beautiful and easy to read, by following all laravel query builder method
like using ->when() instead of if/else

On Some places we use Model and some places we use DB facades for access database, we should go with EloquentModel,
In BookingController index method, I see env('ADMIN_ROLE_ID') use in function,
We can use it through config file, first create a config file, then declare env variable in configs and use them. eg configs('project.admin_role_id');

No proper comments on functions