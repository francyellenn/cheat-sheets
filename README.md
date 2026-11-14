# 📚 Folhas de Consulta

Colinhas rápidas de códigos e atalhos das tecnologias que eu uso e estudo.

## 🗂️ Índice

- [HTML5](#-html5)
- [CSS3](#-css3)
- [JavaScript](#-javascript)
- [TypeScript](#-typescript)
- [React](#️-react)
- [Node.js](#-nodejs)
- [Python](#-python)
- [Java](#-java)
- [Docker](#-docker)
- [Bash](#-bash)
- [Linux](#-linux)
- [Git](#-git)
- [VS Code](#-vs-code)
- [Figma](#-figma)

---

## 🟧 HTML5

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

---

## 🟦 CSS3

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

---

## 🟨 JavaScript

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

---

## 🔷 TypeScript

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

---

## ⚛️ React

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

---

## 🟩 Node.js

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

---

## 🐍 Python

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

---

## ☕ Java

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

---

## 🐳 Docker

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

---

## 🐚 Bash

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

---

## 🐧 Linux

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

---

## 🔴 Git

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

---

## 💙 VS Code

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

---

## 🎨 Figma

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

---

## 🔗 Links úteis

- [MDN Web Docs](https://developer.mozilla.org/pt-BR/) — HTML, CSS e JavaScript
- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)
- [React Docs](https://react.dev/)
- [Node.js Docs](https://nodejs.org/docs/latest/api/)
- [Python Docs](https://docs.python.org/pt-br/3/)
- [Pro Git (PT-BR)](https://git-scm.com/book/pt-br/v2)
- [VS Code Shortcuts (PDF)](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
- [Atalhos do Figma](https://help.figma.com/hc/pt-br/articles/360040328653)
