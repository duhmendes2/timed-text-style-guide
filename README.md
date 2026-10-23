# 🎬 Timed Text Style Guide (TTSG) — Padrão de Legendagem para Streaming

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Standard: Streaming TTSG](https://img.shields.io/badge/Standard-Streaming%20TTSG-blue.svg)](#)
[![Language: PT--BR & EN](https://img.shields.io/badge/Language-PT--BR%20%7C%20EN-green.svg)](#)

Guia definitivo, técnico e editorial consolidado para criação, tradução, temporização e controle de qualidade (QA) de **legendas profissionais (Timed Text)** no padrão ouro adotado pelas maiores plataformas de streaming do mundo.

---

## 📚 Documentos Disponíveis

* 🇧🇷 **[Manual Completo em Português (MANUAL_COMPLETO_TTSG.md)](./MANUAL_COMPLETO_TTSG.md):** Manual exaustivo contendo todas as diretrizes técnicas, regras morfossintáticas, formatação, músicas, pontuação, SDH e particularidades do Português Brasileiro.
* 🇺🇸 **[Universal Guide in English (TIMED_TEXT_GUIDE_EN.md)](./TIMED_TEXT_GUIDE_EN.md):** Especificações universais e métricas internacionais de legendagem.
* ✅ **[Checklist de Controle de Qualidade (CHECKLIST_QA.md)](./CHECKLIST_QA.md):** Lista de verificação prática e ágil para tradutores, revisores e pipelines automatizados.

---

## ⚡ Regras Técnicas Principais (Cheat Sheet)

| Parâmetro | Especificação Oficial |
| :--- | :--- |
| **Linhas por Legenda** | Máximo de **2 linhas** (dar preferência para linha única). |
| **Caracteres por Linha (CPL)** | Máximo de **42 caracteres** (incluindo espaços e pontuação). |
| **Duração Mínima** | **5/6 de segundo (833ms)** $\rightarrow$ **20 frames** a 24 fps (25 frames a 30 fps). |
| **Duração Máxima** | **7 segundos** por evento de legenda. |
| **Intervalo Mínimo (Gap)** | **2 frames** obrigatórios entre legendas consecutivas. |
| **Velocidade de Leitura (CPS)** | **Adultos:** máx. 17 CPS (SDH: 20 CPS) \| **Infantil:** máx. 13 CPS (SDH: 17 CPS). |
| **Alinhamento** | **Centralizado**, base da tela. Reposicionar no topo se houver texto fixo na base. |
| **Cortes de Plano (Shot Changes)** | Snapping a 7 frames ou menos do corte; saída a 2 frames antes do corte. |
| **Quebra de Linha** | **Pirâmide Invertida** (segunda linha igual ou maior). Proibido quebrar artigo/nome/verbo. |
| **Reticências** | Usar estritamente o caractere Unicode **`…`** (`U+2026`). Nunca usar `...`. |
| **Diálogos Duplos** | Hífen com espaço (`- `) no início de cada linha de fala. |
| **Letras de Música** | Em itálico com nota musical e espaço: `♪ Letra cantada ♪`. |
| **Forced Narratives (FN)** | Textos de tela em **CAIXA ALTA (ALL CAPS)**. Sem misturar fala e texto na mesma legenda. |
| **SDH (Acessibilidade)** | Falantes em colchetes com inicial maiúscula (`[Carlos]`), efeitos em minúsculas (`[sussurra]`). |

---

## 🎯 Para Quem é Este Repositório?

1. **Tradutores e Legendadores Audiovisuais:** Para consultar parâmetros formais exigidos por estúdios de pós-produção e distribuidoras globais.
2. **Revisores e Especialistas em QC/QA:** Para checar conformidade antes do envio de masters (.xml, .ttml, .srt).
3. **Desenvolvedores e Engenheiros de IA:** Para implementar algoritmos de transcrição (Whisper, etc.), formatação e quebra inteligente de linha baseada em regras sintáticas.

---

## 📄 Licença

Este projeto é disponibilizado sob a licença [MIT](./LICENSE). As diretrizes representam a consolidação de boas práticas técnicas da indústria de streaming e legendagem aberta.
