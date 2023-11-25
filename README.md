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
<br>

    php artisan config:clear
<br>


## Maintenance Mode
Deixar o servidor em modo de manutenção

    php artisan down
<br>

    view de erro: resources/views/errors/503.blade.php
<br>

    php artisan up
<br>
