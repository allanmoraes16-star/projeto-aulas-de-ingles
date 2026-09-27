# PPC pessoal de fundamentos de Engenharia de Software — Allan Moraes

**Versão:** 26 de setembro de 2026  
**Origem:** reconstrução pessoal, em ordem de pré-requisitos, das disciplinas do PPC de Engenharia de Software de 2017 trazidas na conversa. **Não é o PPC oficial nem equivale a diploma.** As descrições das primeiras disciplinas são inferências de suas bibliografias; as quatro ementas transcritas explicitamente têm mais detalhe.

## Objetivo e ritmo

Aprender a construir software pequeno e confiável para seu projeto de ensino de inglês, compreender o que ocorre dentro do computador e manter uma base para estudos posteriores em Engenharia de Software. Referência de ritmo: **5 horas por semana, 40 semanas, cerca de 200 horas**. As durações são sugestões e podem ser estendidas. Uma entrega funcional por etapa vale mais que concluir cada livro.

**Ponto de partida:** curso de lógica do CETAM concluído, com condicionais, laços, vetores e matrizes em VisuAlg; primeiros contatos com Python, HTML, VS Code, GitHub e Netlify. Reaproveite os algoritmos de notas, tabuada e cadastro como exercícios de migração.

## Mapa de ordem

| Ordem | Bloco, ligação com o PPC de 2017 | Semanas sugeridas | Resultado verificável |
|---|---|---:|---|
| 0 | Ferramentas práticas, adição atual | 1–2 | Executar Python, abrir terminal, criar repositório e fazer commits |
| 1 | Introdução à Programação | 3–6 | Traduzir três algoritmos de VisuAlg para Python e explicar cada parte |
| 2 | Laboratório de Programação A | 7–10 | Programa modular de exercícios com arquivos e verificações simples |
| 3 | Introdução à Organização de Computadores | 11–13 | Explicar bits, memória, CPU, instruções e medir um programa curto |
| 4 | Algoritmos e Estruturas de Dados | 14–19 | Implementar busca, ordenação, pilha e fila; comparar custos |
| 5 | Sistemas Operacionais I | 20–23 | Usar processos, arquivos e ferramentas do sistema; demonstrar memória virtual |
| 6 | Introdução a Bancos de Dados | 24–28 | Modelar aluno, atividade e tentativa; consultas SQL e persistência |
| 7 | Processo de Desenvolvimento de Software | 29–31, com hábitos desde a semana 1 | Requisitos, fluxo de trabalho, revisão e documentação do projeto |
| 8 | Laboratório de Programação Avançada | 32–35 | Reproduzir e corrigir uma condição de corrida; medir ganho de paralelismo |
| 9 | Projeto integrador | 36–40 | Protótipo local de exercícios de inglês com progresso salvo e README |

**Dependências:** algoritmos básicos → estruturas de dados; arquitetura + programação → sistemas operacionais; modelagem + programação → banco de dados; processos/threads + estruturas → concorrência. Banco de dados e sistemas operacionais podem ser estudados em paralelo, se houver tempo. Processo de software é um hábito contínuo e ganha um bloco próprio para aprofundamento.

## Planos de estudo por bloco

### 0. Ferramentas

Aprenda caminho e diretório, terminal, execução de um arquivo `.py`, VS Code, depurador, `git init`, `git status`, `git add`, `git commit` e publicação de repositório. **Git é um programa executado no terminal ou integrado ao editor; GitHub hospeda repositórios.** Entrega: repositório com README e primeiro commit. Use *The Missing Semester* (edição 2026) e a documentação do GitHub. Não espere dominar Git para começar os programas.

### 1. Introdução à Programação

