# Palindrome Checker JS

Uma aplicação web simples para verificar se uma palavra ou frase é um palíndromo.

O projeto foi desenvolvido com **HTML**, **CSS** e **JavaScript puro**, sem frameworks e sem dependências externas.

## Sobre o projeto

O **Palindrome Checker JS** recebe um texto digitado pelo usuário, trata esse texto e verifica se ele continua igual quando lido de trás para frente.

Além de dizer se o texto é ou não um palíndromo, a aplicação também exibe a versão invertida da entrada.

## O que é um palíndromo?

Um palíndromo é uma palavra, frase ou sequência que pode ser lida da mesma forma da esquerda para a direita e da direita para a esquerda.

Exemplos:

```txt
ana
arara
ovo
A mãe te ama
```

## Funcionalidades

- Verifica se uma palavra ou frase é um palíndromo
- Exibe o texto original digitado
- Exibe o texto invertido
- Ignora letras maiúsculas e minúsculas
- Remove acentos
- Ignora espaços, pontuação e caracteres especiais
- Possui interface simples para entrada e saída de dados
- Funciona direto no navegador

## Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript

## Como executar o projeto

Clone o repositório:

```bash
git clone https://github.com/SEU-USUARIO/palindrome-checker-js.git
```

Acesse a pasta do projeto:

```bash
cd palindrome-checker-js
```

Abra o arquivo `index.html` no navegador.

Você também pode usar uma extensão como **Live Server** no VS Code, mas não é obrigatório.

## Exemplo de uso

Entrada:

```txt
A mãe te ama
```

Texto tratado internamente:

```txt
amaeteama
```

Texto invertido:

```txt
amaeteama
```

Resultado:

```txt
É um palíndromo!
```

## Estrutura do projeto

```txt
palindrome-checker-js/
├── index.html
└── README.md
```

## Como funciona a lógica

O algoritmo segue estes passos:

1. Recebe o texto digitado pelo usuário.
2. Converte tudo para letras minúsculas.
3. Remove acentos.
4. Remove espaços, pontuação e caracteres especiais.
5. Inverte o texto tratado.
6. Compara o texto tratado com o texto invertido.
7. Exibe o resultado na tela.

## Trecho principal do algoritmo

```js
const textoTratado = textoOriginal
  .toLowerCase()
  .normalize("NFD")
  .replace(/[\u0300-\u036f]/g, "")
  .replace(/[^a-z0-9]/g, "");

const textoInvertido = textoTratado
  .split("")
  .reverse()
  .join("");

const ehPalindromo = textoTratado === textoInvertido;
```

## Possíveis melhorias futuras

- Adicionar botão para limpar o campo
- Verificar automaticamente enquanto o usuário digita
- Adicionar modo claro e modo escuro
- Melhorar a responsividade para dispositivos móveis
- Publicar o projeto com GitHub Pages

## Autor

Feito por **Kelvin Araújo**.