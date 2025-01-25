# Engenharia de Prompt do Claude: Usando Tags para Interações Aprimoradas

## Introdução

Vamos aprender sobre uma coisa muito legal chamada "Engenharia de Prompt". Imaginem que vocês têm um robô superinteligente chamado Claude, e vocês querem que ele faça coisas por vocês, como escrever histórias, criar jogos ou até mesmo ajudar com o dever de casa. Mas, para isso, vocês precisam saber como "conversar" com o Claude do jeito certo.

Essa "conversa" é o que chamamos de "prompt". E para deixar nossos prompts ainda melhores, nós vamos usar umas coisinhas chamadas "tags". Elas são como palavras mágicas que ajudam o Claude a entender exatamente o que a gente quer.

## O que são Tags?

Tags são como etiquetas que colocamos nas nossas instruções para o Claude. Elas têm um formato especial, como este aqui:

`<nomedatag> Alguma coisa aqui dentro </nomedatag>`

Parece complicado? Não se preocupem, é mais fácil do que parece. Vamos entender melhor para que serve cada parte:

1. `<nomedatag>`: Isso aqui é como a gente "abre" a nossa etiqueta. A gente coloca o nome da tag entre esses sinais de "menor que" e "maior que".
2. `Alguma coisa aqui dentro`: Aqui é onde a gente escreve o que a gente quer que o Claude faça, ou alguma informação importante para ele.
3. `</nomedatag>`: Isso aqui é como a gente "fecha" a nossa etiqueta. É quase igual ao primeiro, mas tem uma barrinha "/" antes do nome da tag.

Essas tags ajudam a organizar nossas conversas com o Claude e a dizer para ele o que é mais importante.

## Deixando o Claude Superpoderoso!

Agora que já sabemos o que são tags, vamos aprender como usá-las para deixar o Claude ainda mais inteligente e fazer coisas incríveis!

### Princípios para Conversar Bem com o Claude

Antes de começarmos a usar as tags, é importante termos em mente algumas dicas para conversar bem com o Claude:

#### 1. Seja Claro e Específico

Quando você pede alguma coisa para o Claude, é importante ser bem claro e dizer exatamente o que você quer. É como quando você pede um sorvete: você não diz só "me dá um sorvete", você diz "me dá um sorvete de chocolate com cobertura de morango e granulado, por favor".

*   **Exemplo ruim**: "Escreva uma história"
*   **Exemplo bom**: "Escreva uma história sobre um cachorro astronauta que vai para Marte e faz amizade com um alienígena"

#### 2. Dê Contexto

Contexto é como contar uma fofoca completa. Você não chega e fala só o final, você conta tudo desde o começo para a pessoa entender bem. Com o Claude é a mesma coisa. Dê todas as informações importantes para ele entender o que você quer.

*   **Exemplo ruim**: "Crie um jogo"
*   **Exemplo bom**: "Crie um jogo de plataforma 2D onde o jogador é um gato que precisa coletar moedas e evitar obstáculos para chegar ao final da fase"

#### 3. Diga o que Você Espera

É importante dizer para o Claude como você quer que ele te responda. É como quando você faz uma pergunta para alguém e espera uma resposta de um certo tipo.

*   **Exemplo ruim**: "Me fale sobre carros"
*   **Exemplo bom**: "Me dê uma lista com 5 modelos de carros elétricos populares, incluindo o nome do fabricante, o ano de lançamento e a autonomia da bateria"

#### 4. Fale das Regras

Se você tem alguma regra ou limitação, é importante contar para o Claude. É como quando você está brincando de um jogo que tem regras específicas.

*   **Exemplo ruim**: "Escreva um poema"
*   **Exemplo bom**: "Escreva um poema com 4 estrofes, cada uma com 4 versos, e que rime o segundo verso com o quarto verso de cada estrofe"

### Organizando Pedidos Complexos

Às vezes, a gente quer pedir coisas mais complicadas para o Claude. Nesses casos, a gente pode usar as tags para organizar melhor o nosso pedido.

