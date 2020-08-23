# Instalando o servidor

Para começarmos com o pé direito e adotando boas práticas ao criar nosso servidor, lembre-se de não executá-lo em modo **`root`**, sendo, dessa forma, interessante criar um usuário especificamente para este fim. A ideia é isolar o diretório do servidor de CS:GO do seu diretório pessoal ou de qualquer outra aplicação.

Para criar um novo usuário no sistema, digite os seguintes comandos no terminal(root):

``` 
useradd -m csgo
```
Depois atribua uma senha:

```
passwd csgo
```

Após esse processo, faça login no usuário criado executando o seguinte comando:

```
su - csgo
```
Ao se logar no novo usuário criado, crie um diretório para o servidor dedicado:
```
mkdir ~/csgo-server
```
<!-- colocar uma imagem do processo até aqui -->
E por fim, execute o seguinte comando para finalmente instalar o servidor dedicado de CS:GO:

```
steamcmd +force_install_dir ~/csgo-server/ +login anonymous +app_update 740 validate +quit
```

Depois de alguns minutos, o seu servidor já estára instalado na sua máquina. Você verá a mensagem **`Success! App '740' fully installed`**.

O comando **`+force_install_dir ~/csgo-server/`** indica para o SteamCMD que o diretório da instalação do servidor é **`/home/<usuario>/csgo-server/`**, o comando **`+login anonymous`** faz login em modo anônimo (sem a necessidade da sua conta Steam) e **`+app_update 740 validate`** indica que você deseja instalar o servidor de código **`740`** (CS:GO). Alguns servidores de outros jogos necessitam que você faça login com a sua conta Steam para baixar os arquivos necessários, porém o servidor de CS:GO não exige, pode fazer, mas não é necessário.


<!-- | Server | ID | SteamCMD | Steam Client | Anonymous login | Notes |
| :---: | :---: | :---: | :---: | :---: | :---: |
|Counter-Strike Global Offensive Dedicated Server| 740 | Yes | - | Yes | Game purchase required for **public servers** | -->

<!-- Recomendo fortemente consultar as referências após executar o guia acima para maiores informações, porém o que é necessário para instalar o servidor está aqui. -->


<!-- EDITAR ESSA PARTE AO FINAL DA ESCRITA -->
[<< Anterior]() || [Próximo >>]()

## Referências

[How to create users in linux using the `useradd` command](https://linuxize.com/post/how-to-create-users-in-linux-using-the-useradd-command/)

[SteamCMD - Valve Developer Community](https://developer.valvesoftware.com/wiki/SteamCMD#Running_SteamCMD)

[Dedicated Server list - Valve Developer Community](https://developer.valvesoftware.com/wiki/Dedicated_Servers_List)