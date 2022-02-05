# Configurando um ambiente de desenvolvimento Tray

> ⚠️ Atenção, esse artigo foi feito no dia 21/01/2022. Entretanto, as dependências estão sujeitas a qualquer tipo de mudança.
> 

---

### Instalando o RVM

1. Para prosseguir instale o `software-properties-common`
    
    ```bash
    sudo apt-get install software-properties-common
    ```
    
2. Adicione o repositório e instale o rvm
    
    ```bash
    sudo apt-add-repository -y ppa:rael-gc/rvm
    sudo apt-get update
    sudo apt-get install rvm
    ```
    
3. Adicione o seu usuário ao grupo rvm
    
    ```bash
    sudo usermod -a -G rvm $USER
    ```
    
4. Mude essa configuração no seu terminal
    
    ![preferências/perfil/comando/executar comando como shell padrão](https://github.com/joaby-eficaz/configurando-ambiente-tray/blob/main/Group%206.png)
    
5. Reinicie sua máquina
6. Instale as gems na sua maquina
    
    ```bash
    rvm user gemsets
    ```
    
7. Instale a versão do RVM que deseja (para usar na Tray é recomendado 2.3)
    
    ```bash
    rvm install ruby 2.3
    ```
    

### Instale agora o Opencode

```bash
gem install opencode_theme
```

### Agora é hora de resolver os erros

```bash
#Instalando faraday
gem install faraday -v 1.0.1

#instalando launchy
gem install launchy -v 2.4.3

#instalando o racc
gem install racc -v 1.5.2

#instalando o nokogiri
gem install nokogiri -v 1.10.10
```

### Instalando o gulp

```bash
#instale o nvm
sudo apt install curl 
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash

#instale a última versão lts do node
nvm install --lts

#finalmente instale o gulp
npm i -g gulp-cli

#atualize seu npm
npm i -g npm@8.3.2
```

### Agora é só usar o open_code e ser feliz!

##

### Passo a passo para edição de um tema (que não seja um tema da Eficaz) com opencode

1. abrir o tema em questão na tray

![one.jpg](https://github.com/izalima-eficaz/configurando-ambiente-tray/blob/main/one.jpg)

2. duplicar o tema

![two.jpg](https://github.com/izalima-eficaz/configurando-ambiente-tray/blob/main/two.jpg)

3. se incluir na lista de desenvolvedores do tema (isso irá gerar uma key e um password que serão utilizados no terminal para conseguir acesso ao código fonte do tema)

![three.jpg](https://github.com/izalima-eficaz/configurando-ambiente-tray/blob/main/three.jpg)

![four.jpg](https://github.com/izalima-eficaz/configurando-ambiente-tray/blob/main/four.jpg)

4. criar uma pasta para o tema e abrir o terminal dentro dela

5. abra o terminal e digite:
```bash
    opencode configure {key} {password} {código-do-tema}
```
* a mesma key e password que foi gerada quando você se incluiu na lista de desenvolvedores
* o código do tema pode ser encontrado em "aparência da loja, logo abaixo do nome do tema que você irá editar"
* lembrando: ao digitar no prompt, as instruções devem ser separadas por um espaço
    * segue o exemplo:
    ```bash
        opencode configure dkf38403kds3840nsa 9348jfoewjr329823j4b345 26
    ```

6. digitar no terminal: 
```bash
    opencode download
```
* irá fazer o download do código fonte do tema

7. após isso, basta abrir sua IDE dentro da pasta onde os arquivos foram baixados

8. ao abrir a IDE, abra seu terminal e digite:
```bash
    opencode w
```
* w = watch
* com isso a IDE ficará ouvindo/assistindo suas mudanças no código e atualizando o preview
