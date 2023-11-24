# Laravel Commands
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
<br>

    php artisan config:clear
<br>
