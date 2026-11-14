<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=230&section=header&text=Folhas%20de%20Consulta&fontSize=52&fontColor=ffffff&fontAlignY=40&desc=colinhas%20de%20c%C3%B3digos%20e%20atalhos&descAlignY=60&descSize=20&color=0:8DA2F0,100:B794F0" alt="Folhas de Consulta" />

<i>"A lógica levará você de A a B. A imaginação levará você a qualquer lugar"</i>

<br><br>

<img src="https://img.shields.io/badge/Defesa_Cibern%C3%A9tica-8DA2F0?style=for-the-badge&logo=linux&logoColor=white" alt="Defesa Cibernética" />
<img src="https://img.shields.io/badge/Foco-Python-B794F0?style=for-the-badge&logo=python&logoColor=white" alt="Foco: Python" />
<img src="https://img.shields.io/badge/Aprendendo-TypeScript_%7C_Docker_%7C_Backend-8DA2F0?style=for-the-badge&logo=typescript&logoColor=white" alt="Aprendendo" />

<br><br>

<img src="https://skillicons.dev/icons?i=python,c,r,java,js,ts,html,css,react,nodejs,postgres,sqlite,docker,bash,linux,kali,git,github,vscode,figma,postman&perline=7" alt="Tech Arsenal" />

<br>

🟦🟦🟪🟪🟦🟦🟪🟪🟦🟦🟪🟪🟦🟦🟪🟪

</div>

## 👾 O que é isso?

São simplesmente **colinhas** de códigos e atalhos das tecnologias do meu Tech Arsenal: aquele material de consulta rápida para quando a memória falha (e ela falha, principalmente antes do café ☕).

> 💡 **Como usar:** clique na seta ▶️ de cada tecnologia para abrir a colinha.
>
> 💪 = já domino mais &nbsp;|&nbsp; 🌱 = ainda aprendendo &nbsp;|&nbsp; 😨 = socorro, tenho medo!

<br>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="22" height="22" alt="Python" />&nbsp; <b>Python</b> 💪</summary>

<br>

> Minha base para defesa cibernética e análise de vulnerabilidades 🛡️

### Básico

```python
nome = "Fran"
idade = 20
print(f"Olá, {nome}! Você tem {idade} anos.")

entrada = input("Digite algo: ")
type(idade)         # <class 'int'>
int("42")           # 42
```

### Estruturas de controle

```python
if idade >= 18:
    print("maior")
elif idade > 12:
    print("adolescente")
else:
    print("criança")

for i in range(5):        # 0 a 4
    print(i)

while condicao:
    ...
```

### Listas, dicionários, sets e tuplas

```python
lista = [1, 2, 3]
lista.append(4)
lista[0]; lista[-1]; lista[1:3]

dic = {"nome": "Fran", "area": "ciber"}
dic["nome"]
dic.get("idade", 0)
for chave, valor in dic.items():
    print(chave, valor)

conjunto = {1, 2, 3}       # sem repetidos
tupla = (1, 2, 3)          # imutável

quadrados = [n**2 for n in range(10)]            # list comprehension
pares = [n for n in range(10) if n % 2 == 0]
```

### Funções e classes

```python
def somar(a, b=0):
    return a + b

class Pessoa:
    def __init__(self, nome):
        self.nome = nome

    def falar(self):
        print(f"Oi, eu sou {self.nome}")
```

### Arquivos e erros

```python
with open("arquivo.txt", "r", encoding="utf-8") as f:
    conteudo = f.read()

try:
    resultado = 10 / 0
except ZeroDivisionError as e:
    print(f"Erro: {e}")
finally:
    print("fim")
```

### Ambiente virtual e pacotes

```bash
python -m venv venv
venv\Scripts\activate         # Windows
source venv/bin/activate      # Linux/Mac
pip install requests
pip freeze > requirements.txt
pip install -r requirements.txt
```

### Bibliotecas úteis para defesa cibernética

```python
import socket       # conexões de rede
import hashlib      # hashes
import re           # expressões regulares
import subprocess   # rodar comandos
import requests     # requisições HTTP (pip install requests)

hashlib.sha256(b"texto").hexdigest()
```

> ⚠️ Use ferramentas de análise de vulnerabilidades apenas em sistemas seus ou com autorização expressa.

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" width="22" height="22" alt="C" />&nbsp; <b>C</b> 😨</summary>

<br>

> Perto do metal: ponteiros, memória e muito cuidado com buffer overflow

### Estrutura básica

```c
#include <stdio.h>

int main(void) {
    printf("Olá, mundo!\n");
    return 0;
}
```

```bash
gcc main.c -o programa                    # compila
gcc -Wall -Wextra -g main.c -o programa   # com avisos e símbolos de debug
./programa                                # executa
```

### Tipos e entrada/saída

```c
int idade = 20;
float peso = 55.5f;
double altura = 1.65;
char letra = 'A';
char nome[50] = "Fran";

printf("Idade: %d\n", idade);
scanf("%d", &idade);
fgets(nome, sizeof(nome), stdin);   // lê texto com segurança
```

| Formato | Tipo |
| --- | --- |
| `%d` | int |
| `%f` | float / double |
| `%c` | char |
| `%s` | string |
| `%p` | ponteiro |
| `%x` | hexadecimal |

### Controle de fluxo

```c
if (idade >= 18) { } else if (idade > 12) { } else { }

for (int i = 0; i < 5; i++) { }
while (condicao) { }
do { } while (condicao);

switch (opcao) {
    case 1: break;
    default: break;
}
```

### Arrays e strings

```c
#include <string.h>

int nums[5] = {1, 2, 3, 4, 5};

strlen(texto);             // tamanho
strcmp(a, b);              // 0 se iguais
strncpy(destino, origem, sizeof(destino) - 1);
strncat(destino, origem, sizeof(destino) - strlen(destino) - 1);
```

