# Laravel Commands
<br>

## Check Environment
Verificar se o servidor está em Desenvolvimento ou em Produção
    
    php artisan about
<br>


## Environment Variable
Passar uma variável de ambiente do arquivo .env para a aplicação

    .env: MINHA_VARIAVEL_GLOBAL="Hello Word"
<br>

    blade: echo env('MINHA_VARIAVEL_GLOBAL');
<br>


## Server Timezone

    config/app.php: 'timezone' => 'America/Sao_Paulo',
<br>

    controller: use Illuminate\Support\Facades\Date;
                $horaServidor = Date::now();
<br>


## Server Cache
Para projetos em produção

    php artisan config:cache
    php artisan route:cache
    php artisan view:cache
<br>

    php artisan config:clear
    php artisan route:clear
    php artisan view:clear
<br>


## Maintenance Mode
Deixar o servidor em modo de manutenção

    php artisan down
<br>

    view de erro: resources/views/errors/503.blade.php
<br>

    php artisan up
<br>


## Routes
Retonar apenas uma view

    Route::view('/', 'index');
<br>

Agrupar controladores

    Route::get("/user/register", [UserController::class, "registerView"])->name("register.user.view");
    Route::post("/user/register", [UserController::class, "store"])->name("register.user");
<br>    

    Route::prefix('user')->group(function () {
    Route::get('/register', [UserController::class, 'registerView'])->name('register.user.view');
    Route::post('/register', [UserController::class, 'store'])->name('register.user');
    });
<br>


## Soft Delete vs Destroy
Soft Delete não destroi o registro, apenas faz uma marcação para não torná-lo disponível

    $user = User::find($id);
    $user->delete();
<br>

O método destroy é chamado diretamente na classe do modelo e exclui o registro pelo ID.

    User::destroy($id);
<br>   
