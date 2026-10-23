# ✅ Checklist de Controle de Qualidade (QA) para Legendas

Este checklist prático serve como guia de revisão rápida para tradutores, revisores, legendadores e desenvolvedores de sistemas automatizados de legendas para streaming.

---

### 1. Métricas Técnicas e Temporais
- [ ] **Máximo de Linhas:** No máximo 2 linhas por legenda (priorizar linha única sempre que possível).
- [ ] **Caracteres por Linha (CPL):** Máximo de 42 caracteres por linha (incluindo espaços e pontuação).
- [ ] **Velocidade de Leitura (CPS):**
  - Adultos: máximo de **17 CPS** (SDH: até **20 CPS**).
  - Infantil: máximo de **13 CPS** (SDH: até **17 CPS**).
- [ ] **Duração Mínima:** Pelo menos **5/6 de segundo (833ms)** $\rightarrow$ 20 frames a 24 fps.
- [ ] **Duração Máxima:** Máximo de **7 segundos** por evento.
- [ ] **Intervalo Mínimo (Gap):** Intervalo de **pelo menos 2 frames** entre legendas consecutivas.

---

### 2. Sincronia e Cortes de Câmera (Shot Changes)
- [ ] **In-time em Cortes:** Se a fala começar de 1 a 7 frames após um corte visual, a entrada da legenda está cravada no frame 0 do novo plano?
- [ ] **Out-time em Cortes:** Se a fala terminar de 1 a 7 frames antes de um corte visual, a saída está fixada a exatamente 2 frames antes do corte?
- [ ] **Travessia de Cortes:** Legendas só atravessam cortes de cena se o diálogo for contínuo e a quebra violar o CPS ou a duração mínima de 20 frames?

---

### 3. Quebra de Linha e Morfossintaxe
- [ ] **Pirâmide Invertida:** A segunda linha é igual ou ligeiramente mais longa que a primeira?
- [ ] **Nenhum Artigo Separado:** O artigo permanece junto ao seu substantivo?
- [ ] **Nenhum Nome Separado:** O primeiro nome permanece junto ao sobrenome?
- [ ] **Nenhum Pronome Sujeito Separado:** O pronome reto/sujeito está junto ao verbo?
- [ ] **Nenhum Verbo Auxiliar Separado:** Verbos auxiliares e de negação estão juntos ao verbo principal?
- [ ] **Sem Palavras Órfãs:** Não há palavras solitárias de 1 ou 2 letras isoladas em uma linha?

---

### 4. Pontuação e Tipografia
- [ ] **Reticências Smart:** Usa estritamente o caractere Unicode **`…`** (`U+2026`) em vez de três pontos digitados (`...`)?
- [ ] **Sem Reticências de Conexão:** Não foram usadas reticências nem travessões para emendar falas contínuas entre legendas sucessivas?
- [ ] **Diálogos Duplos:** Usa hífen seguido de espaço (`- `) no início de cada linha de fala?
- [ ] **Uso do Itálico:** Aplicado exclusivamente a:
  - Vozes em off / narradores fora do ambiente físico.
  - Vozes por dispositivos eletrônicos (telefone, rádio, TV) quando o interlocutor não está em cena.
  - Letras de música cantadas.
  - Palavras e expressões estrangeiras não assimiladas.
- [ ] **Músicas:** Letras possuem a nota oficial **`♪`** (`U+266A`) com espaço nas pontas (`♪ Letra da música ♪`)?
- [ ] **Pontuação em Canções:** Versos iniciam com maiúscula e não terminam com vírgula ou ponto final?

---

### 5. Números e Medidas
- [ ] **Cardinais:** Números de 1 a 10 estão escritos por extenso?
- [ ] **Início de Frase:** Qualquer número no início da oração está escrito por extenso?
- [ ] **Sistema Métrico:** Medidas imperiais foram convertidas para o sistema métrico decimal?
- [ ] **Unidades Métricas:** Abreviações métricas estão anexadas ao número sem espaço (`5km`, `10kg`)?

---

### 6. Acessibilidade (SDH) e Narrativas Forçadas (FN)
- [ ] **Speaker IDs:** Identificadores de personagem estão entre colchetes com inicial maiúscula (`[Carlos]`)?
- [ ] **Efeitos Sonoros:** Descrições sonoras estão entre colchetes em letras minúsculas (`[trovão estrondoso]`)?
- [ ] **Audiodescrição vs. Ação:** A descrição foca na textura acústica sonora e não na ação puramente visual?
- [ ] **FN de Textos na Tela:** Textos em tela traduzidos estão em **CAIXA ALTA (ALL CAPS)**?
- [ ] **Não Redundância:** Não há legendas forçadas para placas ou bilhetes que o personagem já leu em voz alta?