### Ponteiros

```c
int x = 10;
int *p = &x;    // p guarda o endereço de x
*p = 20;        // altera x pelo ponteiro
```

### Memória dinâmica

```c
#include <stdlib.h>

int *v = malloc(10 * sizeof(int));
if (v == NULL) {
    return 1;       // sempre confira se alocou
}
v[0] = 5;
free(v);            // libera a memória
v = NULL;
```

### Struct e funções

```c
typedef struct {
    char nome[50];
    int idade;
} Pessoa;

int somar(int a, int b) {
    return a + b;
}

Pessoa p = {"Fran", 20};
printf("%s\n", p.nome);
```

> 🔒 **Segurança:** estouro de buffer é uma das falhas mais clássicas em C. Evite `gets()`, `strcpy()` e `sprintf()` sem limite. Prefira `fgets()`, `strncpy()` e `snprintf()`, e sempre confira os tamanhos.


<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/r/r-original.svg" width="22" height="22" alt="R" />&nbsp; <b>R</b> 😨</summary>

<br>

> Estatística e análise de dados com gráficos bonitos 📊

### Básico

```r
x <- 10                    # atribuição
nome <- "Fran"
print(paste("Olá,", nome))

class(x)                   # tipo do objeto
is.numeric(x)
```

### Vetores

```r
v <- c(1, 2, 3, 4, 5)

v[2]            # segundo elemento
v[2:4]          # fatia
v[v > 2]        # filtro
length(v)
sum(v); mean(v); median(v); sd(v)
seq(1, 10, by = 2)
rep("a", 3)
```

### Data frames

```r
df <- data.frame(
  nome  = c("Ana", "Bia", "Cris"),
  idade = c(20, 22, 19)
)

df$nome                # coluna
df[1, ]                # linha 1
df[df$idade > 19, ]    # filtro
nrow(df); ncol(df)
head(df); str(df); summary(df)
```

### Ler e salvar arquivos

```r
dados <- read.csv("dados.csv", stringsAsFactors = FALSE)
write.csv(dados, "saida.csv", row.names = FALSE)
```

### Controle de fluxo e funções

```r
if (x > 5) {
  print("maior")
} else {
  print("menor")
}

for (i in 1:5) print(i)

dobro <- function(n) {
  return(n * 2)
}

sapply(v, dobro)       # aplica em cada elemento
```

### Pacotes

```r
install.packages("dplyr")
library(dplyr)

dados %>%
  filter(idade > 18) %>%
  select(nome, idade) %>%
  arrange(desc(idade))
```

### Gráficos

```r
plot(v)                        # base R
hist(dados$idade)
boxplot(dados$idade)

library(ggplot2)
ggplot(dados, aes(x = nome, y = idade)) +
  geom_col(fill = "#8DA2F0") +
  theme_minimal()
```


<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" width="22" height="22" alt="Java" />&nbsp; <b>Java</b></summary>

<br>

> Orientação a objetos e muita xícara de café ☕

### Estrutura básica

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Olá, mundo!");
    }
}
```

```bash
javac Main.java    # compila
java Main          # executa
```

### Variáveis e tipos

```java
int idade = 20;
double altura = 1.65;
boolean ativo = true;
char letra = 'A';
String nome = "Fran";
final int CONSTANTE = 10;   // não pode mudar

var texto = "inferência de tipo";  // Java 10+
```

### Controle de fluxo

```java
if (idade >= 18) {
    System.out.println("maior");
} else {
    System.out.println("menor");
}

for (int i = 0; i < 5; i++) { }
for (String item : lista) { }
while (condicao) { }

switch (dia) {
    case 1 -> System.out.println("Domingo");
    case 2 -> System.out.println("Segunda");
    default -> System.out.println("Outro");
}
```

### Arrays e coleções

```java
int[] nums = {1, 2, 3};
nums.length;

import java.util.*;

List<String> lista = new ArrayList<>();
lista.add("a");
lista.get(0);
lista.size();

Map<String, Integer> mapa = new HashMap<>();
mapa.put("idade", 20);
mapa.get("idade");

Set<Integer> conjunto = new HashSet<>();
```

### Classes e objetos

```java
public class Pessoa {
    private String nome;

    public Pessoa(String nome) {
        this.nome = nome;
    }

    public String getNome() {
        return nome;
    }

    public void falar() {
        System.out.println("Oi, eu sou " + nome);
    }
}

Pessoa p = new Pessoa("Fran");
p.falar();
```

### Herança e interface

```java
public class Aluno extends Pessoa { }

public interface Autenticavel {
    boolean autenticar(String senha);
}

public class Usuario implements Autenticavel { }
```

### Exceções

```java
try {
    int r = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Erro: " + e.getMessage());
} finally {
    System.out.println("fim");
}
```

### Streams (Java 8+)

```java
lista.stream()
     .filter(n -> n > 2)
     .map(n -> n * 2)
     .toList();
```

### Entrada do usuário

```java
import java.util.Scanner;

Scanner sc = new Scanner(System.in);
String entrada = sc.nextLine();
int numero = sc.nextInt();
```

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" width="22" height="22" alt="JavaScript" />&nbsp; <b>JavaScript</b> 💪</summary>

<br>

> Dando vida e lógica às páginas

### Variáveis e tipos

```js
const nome = "Francyellen";   // não pode ser reatribuída
let idade = 20;               // pode ser reatribuída

typeof nome;   // "string"
Number("42");  // 42
String(42);    // "42"
```

### Funções

```js
function somar(a, b) {
  return a + b;
}

const subtrair = (a, b) => a - b;
const dobro = (n) => n * 2;
```

### Arrays

```js
const nums = [1, 2, 3, 4];

