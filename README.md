
# Aula de Versionamento de Código com Git e GitHub

## Objetivos

1. **Entender o que são Git e GitHub.**
2. **Aprender o funcionamento básico do Git.**
3. **Realizar operações essenciais no Git.**
4. **Colaborar de maneira eficiente em um repositório remoto.**

---

## Introdução ao Versionamento de Código

### O que são Git e GitHub?

- **Git**: Um sistema de controle de versão distribuído que registra alterações no código ao longo do tempo.
- **GitHub**: Uma plataforma para hospedar repositórios Git e colaborar em projetos de software.

### Como funciona o Git?

- O código é versionado localmente no computador e, opcionalmente, sincronizado com um repositório remoto.
- Estados principais de arquivos:
  1. **Untracked** (não rastreados).
  2. **Staged** (prontos para commit).
  3. **Committed** (salvos no histórico do repositório).

---

## Configuração Inicial

### Instalação do Git

- Baixe o Git em [git-scm.com](https://git-scm.com).
- Siga as instruções para instalar no seu sistema operacional.

### Configuração Básica

```bash
# Configurando o nome de usuário
git config --global user.name "Seu Nome"

# Configurando o e-mail
git config --global user.email "seuemail@exemplo.com"

# Verificando as configurações
git config --list
```

---

## Primeiros Passos com o Git

### Criando um Repositório Local

```bash
# Inicializando um repositório
git init
```

### Dando o Primeiro Commit

```bash
# Criando um arquivo e adicionando conteúdo
echo "Hello, Git!" > arquivo.txt

# Adicionando ao stage
git add arquivo.txt

# Commitando o arquivo
git commit -m "Primeiro commit"
```

### Verificando o Status do Repositório

```bash
# Mostrando o status atual
git status
```

### Verificando o Histórico de Commits

```bash
# Exibindo o histórico de commits
git log
```

---

## Operações Essenciais no Git

### Revertendo Alterações Fora do Stage

```bash
# Revertendo modificações em arquivos não staged
git checkout -- nome-do-arquivo
```

### Removendo Arquivos do Stage

```bash
# Retirando arquivos do stage
git reset nome-do-arquivo
```

### Voltando para um Commit Anterior

```bash
# Revertendo para um commit anterior
git revert id-do-commit
```

---

## Trabalhando com Branches

### Criando e Alternando Branches

```bash
# Criando uma nova branch
git branch nome-da-branch

# Criando e alternando para a nova branch
git checkout -b nome-da-branch
```

### Deletando e Renomeando Branches

```bash
# Deletando uma branch
git branch -d nome-da-branch

# Renomeando uma branch
git branch -m nome-antigo nome-novo
```

### Juntando Branches

```bash
# Realizando merge
git merge nome-da-branch
```

### Resolvendo Conflitos

- Editar os arquivos manualmente para corrigir os conflitos.
- Após corrigir:

```bash
# Adicionando os arquivos corrigidos
git add nome-do-arquivo

# Finalizando o merge
git commit
```

---

## Trabalhando com Repositórios Remotos

### Criando Conta no GitHub

1. Acesse [github.com](https://github.com) e crie uma conta.
2. Configure um repositório remoto na sua conta.

### Conectando o Git ao GitHub

```bash
# Adicionando um repositório remoto
git remote add origin url-do-repositorio

# Verificando a conexão
git remote -v
```

### Sincronizando com o Repositório Remoto

#### Subindo Alterações Locais

```bash
# Enviando commits para o repositório remoto
git push -u origin main
```

#### Trazendo Alterações do Repositório Remoto

```bash
# Baixando alterações do repositório remoto
git pull
```

#### Clonando um Repositório

```bash
# Clonando um repositório remoto
git clone url-do-repositorio
```

---

## Dicas para Trabalho em Equipe com Git

1. Sempre sincronize seu repositório antes de começar a trabalhar: `git pull`.
2. Faça commits pequenos e frequentes com mensagens claras.
3. Use branches para desenvolver novas funcionalidades.
4. Resolva conflitos rapidamente para evitar atrasos.

---

## Exercícios Práticos

1. Criar um repositório local e realizar um commit inicial.
2. Criar uma nova branch e realizar alterações nela.
3. Fazer merge entre duas branches com resolução de conflitos.
4. Subir alterações para um repositório remoto.
5. Clonar um repositório remoto e verificar o histórico de commits.
