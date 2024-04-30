# Usando o Git
Um guia simples e rápido pra quem está começando.

## Configuração Básica

É muito importante manter a configuração do seu guit atualizada, para isso basta dar uma olhada em:
```bash
git config --global --list
```
para atualizar ou configurar o seu usuário use: 
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.nome@email.com"
```

## Iniciando/Clonando um ropositório

Para iniciar um repositório existem duas maneiras basicamente:

 - Localmente

 ```bash
 # Isso irá iniciar um repositório local a partir da pasta atual
 git init

 # Se precisar vicular ao repositório remoto basta:
 git remote add origin git@github.com:usuario/nome_repo.git

 # puts! meu repo mudou, preciso mudar o remote:
 git remote set-url origin git@github.com:usuario/novo_nome_repo.git

 # para verificar essa configuração é só:

 # linux, se usa windows, decobre aí e faz um PR :-)
 git config --local --list | grep remote 
 ```

 - Remotamente

    Nesse caso, você deve criar o repositório remotamente primeiro, no [github](https://github.com/) por exemplo, então você clona o repositório. nos nossos exemplos usaremos este repositório.

```bash
# este comando irá criar uma pasta com o nome do projeto na sua pasta atual, também irá criar um repositório local vinculado ao github 
git clone https://github.com/jeremyrodrigues/git-usage.git
```
## Trabalhando com git

Carregando mudanças do repositório remoto:
```bash
# atualizar os dados remotos para local
git fetch
# carrear dados do remoto para o local:
git pull
```

Após realizar seu trabalho, haverão mudanças, que precisam ser versionadas e envidas ao remoto.
Para isso fazemos o seguinte:

```bash
# visualizar o status dos arquivos monitorados:
git status
# Indexar (organizar) os arquivos e nudanças que farão parte do commit (unidade báseca de versçao, é de fato uma versão)
git add <nome do arquivo(os)> # aqui aceita coisas como *.py por exemplo
# Realizar o commit
# é recomendável fazer o commit sem o '-m', colocar o título em uma linha, pular uma linha e descrever seu commit, de todo modo:
git commit -m "titulo do seu commit"
# agora enviamos esse commit para o servidor:
git push
```