nums.push(5);                      // adiciona no fim
nums.pop();                        // remove do fim
nums.map((n) => n * 2);            // [2, 4, 6, 8]
nums.filter((n) => n % 2 === 0);   // [2, 4]
nums.reduce((acc, n) => acc + n, 0); // soma
nums.find((n) => n > 2);           // 3
nums.includes(3);                  // true
[...nums, 10];                     // spread
```

### Objetos e desestruturação

```js
const pessoa = { nome: "Fran", area: "Ciber" };

const { nome, area } = pessoa;
const copia = { ...pessoa, idade: 20 };

Object.keys(pessoa);
Object.values(pessoa);
Object.entries(pessoa);
```

### DOM

```js
const el = document.querySelector(".classe");
const todos = document.querySelectorAll("li");

el.textContent = "Olá!";
el.classList.add("ativo");
el.classList.toggle("oculto");
el.addEventListener("click", () => console.log("clicou"));

const novo = document.createElement("p");
document.body.appendChild(novo);
```

### Async / Fetch

```js
async function buscarDados() {
  try {
    const resposta = await fetch("https://api.exemplo.com/dados");
    const dados = await resposta.json();
    console.log(dados);
  } catch (erro) {
    console.error(erro);
  }
}
```

### Úteis

```js
`Olá, ${nome}!`;          // template string
valor ?? "padrão";        // nullish coalescing
objeto?.propriedade;      // optional chaining
JSON.stringify(obj);
JSON.parse(texto);
```

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" width="22" height="22" alt="TypeScript" />&nbsp; <b>TypeScript</b> 🌱</summary>

<br>

> JavaScript com superpoderes de tipagem

### Tipos básicos

```ts
let nome: string = "Fran";
let idade: number = 20;
let ativo: boolean = true;
let lista: number[] = [1, 2, 3];
let tupla: [string, number] = ["a", 1];
let qualquer: unknown;           // prefira unknown a any
```

### Interface e type

```ts
interface Usuario {
  id: number;
  nome: string;
  email?: string;          // opcional
  readonly criadoEm: Date; // somente leitura
}

type Status = "ativo" | "inativo" | "pendente"; // union
type ID = string | number;
```

### Funções tipadas

```ts
function somar(a: number, b: number): number {
  return a + b;
}

const saudacao = (nome: string): void => {
  console.log(`Olá, ${nome}`);
};
```

### Generics

```ts
function primeiro<T>(lista: T[]): T {
  return lista[0];
}

primeiro<number>([1, 2, 3]);
```

### Utilitários

```ts
Partial<Usuario>;            // todos opcionais
Required<Usuario>;           // todos obrigatórios
Pick<Usuario, "id" | "nome">;
Omit<Usuario, "email">;
Record<string, number>;
```

### Comandos

```bash
npm install -D typescript
npx tsc --init     # cria o tsconfig.json
npx tsc            # compila
npx tsc --watch    # compila ao salvar
```

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" width="22" height="22" alt="HTML5" />&nbsp; <b>HTML5</b> 💪</summary>

<br>

> O esqueleto de toda página web

### Estrutura básica

```html
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Título da página</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <script src="script.js"></script>
  </body>
</html>
```

### Tags mais usadas

| Tag | Uso |
| --- | --- |
| `<h1>` a `<h6>` | Títulos |
| `<p>` | Parágrafo |
| `<a href="">` | Link |
| `<img src="" alt="">` | Imagem |
| `<ul>` / `<ol>` / `<li>` | Listas |
| `<div>` / `<span>` | Contêineres (bloco / em linha) |
| `<button>` | Botão |
| `<table>`, `<tr>`, `<td>`, `<th>` | Tabelas |

### Tags semânticas

```html
<header></header>
<nav></nav>
<main>
  <section></section>
  <article></article>
  <aside></aside>
</main>
<footer></footer>
```

### Formulário

```html
<form action="/enviar" method="post">
  <label for="nome">Nome</label>
  <input type="text" id="nome" name="nome" required />

  <input type="email" name="email" placeholder="seu@email.com" />
  <input type="password" name="senha" />
  <input type="checkbox" name="aceito" />
  <input type="radio" name="opcao" value="a" />

  <select name="curso">
    <option value="ciber">Cibersegurança</option>
  </select>

  <textarea name="msg" rows="4"></textarea>
  <button type="submit">Enviar</button>
</form>
```

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="22" height="22" alt="CSS3" />&nbsp; <b>CSS3</b> 💪</summary>

<br>

> Onde a mágica (e o gradiente) acontece 🎨

### Seletores

```css
p { }              /* tag */
.classe { }        /* classe */
#id { }            /* id */
a:hover { }        /* pseudo-classe */
p::first-line { }  /* pseudo-elemento */
div > p { }        /* filho direto */
div p { }          /* descendente */
h1, h2 { }         /* agrupamento */
input[type="text"] { }  /* atributo */
```

### Box model

```css
* {
  box-sizing: border-box;
}

.caixa {
  width: 300px;
  padding: 16px;
  border: 1px solid #ccc;
  margin: 0 auto;
}
```

### Flexbox

```css
.container {
  display: flex;
  flex-direction: row;          /* row | column */
  justify-content: center;      /* eixo principal */
  align-items: center;          /* eixo transversal */
  flex-wrap: wrap;
  gap: 16px;
}

.item {
  flex: 1;
}
```

### Grid

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.grid-auto {
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}
```

### Variáveis, media query e animação

```css
:root {
  --cor-principal: #8b9ff0;
}

.botao {
  background: var(--cor-principal);
  transition: transform 0.2s;
}
.botao:hover {
  transform: scale(1.05);
}

@media (max-width: 768px) {
  .grid { grid-template-columns: 1fr; }
}

@keyframes pulsar {
  from { opacity: 1; }
  to   { opacity: 0.4; }
}
.pulsando {
  animation: pulsar 1s infinite alternate;
}
```

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" width="22" height="22" alt="React" />&nbsp; <b>React</b></summary>

<br>

> Interfaces feitas de componentes