Revisão breve de variáveis, condições e laços; depois funções, listas, dicionários, entrada, saída e tratamento de erros em Python. Faça a conversão do `TURMA_NOTAS_MEDIAS_FINAIS`, do cálculo de IMC e da tabuada; confira com casos normais e limites. **Critério de saída:** conseguir escrever e explicar um programa sem copiar linha por linha do VisuAlg. Leitura central: tutorial oficial de Python 3, com apoio de Menezes para uma segunda explicação. A bibliografia do PPC sugere fundamentos de várias linguagens; não é necessário estudar Java, C++ e XML simultaneamente.

### 2. Laboratório de Programação A

Pratique dividir o código em funções e módulos, ler/gravar JSON ou CSV, depurar e verificar resultados. Faça um banco local de perguntas de inglês em arquivo, com correção, pontuação e retomada após fechar o programa. Depois introduza C: compilação, tipos, vetores, strings, funções e `struct`. **Critério:** resolver o mesmo exercício simples em Python e C e descrever o papel do compilador. King ou Feofiloff são apoios conceituais; use documentação atual da linguagem para detalhes de implementação. Não presuma que toda a ementa histórica da disciplina foi confirmada apenas pela bibliografia.

### 3. Introdução à Organização de Computadores

Estude binário e hexadecimal, portas lógicas, CPU, instruções, registradores, RAM, cache, endereços, assembly e entrada/saída. Faça conversões manuais, represente caracteres em bytes e observe o assembly de uma soma em C. Use Patterson & Hennessy ou *Computer Systems: A Programmer's Perspective* como textos clássicos; a arquitetura específica do livro (MIPS/ARM) é exemplo, não requisito universal. **Critério:** narrar o percurso de uma instrução simples sem confundir programa, processo, CPU e memória.

### 4. Algoritmos e Estruturas de Dados

Aprenda custo de tempo e espaço, busca linear/binária, ordenação, recursão, vetores dinâmicos, listas encadeadas, pilhas, filas, árvores e hash. Primeiro desenhe e implemente em Python; em C, implemente ao menos uma lista encadeada e uma pilha, usando ponteiros e liberando a memória alocada. Compare busca linear e binária em dados ordenados; não transforme medidas pequenas em provas de complexidade. **Critério:** escolher uma estrutura para guardar tentativas por aluno e justificar operações e custos. Celes, Feofiloff e Ziviani continuam úteis como segunda explicação; Cormen entra por assunto, sem obrigação de leitura integral.

### 5. Sistemas Operacionais I

Estude processos, threads, escalonamento, memória virtual/paginação, arquivos, permissões, entrada/saída e virtualização. Use o gerenciador de tarefas e terminal para observar processos e uso de memória; crie dois processos que leiam arquivos e descreva o que pertence ao sistema operacional. **Critério:** explicar por que dois programas parecem rodar ao mesmo tempo e por que fechar um programa não significa necessariamente apagar seus arquivos. Base aberta: *Operating Systems: Three Easy Pieces* (OSTEP); Tanenbaum e Silberschatz como apoio.

### 6. Introdução a Bancos de Dados

Modele entidades e relacionamentos; transforme o desenho em tabelas; estude chaves, restrições, normalização, `SELECT`, `JOIN`, `GROUP BY`, transações, índices, concorrência e recuperação. Comece em SQLite para um projeto local e depois refaça consultas essenciais no PostgreSQL. Entrega: tabelas `alunos`, `atividades`, `tentativas` e consultas de progresso; teste inserção incorreta para verificar restrições. **Critério:** explicar por que uma tentativa liga um aluno a uma atividade e demonstrar que os dados sobrevivem ao fechamento do programa. Elmasri/Navathe e Silberschatz seguem relevantes para a teoria. Índices e transações precisam de prática, sem tentar implementar um SGBD inteiro.

### 7. Processo de Desenvolvimento de Software

