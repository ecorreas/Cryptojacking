# TUTORIAL PRÁTICO CRYPTOJACKING


Ambinete usado na criação deste tutorial:
```
Linux Mint 20 Cinnamon
Kernel: 5.4.0
```

## HOSPEDANDO UM CRYPTOJACKING NO SERVIDOR WEB

**Para o seu cryptojacking funcionar, você deve desativar o bloqueador de _cryptominer_ do seu navegador.**

Foi testado nos seguintes navegadores:
```
Mozilla Firefox 88.0
```

- O primeiro passo é dar um fork nesse repositório, para você ter copia do repositório;

- Crie uma conta no [WebMinePool](https://webminepool.com/), escolha o mode become a provider;

- Em seguida faça o login;

- Vá para Api Keys e copie a chave SiteKey;

- Cole na variável siteKey no arquivo index.html disponível na sua copia do repositório;

- Crie uma conta em [Heroku](https://www.heroku.com/), após criar a conta verifique seu e-mail;

- Click em Create a new app, de um nome para o app e uma região;

- Após isso você deve escolher o método de Deploy, conecte o seu GitHub, e escolha a cópia do repositório;

- Para finalizar o click em Deploy Branch;

pronto, a página já esta com o ataque de cryptojacking funcionando, agora é só esperar as vítimas.


**Desativando o bloqueio de cryptominer do navegador**

 
- Preferências -> Privacidade e Segurança -> Customizado -> Desmarcar a opção "Cryptominers"


## HOSPEDANDO UM CRYPTOJACKING NA SUA MÁQUINA

**Para o seu cryptojacking funcionar, você deve desativar o bloqueador de _cryptominer_ do seu navegador.**

Esta parte do tutorial foi testado no seguinte ambiente:

```
Máquina Virtual - VMware Workstation 16
Mozilla Firefox 78.10esr
Kali Linux 20.04 Kernel: 5.9.0
Apache/2.4.46
```

Antes de iniciar, é recomendado ter uma conta *Provider* no site [WebMinePool](https://webminepool.com/). 

Primeiro de tudo, vamos instalar nosso servidor.

- Para isso, abra um terminal e digite os comandos abaixo:

- Atualizar a lista de repositórios.

```
$ sudo apt update
```

- Instalar o pacote apache2, que será nosso servidor.

```
$ sudo apt install apache2
```

- Devemos iniciar o processo do nosso servidor web.

```
$ sudo service apache2 restart
```

- Para testar seu servidor, abra o navegador e digite `localhost` na barra de endereço.
- Você deve ver uma página de boas-vindas do servidor Apache.

- Agora clone este repositório.

- Abra um terminal e digite o seguinte comando:

```
$ cd /var/www/html && sudo git clone https://github.com/ecorreas/Cryptojacking.git

```

- Agora temos que alterar o arquivo *index.html* e adicionar nossa *siteKey*.

```
$ sudo nano /var/www/html/Cryptojacking/index.html
```

- Altere a variável *siteKey* da linha 9 substituindo pela *siteKey* obtida na aba *API Keys* do site da *WebMinePool*.

- Se tudo ocorreu bem até aqui, seu cryptojacking está pronto para minerar.
- Basta abrir seu navegador e acessar a url: `localhost/Cryptojacking/index.php`.
- Ao digitar ```top``` no seu terminal, observe o processo chamado `Web Content`, ele deve aparecer no topo da lista consumindo bastante CPU.
