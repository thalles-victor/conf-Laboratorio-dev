# Este documento mostra como configurar o ambiente de desenvolvimento no Linux no meu caso [Ubuntu](https://ubuntu.com/).
### Mudanças podem ocorrer como por exemplo autualizações das ferramentas, por isso deixei os comandos de intalação na versão lts, mesmo assim recomendo ver a documentação oficial ou sugerir um  pull request. E a medida do tempo colocarei mais coisas.

# Instalação do curl para fazer requisição http
```console
    sudo apt-get install curl
```

# NodeJS
![alt node](./assets/node.png)

### Adicionando o repositório lts do node

```console
    curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
```
### atualizando o apt
```console
    sudo apt update
```

### instalando Nodejs

```console
    sudo apt install -y nodejs
```

### verificando se ele foi instalado com sucesso

```console
    node --version
```
## Caso queira a referência está em Node [Source Install in Ubuntu](https://github.com/nodesource/distributions/blob/master/README.md#debinstall)

# Yarn

![alt yarn](./assets/yarn.png)


### Adicionando a chave do yarn
```console
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
```
### Adicionando o yarn no pacote

```console
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
```
### atualizando o apt
```console
    sudo apt update
```

### E finalmente instalando o yarn
```console
    sudo apt install yarn
```
### Por último, para verificar se ele foi instalado corretamente.

```console
    yarn --version
```

# VSCode
![alt vscode](./assets/vscode.webp)

### Instalando a versão classica

```console
    sudo snap install code --classic
```

# Git
![atl git](./assets/git.png)
### A instalação do git é bem fácil, mas caso queira consultar a doc. [documentação](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

### atualizando o apt
```console
    sudo apt update
```
### Instalando o git
```console
    sudo apt install git-all
```

### configurando o usuário global obs. use aspas por volta do seu nome
```console
    git config --global user.name "seu-nome-do-git-hub"
```

### configurando o email global obs. não use aspas
```console
    git config --global user.email seu-email
```
### Quando você for fazer um commit para o github, ele vai pedir o nome do usuário, basta você colocar o user.name ou user.email dessa forma.

```console
    Username for 'https://github.com': user.name
```

### Agora para o token (senha entre aspas) você tem que colar o que foi gerado na sua conta 
### podendo acessar com [Persolnal access tokens](https://github.com/settings/tokens)

# Emote
![alt emote](./assets/emote.webp)
### essa ferramenta permite adicionar emotes nos campos de texo e é muito últil no desenvolvimento principalmente no mobile.

```console
    sudo snap install emote
```


# Expo
![atl expo](./assets/expo.png)
### Instalação do expo esta bem detalhada na documentação, mas decidi colocar mesmo assim para servir de roteiro

```console
    sudo npm install --global expo-cli
```

# Docker Engine
![alt docker](./assets/docker.png)
### O docker também tem uma [documentação](https://docs.docker.com/engine/install/ubuntu/) bem detalhada de como installar, porém vou resumi-la.

### Atualizando o apt
```console
    sudo apt update
```

```console
    sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```

```console
 sudo mkdir -p /etc/apt/keyrings
```
```console
 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

```console
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```console
    sudo apt update
```
```console
  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

### Para testar se foi instalado com sucesso rode esse comando

```console
    sudo docker run hello-world
```
# 
## tem que aparecer uma mensagem como essa:

###    Hello from Docker!
###  This message shows that your installation appears to be working correctly.

### Para dar permição ao comando docker, execute o comando abaixo. Dessa forma não vai prcisar do sudo na frente do comando docker.

```console
    sudo usermod -aG docker $USER
```

# Docker Compose
## O Docker compose é usado para subir container de forma muito simplificada, usando arquivos yml (ou yaml). O pre requisito para instalar é o próprio docker que mostramos anteriormente.

### Bora mais uma vez atualizar esse apt
```console
  sudo apt-get update
```

### Agora é só instalar o docker compose

```console
  sudo apt-get install docker-compose-plugin
```
### E para testar se foi instalado corretamente, rode um

```console
  docker compose version
```

## Como disse antes você também pode saber mais sobre o docker compose no artigo que recomendei anteriormente

## Se você quer começar a usar o docker com postgres eu recomendo muito o [post](https://baraus.dev/articles/postgresql-+-docker/) do Bruno de Araujo. Estou compartilhando porque ele me ajudou dms com uma doc bem detalhada e fácil de entender.

# Pip3
![alt pip](./assets/pip3.png)
### As vezes eu gosto de brincar com python, no linux, a terceira versão já vem instalado porém seu gerenciador de pacote não.

### Atualizando o apt
```console
    sudo apt update
```

### Instalando o pip3
```console
    sudo apt install python3-pip
```


