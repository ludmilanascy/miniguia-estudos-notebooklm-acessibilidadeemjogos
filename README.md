# miniguia-estudos-notebooklm-acessibilidadeemjogos
**(EM CONSTRUÇÃO)** Repositório público criado como Desafio de Projeto do Bootcamp "Do Prompt ao Agente" da Dio em parceria com a CI&amp;T em abril de 2026

### Contexto e Objetivos: 

O objetivo deste repositório é mapear uma forma de estudar acessibilidade em jogos no NotebookLM, uma ferramenta da Google.

**OBJETIVO PRINCIPAL**
- Trazer elementos para se fazer de um NotebookLM um auxiliar no processo de consulta de guias de acessbilidade para jogos, facilitando a consulta durante game jams.
  
**OBJETIVOS SECUNDÁRIOS**
- Indicar uma boa curadoria de fontes confiáveis no assunto, em especial em lingua portuguesa;
- Sugerir prompts estratégicos para efetuar consulta de forma qualificada, usando como exemplo base um jogo no estilo visual novel;
- Identificar pontos sensíveis de atenção de possíveis vieses da IA, afim de extrair dela a melhor resposta;
- Elaborar um Miniguia de Estudo contendo: resumo, glossário e conjunto de prompts reutilizáveis para apoiar futuras revisões.
  
### Curadoria de Fontes Iniciais: 

- **Game Accessibility Guidelines** :
  https://gameaccessibilityguidelines.com/

- **Proposta de Diretrizes para Acessibilidade em Jogos Digitais** : https://sol.sbc.org.br/index.php/sbgames/article/download/32301/32098/#:~:text=Game%20accessibility%20guidelines%20for%20people,4%20de%20Janeiro%20de%202023.

- **Link da Documentaçao da engine que se está utilizando. No nosso exemplo de gênero visual novel, Ren'Py**:  https://www.renpy.org/doc/html/index.html

### Engenharia de Prompts e "Cicatrizes": 
#### **TESTE 01 - PROMPT BASE**: 
"Liste a melhor estratégia para fazer um jogo digital estilo visual novel na engine Ren'Py com o máximo possível de acessibilidade durante uma game jam que dura 48 horas.
- **RESPOSTA DO NOTEBOOK LM COM AS TRêS FONTES INICIAIS**
"Para criar um jogo no estilo Visual Novel no Ren'Py com foco total em acessibilidade em apenas 48 horas, a estratégia deve focar em utilizar os recursos nativos da engine e implementar diretrizes práticas que minimizem barreiras para jogadores com deficiências visuais e auditivas
.
Aqui está o plano de ação dividido por áreas críticas:
1. **Fundação e Fluxo de Trabalho Rápido (0-6h)**
- **Ren'Py Launcher**: Utilize o sistema de Quickstart para criar o esqueleto do jogo, definindo personagens, imagens básicas e a estrutura de Labels e Controle de Fluxo
- **Interface Pronta**: Use o guia de Customização de GUI para garantir que o menu e as caixas de diálogo já nasçam com alto contraste e fontes legíveis
- **Salvamento e Rollback**: Não gaste tempo programando sistemas de save; o Ren'Py já fornece nativamente Saving, Loading e Rollback (voltar o texto), o que é essencial para jogadores que precisam reler informações no seu próprio ritmo.
  
2. **Acessibilidade Visual (6-30h)**
- **Legibilidade de Texto**: Utilize fontes simples e de tamanho grande por definição, Garanta um forte contraste entre a cor do texto e o fundo da caixa de diálogo
- **Amostragem de Texto**: Evite textos excessivamente longos em uma única tela e utilize caixas de diálogo claras que identifiquem quem está falando
- **Self-Voicing**: Este é o maior trunfo do Ren'Py para acessibilidade. Certifique-se de que o jogo seja compatível com a função Self-Voicing, que lê o texto para jogadores cegos ou com baixa visão.
- **Ajustes de Imagem**: Se possível, adicione opções simples para ajustar brilho e contraste no menu de preferências, ajudando jogadores com baixa visão ou daltonismo
.
3. **Acessibilidade Auditiva e Canais Adicionais (30-40h)**
- **Controle de Áudio Granular**: Configure o menu de preferências para permitir que o usuário ajuste volumes separadamente para Música, Efeitos Sonoros (SFX) e Vozes. Isso permite que jogadores com baixa audição destaquem as vozes sobre a música
- **Legendas Descritivas**: Além dos diálogos, use o texto para descrever sons importantes (ex: [Porta rangendo]), fornecendo canais adicionais de informação para quem não pode ouvir o áudio.
- **Dicas Visuais**: Sempre que houver uma informação sonora crucial para o progresso, acompanhe-a de um alerta visual ou mudança na interface.
  