### Componente

```jsx
function Cartao({ titulo, children }) {
  return (
    <div className="cartao">
      <h2>{titulo}</h2>
      {children}
    </div>
  );
}

export default Cartao;
```

### Hooks principais

```jsx
import { useState, useEffect, useRef, useMemo } from "react";

function Contador() {
  const [count, setCount] = useState(0);
  const inputRef = useRef(null);

  useEffect(() => {
    document.title = `Cliques: ${count}`;
    return () => {};      // limpeza (opcional)
  }, [count]);            // roda quando count muda

  const dobro = useMemo(() => count * 2, [count]);

  return (
    <button onClick={() => setCount(count + 1)}>
      {count} (dobro: {dobro})
    </button>
  );
}
```

### Renderização condicional e listas

```jsx
{logado ? <Painel /> : <Login />}
{erro && <p>{erro}</p>}

<ul>
  {itens.map((item) => (
    <li key={item.id}>{item.nome}</li>
  ))}
</ul>
```

### Eventos e formulários

```jsx
const [texto, setTexto] = useState("");

<input value={texto} onChange={(e) => setTexto(e.target.value)} />

<form onSubmit={(e) => { e.preventDefault(); /* ... */ }}>
```

### Criar projeto

```bash
npm create vite@latest meu-app -- --template react
cd meu-app
npm install
npm run dev
```

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" width="22" height="22" alt="Node.js" />&nbsp; <b>Node.js</b></summary>

<br>

> JavaScript no servidor: o caminho para o backend

### Comandos

```bash
node -v                  # versão
node arquivo.js          # executar
npm init -y              # criar package.json
npm install pacote       # instalar
npm install -D pacote    # dependência de dev
npm uninstall pacote
npm run script
npx pacote               # executar sem instalar
```

### Módulos

```js
// CommonJS
const fs = require("fs");
module.exports = { funcao };

// ES Modules (package.json: "type": "module")
import fs from "fs";
export const funcao = () => {};
```

### Arquivos (fs)

```js
import { readFile, writeFile } from "fs/promises";

const texto = await readFile("arquivo.txt", "utf-8");
await writeFile("saida.txt", "conteúdo");
```

### Servidor com Express

```bash
npm install express
```

```js
import express from "express";

const app = express();
app.use(express.json());

app.get("/", (req, res) => {
  res.send("Olá, mundo!");
});

app.post("/usuarios", (req, res) => {
  const { nome } = req.body;
  res.status(201).json({ nome });
});

app.listen(3000, () => console.log("Rodando na porta 3000"));
```

### Variáveis de ambiente

```js
const porta = process.env.PORT || 3000;
```

> 🔒 Nunca suba o arquivo `.env` para o GitHub. Adicione-o ao `.gitignore`.

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="22" height="22" alt="PostgreSQL" />&nbsp; <b>PostgreSQL</b> 😨</summary>

<br>

> Banco de dados relacional parrudo 🐘

### Conectar (psql)

```bash
psql -U usuario -d banco -h localhost -p 5432
```

| Comando | Ação |
| --- | --- |
| `\l` | Lista os bancos |
| `\c banco` | Conecta a um banco |
| `\dt` | Lista as tabelas |
| `\d tabela` | Descreve a tabela |
| `\du` | Lista os usuários |
| `\i arquivo.sql` | Executa um arquivo SQL |
| `\q` | Sai |

### Criar banco e tabela

```sql
CREATE DATABASE meu_banco;

CREATE TABLE usuarios (
    id         SERIAL PRIMARY KEY,
    nome       VARCHAR(100) NOT NULL,
    email      VARCHAR(150) UNIQUE NOT NULL,
    criado_em  TIMESTAMP DEFAULT NOW()
);
```

### CRUD

```sql
INSERT INTO usuarios (nome, email) VALUES ('Fran', 'fran@email.com');

SELECT * FROM usuarios;
SELECT nome FROM usuarios WHERE id = 1 ORDER BY nome LIMIT 10;

UPDATE usuarios SET nome = 'Francyellen' WHERE id = 1;

DELETE FROM usuarios WHERE id = 1;
```

> ⚠️ Sempre use `WHERE` em `UPDATE` e `DELETE`, ou você altera a tabela inteira.

### JOIN e agregações

```sql
SELECT u.nome, p.titulo
FROM usuarios u
INNER JOIN posts p ON p.usuario_id = u.id;

-- LEFT JOIN traz todos da esquerda, mesmo sem correspondência

SELECT COUNT(*), AVG(idade), MAX(idade) FROM usuarios;

SELECT cidade, COUNT(*)
FROM usuarios
GROUP BY cidade
HAVING COUNT(*) > 5;
```

### Alterar estrutura e índices

```sql
ALTER TABLE usuarios ADD COLUMN idade INT;
ALTER TABLE usuarios DROP COLUMN idade;
DROP TABLE usuarios;

CREATE INDEX idx_usuarios_email ON usuarios (email);
```

### Usuários e permissões

```sql
CREATE USER app_user WITH PASSWORD 'troque_esta_senha';
GRANT SELECT, INSERT ON usuarios TO app_user;
REVOKE INSERT ON usuarios FROM app_user;
```

### Backup e restauração

```bash
pg_dump -U usuario meu_banco > backup.sql
psql -U usuario -d meu_banco < backup.sql
```

> 🔒 **Segurança:** use consultas parametrizadas (nunca monte SQL concatenando texto do usuário, isso abre porta para SQL Injection), dê só as permissões necessárias a cada usuário e não deixe senhas no código.


<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sqlite/sqlite-original.svg" width="22" height="22" alt="SQLite" />&nbsp; <b>SQLite</b> 😨</summary>

<br>

> Banco de dados leve em um único arquivo

### Linha de comando

```bash
sqlite3 meu.db        # abre ou cria o banco
```

