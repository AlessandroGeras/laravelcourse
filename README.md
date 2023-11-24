# Laravel Commands
<br>

## Environment Variable
Passar uma variável de ambiente do arquivo .env para a aplicação

    .env: MINHA_VARIAVEL_GLOBAL="Hello Word"
<br>

    blade: echo env('MINHA_VARIAVEL_GLOBAL');


## Server Timezone

    config/app.php: 'timezone' => 'America/Sao_Paulo',
<br>

    controller: use Illuminate\Support\Facades\Date;
                $horaServidor = Date::now();
