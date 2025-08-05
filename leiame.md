# Git 
--- 

## Enviar os commits da sua branch local para o repositório remoto.

O comando:

`git push -u origin main`


faz o seguinte:

1. git push
Envia os commits da sua branch local para o repositório remoto.

2. origin
É o nome padrão do repositório remoto (geralmente o GitHub, GitLab, etc.).

3. main
É o nome da branch que você está enviando. Neste caso, a branch principal.

4. -u ou --set-upstream
Define a branch main local para rastrear a branch main no remoto. Isso significa que, no futuro, você poderá usar comandos mais simples como:


sem precisar especificar o nome do repositório e da branch, porque o Git já sabe para onde enviar ou buscar os dados.

`git push`

`git pull`

Quando você está configurando um novo projeto, 
o comando git push -u origin main é especialmente útil porque:

Publica sua branch principal (main) no repositório remoto (origin).
**Estabelece um vínculo entre a branch local e a remota,** 
facilitando comandos futuros como git pull e git push sem precisar repetir os nomes.
**Dica extra:**
Se você acabou de iniciar o repositório com git init, certifique-se de ter feito pelo menos um commit antes de usar esse comando. 

Exemplo:

`git add .`

`git commit -m "Primeiro commit"`

`git push -u origin main`


--- 

##  1. Criar uma nova branch local a baseada em uma branch remota

`git checkout -b nomebranch origin/nomebranch`


faz duas coisas ao mesmo tempo:

1. Cria uma nova branch local chamada nomebranch
O -b indica que você quer criar uma nova branch local.

2. Baseia essa nova branch local na branch remota origin/nomebranch
Ou seja, você está dizendo:

> "Crie uma branch local chamada nomebranch a partir da branch remota origin/nomebranch."

Quando usar esse comando?

Esse comando é útil quando você quer começar a trabalhar em uma branch que existe no repositório remoto, mas ainda não existe localmente.

Exemplo prático:
Se alguém criou uma branch chamada feature/api no GitHub e você quer começar a trabalhar nela localmente, você pode usar:

`git checkout -b feature/api origin/feature/api`

> Isso evita conflitos e garante que sua branch local esteja sincronizada com a versão remota.

--- 
# desfazer o commit 

Você pode desfazer um commit no Git de diferentes formas, dependendo do que exatamente você quer fazer. Aqui estão os principais cenários:

🔙 1. Desfazer o último commit, mas manter as alterações 
no código (no seu diretório de trabalho):

`git reset --soft HEAD~1`

Isso desfaz o commit, mas mantém os arquivos preparados para o commit (stage).

📝 2. Desfazer o último commit e também remover 
os arquivos do stage (mas manter no diretório):

`git reset --mixed HEAD~1`

Os arquivos continuam no seu diretório, mas não estão mais preparados para commit.

🧹 3. Desfazer o commit e apagar as alterações (cuidado!):

`git reset --hard HEAD~1`

Isso desfaz o commit e apaga as alterações feitas. Use com cautela!

🌐 Se o commit já foi enviado para o remoto (git push)
Você pode desfazer localmente e forçar a atualização no remoto:

`git reset --hard HEAD~1`

`git push origin HEAD --force`

⚠️ Atenção: Isso pode causar problemas para outras pessoas que estão trabalhando na mesma branch. Use com cuidado e preferencialmente em branches pessoais.

Como o commit ainda está só local, você pode desfazê-lo com segurança. Aqui estão duas opções comuns:

✅ 1. Manter as alterações no seu diretório (mais seguro)

`git reset --soft HEAD~1`

Desfaz o commit. Mantém os arquivos no stage, prontos para um novo commit.


✅ 2. Remover do stage, mas manter os arquivos modificados:

`git reset --mixed HEAD~1`

Desfaz o commit. Os arquivos voltam para o diretório, 
mas não estão mais preparados para commit.

> Se você quiser ver o histórico antes de desfazer, pode usar:
>  Isso mostra os commits recentes com seus IDs curtos.
> git log --oneline

---

--- 

# 2. configurar o rastreamento da branch local c/ a remoto 

`git branch -u origin/novobranch novobranch`

tem a função de configurar o rastreamento remoto da branch local novobranch
 para a branch remota origin/novobranch.

Explicando cada parte:

git branch: comando para gerenciar branches.

-u ou --set-upstream-to: define qual branch remota a branch local deve rastrear.

origin/novobranch: é a branch remota no repositório chamado origin.

novobranch: é a branch local que você quer configurar.

O que isso faz?
Depois de executar esse comando:
A branch local novobranch passa a rastrear a branch remota origin/novobranch.
Você poderá usar comandos como git pull e git push sem precisar especificar
 o nome da branch remota.

Exemplo prático:
Se você criou uma branch local chamada novobranch e ela já existe no remoto, 
mas ainda não está rastreando, esse comando conecta as duas.

###  como verificar se a branch está rastreando corretamente com:

` git status`  ou   `git branch -vv`


--- 

## Renomear uma Branch

Para renomear uma branch no Git, você pode fazer isso localmente com o seguinte comando:

`git branch -m nome-antigo nome-novo`


--- 

## Para excluir uma branch no Git, você pode seguir os passos abaixo:

**Introdução** Primeiro, é importante entender que existem dois tipos de branches que você pode querer excluir: locais e remotas. A exclusão de uma branch local remove-a do seu repositório local, enquanto a exclusão de uma branch remota remove-a do repositório remoto.

Comandos Git
### 1. Excluir uma branch local:
`git branch -d nome-da-branch`
Use o comando acima para excluir uma branch local. 
Se a branch ainda não foi mesclada, você pode usar a opção -D (maiúscula)
 para forçar a exclusão:  `git branch -D nome-da-branch`

### 2. Excluir uma branch remota:

`git push origin --delete nome-da-branch`
Este comando remove a branch do repositório remoto.


--- 
## merge 

1. Verifique se está no branch main:
`git checkout main`
2. Atualize o branch main:
`git pull origin main`
3. Faça o merge do branch desejado no main:
`git merge nome-do-branch`
4. Resolva conflitos, se houver: Se houver conflitos, o Git indicará os arquivos que precisam ser resolvidos. Edite esses arquivos para resolver os conflitos e depois adicione as mudanças:
`git add nome-do-arquivo`
5. Finalize o merge 
`git commit`
6. Envie as mudanças para o repositório remoto:
`git push origin main`