| Comando | Ação |
| --- | --- |
| `.tables` | Lista as tabelas |
| `.schema tabela` | Mostra a estrutura |
| `.headers on` | Mostra os nomes das colunas |
| `.mode column` | Formata a saída em colunas |
| `.read script.sql` | Executa um arquivo SQL |
| `.dump` | Exporta o banco em SQL |
| `.quit` | Sai |

### Tipos de dados

| Tipo | Uso |
| --- | --- |
| `INTEGER` | Números inteiros |
| `REAL` | Números decimais |
| `TEXT` | Texto |
| `BLOB` | Dados binários |
| `NULL` | Ausência de valor |

### Criar tabela e CRUD

```sql
PRAGMA foreign_keys = ON;   -- ativa chaves estrangeiras

CREATE TABLE IF NOT EXISTS tarefas (
    id        INTEGER PRIMARY KEY AUTOINCREMENT,
    titulo    TEXT NOT NULL,
    feita     INTEGER DEFAULT 0
);

INSERT INTO tarefas (titulo) VALUES ('Estudar Docker');
SELECT * FROM tarefas WHERE feita = 0;
UPDATE tarefas SET feita = 1 WHERE id = 1;
DELETE FROM tarefas WHERE id = 1;
```

### Usando com Python

```python
import sqlite3

conn = sqlite3.connect("meu.db")
cur = conn.cursor()

cur.execute("CREATE TABLE IF NOT EXISTS tarefas (id INTEGER PRIMARY KEY, titulo TEXT)")

# SEMPRE use ? para valores (evita SQL Injection)
cur.execute("INSERT INTO tarefas (titulo) VALUES (?)", ("Estudar SQL",))
conn.commit()

for linha in cur.execute("SELECT * FROM tarefas WHERE titulo LIKE ?", ("%SQL%",)):
    print(linha)

conn.close()
```

> 🔒 Nunca monte a consulta com f-string ou concatenação usando dados de fora. Use sempre os `?` (placeholders).


<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="22" height="22" alt="Docker" />&nbsp; <b>Docker</b> 🌱</summary>

<br>

> Contêineres: funciona na minha máquina e na sua 🐳

### Imagens e contêineres

```bash
docker --version
docker pull nginx                  # baixa imagem
docker images                      # lista imagens
docker run nginx                   # cria e executa
docker run -d -p 8080:80 nginx     # em segundo plano, mapeando porta
docker run -it ubuntu bash         # modo interativo
docker run --name meu-app nginx    # dá um nome
docker run --rm nginx              # remove ao parar
```

### Gerenciar contêineres

```bash
docker ps                  # em execução
docker ps -a               # todos
docker stop <id|nome>
docker start <id|nome>
docker restart <id|nome>
docker rm <id|nome>        # remove contêiner
docker rmi <imagem>        # remove imagem
docker logs <id|nome>
docker logs -f <id|nome>   # acompanha em tempo real
docker exec -it <id|nome> bash   # entra no contêiner
```

### Dockerfile

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "index.js"]
```

```bash
docker build -t meu-app .          # constrói a imagem
docker run -p 3000:3000 meu-app
```

### Volumes e redes

```bash
docker volume create dados
docker run -v dados:/var/lib/dados minha-imagem
docker run -v $(pwd):/app minha-imagem   # monta pasta local

docker network create minha-rede
docker run --network minha-rede minha-imagem
```

### Docker Compose

```yaml
services:
  app:
    build: .
    ports:
      - "3000:3000"
    environment:
      - NODE_ENV=production
    depends_on:
      - db
  db:
    image: postgres:16
    environment:
      - POSTGRES_PASSWORD=senha
    volumes:
      - dados:/var/lib/postgresql/data

volumes:
  dados:
```

```bash
docker compose up -d       # sobe tudo em segundo plano
docker compose down        # derruba
docker compose logs -f
docker compose build
```

### Limpeza

```bash
docker system prune        # remove itens não usados
docker container prune
docker image prune
```

> 🔒 Não coloque senhas e chaves dentro do Dockerfile ou da imagem. Use variáveis de ambiente ou secrets.

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" width="22" height="22" alt="Bash" />&nbsp; <b>Bash</b></summary>

<br>

> Automatizando o terminal

### Básico

```bash
#!/bin/bash

nome="Fran"
echo "Olá, $nome!"

read -p "Digite algo: " entrada
echo "Você digitou: $entrada"
```

```bash
chmod +x script.sh     # dá permissão de execução
./script.sh            # executa
```

### Condições

```bash
if [ "$idade" -ge 18 ]; then
    echo "maior"
elif [ "$idade" -gt 12 ]; then
    echo "adolescente"
else
    echo "criança"
fi

# testes de arquivo
[ -f arquivo ]   # existe e é arquivo
[ -d pasta ]     # existe e é diretório
[ -z "$var" ]    # string vazia
```

| Operador | Significado |
| --- | --- |
| `-eq` / `-ne` | Igual / diferente (números) |
| `-gt` / `-ge` | Maior / maior ou igual |
| `-lt` / `-le` | Menor / menor ou igual |
| `==` / `!=` | Igual / diferente (strings) |

### Laços

```bash
for i in 1 2 3; do
    echo "$i"
done

for arquivo in *.txt; do
    echo "$arquivo"
done

while read -r linha; do
    echo "$linha"
done < arquivo.txt
```

### Funções e argumentos

```bash
saudacao() {
    echo "Olá, $1!"
}
saudacao "Fran"