Na semana 1, use uma lista curta de tarefas, commits legíveis e uma definição de pronto. Aqui aprofunde requisitos, histórias de usuário, análise de risco, revisão, qualidade, escolha de ciclo de vida, métricas simples e melhoria do processo. Reescreva os requisitos da plataforma de exercícios, registre bugs e faça uma pequena retrospectiva. **Critério:** outra pessoa entende como instalar, usar, testar e continuar o projeto pelo README. Consulte Sommerville para fundamentos; Scrum Guide oficial para Scrum; Guia Geral MPS de Software 2024 para o modelo brasileiro. O PPC registra “MSP.BR” numa passagem, mas as referências e demais ocorrências apontam para **MPS.BR**. Para um projeto individual, adapte as práticas úteis; certificação e governança formal não são pré-requisitos do protótipo.

### 8. Laboratório de Programação Avançada

Diferencie **concorrência** (tarefas com progresso intercalado), **paralelismo** (execução simultânea possível em vários núcleos) e **distribuição** (processos em máquinas ou espaços separados trocam mensagens). Crie um contador compartilhado em C com threads, provoque perda de atualizações e conserte usando mutex; depois experimente produtor/consumidor ou uma fila com condição. Meça uma tarefa divisível de processamento e compare com execução sequencial. Finalmente troque mensagens entre processos locais, começando por sockets ou pipes; MPI/OpenMP podem ser aprofundamentos posteriores. **Critério:** explicar race condition, deadlock e quando a paralelização piora o desempenho. O texto histórico destaca POSIX threads, semáforos, monitores e passagem de mensagens; ferramentas atuais devem ser verificadas pela documentação oficial. Não comece este bloco antes de processos, memória, C e depuração.

### 9. Projeto integrador: English Quest

Versão mínima: atividades de inglês; aluno escolhe atividade, responde, recebe retorno e reencontra seu progresso ao reabrir. Comece **localmente** com Python + SQLite; uma interface web simples com HTML/CSS/JavaScript é uma extensão. Versione no Git, documente esquema de dados e fluxo, registre testes de caminhos relevantes e um bug corrigido. Só depois decida se precisa de contas, servidor, publicação, pagamentos ou escala. A página de venda do curso e o sistema de aprendizagem são projetos distintos e podem evoluir em ritmos diferentes.

## Rotina de cinco horas por semana

- 1 hora: leitura guiada e anotação de conceitos.
- 3 horas: exercícios e implementação do projeto.
- 1 hora: depuração, revisão, commit e breve registro do que aprendeu.

Se estiver apertado pela feira, aulas ou concurso, faça **uma sessão de 90 minutos de código e uma revisão de 30 minutos**; pause o cronograma, não acumule capítulos para “compensar”. Antes de avançar, produza a entrega do bloco e explique-a em voz alta como se ensinasse a um aluno.

## Referências atuais e abertas para consulta

- Python: https://docs.python.org/3/tutorial/index.html
- Ferramentas, Git, depuração e qualidade: https://missing.csail.mit.edu/2026/ ; https://docs.github.com/en/get-started
- Revisão ampla de fundamentos, C e SQL: https://cs50.harvard.edu/x/2026/syllabus/
- Sistemas operacionais e concorrência: https://pages.cs.wisc.edu/~remzi/OSTEP/
- Primeiros passos em SQLite: https://www.sqlite.org/quickstart.html
- Tutorial de PostgreSQL: https://www.postgresql.org/docs/current/tutorial.html
- Processo: https://scrumguides.org/scrum-guide.html ; https://softex.br/download/guia-geral-mps-de-software2024/
- Aprofundamento em passagem de mensagens e paralelismo: https://www.mpi-forum.org/docs/ ; https://www.openmp.org/specifications/

**Acesso a livros antigos:** referência bibliográfica ou PDF encontrado online não indica licença aberta. Consulte páginas de autores, bibliotecas e editoras; OSTEP e as documentações acima têm acesso aberto confirmado em suas páginas oficiais. Este plano cobre as disciplinas compartilhadas na conversa; matemática discreta, redes, requisitos, testes, segurança, interfaces e outras matérias de uma graduação completa podem ser adicionadas numa segunda fase após a leitura do PPC integral.
