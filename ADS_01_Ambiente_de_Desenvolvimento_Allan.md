# ADS pessoal — Disciplina 1
## Ambiente de desenvolvimento e diagnóstico

**Apostila de estudo e laboratório para Allan Douglas**  
**Projeto condutor:** Inglês Autodidata com Allan Moraes  
**Carga sugerida:** 10 horas de estudo ativo  
**Ambiente principal:** Windows 11, VS Code e Python 3  
**Edição:** 1 de outubro de 2026

> **Sua entrega ao terminar:** uma pasta de projeto organizada, um programa Python executado no ambiente correto, uma dependência instalada e registrada, um erro investigado e duas versões registradas no Git.
>
> Esta é uma trilha pessoal de estudos inspirada em ADS. Não constitui graduação ou certificação acadêmica. O foco desta disciplina é preparar e compreender as ferramentas; cadastro persistente, MySQL e Google Sheets serão construídos nas próximas disciplinas.

## Sumário

1. [Por que começar aqui](#1-por-que-começar-aqui)
2. [Plano de estudo](#2-plano-de-estudo)
3. [O papel de cada ferramenta](#3-o-papel-de-cada-ferramenta)
4. [Arquivos, pastas e terminal](#4-arquivos-pastas-e-terminal)
5. [Preparação do computador](#5-preparação-do-computador)
6. [Primeiro laboratório Python](#6-primeiro-laboratório-python)
7. [Ambiente virtual e dependências](#7-ambiente-virtual-e-dependências)
8. [Diagnóstico e depuração](#8-diagnóstico-e-depuração)
9. [Git e documentação](#9-git-e-documentação)
10. [GitHub e aparência da apostila](#10-github-e-aparência-da-apostila)
11. [Entrega integradora](#11-entrega-integradora)
12. [Exercícios e gabarito](#12-exercícios-e-gabarito)
13. [Aula no YouTube e avaliação](#13-aula-no-youtube-e-avaliação)
14. [Referências e próximos passos](#14-referências-e-próximos-passos)

---

## 1. Por que começar aqui

Você já praticou lógica, começou Python e SQL e quer conectá-los para cadastrar pessoas e produzir planilhas. Também pretende ter páginas com vídeos, quizzes, progresso salvo e, mais adiante, prática oral.

A primeira dificuldade costuma aparecer antes da regra de negócio: **onde escrever, qual programa executar e onde os dados estão?** Aprender isso permite distinguir erro de código, arquivo na pasta errada, biblioteca ausente e problema de conexão.

Nesta disciplina, o projeto se chama `ingles-autodidata`. Usaremos dados fictícios. A mesma organização poderá servir depois a um cadastro de clientes da feira.

### Competências esperadas

Ao concluir, você deverá conseguir:

- Distinguir editor, interpretador, terminal, biblioteca, banco e hospedagem.
- Encontrar a pasta do projeto e reconhecer extensões de arquivos.
- Executar um arquivo Python pelo terminal.
- Identificar qual Python está executando o programa.
- Instalar uma biblioteca no ambiente do projeto.
- Ler uma mensagem de erro e testar uma hipótese por vez.
- Registrar versões locais com Git.
- Documentar como outra pessoa pode executar seu projeto.

### O limite desta primeira entrega

O programa mostrará uma ficha de aluno fictício. Isso confirma que a ferramenta executa seu código. Ainda não será um cadastro com persistência: uma mensagem na tela não prova que algo foi salvo em banco ou planilha.

---

## 2. Plano de estudo

| Encontro | Duração | Conteúdo | Evidência de aprendizagem |
|---|---:|---|---|
| 1 | 1h30 | Ferramentas, arquivos e terminal | Explicar onde escrever e onde executar |
| 2 | 2h | Preparar ferramentas e rodar Python | Executar `app.py` e alterar a saída |
| 3 | 2h | Ambiente virtual, pip e dependências | Mostrar o caminho do Python e importar um pacote |
| 4 | 1h30 | Diagnóstico e depuração | Corrigir um erro documentando a causa |
| 5 | 2h | Git, README e GitHub | Registrar duas versões e visualizar Markdown |
| 6 | 1h | Entrega e autoavaliação | Reabrir o projeto e repetir a execução |
| **Total** | **10h** | | |

São estimativas, não prazos de aprovação. Se a instalação consumir um encontro, continue dali. Você pode dividir cada encontro em blocos de 25 minutos com pausas.

**Como estudar:** leia um trecho, execute, modifique uma coisa e explique o resultado com suas palavras. Reserve o vídeo para acompanhar uma prática, não apenas assistir.

---

## 3. O papel de cada ferramenta

| Nome | Categoria | O que faz | Exemplo no seu projeto |
|---|---|---|---|
| VS Code | Editor extensível | Organiza arquivos e oferece ferramentas | Editar `app.py` |
| Python | Linguagem e seu interpretador | O interpretador executa código Python | Processar o cadastro |
| Terminal | Interface de comandos | Recebe comandos para o shell | Executar um programa |
| PowerShell | Shell | Interpreta comandos do terminal no Windows | Navegar e chamar Python |
| pip | Gerenciador de pacotes | Instala bibliotecas Python | Instalar o conector MySQL |
| Git | Controle de versão | Registra alterações locais | Guardar uma versão funcional |
| GitHub | Serviço para repositórios | Hospeda código e documentação | Exibir esta apostila |
| SQL | Linguagem de banco | Expressa consultas e alterações | Consultar alunos |
| MySQL Server | Sistema de banco de dados | Armazena e processa dados | Guardar matrículas |
| MySQL Workbench | Cliente gráfico | Permite administrar e consultar MySQL | Testar um comando SQL |
| Navegador | Aplicativo web | Exibe páginas e executa JavaScript | Abrir um quiz |

**VS Code não conecta linguagens automaticamente.** O programa utiliza bibliotecas e protocolos para estabelecer a comunicação.

Exemplos de execução:

| Conteúdo | Onde escrever | Quem interpreta ou executa |
|---|---|---|
| `print("Olá")` | Arquivo `.py` | Interpretador Python |
| `SELECT * FROM alunos;` | Editor SQL, como o Workbench | Servidor MySQL |
| `git status` | Terminal | Git |
| `Get-Location` | Terminal PowerShell | PowerShell |
| HTML e CSS | Arquivos `.html` e `.css` | Navegador |

O SSMS pertence ao ecossistema SQL Server. Como seu caminho escolhido usa MySQL, trabalharemos com MySQL e seu cliente. Não precisamos instalar dois sistemas de banco para esta aula.

**Cheque sua compreensão:** se o editor fechar, seus arquivos continuam no disco. Se o programa terminar, os valores que estavam apenas na memória não se tornam automaticamente registros permanentes.

---

## 4. Arquivos, pastas e terminal

### 4.1 Extensões que você encontrará

| Extensão | Conteúdo típico |
|---|---|
| `.py` | Código Python |
| `.sql` | Comandos SQL |
| `.md` | Texto formatável com Markdown |
| `.html` | Estrutura de página web |
| `.css` | Regras de aparência |
| `.js` | Código JavaScript |
| `.json` | Dados estruturados |
| `.csv` | Dados tabulares em texto |
| `.xlsx` | Pasta de trabalho de planilha |

No Explorador de Arquivos, habilite a exibição de extensões. Confirme que o nome é `app.py`, e não `app.py.txt`. Renomear a extensão não converte o conteúdo: um documento Word renomeado para `.md` não vira Markdown.

### 4.2 Uma pasta para este projeto

Crie uma pasta chamada `ingles-autodidata` em um local de estudos que você encontre facilmente. No VS Code, use **File > Open Folder** e abra essa pasta.

Criaremos estes itens ao longo da aula:

| Caminho dentro do projeto | Finalidade |
|---|---|
| `app.py` | Programa inicial |
| `verificar_mysql.py` | Verificação de importação do conector |
| `README.md` | Instruções do projeto |
| `diario.md` | Registro de diagnóstico |
| `requirements.txt` | Dependências instaladas |
| `.gitignore` | Itens que não devem entrar no Git |
| `.venv/` | Ambiente Python local |

### 4.3 Comandos no PowerShell

No VS Code, abra **Terminal > New Terminal**. O roteiro usa PowerShell. Confira o perfil do terminal; comandos de Git Bash ou Prompt de Comando podem ser diferentes.

```powershell
Get-Location
Get-ChildItem
```

O primeiro mostra a pasta atual. O segundo lista seu conteúdo. Procure o nome `ingles-autodidata` no caminho.

Para entrar em uma pasta existente, adapte o caminho:

```powershell
Set-Location "C:\Users\SEU_USUARIO\Documents\ingles-autodidata"
```

`SEU_USUARIO` é um marcador, não um nome para copiar literalmente. Sua pasta Documents pode estar em outro local. Abrir a pasta pelo VS Code evita precisar adivinhar esse caminho.

Outros comandos úteis:

```powershell
Set-Location ..
New-Item -ItemType Directory -Name estudos
```

O primeiro sobe um nível; o segundo cria uma pasta chamada `estudos` no local atual. Use-os como exercício e depois reabra a pasta principal do projeto.

### 4.4 Terminal não é o console interativo do Python

Se você digitar `python` sozinho, pode entrar em um console com o símbolo `>>>`. Nesse console, escrevemos código Python. Para voltar ao terminal:

```python
exit()
```

Não digite `pip install ...` ou `git status` depois de `>>>`. Nesta apostila, blocos marcados `powershell` são comandos de terminal; blocos `python` são código Python.

**Prática:** abra o terminal, descubra a pasta atual, liste os arquivos e explique onde está o projeto. Registre a resposta em `diario.md`.

---

## 5. Preparação do computador

### 5.1 Confira antes de instalar

Como você já usa algumas ferramentas, comece verificando:

```powershell
python --version
py --version
git --version
```

Se `python` ou `py` funcionar e indicar Python 3, você já tem um caminho inicial. Se um comando não existir, isso não significa que todos falharam. Um atalho também pode abrir a instalação: leia o resultado.

### 5.2 Instale apenas o necessário

- [Python para Windows](https://www.python.org/downloads/windows/).
- [VS Code](https://code.visualstudio.com/download).
- [Git](https://git-scm.com/downloads).

No VS Code, abra **Extensions**, pesquise **Python** e escolha a extensão publicada pela **Microsoft**. A extensão auxilia o editor, mas o interpretador Python é instalado separadamente.

O fluxo de instalação do Python no Windows evoluiu e pode usar o Python Install Manager. Siga as instruções da página oficial apresentada no seu computador. Tutoriais antigos podem mostrar uma tela diferente. Após instalar, feche e reabra o terminal; se necessário, reabra o VS Code.

### 5.3 Diagnóstico inicial

```powershell
python -c "import sys; print(sys.executable)"
```

Esse comando mostra o executável usado. Se apenas `py` funcionar, use:

```powershell
py -c "import sys; print(sys.executable)"
```

Registre no diário a versão e o caminho, sem publicar informações pessoais desnecessárias. O objetivo é saber qual ferramenta está sendo chamada, não memorizar um caminho longo.

**Critério de conclusão:** pelo menos um dos comandos de Python executa e você consegue abrir a pasta no VS Code. O Git deve estar disponível antes do capítulo 9.

---

## 6. Primeiro laboratório Python

### 6.1 Crie e salve o arquivo

Na pasta aberta, crie `app.py` e escreva:

```python
print("Inglês Autodidata — laboratório de ADS")
aluno = "Ana Exemplo"
curso = "Greetings"
print("Aluno:", aluno)
print("Curso:", curso)
print("Situação: demonstração; nenhum dado foi salvo.")
```

Salve com **Ctrl+S**. No terminal da pasta do projeto:

```powershell
python app.py
```

Se seu comando disponível for `py`, execute `py app.py`.

Resultado esperado:

```text
Inglês Autodidata — laboratório de ADS
Aluno: Ana Exemplo
Curso: Greetings
Situação: demonstração; nenhum dado foi salvo.
```

### 6.2 Entenda o suficiente para modificar

`print` exibe informações. `aluno` e `curso` são nomes associados a valores. Textos ficam entre aspas. O programa é executado, mostra a saída e termina.

Troque `Greetings` por `English for Business`, salve e rode novamente. Depois restaure `Greetings` para acompanhar o restante da apostila.

**Perguntas de controle:** você alterou o arquivo certo? Salvou? Rodou novamente? A saída antiga pode continuar visível acima da nova no terminal; compare a execução mais recente.

### 6.3 Experimento: encerrar e reabrir

Feche o VS Code, reabra a pasta e execute de novo. O código permanece porque está em arquivo. A ficha reaparece porque o programa contém os textos, não porque já existe um banco de alunos.

---

## 7. Ambiente virtual e dependências

### 7.1 O que estamos isolando

Um ambiente virtual mantém as bibliotecas deste projeto separadas das de outros projetos. Ele não é uma máquina virtual, não hospeda um site e não instala o servidor MySQL.

Na pasta principal, crie o ambiente:

```powershell
python -m venv .venv
```

Se necessário, use `py -m venv .venv` em vez do comando acima. Escolha uma das formas. Aguarde o terminal retornar.

### 7.2 Use o executável do ambiente diretamente

Para evitar que diferenças de ativação atrapalhem esta primeira aula, usaremos o caminho explícito:

```powershell
.\.venv\Scripts\python.exe --version
.\.venv\Scripts\python.exe app.py
.\.venv\Scripts\python.exe -c "import sys; print(sys.executable)"
```

O caminho impresso deve apontar para `.venv\Scripts\python.exe` dentro do projeto.

No VS Code, abra **Ctrl+Shift+P**, execute **Python: Select Interpreter** e selecione esse ambiente. Se não aparecer, use a opção de informar o caminho do interpretador.

Ativar o ambiente é uma conveniência opcional. No PowerShell, o comando costuma ser:

```powershell
.\.venv\Scripts\Activate.ps1
```

Se houver bloqueio de execução de scripts, continue com o executável explícito. Não é necessário alterar políticas do computador para concluir o laboratório. A seleção do editor e o terminal aberto podem divergir; o caminho explícito reduz essa ambiguidade.

### 7.3 Instale a primeira dependência

Usaremos o conector que será útil na integração futura. Requer internet para baixar o pacote:

```powershell
.\.venv\Scripts\python.exe -m pip install mysql-connector-python
.\.venv\Scripts\python.exe -m pip show mysql-connector-python
```

`-m pip` chama o pip do Python indicado. O nome instalado é `mysql-connector-python`, mas o nome importado é `mysql.connector`.

Crie `verificar_mysql.py`:

```python
import sys
import mysql.connector

print("Python em uso:", sys.executable)
print("Versão do conector:", mysql.connector.__version__)
print("Importação concluída. Nenhuma conexão com banco foi feita.")
```

Execute:

```powershell
.\.venv\Scripts\python.exe verificar_mysql.py
```

**Interpretação:** a importação funcionando confirma a disponibilidade da biblioteca. Ainda faltam servidor, credenciais, banco e código de conexão para haver integração real.

### 7.4 Registre as dependências

No PowerShell:

```powershell
.\.venv\Scripts\python.exe -m pip freeze | Set-Content -Encoding utf8 requirements.txt
```

O arquivo registra pacotes e versões daquele ambiente. Para instalá-los em um ambiente compatível, usamos:

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

Esse arquivo ajuda a reproduzir o ambiente, mas não substitui registrar a versão do Python nem garante compatibilidade com todo sistema operacional futuro.

**Não envie `.venv` ao GitHub.** Ela será recriada a partir das instruções e dependências.

---

## 8. Diagnóstico e depuração

### 8.1 Um método para investigar

Antes de reinstalar ferramentas, responda:

1. O que eu esperava?
2. O que aconteceu, exatamente?
3. Qual comando executei?
4. Em qual pasta?
5. Qual interpretador foi usado?
6. Qual é a última linha do erro?
7. Qual pequena mudança testa minha hipótese?

A última linha costuma indicar o tipo de erro; as linhas anteriores ajudam a localizar a origem. Leia ambas.

### 8.2 Laboratório de erro intencional

Crie temporariamente `erro.py`:

```python
aluno = "Ana Exemplo"
print(alunos)
```

Execute com o Python da `.venv`. O nome definido é `aluno`, mas o nome solicitado é `alunos`. É esperado um `NameError`.

Corrija para `print(aluno)` e execute novamente. Registre a hipótese e a evidência: o erro desapareceu e a saída passou a mostrar o texto esperado. Depois remova apenas esse arquivo de exercício pelo editor ou mantenha-o corrigido em uma pasta de estudos.

### 8.3 Erro lógico

Este programa executa, mas o resultado pode estar errado:

```python
acertos = 3
total = 4
percentual = acertos / total
print("Percentual:", percentual)
```

Se a intenção era mostrar porcentagem, a saída `0.75` representa uma proporção. A correção é calcular `acertos / total * 100`, produzindo `75.0`. A ausência de mensagem de erro não prova que a regra está correta.

### 8.4 Depurador: observar a execução

No `app.py`, clique na margem à esquerda do número da linha `print("Aluno:", aluno)` para marcar um breakpoint. Abra **Run and Debug** e inicie a depuração Python; se solicitado, selecione **Python File**. Confirme que o interpretador escolhido é o da `.venv` e que o suporte **Python Debugger**, da Microsoft, está instalado.

Quando a execução parar, observe `aluno` e `curso` na área de variáveis. Avance pelo botão **Step Over**. O breakpoint pausa antes de executar aquela linha. Continue ou encerre pelo painel de depuração.

Use os botões da interface se as teclas F do notebook controlarem brilho ou volume.

### 8.5 Tabela de investigação

| Sintoma | Hipótese | Primeiro teste |
|---|---|---|
| Python não é reconhecido | Comando indisponível ou terminal antigo | Reabrir terminal e testar `py --version` |
| `can't open file` | Caminho ou nome incorreto | Listar arquivos e conferir extensão |
| `SyntaxError` | Código com estrutura inválida | Ler linha indicada e conferir aspas/parênteses |
| `NameError` | Nome inexistente naquele ponto | Comparar grafia e onde foi definido |
| `ModuleNotFoundError` | Pacote ausente nesse interpretador | Rodar `-m pip show` com o mesmo Python |
| Código antigo continua aparecendo | Arquivo não salvo ou outro arquivo executado | Salvar e confirmar caminho |
| Ativação bloqueada | Política do PowerShell | Executar diretamente o Python da `.venv` |
| Download do pacote falha | Rede, certificado ou versão incompatível | Ler erro completo e verificar requisito do pacote |

Não desative verificações de certificado para tentar resolver um download. A mensagem exata deve orientar a investigação.

### 8.6 Diário de diagnóstico

Crie `diario.md` e use este modelo:

```markdown
## Tentativa 1
- Objetivo:
- Comando executado:
- Pasta atual:
- Resultado esperado:
- Resultado observado:
- Hipótese:
- Mudança feita:
- Resultado após a mudança:
- Explicação com minhas palavras:
```

Quando pedir ajuda, envie o código relevante, o comando e o erro em texto. Remova senhas e tokens. Isso permite investigar melhor do que uma foto parcial da tela.

---

## 9. Git e documentação

### 9.1 Três ações diferentes

**Salvar** grava o arquivo no disco. **Commit** registra uma versão no Git local. **Push** envia commits a um repositório remoto configurado. Um commit não publica automaticamente seu código na internet.

### 9.2 Prepare o que poderá ser versionado

Crie `.gitignore` antes de adicionar arquivos:

```gitignore
.venv/
__pycache__/
*.pyc
.env
credentials.json
token.json
dados_privados/
```

Esse arquivo orienta o Git a ignorar itens ainda não rastreados. Ele não apaga arquivos do histórico e não torna segura uma credencial já publicada.

### 9.3 Faça o primeiro registro

Na pasta deste projeto novo:

```powershell
git init
git status
git add app.py verificar_mysql.py requirements.txt .gitignore diario.md
git diff --cached
git commit -m "Prepara ambiente e demonstra ficha de aluno"
git log --oneline
```

Se o Git pedir sua identidade, configure para este repositório e repita o commit:

```powershell
git config user.name "SEU NOME"
git config user.email "SEU EMAIL DE COMMIT"
```

Substitua os marcadores. Você pode usar o endereço de privacidade fornecido na sua conta GitHub.

Altere o curso no programa, salve e revise:

```powershell
git diff
git add app.py
git commit -m "Atualiza curso da ficha de demonstração"
git status
```

### 9.4 Escreva o README do projeto

Crie `README.md` contendo:

- Nome e objetivo do laboratório.
- Versão do Python utilizada.
- Como criar `.venv`.
- Como instalar `requirements.txt`.
- Comandos para executar os dois programas.
- Saída esperada.
- Limites atuais: sem persistência e sem conexão com MySQL.

Adicione e registre esse arquivo com `git add README.md` e um novo commit. A pessoa que abrir seu repositório deve conseguir entender o que já funciona.

---

## 10. GitHub e aparência da apostila

### 10.1 Publicar o texto para leitura

Você pode subir **este arquivo `.md`** pelo recurso de adicionar/enviar arquivos do GitHub. Ao abrir o arquivo no repositório, selecione a visualização renderizada, normalmente **Preview**, se aparecer o código-fonte.

Se desejar que a apostila seja a apresentação principal de um repositório exclusivo de estudos, salve uma cópia com o nome `README.md` na raiz desse repositório. Preserve o README do projeto de código: são documentos com finalidades diferentes.

O GitHub renderiza títulos, tabelas, links, listas e blocos de código. **Exibir o Markdown não executa o Python nem hospeda automaticamente seu backend.**

### 10.2 Enviar o projeto com Git

Para este laboratório, crie no GitHub um repositório remoto vazio, sem gerar README ou licença automaticamente. Copie o endereço HTTPS que a própria página fornecer. Depois, no terminal do projeto:

```powershell
git branch -M main
git remote add origin URL_HTTPS_COPIADA_DO_GITHUB
git push -u origin main
```

O marcador `URL_HTTPS_COPIADA_DO_GITHUB` deve ser substituído pelo endereço real. Siga a autenticação apresentada pela ferramenta, sem colocar tokens no código.

Se já houver um remoto, confira `git remote -v` antes de adicionar outro. Se o push for rejeitado porque o remoto tem arquivos, não use `--force`: será necessário reconciliar os históricos. O caminho acima pressupõe um remoto vazio.

### 10.3 Alterações feitas no site

Se editar no GitHub depois, confira `git status` no computador. Com o trabalho local salvo e registrado, tente:

```powershell
git pull --ff-only
```

Se houver divergência, esse comando pode parar sem integrar. Guarde a mensagem para investigar. Nesta etapa, alterne conscientemente onde edita para não criar duas versões concorrentes sem perceber.

---

## 11. Entrega integradora

**Missão:** preparar a primeira base técnica do Inglês Autodidata.

### Checklist

- [ ] Abri a pasta correta no VS Code.
- [ ] Identifiquei a versão do Python.
- [ ] Criei a `.venv` e executei seu Python.
- [ ] Rodei `app.py` e expliquei a saída.
- [ ] Instalei e importei o conector MySQL.
- [ ] Registrei as dependências em `requirements.txt`.
- [ ] Investiguei um erro e registrei a causa em `diario.md`.
- [ ] Criei `.gitignore` e README.
- [ ] Registrei pelo menos dois commits.
- [ ] Fechei, reabri e executei o projeto novamente.
- [ ] Sei explicar por que ainda não existe persistência.

### Avaliação sugerida

| Critério | Pontos |
|---|---:|
| Explicar ferramentas e localizar arquivos | 2 |
| Executar com o interpretador correto | 2 |
| Instalar, importar e registrar dependência | 2 |
| Diagnosticar erro com evidência | 2 |
| Versionar e documentar o projeto | 2 |

Meta: 8/10, com execução e importação funcionando obrigatoriamente. Publicar no GitHub é recomendado, mas problemas de login não devem impedir a avaliação do trabalho local.

**Desafio de transferência:** altere a demonstração para mostrar um cliente fictício e um produto da feira. Explique quais ferramentas permaneceram iguais. Depois retome a versão de alunos. Você estará aplicando a mesma infraestrutura a outro domínio.

---

## 12. Exercícios e gabarito

Responda antes de abrir a resolução.

1. Instalar a extensão Python no VS Code garante que o interpretador esteja instalado?
2. Qual é a diferença entre arquivo salvo e commit?
3. Por que o comando de instalação usa o Python da `.venv`?
4. O conector foi importado. Isso prova que o MySQL está conectado?
5. Onde você digita `git status`?
6. Um erro diz que `app.py` não existe. Quais duas coisas verificar primeiro?
7. O programa exibe “aluno cadastrado”. Isso prova que salvou dados?
8. Qual arquivo registra as dependências? Qual impede o envio da `.venv` por padrão?
9. Por que não basta copiar a pasta `.venv` para outro computador?
10. GitHub exibiu o Markdown. O backend Python já está online?
11. O código calcula `3 / 4` e mostra `0.75`. Existe erro de sintaxe? O que falta se o objetivo é percentual?
12. Você instalou um pacote, mas o programa não o encontra. Que relação precisa conferir?

<details>
<summary><strong>Abrir gabarito comentado</strong></summary>

1. Não. Extensão e interpretador têm funções distintas.
2. Salvar grava o estado atual no disco; commit registra uma versão no histórico local.
3. Para instalar no ambiente que executará o programa, reduzindo confusão entre instalações.
4. Não. Prova apenas que o pacote está disponível para importação naquele ambiente.
5. No terminal, preferencialmente dentro da pasta do repositório.
6. A pasta atual e o nome/extensão do arquivo, inclusive possível `.py.txt`.
7. Não. O programa pode simplesmente imprimir uma frase sem salvar nada.
8. `requirements.txt` e `.gitignore`, respectivamente. O ignore não remove itens já rastreados.
9. O ambiente contém caminhos e componentes locais. É mais adequado recriá-lo e instalar dependências compatíveis.
10. Não. A visualização do documento não executa um servidor Python.
11. Não há erro de sintaxe. Para apresentar porcentagem numérica, multiplicar a proporção por 100.
12. Se o Python usado para instalar é o mesmo usado para executar. Confira `sys.executable` e use esse executável com `-m pip show`.

</details>

### Exercício de explicação

Escreva um parágrafo respondendo: “Para integrar Python com SQL, o que o editor faz, o que o conector faz e o que o servidor MySQL faz?”

Resposta esperada: o editor ajuda a escrever e organizar; o conector permite ao Python comunicar-se com MySQL; o servidor executa os comandos SQL e mantém os dados. Nas próximas disciplinas implementaremos essa comunicação.

---

## 13. Aula no YouTube e avaliação

### Aula escolhida

**Getting Started with Python in VS Code (Official Video)**  
Canal: **Visual Studio Code** — apresentador: **Reynald Adolphe**  
Idioma: inglês; escolhido também porque você já tem formação e experiência nesse idioma.

**YouTube:** https://www.youtube.com/watch?v=D2cwvpJSBX4

**Descrição e capítulos oficiais:** https://learn.microsoft.com/en-us/shows/visual-studio-code/getting-started-with-python-in-vs-code-official-video

### Como foi avaliada

A análise usou a descrição e os capítulos publicados pela Microsoft, comparados aos objetivos desta disciplina e à documentação atual. Não foi possível obter a transcrição completa nem verificar cada demonstração do vídeo. Portanto, a avaliação é de adequação do escopo, não uma certificação de cada instrução apresentada.

| Capítulo oficial | Uso nesta apostila |
|---|---|
| 00:23 — instalação do Python | Apoio à preparação; telas atuais podem diferir |
| 01:31 — extensão Python | Entender o suporte do editor |
| 02:29 — ambiente virtual | Acompanhar o capítulo 7 |
| 04:50 — execução de arquivo | Comparar formas de executar |
| 05:25 — REPL | Distinguir console Python de terminal |
| 06:20 e 08:27 — navegação e depuração | Apoio à investigação de erros |

**Parecer:** adequada como demonstração introdutória do ambiente. Não é suficiente sozinha para as 10 horas da disciplina. Pelo escopo anunciado, não cobre integralmente nosso fluxo de Git/GitHub, diário de diagnóstico e laboratório personalizado. A apostila fornece esses complementos. Use a documentação atual se menus ou instalação forem diferentes.

### Como assistir ativamente

1. Faça primeiro a verificação do capítulo 5, evitando reinstalar ferramentas que já funcionam.
2. Pause na criação do ambiente e identifique seu próprio interpretador.
3. Execute a ficha de aluno desta apostila.
4. Ao chegar à depuração, repita com seu arquivo.
5. Termine registrando o que conseguiu reproduzir e qual ponto ficou pendente.

---

## 14. Referências e próximos passos

Fontes consultadas em 01/10/2026. Os exemplos, exercícios e organização pedagógica foram elaborados para esta trilha.

- [Python no Windows](https://docs.python.org/3/using/windows.html): instalação e comandos no Windows.
- [Python no VS Code](https://code.visualstudio.com/docs/python/python-tutorial): editor, extensão e execução.
- [Ambientes Python no VS Code](https://code.visualstudio.com/docs/python/environments): escolha do interpretador.
- [venv](https://docs.python.org/3/library/venv.html): ambientes virtuais.
- [Guia do pip](https://pip.pypa.io/en/stable/user_guide/): instalação e dependências.
- [MySQL Connector/Python](https://dev.mysql.com/doc/connector-python/en/): integração futura com o banco.
- [Depuração Python no VS Code](https://code.visualstudio.com/docs/python/debugging): execução passo a passo.
- [Tutorial do Git](https://git-scm.com/docs/gittutorial): versionamento básico.
- [README no GitHub](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes): apresentação do repositório.

### O que vem depois

Na **Disciplina 2 — Programação aplicada com Python**, transformaremos a ficha fixa em um cadastro com entrada de dados, funções, listas, dicionários e validação. Na **Disciplina 3**, modelaremos o banco. Na **Disciplina 4**, conectaremos Python e MySQL. Exportação de arquivos e Google Sheets entram em seguida.

Seu primeiro passo hoje: abrir a pasta, confirmar o Python e executar `app.py`. Ao pedir a próxima orientação, envie o resultado desse laboratório e a primeira dificuldade encontrada.