#### Exemplo: Criando uma Estratégia de Marketing

Imaginem que vocês têm uma loja de brinquedos e querem que o Claude ajude vocês a criar uma estratégia de marketing. Vocês podem usar as tags assim:

```xml
<context>
Tarefa principal: Criar uma estratégia de marketing para minha loja de brinquedos
Recursos disponíveis: R$ 10.000 de orçamento, prazo de 2 meses
Público-alvo: Crianças de 5 a 10 anos e seus pais
</context>

<instructions>
1. Primeiro, analise o público-alvo e seus interesses
2. Depois, sugira canais de divulgação (ex: redes sociais, TV, escolas)
3. Por fim, crie um plano de gastos para o orçamento disponível
</instructions>
```

Viram só? A gente usou a tag `<context>` para explicar a situação para o Claude e a tag `<instructions>` para dizer o passo a passo do que a gente quer que ele faça.

### Melhorando aos Poucos

A gente não precisa fazer tudo de uma vez. A gente pode ir conversando com o Claude e melhorando as coisas aos poucos. É como construir uma torre de blocos de montar: a gente vai colocando um bloquinho de cada vez até a torre ficar bem alta e bonita.

#### Exemplo: Criando um Personagem

1. **Primeiro, a gente dá uma ideia geral**:
    ```xml
    <instructions>Crie um personagem para uma história em quadrinhos</instructions>
    ```
2. **Depois, a gente pede para melhorar**:
    ```xml
    <instructions>
    Agora, dê mais detalhes sobre a aparência física desse personagem
    </instructions>
    ```
3. **A gente pode pedir coisas novas**:
    ```xml
    <instructions>
    Crie uma história de origem para esse personagem
    </instructions>
    ```
4. **E também podemos pedir variações**:
    ```xml
    <instructions>
    Quais seriam os poderes desse personagem se ele fosse um vilão, em vez de um herói?
    </instructions>
    ```

### Resolvendo Problemas Passo a Passo

Quando a gente tem um problema difícil, é melhor dividir ele em pedaços menores, como um quebra-cabeça. Assim fica mais fácil de resolver!

#### Exemplo: Planejando uma Viagem

Imaginem que vocês querem planejar uma viagem, mas não sabem por onde começar. Vocês podem usar a tag `<chain_of_thoughts>` (que é como o Claude chama "jeito de pensar") para organizar as ideias:

```xml
<chain_of_thoughts>
Passo 1: Definir o destino
→ Escolher um país ou cidade
→ Pesquisar sobre o clima e a melhor época para visitar
→ Verificar a necessidade de visto ou vacinas

Passo 2: Definir o orçamento
→ Estimar gastos com passagens, hospedagem, alimentação e passeios
→ Pesquisar preços e promoções
→ Definir uma quantia diária para gastar

Passo 3: Montar o roteiro
→ Listar os pontos turísticos que quer visitar
→ Organizar os passeios por dia e região
→ Pesquisar opções de transporte entre os locais

Passo 4: Fazer as reservas
→ Comprar as passagens aéreas ou de ônibus
→ Reservar a hospedagem
→ Comprar ingressos para atrações, se necessário
</chain_of_thoughts>
```

Viram como ficou mais fácil? O Claude vai usar esse "jeito de pensar" para ajudar vocês a planejarem a viagem passo a passo.

### Coisas para Evitar

Assim como tem coisas que ajudam, tem coisas que atrapalham a nossa conversa com o Claude. Vamos ver algumas delas:

#### 1. Pedidos Vagos ou Ambíguos

*   **Ruim**: "Melhore isso" (isso o quê?)
*   **Bom**: "Melhore a introdução do texto, deixando-a mais atraente para o leitor"

#### 2. Falta de Contexto

*   **Ruim**: "Revise este código" (que código? para que ele serve?)
*   **Bom**: "Revise este código Python que implementa uma função de busca binária, verificando se há erros de lógica ou de sintaxe"

#### 3. Muitas Instruções de Uma Vez