4. **Gameplay e Documentação (40-48h)**
- **Controles Simplificados**: O Ren'Py permite o uso de mouse, teclado ou controle. Ofereça a opção de remapeamento de botões para jogadores com deficiências motoras.
- **Modo de Alternância**: Use as preferências para permitir que ações que exigiriam "segurar" um botão sejam feitas com um simples "clique para ativar/desativar".
- **Tutorial e Ajuda**: Inclua uma tela de Documentação ou Tutorial acessível logo no início, explicando como ativar os recursos de acessibilidade e os comandos básicos
- **Builds de Distribuição**: Use as ferramentas de build do Ren'Py para gerar versões para múltiplas plataformas (Windows, Mac, Web), garantindo que o hardware do usuário não seja uma barreira
- **Dica de Ouro para Game Jams**: Priorize o que é "Básico" e de fácil implementação. O uso correto do Self-Voicing e a escolha de fontes legíveis com alto contraste já colocarão seu jogo à frente em termos de inclusão"

#### Pontos de atenção (troubleshottings)
- "A melhor estratégia" é relativo, subjetivo. Descrever melhor para a I.A.
- As fontes iniciais estão priorizando apenas deficiência visual e auditivia. Diversificar outras questões de acessibilidade.

### Miniguia de Estudo: 

#### RESUMO DO REPOSITÓRIO

Esse repositório é um exercício do bootcamp "Do prompt até o agente" da Dio em parceria com a CI&T que consiste em aplicar os conhecimentos aprendidos sobre a ferramenta do Google "notebookLM" a um assunto de interesse do estudante: no caso, um guia de consulta mais prático e rápido sobre acessibilidade em jogos digitais aplicados a um gênero de game chamado visual novel. Usou-se como base 3 fontes iniciais, sendo 2 delas guias internacionais e nacionais de acessibilidade em jogos digitais e 1 a documentação da engine de jogos escolhida para a criação do jogo. Em seguida, sugeriu-se um prompt inicial em que pedidos ao notebookLM descrever a melhor estratégia de implementação de recursos acessíveis em jogos de visual novel baseado na fonte e no limite de tempo de uma game jam tradicional de 48 horas. Para finalizar, relatou-se pontos sensíveis do prompt, além de concluir com um resumo do repositório, glossário da área estudada e uma lista de sugestão de prompts relacionados ao tema.

#### GLOSSÁRIO DO TESTE 01 DE PROMPT BASE

