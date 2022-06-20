# Git e GitHub

### Git

- Utilizado para controle de versionamento de arquivos.
- Faz o versionamento dos arquivos no repositório local e pode fazer a integração com o repositório Remoto (GitHub).

#### Comandos Git

- **cd** - direciona o local para criação do GIT (inicia o nome da pasta + tab completa o nome)
- **cd ..** - volta uma pasta
- **clear** - limpa o terminal
- **openssl sha1 (arquivo)** - Mostra os 40 caracteres de  encriptação do arquivo.
- **mkdir** - nome da pasta (cria pasta no local definido no cd)
- **rmdir** - deleta a pasta selecionada
- **ls** (mostra os arquivos no local)
- **echo > arquivo.txt** (cria arquivo na pasta)

#### Iniciar Repositório local

- **git init** - iniciar o repositório local
- **git status** - verifica o status dos arquivos
- **git add** - adiciona arquivo ao commit/branch)  *atalho . ou *(coloca todos os arquivos)*
- **git commit -m "descreve a alteração feita no arquivo"** - Descrever bem a alteração feita no commit.

#### GitHub (Colocar o projeto no repositório remoto)

- criar um novo repositório no GitHub e copiar o link do repositório (URL). 
- **git remote add origin (Link do repositório)** - Aponta o diretório remoto e o vincula ao origin
- **git remote -v** - verifica o link do origin
- **git push origin master** - Faz a transferência dos arquivos para o repositório remoto.