*   **Ruim**: "Escreva uma história, um poema e uma música sobre o espaço" (muita coisa ao mesmo tempo!)
*   **Bom**: Dividir em etapas, pedindo uma coisa de cada vez

### Melhores Práticas para Tarefas Complexas

Quando temos uma tarefa muito grande e complicada, podemos usar algumas estratégias para facilitar as coisas:

#### 1. Montar um Esqueleto

É como o esqueleto de um dinossauro no museu. Primeiro, a gente monta a estrutura principal e, depois, vai adicionando os detalhes.

```xml
<context>
Estou escrevendo um trabalho sobre a história da internet
</context>

<format>
1. Introdução
2. O surgimento da ARPANET
3. A criação da World Wide Web
4. A popularização da internet nos anos 90
5. A internet nos dias atuais
6. Conclusão
</format>

<instructions>
Primeiro, escreva um parágrafo para cada um desses tópicos.
Depois, revise e adicione mais informações relevantes em cada seção.
</instructions>
```

#### 2. Validar aos Poucos

É como quando a gente está cozinhando e vai provando a comida para ver se está bom de sal. A gente vai pedindo para o Claude mostrar partes do trabalho e vamos validando aos poucos.

#### 3. Pensar nas Exceções

Sempre tem alguma coisa que pode dar errado. Então, é bom pensar no que pode acontecer e como lidar com isso.

```xml
<thinking>
1. Considerar casos normais de uso do aplicativo
2. Pensar em casos extremos, como muitos usuários ao mesmo tempo
3. Planejar como lidar com erros, como falhas de conexão
4. Criar planos alternativos para situações inesperadas, como uma queda de energia
</thinking>
```

### Fazendo Perguntas Inteligentes

Saber fazer as perguntas certas é muito importante para ter uma boa conversa com o Claude.

#### 1. Perguntas para Esclarecer

*   "Você pode explicar melhor sobre \[tal coisa]?"
*   "Quais são as principais características de \[tal coisa]?"
*   "Como \[tal coisa] funciona na prática?"

#### 2. Perguntas para Melhorar

*   "Como podemos otimizar \[essa parte]?"
*   "Quais outras opções existem para \[essa parte]?"
*   "O que mudaria se a gente precisasse \[fazer tal coisa]?"

## Exemplos Práticos

Vamos ver agora alguns exemplos de como usar as tags em situações reais.

### 1. Revisão de Código

```xml
<context>
Preciso de uma revisão de código para um script Python que fiz.
O script processa dados de um arquivo CSV e calcula a média dos valores de uma coluna específica.
Estou preocupado com a performance e com possíveis erros.
</context>

<instructions>
1. Verifique a eficiência do código, especialmente no loop de leitura do arquivo.
2. Procure por erros comuns, como não tratar exceções ou não fechar o arquivo corretamente.
3. Sugira melhorias de performance, se possível.
4. Indique se o código segue as boas práticas de programação em Python (PEP 8).
</instructions>

<output>
Revisão estruturada com:
- Problemas críticos encontrados
- Sugestões de melhoria de performance
- Recomendações de boas práticas
- Exemplos de código corrigido, quando aplicável
</output>
```

### 2. Design de Sistemas

```xml
<tree_of_thoughts>
Arquitetura do Sistema
├── Interface do Usuário
│   ├── Design Responsivo
│   └── Componentes Reutilizáveis
├── Camada de Aplicação
│   ├── API RESTful
│   └── Autenticação e Autorização
└── Camada de Dados
    ├── Banco de Dados SQL
    └── Sistema de Cache
</tree_of_thoughts>

<chain_of_thoughts>
Processo de Design
→ Coletar requisitos
→ Identificar componentes principais
→ Desenhar interfaces entre componentes
→ Planejar a implementação
</chain_of_thoughts>
```

## Dicas para Desenvolvimento Iterativo

Desenvolvimento iterativo é como esculpir uma estátua. Você começa com um bloco de pedra e vai tirando pedacinhos e ajustando até chegar na forma final.

### 1. Começar do Geral para o Específico