**Conceitos de Desenvolvimento (Ren'Py)**

- **Ren'Py**: Uma engine de código aberto focada na criação de Visual Novels e jogos baseados em narrativa.
- **Quickstart**: Um guia e conjunto de ferramentas iniciais do Ren'Py que permite configurar rapidamente os elementos básicos de um jogo, como personagens, imagens e transições.
- **Labels & Control Flow**: O sistema que organiza o roteiro do jogo; as "labels" marcam pontos na história, e o "control flow" gerencia como o jogador navega por elas.
- **GUI Customization**: O processo de personalizar a Interface Gráfica do Usuário, permitindo alterar cores, fontes e o layout de menus e caixas de diálogo.
- **Rollback**: Funcionalidade nativa que permite ao jogador voltar o texto para revisar diálogos ou escolhas anteriores
- **Builds de Distribuição**: O processo final de compilar o jogo para diferentes plataformas, como Windows, Mac, Linux, Android e Web/HTML5

**Conceitos de Acessibilidade**

- **Self-Voicing**: Recurso nativo do Ren'Py que utiliza síntese de voz para ler o texto na tela, essencial para jogadores cegos ou com baixa visão.
- **Alto Contraste** : Diretriz visual que recomenda uma diferença nítida entre a cor do texto e o fundo para facilitar a leitura por pessoas com baixa visão ou daltonismo.
- **Amostragem de Texto**: Refere-se à apresentação de informações textuais em elementos como caixas de diálogo e menus, devendo focar na legibilidade e clareza.
- **Canais Adicionais de Informação**: A estratégia de fornecer a mesma informação por múltiplos sentidos (ex: um alerta que é visual e sonoro ao mesmo tempo) para garantir que jogadores com deficiências sensoriais recebam o conteúdo.
- **Legendas Descritivas**: Além dos diálogos, são textos que descrevem efeitos sonoros e música (ex: [Música tensa toca]), permitindo que jogadores com deficiência auditiva compreendam o contexto sonoro.
- **Ajuste de Som Granular**: A opção de controlar o volume de diferentes fontes (música, vozes, efeitos) separadamente, ajudando jogadores a destacar informações auditivas cruciais.

#### **(EM CONSTRUÇÃO)** Um conjunto de prompts reutilizáveis que possam apoiar futuras revisões sobre o tema.

##### **Diretrizes na Criação de um bom prompt**
Fonte: https://elidianaandrade.gitbook.io/cursos/introducao-a-engenharia-de-prompts/visao-geral-da-engenharia-de-prompts/elementos-essenciais-de-um-bom-prompt

- **Instrução Inicial**: é a tarefa específica que você deseja que o modelo realize. Deve ser direta e sem ambiguidade para evitar interpretações erradas.
- **Contexto Adequado**: fornece informações adicionais que ajudam o modelo a entender melhor a tarefa e a produzir uma resposta mais precisa e relevante.
- **Exemplos**: ajudam a orientar o modelo sobre o formato ou estilo da resposta desejada. Eles podem ser usados para ilustrar como a tarefa deve ser realizada ou para fornecer uma referência clara.
- **Dados de Entrada**:  são as informações ou o problema específico que o modelo deve processar ou resolver. Pode ser uma pergunta, uma situação ou um texto que precisa ser analisado ou trabalhado.
- **Formato de Saída**: especifica o que é esperado da resposta do modelo em termos de comprimento, detalhes ou tipo de formato.

##### **POSSÍVEIS PROMPTS SEGUNDO AS DIRETRIZES DESCRITAS ACIMA**

- "Sugira um passo a passo de como aplicar acessibilidade em jogos digitais em (insira aqui o gênero do jogo) na engine (insira aqui a engine, não esquecendo de colocar a documentação da mesma como uma fonte para o notebookLM) considerando o tempo reduzido de uma game jam que dura 48 horas. Tente abordar o máximo de possíveis deficiências além da auditiva e da visual nesse curto espaço de produção de um jogo digital, considerando que ele está sendo feito por (insira aqui o número de membros da sua equipe) pessoas na equipe nas funçoes (liste as funções da sua equipe: arte 2d, programação, música, UI, roteiro). Siga os exemplos dos jogos acessíveis (nomear os jogos de referência), que possuem (listar as característica de acessibilidade do jogo de referência). Como você avalia o que é possível fazer no intervalo de tempo de produção levando em conta as habilidades (listar habilidades de cada pessoa da equipe) reunidas nessa game jam? Documente em um formato adaptado para ser inserido num Game Design Document que será lido por todos da equipe. Em seguida, faça no formato checklist para ser adicionado como tarefa de gerenciamento de equipe (especificar o app de gerenciamento de equipe. Ex.: Trello)".

- "Restahdo X horas para o final dessa game jam, faça uma lista de prioridades para garantir a acessiblidade do jogo em produção considerando os seguintes critérios: (listar os critérios prioritários). Documente em um formato adaptado para ser inserido em um Game Design Document. Em seguida, faça no formato checklist para ser adicionado como tarefa de gerenciamento de equipe (especificar o app de gerenciamento de equipe. Ex.: Trello)" 