# $0 nome do script | $1, $2 argumentos
# $# quantidade de argumentos | $@ todos | $? status do último comando
```

### Redirecionamento e pipes

```bash
comando > arquivo.txt      # sobrescreve
comando >> arquivo.txt     # acrescenta
comando 2> erros.txt       # só erros
comando &> tudo.txt        # saída e erros
comando1 | comando2        # pipe
comando1 && comando2       # executa o 2º se o 1º der certo
comando1 || comando2       # executa o 2º se o 1º falhar
```

### Atalhos do terminal

| Atalho | Ação |
| --- | --- |
| `Ctrl + C` | Interrompe o comando |
| `Ctrl + L` | Limpa a tela |
| `Ctrl + R` | Busca no histórico |
| `Ctrl + A` / `Ctrl + E` | Início / fim da linha |
| `Ctrl + U` | Apaga até o início da linha |
| `Tab` | Autocompleta |
| `!!` | Repete o último comando |

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="22" height="22" alt="Linux" />&nbsp; <b>Linux</b></summary>

<br>

> Casa de quem trabalha com segurança 🐧

### Navegação e arquivos

```bash
pwd                  # diretório atual
ls -la               # lista tudo, com detalhes
cd pasta             # entra
cd ..                # sobe um nível
cd ~                 # vai para a home
mkdir pasta
mkdir -p a/b/c       # cria pastas aninhadas
touch arquivo
cp origem destino
cp -r pasta copia    # copia pasta
mv origem destino    # move ou renomeia
rm arquivo
rm -r pasta          # remove pasta
```

> ⚠️ `rm` não tem lixeira. Confira o caminho antes de rodar `rm -r`.

### Ver e buscar conteúdo

```bash
cat arquivo
less arquivo         # navega (q para sair)
head -n 10 arquivo
tail -n 10 arquivo
tail -f arquivo.log  # acompanha em tempo real
grep "texto" arquivo
grep -rn "texto" .   # busca recursiva com número da linha
find . -name "*.py"
wc -l arquivo        # conta linhas
```

### Permissões

```bash
ls -l
chmod 755 arquivo         # rwxr-xr-x
chmod +x script.sh
chown usuario:grupo arquivo
```

| Número | Permissão |
| --- | --- |
| `4` | Leitura (r) |
| `2` | Escrita (w) |
| `1` | Execução (x) |
| `7` | rwx |
| `6` | rw- |
| `5` | r-x |

Ordem: **dono / grupo / outros**. Exemplo: `640` = dono lê e escreve, grupo lê, outros nada.

### Processos

```bash
ps aux
top                  # ou htop
kill <PID>
kill -9 <PID>        # força
jobs
comando &            # roda em segundo plano
```

### Pacotes (Debian/Ubuntu)

```bash
sudo apt update
sudo apt upgrade
sudo apt install pacote
sudo apt remove pacote
```

### Rede

```bash
ip a                 # interfaces e IPs
ping google.com
curl -I https://site.com     # cabeçalhos HTTP
ss -tulpn            # portas em escuta
nslookup site.com    # consulta DNS
traceroute site.com
```

### Usuários e sistema

```bash
whoami
sudo comando         # executa como administrador
sudo su              # vira root
uname -a             # informações do sistema
df -h                # uso de disco
free -h              # uso de memória
history              # histórico de comandos
man comando          # manual
```

### Úteis para defesa cibernética

```bash
sha256sum arquivo            # hash do arquivo
last                         # últimos logins
sudo journalctl -xe          # logs do sistema
sudo tail -f /var/log/auth.log   # tentativas de login
sudo ufw status              # firewall
```

<br>

</details>

<details>
<summary><img src="https://cdn.simpleicons.org/kalilinux/557C94" width="22" height="22" alt="Kali Linux" />&nbsp; <b>Kali Linux</b> 😨</summary>

<br>

> Laboratório de segurança: só com autorização e em ambiente seu 🐉

> ⚠️ **Use só em ambientes seus ou com autorização por escrito.** Escanear ou testar sistemas de terceiros sem permissão é crime. O ideal é treinar em laboratório próprio (máquinas virtuais, redes isoladas).

### Atualizar o sistema

```bash
sudo apt update && sudo apt full-upgrade -y
sudo apt install kali-linux-default      # conjunto padrão de ferramentas
```

### Descobrir informações da rede

```bash
ip a                        # meus IPs
ip route                    # rotas
whois exemplo.com
dig exemplo.com
nslookup exemplo.com
```

### Nmap (mapeamento do meu laboratório)

```bash
nmap 192.168.56.0/24             # descobre hosts da rede de teste
nmap -sn 192.168.56.0/24         # só verifica quem está ativo
nmap -p 22,80,443 192.168.56.10  # portas específicas
nmap -sV 192.168.56.10           # versão dos serviços
nmap -A 192.168.56.10            # detecção mais completa
```

### Análise de tráfego

```bash
sudo tcpdump -i eth0                       # captura no terminal
sudo tcpdump -i eth0 port 80 -w captura.pcap
wireshark captura.pcap                     # abre a captura na interface gráfica
```

### Auditoria e defesa

```bash
sudo lynis audit system          # auditoria de segurança do sistema
sudo chkrootkit                  # procura rootkits
sudo apt install clamav && freshclam && clamscan -r ~/Downloads
sudo ss -tulpn                   # serviços em escuta
sudo ufw enable && sudo ufw status
```

### Hashes e integridade

```bash
sha256sum arquivo.iso
md5sum arquivo
echo -n "texto" | sha256sum
```

### Dicas

- Use **VM com snapshot**: se quebrar algo, volta ao estado anterior.
- Deixe o laboratório em rede **isolada** (host-only ou NAT interna).
- Mantenha anotações do que foi feito (isso vira relatório depois).
- Para estudar, existem laboratórios legais e gratuitos, como TryHackMe, Hack The Box e DVWA em máquina local.


<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="22" height="22" alt="Git" />&nbsp; <b>Git</b></summary>

<br>

> A máquina do tempo do código

### Configuração inicial

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

### Fluxo do dia a dia

```bash
git init                     # inicia repositório
git clone <url>              # clona repositório
git status                   # situação atual
git add arquivo              # adiciona um arquivo
git add .                    # adiciona tudo
git commit -m "mensagem"     # salva
git push origin main         # envia
git pull                     # baixa e mescla
```

### Branches

```bash
git branch                   # lista branches
git branch nova              # cria
git checkout nova            # troca (ou: git switch nova)
git checkout -b nova         # cria e troca
git merge nova               # mescla na branch atual
git branch -d nova           # apaga
```

### Histórico e desfazer

```bash
git log --oneline            # histórico resumido
git diff                     # diferenças não commitadas
git restore arquivo          # descarta alterações do arquivo
git restore --staged arquivo # tira do stage
git commit --amend           # edita o último commit
git revert <hash>            # desfaz um commit com novo commit
git stash                    # guarda alterações temporariamente
git stash pop                # recupera
```

### Remoto

```bash
git remote -v
git remote add origin <url>
git fetch
```

### Mensagens de commit (convenção)

| Prefixo | Uso |
| --- | --- |
| `feat:` | Nova funcionalidade |
| `fix:` | Correção de bug |
| `docs:` | Documentação |
| `style:` | Formatação |
| `refactor:` | Refatoração |
| `test:` | Testes |
| `chore:` | Tarefas gerais |

### .gitignore comum

```
node_modules/
venv/
.env
__pycache__/
*.log
```

<br>

</details>

<details>
<summary><img src="https://cdn.simpleicons.org/github/8B949E" width="22" height="22" alt="GitHub" />&nbsp; <b>GitHub</b> 😨</summary>

<br>

> Onde o código mora, colabora e aparece no perfil 🐙

### Fluxo com Pull Request

```bash
git clone https://github.com/usuario/repo.git
git checkout -b minha-feature
# ...edita os arquivos...
git add .
git commit -m "feat: adiciona minha feature"
git push -u origin minha-feature
# abre o Pull Request no site (Compare & pull request)
```

### Fork e atualizar

```bash
git remote add upstream https://github.com/original/repo.git
git fetch upstream
git merge upstream/main
```

### Chave SSH

```bash
ssh-keygen -t ed25519 -C "seu@email.com"
cat ~/.ssh/id_ed25519.pub      # copie e cole em Settings > SSH keys
ssh -T git@github.com          # testa a conexão
```

### GitHub CLI (`gh`)

```bash
gh auth login
gh repo create meu-repo --public --clone
gh repo clone usuario/repo
gh pr create --fill
gh pr list
gh issue create
gh issue list
```

### Markdown para README

````markdown
# Título
## Subtítulo

**negrito**  *itálico*  ~~riscado~~  `código`

- item
1. item numerado
- [x] tarefa feita
- [ ] tarefa pendente

[texto do link](https://exemplo.com)
![texto alternativo](imagem.png)

> citação

```python
print("bloco de código")
```

| Coluna A | Coluna B |
| --- | --- |
| 1 | 2 |
````

### README do perfil

Crie um repositório **com o mesmo nome do seu usuário** (`francyellenn/francyellenn`) e o `README.md` dele aparece no seu perfil.

### Recolher conteúdo no README

```html
<details>
<summary>Clique para abrir</summary>