*   Primeiro, pense no conceito geral
*   Depois, vá detalhando cada parte
*   Ajuste cada elemento individualmente
*   Confira se tudo está de acordo com o que você queria no início

### 2. Usar Ciclos de Feedback

*   Peça revisões intermediárias
*   Confirme se o que está sendo feito é o que você imaginou
*   Teste as coisas que podem dar errado
*   Ajuste o que for necessário com base no que você aprendeu

### 3. Documentar a Evolução

```xml
<context>
Versão atual: 1.2
Feedback anterior: O processo de login está confuso para novos usuários
Objetivo: Simplificar o fluxo de login, reduzindo o número de etapas
</context>

<thinking>
1. Analisar o fluxo de login atual
2. Identificar etapas desnecessárias ou redundantes
3. Propor um novo fluxo simplificado
4. Testar o novo fluxo com usuários reais
</thinking>
```

## Detalhamento das Tags

Agora que já vimos vários exemplos, vamos entender melhor cada uma das tags que aprendemos?

### 1. Tag de Pensamento (`<thinking>` ou `<thinking>`)

**Para que serve**: Para mostrar para o Claude como ele deve organizar o pensamento dele para resolver um problema.

**Como usar**:

```xml
<thinking>
1. Primeiro, preciso entender bem o problema
2. Depois, devo considerar diferentes soluções
3. Por fim, escolho a melhor solução e explico o porquê
</thinking>
```

**Melhores práticas**:

*   Usar passos numerados para problemas complexos
*   Dividir o problema em partes menores
*   Mostrar o raciocínio, principalmente em problemas de lógica ou matemática

### 2. Tag de Saída (`<output>` ou `<output>`)

**Para que serve**: Para dizer para o Claude como ele deve formatar a resposta dele.

**Formatos suportados**:

1. **JSON**: Para dados estruturados, como uma lista de objetos
    
    ```xml
    <output>
    {
      "formato": "json",
      "campos": ["nome", "idade", "profissao"],
      "estilo": "compacto"
    }
    </output>
    ```
    
2. **Tabela**: Para mostrar dados em formato de tabela
    
    ```xml
    <output>
    | Nome    | Idade | Pontuação |
    |---------|-------|-----------|
    | Alice   | 25    | 95        |
    | Bob     | 30    | 88        |
    </output>
    ```
    
3. **YAML**: Outro formato para dados estruturados
    
    ```xml
    <output>
    formato: yaml
    usuario:
      nome: João da Silva
      idade: 30
      hobbies:
        - programar
        - jogar videogame
        - ler
    </output>
    ```
    
4. **CSV**: Para dados em formato de planilha
    
    ```xml
    <output>
    nome,idade,pontuacao
    Alice,25,95
    Bob,30,88
    Carlos,28,92
    </output>
    ```
    
5. **Lista Estruturada**: Para criar listas com subitens
    
    ```xml
    <output>
    1. Categoria Principal
       1.1. Subcategoria A
            - Item 1
            - Item 2
       1.2. Subcategoria B
            - Item 3
            - Item 4
    </output>
    ```
    
6. **Bloco de Código**: Para mostrar código-fonte
    
    ```xml
    <output>
    ```python
    def calcular_media(numeros):
        soma = sum(numeros)
        quantidade = len(numeros)
        return soma / quantidade
    ```
    </output>
    ```
    
7. **Template de Documento**: Para criar um modelo de documento
    
    ```xml
    <output>
    Título: Relatório do Projeto
    Autor: [Seu Nome]
    Data: [Data Atual]

    Resumo Executivo:
    [Resumo do Projeto]

    1. Introdução
    2. Metodologia
    3. Resultados
    4. Conclusões
    </output>
    ```
    
8. **XML**: Para dados estruturados (sim, XML dentro de XML!)
    
    ```xml
    <output>
    <usuario>
        <nome>Maria</nome>
        <idade>28</idade>
        <habilidades>
            <habilidade>HTML</habilidade>
            <habilidade>CSS</habilidade>
        </habilidades>
    </usuario>
    </output>
    ```
    
