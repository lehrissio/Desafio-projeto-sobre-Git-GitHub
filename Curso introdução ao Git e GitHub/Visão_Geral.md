# Introdu��o ao Git e GitHub

### Entendendo como o Git Funciona por baixo dos panos:
**Sha1 (Secure Hash Algorithm)**
* � uma forma curta de representar um arquivo
*  Consiste em um conjunto de Fun��es Hash criptograficas projetadas pela Ag�ncia Nacional dos EUA
* A encripta��o gera um conjunto de caracteres de 40 digitos


### Objetos internos do Git:
```mermaid
graph LR
A(tree) --> B(tree)
B --> C((blob))
A --> D((blob))
A --> E((blob))
```

### Objetos internos do git
* **Blobs:**
Local onde � guardado o SHA e metadados (tamanho do arquivo, tipo do arquivo etc)
* **Tree:**
Armazena blobs e aponta para o diret�rio, al�m de possuir um SHA pr�prio
* **Commit:**
Aponta para a tree, �lyimo commit realizado, autor, mensagem e timestamp. Possui SHA pr�prio

###  Principais comandos com Git:
* **Iniciar git:** git init
* **Mover arquivos:** git add .
* **Add commit:** git commit -m "nome do commit"
* **Reposit�rio GitHub:** git romote add origin **link SSH/https**
* **Add no reposit�rio:** git push origin main

###  Ciclo de vida dos arquivos Git:
```mermaid
graph LR
A(Working area) --> B(Staging area)
B --> C(Local repository)
C --> D(Remote repository)
```

###  Outros comandos com Git:
* **como est� o reposit�rio:** git status
* **clonar um reposit�rio remoto:** git clone ~~link~~
* **verificar nome e email cadastrado:** git config --list