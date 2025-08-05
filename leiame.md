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