9. **Pares Chave-Valor**: Para dados simples, como configurações
    
    ```xml
    <output>
    Nome: Ana
    Idade: 35
    Cidade: São Paulo
    Status: Ativo
    Último Login: 2024-03-15
    </output>
    ```
    
10. **Formato Customizado**: Para criar seu próprio formato
    
    ```xml
    <output format="custom">
    [Início do Relatório]
    ======================
    Título: {titulo}
    Data: {data}
    Conteúdo: {conteudo}
    ======================
    [Fim do Relatório]
    </output>
    ```
    

**Melhores práticas**:

*   Definir estruturas de dados claras
*   Especificar requisitos de formatação
*   Incluir regras de validação, se necessário
*   Usar formatação consistente dentro de cada tipo de saída
*   Incluir dados de exemplo para formatos complexos
*   Especificar caracteres especiais ou delimitadores
*   Considerar a legibilidade e a facilidade de processamento

### 3. Tag de Contexto (`<context>` ou `<context>`)

**Para que serve**: Para dar informações de base ou definir o cenário para o Claude.

**Como usar**:

```xml
<context>
Você está escrevendo um guia de estudos para alunos do ensino médio.
O público tem conhecimentos básicos de matemática, mas precisa de explicações claras e simples.
O assunto é geometria básica, especificamente triângulos.
</context>
```

**Melhores práticas**:

*   Ser específico sobre o público-alvo
*   Incluir informações de base relevantes
*   Definir restrições ou premissas

### 4. Tag de Formato (`<format>` ou `<format>`)

**Para que serve**: Para definir a estrutura geral da resposta do Claude.

**Como usar**:

```xml
<format>
1. Título
2. Resumo (máximo de 50 palavras)
3. Pontos Principais (3 a 5 bullets)
4. Análise Detalhada
5. Recomendações
</format>
```

**Melhores práticas**:

*   Fornecer uma estrutura clara
*   Incluir requisitos de tamanho, se necessário
*   Especificar necessidades especiais de formatação

### 5. Tag de Tom (`<tone>` ou `<tone>`)

**Para que serve**: Para definir o estilo de escrita e a "voz" do Claude.

**Como usar**:

```xml
<tone>
Profissional, mas acessível. Use uma linguagem simples, mas mantenha a precisão técnica.
Evite jargões desnecessários e explique termos técnicos quando forem usados.
</tone>
```

**Melhores práticas**:

*   Ser específico sobre o nível de formalidade
*   Definir restrições de estilo
*   Especificar a complexidade da linguagem

### 6. Tag de Exemplo (`<example>` ou `<example>`)

**Para que serve**: Para mostrar ao Claude um exemplo do que você quer, ou do que você não quer.

**Como usar**:

```xml
<example>
Boa resposta:
"A fotossíntese é o processo pelo qual as plantas convertem luz solar em energia, produzindo oxigênio como subproduto."

Má resposta:
"Fotossíntese é quando as plantas respiram."
</example>
```

**Melhores práticas**:

*   Incluir exemplos positivos e negativos
*   Ser específico e concreto
*   Mostrar o contexto, quando relevante

### 7. Tag de Instruções (`<instructions>` ou `<instructions>`)

**Para que serve**: Para dar orientações específicas sobre como o Claude deve executar a tarefa.

**Como usar**:

```xml
<instructions>
1. Revise o texto procurando por erros gramaticais e ortográficos.
2. Verifique a consistência do uso de tempos verbais.
3. Sugira melhorias de estilo para tornar o texto mais claro e conciso.
4. Indique se o texto está adequado ao público-alvo (adolescentes).
5. Forneça exemplos específicos de trechos que podem ser melhorados.
</instructions>
```

**Melhores práticas**:

*   Usar passos claros e acionáveis
*   Ser específico sobre os requisitos
*   Incluir restrições ou limitações

## Combinando Tags com Árvore de Pensamentos (Tree of Thoughts)

