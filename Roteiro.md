
# v1
- criar a pasta do arquivo
- crir uma página simples de html
~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loja</title>
</head>
<body>
    <h1>Loja Água 🇯🇲 </h1>
</body>
</html>
~~~

- Criar o arquivo `main.go`;

- Criar uma pasta `templates` - nessa pasta  adicionar o(s) arquivo(s) html do projeto;

- Criar uma `var temp` para que todos os  templates sejam armazenados dentro dessa variável.

    - `var temp = template.Must(template.ParseGlob("templates/*.html"))`

    - `must` encapsula todos os templates e devolve dois retornos

    - vai devolver o template e uma mensagem de erro,

    -  para saber onde os templates estão, utilizamos mais uma função chamada _template Parse Glob_ 

- Na função main adicionamos a chamda da função `HandleFunc`
    - `http.HandleFunc("/", index)`
    - o primeiro parâmetro que ela espera é “qual é o caminho que você quer atender?
    - o segundo parametro é a funnção que irá tratar essa chamada, no nosso caso index

- Criar a função index - para exibir o conteúdo da página html
    - essa função precisa de dois parâmetros
    - `w http.RespondeWtriter` - 
    - `r *http.Request`

- Executar o código - nada é exibido na tela

- Para conseguir executar esse index precisa embedar um código HTML

    - Nosso ódigo HTL deve estar dentro de 
    ~~~htlm
    {{define “Index”}}
    ...
    {{end}}
    ~~~

    Para que o código seja executado




- 