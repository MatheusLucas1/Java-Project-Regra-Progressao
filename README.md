# Java-Project-Regra-Progressao

# Regra de Progressão

Boas-vindas ao repositório do projeto `Regra de Progressão`.  


   <summary><strong>‼ Como Fazer a instalação </strong></summary>

1. Clone o repositório

- Use o comando: `git clone <url do repositório>`
- Entre na pasta do repositório que você acabou de clonar:
    - `cd <nome do repositório>`

2. Instale as dependências

    - `mvn install`

<details>
  <summary>👨‍💻 O que foi desenvolvido</summary><br />

Descubra seu caminho para o sucesso com a Trybe!

Na Trybe, uma escola inovadora, nossas avaliações são conduzidas em períodos de 21 dias, repletos de desafios e oportunidades de aprendizado. Cada período é composto de uma variedade de seções instigantes, abrangendo conteúdos teóricos e atividades práticas que avaliam o seu progresso. Projetos empolgantes, exercícios envolventes, quizzes instigantes e atividades de carreira, além de propor situações reais de mercado para o desenvolvimento de habilidades pessoais, compõem a trilha para o seu crescimento profissional.

A cada período, o objetivo da pessoa estudante é alcançar 85% dos pontos adiquiridos nas atividades avaliativas. Cada uma dessas atividades vale até 100%, porém cada atividade com um peso diferente. Isto é, a nota final é uma média ponderada de todas as atividades avaliativas do período. É com essa pontuação que você avança na formação, alcançando novos patamares de conhecimento e habilidades.

Ao final de cada período, duas possibilidades se abrem diante de você: a Aprovação ou a Reprovação. Seu desempenho determinará qual caminho seguir. Atingindo a pontuação mínima exigida para o período, você conquista a Aprovação, avançando para o próximo período e prosseguindo com sua turma. É um passo à frente em direção ao seu sucesso!

Porém, caso não alcance a pontuação mínima, não se preocupe! A Reprovação não é um obstáculo, mas uma oportunidade de aprimoramento. Você poderá refazer o mesmo período na próxima turma disponível, fortalecendo seus conhecimentos e suas habilidades até alcançar a Aprovação desejada.

E agora, a grande novidade! Para facilitar sua jornada e auxiliar na gestão das atividades avaliativas, iremos implementar um programa em Java com uma interface intuitiva no terminal, que permitirá:

a. Cadastrar atividades avaliativas para o período, seja exercícios ou projetos. Assim, você terá um controle completo sobre suas tarefas e metas.

b. Inserir as notas dos exercícios e projetos cadastrados para o período. O programa calculará automaticamente o percentual alcançado, revelando seu desempenho de forma nítida e objetiva.

c. Com base no percentual alcançado, você descobrirá se foi aprovado ou reprovado. A mágica acontece quando você supera o limite de 85%. É a sua passagem para o próximo período, uma conquista a ser comemorada!

Chegou a hora de embarcar nesse projeto desafiador e inspirador na Trybe! O programa em Java será seu aliado nessa caminhada, tornando seu aprendizado ainda mais dinâmico e empolgante.

Prepare-se para abraçar o futuro e transformar sua vida. Aventure-se, aprenda e alcance o sucesso com a gente!

</details>


## Requisitos do projeto

### 1 - Cadastrar atividades avaliativas

<details>
  <summary>Descrição</summary><br />

Como regra de negócio, você deve permitir à pessoa estudante que cadastre as atividades avaliativas para o período atual, que podem ser do tipo exercícios ou projetos. Cada atividade deve ter um nome descritivo que identifique sua natureza e um peso atribuída a ela.
Certifique-se de que a pessoa estudante possa cadastrar quantas atividades forem necessárias, para que todas sejam levadas em consideração no cálculo do percentual alcançado. É necessário que a soma de todos os pesos atinga o valor de 100.

Por exemplo, digamos que temos três atividades avaliativa em um dado período. O exercício alfa com peso 30, o exercício beta com peso 10 e o projeto gama com peso 60. Note que o somatório de todos os pesos (30+10+60) precisa, necessariamente, ser 100. Digamos que uma pessoa estudante atingiu a nota de 65 para o exercício alfa, 100 para o exercício beta e 93 no projeto gama, com isso o cálculo da nota final do período faz se:

$` {(30*65) + (10*100) + (60*93)\over(30+10+60)} = 85,3 `$

Assim, a nota dessa pessoa estudante no período foi de 85,3%.

A fórmula é:

$` {(Peso1*Nota1) + (Peso2*Nota2) + ... + (PesoN*NotaN)\over(Peso1 + Peso2 + ... + PesoN)} = NotaFinal `$

O programa deve seguir as seguintes regras:

- Exibir a mensagem `Digite a quantidade de atividades para cadastrar: ` para saber quantas atividades serão cadastradas para o período e salvar essa informação.
- Dado o número de atividades, repetir as mensagens `Digite o nome da atividade N: ` e `Digite o peso da atividade N:`  para salvar o nome da atividade e seu respectivo peso, sendo N o número da atividade.

_**Nota: As mensagens devem ser EXATAMENTE iguais como sugerido, caso contrario os testes irão falhar**_

Exemplo:

```bash
Digite a quantidade de atividades para cadastrar:
3
Digite o nome da atividade 1:
Projeto Lista de Tarefas
Digite o peso da atividade 1: 
30
Digite o nome da atividade 2:
Projeto Lista de Compras
Digite o peso da atividade 2: 
30
Digite o nome da atividade 3:
Projeto Jogo de Advinhação
Digite o peso da atividade 3: 
40
```

</details>

---

### 2 - Inserir as notas obtidas

<details>
  <summary>Descrição</summary><br />

Para cumprir este requisito, a pessoa estudante precisa ter a capacidade de inserir as notas obtidas em cada exercício ou projeto onde acabou de cadastrar seu nome e peso para o período em questão. Essas notas devem ser armazenadas para posteriormente às atividades correspondentes. Certifique-se de que o programa permita a inserção das notas de forma nítida e intuitiva, para que a pessoa estudante possa registrar sua pontuação em cada atividade avaliativa.

Em outras palavras:

- Repita para cada atividade cadastrada no período a mensagem `Digite a nota obtida para [Nome da Atividade]:` para obter sua respectiva nota.

Exemplo, continuando o exemplo anterior:

```bash
Digite a quantidade de atividades para cadastrar:
3
Digite o nome da atividade 1:
Projeto Lista de Tarefas
Digite o peso da atividade 1: 
30
Digite a nota obtida para Projeto Lista de Tarefas:
22
Digite o nome da atividade 2:
Projeto Lista de Compras
Digite o peso da atividade 2: 
30
Digite a nota obtida para Projeto Lista de Compras:
30
Digite o nome da atividade 3:
Projeto Jogo de Advinhação
Digite o peso da atividade 3: 
40
Digite a nota obtida para Projeto Jogo de Advinhação:
35
```

</details>

---

### 3 - Informar o resultado alcançado

<details>
  <summary>Descrição</summary><br />

A fim de avaliar o desempenho da pessoa estudante, é necessário calcular o percentual alcançado com base nas notas obtidas nas atividades avaliativas cadastradas. Após inserir todas as notas, o programa deve realizar o cálculo automático do percentual alcançado, considerando o peso de cada atividade. Em seguida, compare esse percentual com o valor de referência de 85%. Se o percentual for menor que 85%, a pessoa estudante será considerada reprovada. Caso contrário, com um percentual igual ou superior a 85%, ela será aprovada.

Em outras palavras:

- Após calcular o resultado considerando a nota de todas as atividades, utilize a mensagem:
- `Parabéns! Você alcançou [resultado]%! E temos o prazer de informar que você obteve aprovação!`; ou
- `Lamentamos informar que, com base na sua pontuação alcançada neste período, [resultado]%, você não atingiu a pontuação mínima necessária para sua aprovação.

Exemplos:

```bash
Parabéns! Você alcançou 87%! E temos o prazer de informar que você obteve aprovação! 
```

```bash
Lamentamos informar que, com base na sua pontuação alcançada neste período, 70%, você não atingiu a pontuação mínima necessária para sua aprovação.
```

</details>

---