Árvore de Pensamentos é uma forma de resolver problemas pensando em várias possibilidades ao mesmo tempo, como os galhos de uma árvore.

**Exemplo**:

```xml
<thinking>
Deixe-me decompor isso usando a Árvore de Pensamentos:

Ramo 1: Análise de Segurança
├── Riscos de Injeção de SQL
│   ├── Validação de Entrada
│   └── Uso de Prepared Statements
└── Vulnerabilidades de XSS
    ├── Codificação de Saída
    └── Política de Segurança de Conteúdo

Ramo 2: Otimização de Performance
├── Consultas ao Banco de Dados
│   ├── Indexação
│   └── Otimização de Consultas
└── Carregamento do Frontend
    ├── Compressão de Ativos
    └── Estratégias de Cache
</thinking>

<output>
Análise detalhada para cada ramo, com recomendações específicas...
</output>
```

## Combinando Tags com Cadeia de Pensamentos (Chain of Thought)

Cadeia de Pensamentos é uma forma de resolver problemas pensando em um passo de cada vez, em sequência.

**Exemplo**:

```xml
<thinking>
Passo 1: Analisar o domínio do problema
→ O sistema lida com dados sensíveis de usuários
→ Existem múltiplos pontos de entrada para os dados

Passo 2: Identificar potenciais vulnerabilidades
→ A validação de entrada do usuário é mínima
→ Não há limitação de taxa implementada

Passo 3: Desenvolver soluções
→ Implementar validação de entrada
→ Adicionar middleware de limitação de taxa
</thinking>

<instructions>
Com base nessa análise:
1. Implemente a validação de entrada
2. Adicione a limitação de taxa
3. Teste as medidas de segurança
</instructions>
```

## Melhores Práticas para o Uso de Tags

### 1. Aninhamento

Podemos colocar tags dentro de outras tags, quando fizer sentido.

```xml
<context>
  <format>
    Documentação técnica
  </format>
  <tone>
    Profissional e preciso
  </tone>
</context>
```

### 2. Ordem

Usar as tags em uma ordem lógica:

*   Contexto primeiro
*   Pensamento/raciocínio em seguida
*   Saída/formato por último

### 3. Clareza

Manter o conteúdo das tags focado e específico.

```xml
<thinking>
Processo de pensamento claro e específico:
1. Analisar os requisitos
2. Identificar as restrições
3. Desenvolver uma solução
</thinking>
```

### 4. Consistência

Manter um formato consistente dentro das tags.

```xml
<format>
Todas as seções devem usar:
- Cabeçalhos em Markdown
- Blocos de código para exemplos
- Listas com marcadores para características
</format>
```

## Tags de Pensamento Adicionais

Além da tag `<thinking>`, temos também:

### Tag de Árvore de Pensamentos

**Uso**: `<tree_of_thoughts>...</tree_of_thoughts>`

### Tag de Cadeia de Pensamentos

**Uso**: `<chain_of_thoughts>...</chain_of_thoughts>`

## Amostra Completa: Desenvolvimento de Jogos

Vamos criar um exemplo bem completo, usando várias tags, para planejar o desenvolvimento de um jogo:

```xml
<context>
Precisamos desenvolver um jogo de plataforma 2D com tema espacial. O público-alvo são jogadores casuais entre 12 e 18 anos. O jogo deve ser desafiador, mas não frustrante, com uma curva de aprendizado que aumenta gradualmente a dificuldade.
</context>

<format>
- Documento de Design do Jogo (GDD)
- Mecânicas Principais
- Requisitos Técnicos
- Plano de Implementação
- Estratégia de Testes
</format>

<tree_of_thoughts>
Sistemas Principais do Jogo
├── Mecânicas do Jogador
│   ├── Movimento
│   │   ├── Caminhada/corrida básica
│   │   ├── Mecânica de pulo
│   │   └── Seções de gravidade zero
│   └── Habilidades
│       ├── Impulso de jetpack
│       └── Ativação de escudo
├── Design de Níveis
│   ├── Tipos de ambiente
│   │   ├── Estações espaciais
│   │   ├── Planetas alienígenas
│   │   └── Campos de asteroides
│   └── Progressão de dificuldade
│       ├── Seção de tutorial
│       ├── Níveis iniciais
│       └── Desafios avançados
└── Sistemas do Jogo
    ├── Rastreamento de pontuação
    ├── Coleta de power-ups
    └── Sistema de conquistas
</tree_of_thoughts>

<chain_of_thoughts>
Passo 1: Análise do Loop de Jogabilidade Principal
→ Jogador explora ambientes espaciais
→ Coleta power-ups e recursos
→ Supera desafios de plataforma
→ Alcança checkpoint ou fim do nível

Passo 2: Requisitos Técnicos
→ Sistema de física para gravidade variável
→ Efeitos de partículas para atmosfera espacial
→ Controles de personagem suaves
→ Detecção de colisão eficiente

Passo 3: Prioridades de Desenvolvimento
→ Prototipar movimento básico
→ Implementar mecânicas principais
→ Projetar níveis iniciais
→ Adicionar polimento e efeitos
</chain_of_thoughts>

<instructions>
1. Criar o controle básico do jogador
   - Implementar movimento horizontal
   - Adicionar mecânica de pulo
   - Desenvolver sistema de mudança de gravidade

2. Projetar blocos de construção de níveis
   - Tipos de plataforma
   - Perigos e obstáculos
   - Pontos de colocação de power-ups

3. Implementar sistemas do jogo
   - Rastreamento de pontuação
   - Sistema de vida/saúde
   - Sistema de checkpoint
   - Efeitos de power-ups

4. Criar nível de tutorial
   - Introduzir controles básicos
   - Ensinar mecânicas principais
   - Fornecer orientação clara

5. Desenvolver plano de testes
   - Testes de sensação de movimento
   - Análise da curva de dificuldade
   - Sistema de rastreamento de bugs
   - Sessões de feedback do jogador
</instructions>

<tone>
Técnico e preciso ao discutir detalhes de implementação, mas manter a acessibilidade para membros da equipe que podem não ser programadores.
</tone>

<example>
Boa descrição de implementação:
"O controle do jogador deve usar movimento baseado em física com parâmetros configuráveis para aceleração, velocidade máxima e força de pulo. Implementar uma verificação de solo usando raycasts para garantir a detecção precisa do pulo."

Má descrição de implementação:
"Fazer o jogador se mover e pular suavemente."

Boa orientação de design de níveis:
"A seção de tutorial deve introduzir as mecânicas sequencialmente: 1) movimento básico, 2) pulo, 3) jetpack, com dicas visuais claras e prompts de texto opcionais."

Má orientação de design de níveis:
"Começar com níveis fáceis e torná-los mais difíceis."
</example>

<output>
Entregas esperadas:
1. Documento de Design do Jogo (GDD)
2. Documento de especificação técnica
3. Detalhamento do planejamento de sprint
4. Modelo de documentação de testes
5. Lista de requisitos de assets
</output>
```

## Solicitando Diagramas de Pensamento

### Árvore de Pensamentos em ASCII

#### Melhor formato:

```xml
<context>
Preciso desenvolver um diagrama de Árvore de Pensamentos para [seu tópico].
Elementos-chave a considerar:
- [Listar componentes principais]
- [Listar considerações importantes]
- [Listar restrições]
</context>

<format>
Diagrama ASCII com:
- Ramos principais usando símbolos ├── e └──
- Sub-ramos indentados com espaçamento adequado
- Hierarquia clara de pensamentos
- Profundidade máxima de [número] níveis
</format>

<output>
Estrutura em árvore com:
- Descrições claras dos nós
- Indentação adequada
- Agrupamento lógico de pensamentos relacionados
</output>
```

#### Exemplo de Solicitação:

```xml
<context>
Preciso desenvolver um diagrama de Árvore de Pensamentos para construir um aplicativo de finanças pessoais.
Elementos-chave:
- Recursos principais
- Experiência do usuário
- Requisitos técnicos
- Considerações de segurança
</context>

<format>
Diagrama ASCII com:
- Ramos principais para cada elemento-chave
- Sub-ramos para componentes específicos
- Profundidade máxima de 3 níveis
- Relações claras entre os elementos
</format>

<output>
Aplicativo de Finanças Pessoais
├── Recursos Principais
│   ├── Rastreamento de Despesas
│   │   ├── Entrada Manual
│   │   └── Digitalização de Recibos
│   └── Gerenciamento de Orçamento
│       ├── Configuração de Categorias
│       └── Sistema de Alertas
└── Experiência do Usuário
    ├── Design de Interface
    │   ├── Mobile First
    │   └── Acessibilidade
    └── Fluxo do Usuário
        ├── Onboarding
        └── Uso Diário
</output>
```

### Cadeia de Pensamentos em ASCII

#### Melhor formato:

```xml
<context>
Preciso desenvolver um diagrama de Cadeia de Pensamentos para [seu processo].
Etapas sequenciais devem incluir:
- [Listar etapas principais]
- [Listar dependências]
- [Listar pontos de decisão]
</context>

<format>
Diagrama ASCII com:
- Etapas sequenciais usando setas → ou ⟶
- Descrições claras das etapas
- Pontos de decisão marcados
- Caminhos de ramificação opcionais
</format>

<output>
Fluxo sequencial com:
- Etapas numeradas
- Progressão lógica
- Conexões claras
</output>
```

#### Exemplo de Solicitação:

```xml
<context>
Preciso desenvolver um diagrama de Cadeia de Pensamentos para o processo de autenticação do usuário.
Etapas sequenciais incluindo:
- Tentativa de login
- Validação
- Verificações de segurança
- Concessão de acesso
</context>

<format>
Diagrama ASCII mostrando o processo passo a passo com setas e pontos de decisão
</format>

<output>
Fluxo de Autenticação do Usuário
Etapa 1: Tentativa de Login
→ Usuário insere credenciais
  → Validar formato de entrada
    → Verificar no banco de dados
      → [Ponto de Decisão]
        ├── Sucesso → Conceder acesso
        └── Falha → Tratamento de erros
          → Opções de nova tentativa ou redefinição
</output>
```

### Dicas para Melhores Resultados:

1. **Seja Específico**:
    *   Declare claramente o tópico ou processo
    *   Defina a profundidade desejada
    *   Especifique preferências de formatação
2. **Forneça Contexto**:
    *   Inclua informações básicas relevantes
    *   Mencione requisitos específicos
    *   Destaque considerações importantes
3. **Defina a Estrutura**:
    *   Especifique os níveis máximos de profundidade
    *   Indique se certos ramos precisam de mais detalhes
    *   Mencione qualquer agrupamento ou categorização necessária
4. **Solicite Formatação**:
    *   Peça caracteres ASCII específicos, se preferir
    *   Especifique preferências de indentação
    *   Mencione necessidades especiais de notação
5. **Considere a Legibilidade**:
    *   Solicite espaçamento adequado
    *   Peça rótulos claros
    *   Especifique se certos elementos precisam de ênfase

### Exemplo de Solicitação Combinada:

```xml
<context>
Preciso de diagramas de Árvore e Cadeia de Pensamentos para desenvolver um novo recurso de produto.
O processo deve cobrir tanto a decomposição de componentes quanto as etapas sequenciais de implementação.
</context>

<format>
Forneça ambos:
1. Diagrama em árvore mostrando os componentes do recurso
2. Diagrama em cadeia mostrando a sequência de implementação
Use formatação ASCII clara e indentação adequada
</format>

<output>
[A Árvore de Pensamentos será exibida aqui]

[A Cadeia de Pensamentos será exibida aqui]
</output>

<instructions>
Por favor, garanta:
- Conexão clara entre os componentes da árvore e as etapas da cadeia
- Fluxo lógico entre os elementos
- Indentação e formatação adequadas
- Rótulos e descrições legíveis
</instructions>