Conteúdo escondido aqui.

</details>
```

### GitHub Actions (exemplo simples)

```yaml
# .github/workflows/teste.yml
name: Testes
on: [push, pull_request]
jobs:
  testar:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: "3.12"
      - run: pip install -r requirements.txt
      - run: pytest
```

### Segurança da conta e do repositório

- Ative a **autenticação em dois fatores (2FA)**.
- **Nunca** suba senhas, tokens ou arquivos `.env` (use `.gitignore`).
- Se vazou um segredo, **revogue/troque a chave** na hora (apagar o commit não basta).
- Ative o **Dependabot** e o **Secret scanning** em Settings > Code security.


<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" width="22" height="22" alt="VS Code" />&nbsp; <b>VS Code</b></summary>

<br>

> Meu editor: atalhos que poupam tempo

Atalhos para **Windows** (no Mac, troque `Ctrl` por `Cmd`).

### Geral

| Atalho | Ação |
| --- | --- |
| `Ctrl + P` | Abrir arquivo por nome |
| `Ctrl + Shift + P` | Paleta de comandos |
| `Ctrl + B` | Mostrar/ocultar barra lateral |
| `Ctrl + '` ou `` Ctrl + ` `` | Abrir/fechar terminal |
| `Ctrl + ,` | Configurações |
| `Ctrl + S` | Salvar |
| `Ctrl + Shift + E` | Explorador de arquivos |
| `Ctrl + Shift + X` | Extensões |

### Edição

| Atalho | Ação |
| --- | --- |
| `Ctrl + D` | Seleciona a próxima ocorrência |
| `Ctrl + Shift + L` | Seleciona todas as ocorrências |
| `Alt + Clique` | Múltiplos cursores |
| `Alt + ↑ / ↓` | Move a linha |
| `Shift + Alt + ↑ / ↓` | Duplica a linha |
| `Ctrl + Shift + K` | Apaga a linha |
| `Ctrl + /` | Comenta/descomenta |
| `Ctrl + ]` / `Ctrl + [` | Indenta / remove indentação |
| `Ctrl + Z` / `Ctrl + Y` | Desfazer / refazer |
| `Shift + Alt + F` | Formatar documento |

### Navegação e busca

