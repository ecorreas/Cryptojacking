TUTORIAL PRÁTICO CRYPTOJACKING

- Fizemos um passo-a-passo de como implentar um ateque de cryptojacking

- O primeiro passo é dar um fork nesse repositório, para você ter copia do repositório;

- Crie uma conta no https://webminepool.com/, escolha o mode become a provider;

- Em seguida faça o login;

- Vá para Api Keys e copie a chave SiteKey;

- Cole na variável siteKey no arquivo index.html disponível na sua copia do repositório;

- Crie uma conta em https://www.heroku.com/, após criar a conta verifique seu e-mail;

- Click em Create a new app, de um nome para o app e uma região;

- Após isso você deve escolher o método de Deploy, conecte o seu GitHub, e escolha a cópia do repositório;

- Para finalizar o click em Deploy Branch;

pronto, a página já esta com o ataque de cryptojacking funcionando, agora é só esperar as vitimas.


HOSPEDANDO UM CRYPTOJACKING NA SUA MÁQUINA
**Para o seu cryptojacking funcionar você deve desativar o bloqueador de _cryptominer_ do seu navegador.**


Antes de iniciar, é recomendado ter uma conta *Provider* no site https://webminepool.com/. 

Primeiro de tudo, vamos instalar nosso servidor em uma máquina Linux.

- Para isso, abra um terminal e digite os comandos abaixo:

- Atualizar a lista de repositórios

#apt update

- Instalar o pacote apache2, que será nosso servidor

#apt install apache2

- Para testar seu servidor, abra um navegador e digite *localhost*

- Temos agora que baixar o código do github disponibilizado

- Em seu terminal, digite:

- Acesse o diretório em que nossa página será hospedada

$ cd /var/www/

- Vamos baixar o código para o nosso servidor

$ git clone https://github.com/ecorreas/Cryptojacking.git

- Agora temos que alterar o arquivo *index.html* e adicionar nossa *siteKey*

- Abra um editor de texto e altere a variável *siteKey* (linha 9) para a *siteKey* obtida na aba *API Keys* do site da *WebMinePool*.

Basta abrir no seu navegador o seguinte endereço: *localhost/index.html*
Se tudo ocorreu certo, você verá seu consumo de CPU aumentar radicalmente.

