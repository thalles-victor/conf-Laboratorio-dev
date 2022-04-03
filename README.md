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
    sudo apt-get install -y nodejs
```

### verifiando se ele foi instalado com sucesso

```console
    node --version
```


# Yarn

### Adicionando o a chave do yarn
![alt yarn](./assets/yarn.png)
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

### instalando o yarn
```console
    sudo apt install yarn
```
### verificando se ele foi instalado com sucesso

```console
    yarn --version
```

# VSCode
![alt vscode](./assets/vscode.webp)

### instalando a versão classica

```console
    sudo snap install code --classic
```

# Emote
![alt emote](./assets/emote.webp)
### essa ferramenta permite adicionar emotes nos campos de texo e é muito últil no desenvolvimento mobile.

```console
    sudo snap install emote
```

# Pip3
![alt pip](./assets/pip3.png)
### As vezes eu gosto de brincar com python, no linux, a terceira versão já vem instalado porém seu gerenciador de pacote não.

### Atualizando o apt
```console
    sudo apt-get update
```

### Instalando o pip3
```console
    sudo apt install python3-pip
```

# Expo
![atl expo](./assets/expo.png)
### Instalação do expo esta bem detalhada na documentação, mas decidi colocar mesmo assim para servir de roteiro

```console
    sudo npm install --global expo-cli
```

# Docker
![alt docker](./assets/docker.png)
### O docker também tem uma [documentação](https://docs.docker.com/engine/install/ubuntu/) bem detalhada de como installar, porém vou resumila.

### Atualizando o apt
```console
    sudo apt-get update
```

```console
    sudo apt-get install ca-certificates curl gnupg lsb-release
```

```console
    -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

```console
    echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```console
    sudo apt-get update
```
```console
    sudo apt-get install docker-ce docker-ce-cli containerd.io
```

### Para testar se foi instalado com sucesso reode esse comando

```console
    sudo docker run hello-world
```
# 
## tem que aparecer uma mensagem como essa:

###    Hello from Docker!
###  This message shows that your installation appears to be working correctly.


