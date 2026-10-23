# Manual Completo de Diretrizes de Legendagem — Timed Text Style Guide (TTSG)

> **Documento Oficial de Referência Técnica e Editorial para Streaming**  
> Compilação integral das diretrizes globais (*General Requirements*), temporização (*Subtitle Timing Guidelines*), legendagem para surdos e ensurdecidos (*SDH*), narrativas forçadas (*Forced Narratives*) e especificações locais para Português Brasileiro (*Portuguese - Brazil Timed Text Style Guide*).

---

## Sumário

1. [Filosofia Central: Leitura Invisível no Streaming](#1-filosofia-central-leitura-invisível-no-streaming)
2. [Parâmetros Técnicos Universais (General Requirements)](#2-parâmetros-técnicos-universais-general-requirements)
   - 2.1 Limites de Linhas e Caracteres
   - 2.2 Duração Mínima e Máxima
   - 2.3 Velocidade de Leitura (CPS - Characters Per Second)
   - 2.4 Intervalo Mínimo Entre Legendas (Gap de Frames)
   - 2.5 Formatos de Arquivo e Codificação
   - 2.6 Lista de Caracteres Permitidos (Glyph List)
3. [Posicionamento e Alinhamento na Tela](#3-posicionamento-e-alinhamento-na-tela)
   - 3.1 Alinhamento Padrão
   - 3.2 Reposicionamento para o Topo
   - 3.3 Conflito com Textos Queimados na Imagem (Burn-ins)
   - 3.4 Área de Segurança (Safe Area)
4. [Temporização e Cortes de Câmera (Subtitle Timing Guidelines)](#4-temporização-e-cortes-de-câmera-subtitle-timing-guidelines)
   - 4.1 Sincronia com o Áudio (Waveform)
   - 4.2 Interação com Cortes de Plano (Shot Changes)
   - 4.3 A Regra dos 12 Frames (Meio Segundo a 24 fps)
   - 4.4 Travessia de Cortes de Plano (Crossing Shot Changes)
   - 4.5 Hierarquia: Taxa de Leitura vs. Cortes de Câmera
5. [Morfossintaxe e Quebra de Linha (Line Breaks)](#5-morfossintaxe-e-quebra-de-linha-line-breaks)
   - 5.1 Princípio da Pirâmide Invertida (Bottom-Heavy)
   - 5.2 Onde Quebrar Linha (Pontos Preferenciais)
   - 5.3 Onde NUNCA Quebrar Linha (Proibições Absolutas)
   - 5.4 Divisão de Sentenças entre Múltiplas Legendas
6. [Pontuação, Símbolos e Formatação Tipográfica](#6-pontuação-símbolos-e-formatação-tipográfica)
   - 6.1 Aspas (Citações e Ênfases)
   - 6.2 Reticências (Caractere Smart U+2026)
   - 6.3 Hífens, Travessões e Diálogos Duplos
   - 6.4 Uso do Itálico: Diretrizes Rígidas
   - 6.5 Parênteses e Colchetes
7. [Números, Medidas e Grafias](#7-números-medidas-e-grafias)
   - 7.1 Cardinais: Escrita por Extenso vs. Numerais
   - 7.2 Ordinais, Horários e Moedas
   - 7.3 Conversão para o Sistema Métrico
   - 7.4 Abreviações e Siglas
8. [Tratamento de Músicas e Canções (Songs & Lyrics)](#8-tratamento-de-músicas-e-canções-songs--lyrics)
   - 8.1 Quando Legendar Músicas
   - 8.2 A Nota Musical Oficial (`♪`)
   - 8.3 Pontuação em Canções
   - 8.4 Duetos e Diálogos Cantados
9. [Forced Narratives (FN) / Legendas Forçadas](#9-forced-narratives-fn--legendas-forçadas)
   - 9.1 Definição e Aplicação
   - 9.2 Regra da Não Redundância
   - 9.3 Uso de Caixa Alta (ALL CAPS)
   - 9.4 Separação Estrita de Diálogos e Gráficos
10. [SDH: Legendas para Surdos e Ensurdecidos](#10-sdh-legendas-para-surdos-e-ensurdecidos)
    - 10.1 Identificação de Falantes (Speaker IDs)
    - 10.2 Descrição de Efeitos Sonoros e Ambiência
    - 10.3 Tom de Voz e Maneirismos
    - 10.4 Descrições Musicais
    - 10.5 CPS Específico para SDH
11. [Especificidades do Português Brasileiro (PT-BR)](#11-especificidades-do-português-brasileiro-pt-br)
    - 11.1 Acordo Ortográfico
    - 11.2 Nomes Próprios, Figuras Históricas e Mitológicas
    - 11.3 Títulos de Filmes, Livros e Músicas
    - 11.4 Registro Coloquial, Gírias e Palavrões
    - 11.5 Key Names and Phrases (KNP) e Tabelas de Consistência
12. [Checklist Geral de Controle de Qualidade (QA)](#12-checklist-geral-de-controle-de-qualidade-qa)

---

## 1. Filosofia Central: Leitura Invisível no Streaming

O padrão ouro da indústria audiovisual define a experiência de timed text (legendagem interlingual e acessível) sob o preceito da **leitura invisível** (*invisible reading*). A legenda nunca deve competir com a narrativa visual ou chamar atenção para si mesma; ela existe para transmitir fielmente a intenção do criador com o menor esforço cognitivo possível para o espectador.

### Pilares Fundamentais:
1. **Semântica e Unidade de Pensamento:** O cérebro humano processa blocos sintáticos inteiros. Uma legenda não é apenas uma sequência de caracteres cortados por espaço, mas uma unidade semântica coerente.
2. **Equilíbrio Sensorial:** O espectador deve ter tempo para ler o texto, olhar a imagem, absorver as expressões faciais dos atores e ouvir a sonoridade original.
3. **Fidelidade ao Tom:** Traduzir gírias, trocadilhos, regionalismos e formalidades com precisão contextual, mantendo o mesmo impacto emocional da fala em áudio.

---

## 2. Parâmetros Técnicos Universais (General Requirements)

Salvo quando especificado de forma diferente em um guia de idioma local específico, as seguintes regras gerais governam todos os arquivos de legendagem de alto padrão para streaming.

### 2.1 Limites de Linhas e Caracteres
* **Máximo de linhas:** **2 linhas** por evento de legenda.
* **Linha única:** Sempre dê preferência a **uma única linha**. Só quebre em duas linhas se o texto ultrapassar o limite de caracteres por linha ou se houver dois falantes em cena.
* **Caracteres por linha (CPL):**
  * Idiomas de alfabeto latino (incluindo **Português Brasileiro**, Inglês, Espanhol, Francês, Italiano, etc.): **Máximo de 42 caracteres por linha**.
  * Coreano: Máximo de 37 caracteres.
  * Chinês tradicional e simplificado: 16 caracteres por linha.
  * Japonês horizontal: 13 caracteres por linha.

### 2.2 Duração Mínima e Máxima
* **Duração mínima:** **5/6 de segundo (aproximadamente 833 milissegundos)** por legenda.
  * Em 24 fps: **20 frames**.
  * Em 25 fps: **21 frames**.
  * Em 29.97 / 30 fps: **25 frames**.
  * *Objetivo:* Evitar que a legenda apareça e desapareça num piscar de olhos, causando desconforto ("flash").
* **Duração máxima:** **7 segundos** por evento de legenda, independentemente do tamanho do texto falado.

### 2.3 Velocidade de Leitura (CPS - Characters Per Second)
A densidade da legenda é calculada pela taxa de caracteres por segundo (CPS). Espaços e caracteres de pontuação **são contabilizados** no cálculo.

$$\text{CPS} = \frac{\text{Total de caracteres (incluindo espaços e pontuações)}}{\text{Duração da legenda em segundos}}$$

#### Limites Oficiais de CPS:
| Modalidade | Público | Idiomas Gerais / PT-BR | Inglês (Referência) |
| :--- | :--- | :--- | :--- |
| **Legenda Regular (Interlingual)** | Adultos | **Até 17 CPS** | Até 20 CPS |
| **Legenda Regular (Interlingual)** | Infantil | **Até 13 CPS** | Até 17 CPS |
| **SDH (Acessibilidade)** | Adultos | **Até 20 CPS** | Até 20 CPS |
| **SDH (Acessibilidade)** | Infantil | **Até 17 CPS** | Até 17 CPS |

> [!IMPORTANT]
> **Condensação Textual Obrigatória:** Se um personagem fala muito rápido e a transcrição literal ultrapassar o limite de CPS permitido, o tradutor/legendador **DEVE sintetizar e condensar o texto**, preservando o sentido primordial, nuances emocionais e informações vitais da trama, sem omitir elementos essenciais.

### 2.4 Intervalo Mínimo Entre Legendas (Gap de Frames)
* Deve haver um intervalo de **pelo menos 2 frames** entre o out-time da legenda anterior e o in-time da legenda seguinte.
* Essa regra é universal para todos os frame rates (24, 25, 29.97, 30, 50, 60 fps).
* **Finalidade:** O olho humano precisa de pelo menos 2 frames escuros no canal de texto para perceber a troca de blocos legendados; sem esse intervalo, o espectador não nota que o texto mudou ou percebe um flicker borrado.

### 2.5 Formatos de Arquivo e Codificação
* Formato primário de entrega de master: **TTML1 (.xml ou .ttml)** em conformidade com o padrão W3C TTML, ou **IMSC 1.1**.
* Codificação de caracteres: **UTF-8 estrito** sem BOM.
* Formatos auxiliares de trabalho em ferramentas de terceiros: SubRip (.srt) e WebVTT (.vtt) só são aceitos quando especificamente solicitados para fluxos de rascunho, convertidos depois para TTML/IMSC.
* **Proibição de Tags de Estilização Próprias:** Não incluir estilos de cores arbitrárias, tamanhos de fonte customizados ou folhas CSS locais; a plataforma renderiza o texto pelo leitor nativo.

### 2.6 Lista de Caracteres Permitidos (Glyph List)
* Apenas caracteres presentes na **Lista Oficial de Glifos Suportados (Glyph List)** para a língua de destino são aceitos.
* Caracteres não suportados, símbolos matemáticos obscuros ou emojis **são expressamente proibidos**.

---

## 3. Posicionamento e Alinhamento na Tela

### 3.1 Alinhamento Padrão
* **Alinhamento horizontal:** As legendas devem ser **centralizadas** na largura da tela (*center-justified*).
* **Alinhamento vertical:** Posicionadas na **base da tela** (área inferior central).

### 3.2 Reposicionamento para o Topo (Top Placement)
A legenda deve ser movida para a **área superior central da tela** exclusivamente para evitar colisão visual nas seguintes situações:
1. Nomes de atores, créditos de abertura ou encerramento fixos na base.
2. Identificadores de locais, cargos ou datas (*lower thirds* de documentários ou reportagens).
3. Textos gravados na imagem original (placas, cartas na mesa, mensagens de celular na parte inferior).
4. Legendas originais queimadas no master de vídeo (*burned-in subtitles*).

### 3.3 Conflito com Textos Queimados na Imagem (Burn-ins)
* Se houver texto em tela simultaneamente no topo e na base: posicione a legenda na área que oferecer **menor conflito de leitura e melhor contraste**.
* A legenda **nunca** deve cobrir o rosto dos personagens em close-up, a menos que seja a única alternativa para evitar sobreposição ilegível com textos queimados no vídeo.

### 3.4 Área de Segurança (Safe Area)
* Todas as legendas devem respeitar a margem de segurança de **80% a 90% (Title Safe Area)** para garantir que aparelhos de TV com diferentes formatos de tela e dispositivos móveis não cortem as pontas das linhas.

---

## 4. Temporização e Cortes de Câmera (Subtitle Timing Guidelines)

A temporização (*timing/spotting*) não é feita apenas contra a onda sonora; ela deve dialogar dinamicamente com a edição cinematográfica da cena.

### 4.1 Sincronia com o Áudio (Waveform)
* **In-time:** Sincronizado com o início exato da emissão de voz (primeiro frame audível).
* **Out-time:** Mantido até o encerramento da fala, acrescido da permanência necessária para cumprir o tempo de leitura confortável, estendendo-se ligeiramente após o término do som (cerca de 2 a 4 frames), desde que não ultrapasse um corte de plano.

### 4.2 Interação com Cortes de Plano (Shot Changes)
Cortes de cena alteram o foco cognitivo do cérebro. Uma legenda que surge fração de segundo antes ou depois de um corte visual provoca incômodo sensorial.

Para conteúdo padrão a **24 fps**:

#### 1. Início de Fala Próximo a um Corte:
* **Se a fala começa de 1 a 7 frames APÓS o corte:** O in-time da legenda deve ser **puxado para o Frame 0 do novo corte** (*snap to shot change*).
* **Se a fala começa de 8 a 11 frames APÓS o corte:** Mantenha o in-time no início do áudio (ou respeite a almofada de meio segundo).
* **Se a fala começa de 1 a 7 frames ANTES de um corte:** Antecipe a entrada da legenda para sincronizar no corte ou sintetize a quebra.

#### 2. Término de Fala Próximo a um Corte:
* **Se a fala termina de 1 a 7 frames ANTES de um corte:** O out-time deve ser **estendido até exatamente 2 frames ANTES do corte de plano** (*snap out to cut - 2 frames*).
* **Se a fala termina de 8 a 11 frames ANTES de um corte:** Estenda o out-time até completar pelo menos **12 frames antes do corte** para evitar que a legenda suma quase em cima do corte.

### 4.3 A Regra dos 12 Frames (Meio Segundo)
O padrão estabelece 12 frames a 24 fps (meio segundo) como a unidade mínima de respiração visual entre eventos e transições de cena:
* Para 24 fps $\rightarrow$ 12 frames = 0,5s
* Para 30 fps $\rightarrow$ 15 frames = 0,5s
* Para 60 fps $\rightarrow$ 30 frames = 0,5s

### 4.4 Travessia de Cortes de Plano (Crossing Shot Changes)
* **Regra básica:** Evite que uma legenda atravesse um corte de câmera sempre que possível.
* **Exceção permitida:** Uma legenda **PODE** atravessar um corte de cena se o diálogo do personagem for contínuo através da transição de câmera **E** se dividir a legenda em duas violar o limite mínimo de duração (20 frames) ou estourar a taxa de leitura (CPS).

### 4.5 Hierarquia: Taxa de Leitura vs. Cortes de Câmera
> [!TIP]
> **A leitura sempre vence o corte:** Se o respeito cego ao corte de câmera forçar uma legenda ilegível (por exemplo, 8 frames de duração com 30 caracteres), **a regra do corte deve ser flexibilizada**. Permita que a legenda atravesse o corte para garantir a duração mínima de 20 frames e o CPS regulamentar.

---

## 5. Morfossintaxe e Quebra de Linha (Line Breaks)

A quebra de linha nunca deve ser aleatória ou baseada apenas no espaço gráfico da tela. Ela deve seguir estritamente a estrutura sintática da língua falada.

### 5.1 Princípio da Pirâmide Invertida (Bottom-Heavy)
Quando uma legenda exigir duas linhas:
* A **segunda linha deve ser igual ou mais longa que a primeira**.
* Isso alinha a base visual do texto e cria uma progressão visual mais ergonômica para a leitura.

```
✅ CORRETO (Pirâmide Invertida):
Eu não fazia ideia de que você
viria para a reunião hoje à tarde.

❌ INCORRETO (Pirâmide Normal / Desequilibrada):
Eu não fazia ideia de que você viria para a
reunião hoje à tarde.

❌ INCORRETO (Palavra órfã):
Nós já combinamos tudo sobre a viagem e
vamos.
```

### 5.2 Onde Quebrar Linha (Pontos Preferenciais)
A quebra deve ocorrer nos pontos naturais de articulação sintática, respeitando a seguinte ordem de prioridade:

| Prioridade | Local de Quebra | Exemplo Prático |
| :---: | :--- | :--- |
| **1ª** | Após sinais de pontuação forte (ponto final, vírgula, ponto e vírgula, dois-pontos, exclamação, interrogação) | *Eu avisei que seria perigoso,<br>mas ninguém quis me ouvir.* |
| **2ª** | Antes de conjunções coordenativas e subordinativas (*e, mas, ou, porque, quando, se, embora, contudo*) | *Ela decidiu voltar para casa<br>porque começou a chover.* |
| **3ª** | Antes de preposições que iniciam locuções adverbiais ou adjuntos (*em, para, com, de, sobre, até, sem*) | *Eles estavam conversando<br>sobre o projeto da escola.* |
| **4ª** | Entre sujeito oracional complexo e predicado | *O homem de casaco escuro<br>atravessou a rua correndo.* |

### 5.3 Onde NUNCA Quebrar Linha (Proibições Absolutas)

Nunca separe elementos que formam uma unidade léxica, morfológica ou sintática indivisível:

1. **Artigo e Substantivo:**
   * ❌ *Eu deixei a* / *chave na gaveta.*
   * ✅ *Eu deixei* / *a chave na gaveta.*
2. **Substantivo e Adjetivo:**
   * ❌ *Ela comprou um casaco* / *azul na liquidação.*
   * ✅ *Ela comprou* / *um casaco azul na liquidação.*
3. **Nome Próprio e Sobrenome / Título Honorífico:**
   * ❌ *Conversei com o Dr.* / *Roberto ontem.*
   * ✅ *Conversei com* / *o Dr. Roberto ontem.*
   * ❌ *Aquele livro do Carlos* / *Drummond é ótimo.*
   * ✅ *Aquele livro* / *de Carlos Drummond é ótimo.*
4. **Pronome Sujeito e Verbo:**
   * ❌ *Naquela hora, nós* / *percebemos o perigo.*
   * ✅ *Naquela hora,* / *nós percebemos o perigo.*
5. **Verbo e Auxiliar / Locução Verbal / Negação:**
   * ❌ *Eles não* / *vão chegar a tempo.*
   * ✅ *Eles não vão* / *chegar a tempo.*
   * ❌ *Ela tinha* / *falado com o diretor.*
   * ✅ *Ela tinha falado* / *com o diretor.*
6. **Verbo e Pronome Oblíquo / Reflexivo:**
   * ❌ *Ele se* / *esqueceu do compromisso.*
   * ✅ *Ele se esqueceu* / *do compromisso.*
7. **Verbo Preposicionado e Preposição Obrigatória:**
   * ❌ *Eu preciso de* / *ajuda para terminar.*
   * ✅ *Eu preciso* / *de ajuda para terminar.*
8. **Número e Substantivo / Unidade de Medida:**
   * ❌ *O trem percorreu 150* / *quilômetros hoje.*
   * ✅ *O trem percorreu* / *150 quilômetros hoje.*

### 5.4 Divisão de Sentenças entre Múltiplas Legendas
Quando uma frase for muito longa e precisar ser distribuída por duas ou três legendas consecutivas:
* **Não use reticências nem travessões** para indicar continuação de uma frase entre legendas sucessivas.
* A ausência de pontuação no final da primeira legenda já sinaliza ao cérebro do espectador que a ideia continua no próximo quadro.

---

## 6. Pontuação, Símbolos e Formatação Tipográfica

### 6.1 Aspas (Citações e Ênfases)
* **Aspas duplas (`" "`):** Usadas para citações diretas, leituras em voz alta de cartas/livros ou ironia explícita (*air quotes* feitas pelo ator).
* **Aspas simples (`' '`):** Usadas exclusivamente para citações dentro de citações já abertas por aspas duplas.
* **Pontuação com aspas:**
  * O ponto final ou vírgula fica **dentro das aspas** se a citação contiver uma sentença completa e autônoma:  
    *Ele disse: "Não faça isso."*
  * Fica **fora das aspas** se apenas uma palavra ou expressão for citada:  
    *Ele chamou o projeto de "revolucionário".*

### 6.2 Reticências (Caractere Smart U+2026)
* **Formatação obrigatória:** Usar estritamente o caractere Unicode único de reticências **`…`** (`U+2026`).  
  **É expressamente proibido digitar três pontos comuns sucessivos (`...`).**
* **Quando usar:**
  1. Para pausas significativas na fala (geralmente pausas superiores a 2 segundos).
  2. Quando um personagem hesita ou gagueja (*"Eu… eu não sei"*).
  3. Quando a frase se perde no ar (*trailing off*) e o falante não conclui o pensamento (*"Se você diz…" *).
* **Quando NÃO usar:**
  * **Nunca use reticências no final de uma legenda e no início da seguinte para indicar fala contínua.**

### 6.3 Hífens, Travessões e Diálogos Duplos
Quando dois personagens dialogam no mesmo evento de legenda:
* Use **hífen seguido de espaço (`- `)** no início de cada linha de fala.
* Máximo de **um personagem por linha**.
* Cada linha deve conter uma oração completa que termine em si mesma (não arraste a fala de um personagem do diálogo duplo para uma linha seguinte de outra legenda).

```
Exemplo Correto:
- Você vai amanhã?
- Sim, bem cedo.
```

* **Interrupção súbita de fala:** Se um personagem for subitamente interrompido por outro ou por um evento (como um estampido), use travessão longo (*em-dash* `—`) colado à última palavra, ou o padrão definido no guia do idioma.

### 6.4 Uso do Itálico: Diretrizes Rígidas
O itálico deve ser aplicado estritamente nas seguintes situações:
1. **Vozes fora de cena (Off-screen) e Narrações:** Vozes de narradores em off e pensamentos íntimos (monólogos interiores).
2. **Dispositivos Eletrônicos:** Vozes reproduzidas por telefones, walkie-talkies, caixas de som, rádio, televisão, secretárias eletrônicas, inteligências artificiais e assistentes virtuais, **desde que o interlocutor não esteja presente na cena**.
3. **Canções:** Todas as letras de música cantadas são **obrigatoriamente grafadas em itálico**.
4. **Palavras e Expressões Estrangeiras:** Termos em outro idioma que não foram naturalizados na língua de destino (*ex: déjà vu, carpe diem, rendezvous*). Palavras incorporadas (como *download, jeans, pizza*) não levam itálico.
5. **Títulos de Obras Culturais:** Livros, filmes, jornais, programas de TV, quadros e álbuns musicais. *(Títulos de faixas e canções individuais levam aspas, não itálico).*

> [!CAUTION]
> **Proibição de Alternância Falsa:** Se um personagem fala enquanto caminha pela sala e sai temporariamente do enquadramento da câmera (mas continua no mesmo ambiente), **NÃO aplique itálico**. O itálico só se aplica se o personagem estiver genuinamente fora do ambiente ou em outra dimensão espacial (ex: telefonema de outro lugar).

---

## 7. Números, Medidas e Grafias

### 7.1 Cardinais: Escrita por Extenso vs. Numerais
* **De zero a dez (1 a 10):** Devem ser escritos **por extenso** (*um, dois, três, quatro, cinco, seis, sete, oito, nove, dez*).
* **De 11 em diante:** Devem ser grafados em **algarismos arábicos** (*11, 12, 100, 1.500, 20.000*).
* **Início de frase:** Qualquer número que inicie uma oração deve ser **sempre escrito por extenso**, sem exceções:
  * ✅ *Vinte e cinco pessoas foram convocadas.*
  * ❌ *25 pessoas foram convocadas.*
* **Exceção de consistência e limite:** Se números menores e maiores aparecerem em série numa mesma frase de enumeração técnica ou se houver restrição gravíssima de CPS, algarismos podem ser usados.

### 7.2 Ordinais, Horários e Moedas
* **Ordinais:** Do primeiro ao décimo por extenso (*primeiro, segundo... décimo*); a partir do 11º em numerais com a terminação ordinal (*11º, 12ª*). Abreviações ordinais só são permitidas antes de substantivos (*a 1ª vez*; mas *foi a primeira a chegar*).
* **Horários:** Em contextos cotidianos casuais, escreva por extenso (*oito horas, sete e meia*). Para referências específicas, use numerais (*às 8h30* ou *8h* conforme norma da língua).
* **Moeda:** Grafar por extenso em quantias correntes (*dez dólares, 50 reais*); símbolos monetários só se forem indispensáveis ao contexto espacial ou listas.

### 7.3 Conversão para o Sistema Métrico
* Na legendagem para países lusófonos (Brasil e Portugal), as unidades imperiais (milhas, pés, polegadas, jardas, galões, libras, fahrenheit) devem ser **convertidas para o sistema métrico decimal** (*quilômetros, metros, centímetros, quilos, graus Celsius*).
* **Exceção:** Só mantenha a unidade original se ela for vital para um trocadilho, uma piada textual ou uma metáfora inalterável.
* **Espaçamento de unidades:** Abreviações métricas não recebem ponto, plural ou espaço em relação ao número:
  * ✅ `5km`, `10kg`, `2m`
  * ❌ `5 km`, `10 kg.`, `5kms`

### 7.4 Abreviações e Siglas
* Títulos honoríficos e profissionais usam abreviações canônicas: *Dr.*, *Dra.*, *Sr.*, *Sra.*, *Prof.*
* Siglas e acrônimos não levam pontos intermediários: *EUA, ONU, FBI, BBC, TV, IA*.

---

## 8. Tratamento de Músicas e Canções (Songs & Lyrics)

### 8.1 Quando Legendar Músicas
Músicas só devem ser legendadas se cumprirem pelo menos um dos requisitos:
1. A letra contiver informações vitais para a narrativa, enredo ou desenvolvimento psicológico dos personagens.
2. A música for diegética (cantada por um personagem em cena).
3. For uma trilha de abertura ou encerramento formalmente licenciada com tradução obrigatória no projeto.
* Se a música for mero fundo instrumental/sonoro sem relevância narrativa direta, ela **não deve ser legendada** na modalidade padrão (apenas em SDH).

### 8.2 A Nota Musical Oficial (`♪`)
* Utilize exclusivamente o caractere Unicode de colcheia única: **`♪`** (`U+266A`).
* **Espaçamento:** Insira um espaço simples entre a nota musical e a letra da canção:
  * *♪ Letra da música cantada ♪*
* **Posição:** Coloque uma nota no **início e no final de cada evento de legenda**. Se a legenda tiver duas linhas cantadas pelo mesmo intérprete, a nota vai no início da linha 1 e no final da linha 2:
  ```
  ♪ Amar você é tão fácil
  que esqueço do mundo ♪
  ```
* Se for um **dueto** em que cada linha representa um intérprete diferente, inclua notas no início e no final de **cada linha**:
  ```
  - ♪ Eu vejo você ♪
  - ♪ E sinto o amor ♪
  ```

### 8.3 Pontuação em Canções
* Inicie cada verso/linha com **letra maiúscula**.
* **Não use ponto final nem vírgula** no final das linhas de música.
* Pontuações expressivas como **ponto de interrogação (`?`)** e **ponto de exclamação (`!`)** são mantidas se o tom da música demandar.
* Se a música estiver tocando e for interrompida pelo diálogo de um personagem em primeiro plano, encerre a estrofe musical com reticências (`…`) para indicar desvanecimento da canção.

---

## 9. Forced Narratives (FN) / Legendas Forçadas

### 9.1 Definição e Aplicação
Uma legenda forçada (FN) é uma legenda direcionada ao público que assiste à produção no áudio original ou dublado, necessária para compreender:
* Falas em idiomas secundários que não foram dubladas.
* Textos na tela que sejam essenciais para o enredo (cartas, bilhetes, mensagens de texto em smartphones, placas de rua, datas históricas, créditos de identificação de local e época).

### 9.2 Regra da Não Redundância
* **Nunca crie uma legenda forçada** para um texto em tela que seja universalmente óbvio ou que o personagem já leia em voz alta no diálogo dublado/original.
* Se um ator lê em voz alta o bilhete que pegou na mão, nenhuma FN de texto em tela deve ser inserida.

### 9.3 Uso de Caixa Alta (ALL CAPS)
* Todas as legendas forçadas que traduzem **textos escritos no vídeo** devem ser grafadas inteiramente em **CAIXA ALTA (MAIÚSCULAS)**:
  * `PARIS, 1944`
  * `NÃO ABRA ESTA PORTA`
  * `DEPARTAMENTO DE HOMICÍDIOS`
* **Exceções à Caixa Alta:** Prólogos longos de abertura, pergaminhos extensos, poemas ou telas de conversas longas de mensagens de chat (que devem ser formatadas em caixa normal com pontuação padrão para facilitar a fluidez de leitura).
* Diálogos falados em línguas estrangeiras (áudio secundário) **seguem caixa normal** (Sentence case), exatamente como qualquer diálogo comum.

### 9.4 Separação Estrita de Diálogos e Gráficos
* **Nunca combine uma legenda forçada de texto em tela com fala de diálogo no mesmo evento de legenda.**
* Se um personagem fala no exato momento em que uma placa crucial aparece, divida em eventos sequenciais ou dê prioridade de posicionamento (placa no topo em caixa alta, fala na base em caixa normal).

---

## 10. SDH: Legendas para Surdos e Ensurdecidos

As diretrizes de SDH (*Subtitles for the Deaf and Hard of Hearing*) expandem o texto falado para abranger todo o espectro sonoro que carrega sentido narrativo.

### 10.1 Identificação de Falantes (Speaker IDs)
* Nomes de personagens e identificadores de falantes devem ser inseridos entre **colchetes `[ ]`**.
* Use letras **minúsculas** dentro dos colchetes, exceto para a inicial maiúscula de nomes próprios:
  * `[Carlos]`
  * `[policial]`
  * `[mulher no rádio]`
* **Evite Spoilers:** Se um personagem fala antes de ser revelado na tela ou antes que seu nome seja pronunciado, use identificadores genéricos (`[homem]`, `[voz misteriosa]`). Só use o nome oficial após o personagem se apresentar ou ser nomeado na trama.
* O identificador deve anteceder a fala na mesma linha ou preceder o diálogo:
  * `[Carlos] Não vá embora agora.`

### 10.2 Descrição de Efeitos Sonoros e Ambiência
* Descrições sonoras devem ser inseridas entre **colchetes `[ ]`**, escritas inteiramente em **letras minúsculas**:
  * `[trovão estrondoso]`
  * `[porta estalando]`
  * `[respiração ofegante]`
  * `[vidro se quebrando]`
* **Descreva o som, não a ação visual:** Não escreva `[Carlos chora]` se o público já está vendo Carlos chorar; escreva `[soluços contidos]` se o som for relevante, ou descreva sons de fontes invisíveis no quadro.
* Seja específico e evoque a textura acústica com adjetivos precisos quando enriquecer a imersão (`[sussurro abafado]`, `[alarme agudo]` em vez de apenas som genérico).

### 10.3 Tom de Voz e Maneirismos
* Quando a entonação for sarcástica, sussurrada ou transmitir um estado de espírito indispensável não visual:
  * `[em tom irônico]`
  * `[sussurrando]`
  * `[com a voz trêmula]`

### 10.4 Descrições Musicais
* Para músicas incidentais sem letra falada ou temas sonoros marcantes:
  * `[música de suspense tocando]`
  * `[rock acelerado no rádio]`
  * `[melodia suave ao piano]`
* Se a canção contiver vocais cruciais, use a descrição do estilo seguida pela letra com as notas musicais `♪`.

### 10.5 CPS Específico para SDH
Como o espectador de SDH depende exclusivamente da visão para processar fala + efeitos + trilha, a tolerância de velocidade é ligeiramente superior:
* **Adultos:** Até **20 CPS**.
* **Infantil:** Até **17 CPS**.

---

## 11. Especificidades do Português Brasileiro (PT-BR)

### 11.1 Acordo Ortográfico
* Uso obrigatório da norma-padrão do **Acordo Ortográfico da Língua Portuguesa** (abolição do trema, novas regras de hifenização, acentuação de ditongos abertos e hiatos).

### 11.2 Nomes Próprios, Figuras Históricas e Mitológicas
* Nomes de pessoas contemporâneas são mantidos na grafia original do idioma de origem (*John, Charles, François*).
* Preservar diacríticos e acentos de nomes próprios originários de línguas românicas (*García, François, Müller*).
* Nomes consagrados de santos, monarcas históricos, personagens mitológicos e personalidades da Antiguidade devem ser traduzidos para o formato canônico em português:
  * *Alexander the Great* $\rightarrow$ **Alexandre, o Grande**
  * *Saint Peter* $\rightarrow$ **São Pedro**
  * *Queen Elizabeth* $\rightarrow$ **Rainha Elizabeth**
  * *Santa Claus* $\rightarrow$ **Papai Noel**

### 11.3 Títulos de Filmes, Livros e Músicas
* Filmes e séries: Se a obra já possuir um título oficial no catálogo de exibição nacional, use a versão consagrada em português (*Star Wars* $\rightarrow$ *Guerra nas Estrelas* / *Star Wars*, conforme a política editorial da franquia).
* Se a obra citada não tiver tradução lançada no país, mantenha o título original em itálico.

### 11.4 Registro Coloquial, Gírias e Palavrões
* Respeitar o tom e a faixa etária da produção. Não higienize nem amenize palavrões se eles forem intencionais do áudio original; encontre termos de força expressiva equivalente no vernáculo brasileiro.
* Evite regionalismos excessivos que fiquem incompreensíveis fora de um estado brasileiro, optando por coloquialismos neutros compartilhados por todo o território nacional, a menos que a trama se passe expressamente em determinada região com sotaque característico.

### 11.5 Key Names and Phrases (KNP) e Tabelas de Consistência
* Em produções seriadas ou franquias, termos fictícios, jargões tecnológicos, feitiços, nomes de naves e patentes devem ser consolidados numa planilha KNP (*Key Names and Phrases*) para assegurar que tradutores de episódios distintos mantenham 100% de uniformidade terminológica.

---

## 12. Checklist Geral de Controle de Qualidade (QA)

Antes de validar qualquer arquivo de legendas no ecossistema profissional de streaming, execute a checagem rigorosa de cada um dos itens abaixo:

```markdown
### 1. Parâmetros Temporais e Métricas
- [ ] O limite máximo de 42 caracteres por linha (CPL) foi rigorosamente respeitado?
- [ ] O número de linhas por evento é de no máximo 2?
- [ ] A velocidade de leitura está abaixo de 17 CPS (adultos) ou 13 CPS (crianças)?
- [ ] A duração mínima de cada legenda respeita 20 frames / 833ms (5/6 de segundo)?
- [ ] A duração máxima não ultrapassa 7 segundos?
- [ ] Há um intervalo (gap) de pelo menos 2 frames entre legendas consecutivas?

### 2. Edição e Cortes de Câmera (Shot Changes)
- [ ] Legendas que terminam perto de um corte saem 2 frames antes do corte?
- [ ] Legendas que iniciam perto de um corte cravam no frame exato da mudança de plano?
- [ ] Legendas que atravessam cortes só o fazem para proteger a integridade do CPS e da duração mínima?

### 3. Morfossintaxe e Equilíbrio Visual
- [ ] A quebra de linha segue o formato de pirâmide invertida (segunda linha igual ou maior)?
- [ ] Não há separação de artigo e substantivo?
- [ ] Não há separação de pronome sujeito e verbo?
- [ ] Não há separação de nome e sobrenome?
- [ ] Não há separação de verbo e auxiliar/particípio/negação?
- [ ] Não existem palavras órfãs com 1 ou 2 letras sozinhas na linha?

### 4. Pontuação e Formatação
- [ ] Reticências utilizam estritamente o caractere único Unicode `…` (U+2026)?
- [ ] Não foram usadas reticências ou travessões para emendar falas contínuas entre legendas?
- [ ] Diálogos duplos usam hífen seguido de espaço (`- `) em ambas as falas?
- [ ] O itálico foi reservado estritamente para vozes eletrônicas/off-screen, músicas e estrangeirismos?
- [ ] Músicas contêm a nota oficial `♪` com espaço nas extremidades do evento?
- [ ] Letras de música não terminam com pontos finais ou vírgulas?
- [ ] Números de 1 a 10 estão escritos por extenso (e sempre por extenso em início de frase)?
- [ ] Unidades métricas decimais estão convertidas e anexadas ao número sem espaço (`5km`, `10kg`)?

### 5. Posicionamento e Acessibilidade
- [ ] Legendas com textos queimados na base foram reposicionadas centralizadas no topo?
- [ ] Foram removidas legendas forçadas redundantes de textos que o personagem já leu em voz alta?
- [ ] Elementos de SDH utilizam colchetes `[ ]` em minúsculas para efeitos e com iniciais para nomes?
```

---
*Manual estruturado e adaptado conforme as melhores práticas e especificações técnicas de referência da indústria audiovisual e streaming global.*