| Atalho | Ação |
| --- | --- |
| `Ctrl + F` | Buscar no arquivo |
| `Ctrl + H` | Buscar e substituir |
| `Ctrl + Shift + F` | Buscar em todos os arquivos |
| `Ctrl + G` | Ir para a linha |
| `F12` | Ir para a definição |
| `F2` | Renomear símbolo |
| `Ctrl + Tab` | Alternar entre abas |
| `Ctrl + \` | Dividir editor |

### Extensões úteis

- **Prettier** (formatação)
- **ESLint** (qualidade de código JS/TS)
- **Python** (suporte oficial)
- **GitLens** (histórico do Git)
- **Live Server** (servidor local com recarregamento)
- **Material Icon Theme** (ícones de arquivos)

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" width="22" height="22" alt="Figma" />&nbsp; <b>Figma</b></summary>

<br>

> Design de interfaces e protótipos

### Ferramentas

| Atalho | Ação |
| --- | --- |
| `V` | Mover |
| `F` ou `A` | Frame |
| `R` | Retângulo |
| `O` | Elipse |
| `L` | Linha |
| `T` | Texto |
| `P` | Caneta (pen) |
| `H` | Mão (arrastar a tela) |
| `K` | Escala |
| `C` | Comentário |

### Seleção e organização

| Atalho | Ação |
| --- | --- |
| `Ctrl + G` | Agrupar |
| `Ctrl + Shift + G` | Desagrupar |
| `Ctrl + Alt + G` | Criar frame a partir da seleção |
| `Ctrl + D` | Duplicar |
| `Ctrl + ]` / `Ctrl + [` | Trazer para frente / enviar para trás |
| `Ctrl + Shift + ]` / `[` | Trazer ao topo / enviar ao fundo |
| `Ctrl + Alt + K` | Criar componente |
| `Shift + A` | Adicionar auto layout |

### Visualização

| Atalho | Ação |
| --- | --- |
| `Ctrl + +` / `Ctrl + -` | Zoom |
| `Shift + 1` | Zoom para ver tudo |
| `Shift + 2` | Zoom na seleção |
| `Shift + 0` | Zoom 100% |
| `Ctrl + '` | Mostrar/ocultar grade de pixels |
| `Ctrl + Shift + R` | Mostrar/ocultar réguas |
| `Ctrl + \` | Mostrar/ocultar interface |

### Dicas

- Segure `Shift` ao redimensionar para manter a proporção.
- Segure `Alt` ao arrastar para duplicar.
- Segure `Alt` para ver as distâncias entre elementos.
- Use **Auto Layout** (`Shift + A`) para criar interfaces responsivas.
- Use **Componentes** e **Variantes** para reaproveitar elementos.

<br>

</details>

<details>
<summary><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postman/postman-original.svg" width="22" height="22" alt="Postman" />&nbsp; <b>Postman</b> 😨</summary>

<br>

> Testando APIs sem sofrer

### Fazendo uma requisição

1. Clique em **New > HTTP Request**.
2. Escolha o método (`GET`, `POST`...) e cole a URL.
3. Configure **Params**, **Headers** ou **Body**.
4. Clique em **Send** e veja a resposta (status, tempo, corpo).

### Métodos HTTP

| Método | Uso |
| --- | --- |
| `GET` | Buscar dados |
| `POST` | Criar um recurso |
| `PUT` | Substituir um recurso |
| `PATCH` | Alterar parte de um recurso |
| `DELETE` | Remover um recurso |

### Códigos de status

| Código | Significado |
| --- | --- |
| `200` | OK |
| `201` | Criado |
| `204` | Sem conteúdo |
| `400` | Requisição inválida |
| `401` | Não autenticado |
| `403` | Sem permissão |
| `404` | Não encontrado |
| `429` | Muitas requisições |
| `500` | Erro no servidor |

### Body (JSON)

Em **Body > raw > JSON**:

```json
{
  "nome": "Fran",
  "email": "fran@email.com"
}
```

E em **Headers**: `Content-Type: application/json`

### Autenticação

- **Authorization > Bearer Token**: cole o token de acesso.
- **Basic Auth**: usuário e senha.
- **API Key**: envia em header ou query.

### Variáveis e ambientes

```text
{{base_url}}/usuarios
{{token}}
```

Crie um **Environment** (ex.: Local, Produção) com `base_url`, `token` etc. Assim você troca de ambiente sem editar cada requisição.

> 🔒 Guarde tokens e senhas em variáveis de ambiente do Postman e **não compartilhe** coleções com segredos dentro.

### Testes (aba Tests)

```javascript
pm.test("Status é 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Retorna um nome", function () {
    const dados = pm.response.json();
    pm.expect(dados.nome).to.be.a("string");
});

// salvar valor para a próxima requisição
pm.environment.set("token", pm.response.json().token);
```

### Newman (rodar coleções no terminal)

```bash
npm install -g newman
newman run minha-colecao.json -e ambiente.json
```


<br>

</details>

## 🔗 Links úteis

- [MDN Web Docs](https://developer.mozilla.org/pt-BR/) — HTML, CSS e JavaScript
- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)
- [React Docs](https://react.dev/)
- [Node.js Docs](https://nodejs.org/docs/latest/api/)
- [Python Docs](https://docs.python.org/pt-br/3/)
- [Pro Git (PT-BR)](https://git-scm.com/book/pt-br/v2)
- [VS Code Shortcuts (PDF)](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
- [Atalhos do Figma](https://help.figma.com/hc/pt-br/articles/360040328653)
- [Documentação do PostgreSQL](https://www.postgresql.org/docs/)
- [Documentação do SQLite](https://www.sqlite.org/docs.html)
- [Documentação do Docker](https://docs.docker.com/)
- [Documentação do Kali Linux](https://www.kali.org/docs/)
- [Documentação do GitHub](https://docs.github.com/pt)
- [Documentação do Postman](https://learning.postman.com/docs/)
- [R para Ciência de Dados (livro gratuito)](https://r4ds.hadley.nz/)
- [Beej's Guide to C](https://beej.us/guide/bgc/)

<br>

<div align="center">

🟪🟪🟦🟦🟪🟪🟦🟦🟪🟪🟦🟦🟪🟪🟦🟦

**Feito com ☕, pixel art 👾 e muita curiosidade por [Francyellen Pimenta](https://github.com/francyellenn)**

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=120&section=footer&color=0:8DA2F0,100:B794F0" alt="" />

</div>
