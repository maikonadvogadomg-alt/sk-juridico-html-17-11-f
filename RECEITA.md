# 🧬 Receita para recriar: Caça-Bug

_Gerada sem IA, lendo 112 arquivo(s). Serve para remontar este app como HTML modular — com qualquer IA, um arquivo por vez._

## 1. O que é

- **Nome:** Caça-Bug
- **Partes de código:** 86 (16 tela, 67 logica, 0 servidor, 0 dados, 3 estilo)
- **Tem servidor (rotas /api):** não — dá para ser só HTML
- **Peças de fora (bibliotecas):** @capacitor/cli, fs, http, os, path

## 2. Estrutura modular proposta

```
index.html            ← a página; chama os módulos NA ORDEM
css/app.css           ← o visual
js/00-core.js         ← a "locomotiva": cria window.APP (registrar, guardar, avisar)
js/10-ai-code-studio.js← Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite a (era ferramentas/cacabug/ferramentas/ai-code-studio.js)
js/15-analisador-universal.js← Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite a (era ferramentas/cacabug/ferramentas/analisador-universal.js)
js/20-cirurgiao.js    ← Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite a (era ferramentas/cacabug/ferramentas/cirurgiao.js)
js/25-desembrulhar.js ← Ferramenta do Caça-Bug — vinda do Laboratório (16/11) (era ferramentas/cacabug/ferramentas/desembrulhar.js)
js/30-gerador-eas.js  ← Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite a (era ferramentas/cacabug/ferramentas/gerador-eas.js)
js/35-montar.js       ← Monta ferramentas/*.js do Caça-Bug a partir dos HTML originais (sem me (era ferramentas/cacabug/ferramentas/montar.py)
js/40-projeto-lab.js  ← Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite a (era ferramentas/cacabug/ferramentas/projeto-lab.js)
js/45-raiox.js        ← Ferramenta do Caça-Bug — vinda do Laboratório (16/11) (era ferramentas/cacabug/ferramentas/raiox.js)
js/50-triagem.js      ← Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite a (era ferramentas/cacabug/ferramentas/triagem.js)
js/55-zip.js          ← Caça-Bug — 20-zip.js (o mesmo do Mini SK) Lê e cria arquivos .zip SEM  (era ferramentas/cacabug/js/20-zip.js)
js/60-projeto.js      ← Caça-Bug — 30-projeto.js Projetos: importar (.zip, arquivos soltos ou  (era ferramentas/cacabug/js/30-projeto.js)
js/65-ferramentas.js  ← Caça-Bug — 40-ferramentas.js Abre cada ferramenta (Cirurgião, Projeto  (era ferramentas/cacabug/js/40-ferramentas.js)
js/70-organizar.js    ← Caça-Bug — 45-organizar.js Aba 🗂️ Organizar: pega o projeto em uso (a (era ferramentas/cacabug/js/45-organizar.js)
js/75-limpo.js        ← Caça-Bug 1.4 — 46-limpo.js · 🧼 ZIP LIMPO (16/11) Projeto baixado da R (era ferramentas/cacabug/js/46-limpo.js)
js/80-relatorios.js   ← Caça-Bug — 50-relatorios.js 📋 Relatórios guardados: cada análise fica (era ferramentas/cacabug/js/50-relatorios.js)
js/85-comparar.js     ← Caça-Bug — 60-comparar.js ⚖️ Comparar versões: escolha 2 ou mais proje (era ferramentas/cacabug/js/60-comparar.js)
js/90-ia.js           ← Caça-Bug — 70-ia.js · 🤖 IA O MEU CHAT aqui dentro: as suas chaves (Ge (era ferramentas/cacabug/js/70-ia.js)
js/91-terminal.js     ← Caça-Bug 1.4 — 80-terminal.js · 💻 TERMINAL DE VERDADE (16/11) O mesmo (era ferramentas/cacabug/js/80-terminal.js)
js/92-expo-core.js    ← expo-core.js — ☁️ Consertar um projeto EXPO para gerar APK pelo EAS Us (era ferramentas/cacabug/js/lib/expo-core.js)
js/93-organizar-core.js← logica (era ferramentas/cacabug/js/lib/organizar-core.js)
js/94-plano-core.js   ← logica (era ferramentas/cacabug/js/lib/plano-core.js)
js/95-base.js         ← Meu Chat — 00-base.js: peças comuns (MC) (era ferramentas/meu-chat/js/00-base.js)
js/96-banco.js        ← Meu Chat — 10-banco.js: onde tudo fica guardado (IndexedDB do aparelho (era ferramentas/meu-chat/js/10-banco.js)
js/97-nuvem.js        ← Meu Chat — 12-nuvem.js · ☁️ NUVEM (Supabase) — 17/11 - O chat continua (era ferramentas/meu-chat/js/12-nuvem.js)
js/98-provedores.js   ← Meu Chat — 20-provedores.js: conversar com as IAs (Gemini, Groq, OpenR (era ferramentas/meu-chat/js/20-provedores.js)
js/98-memoria.js      ← Meu Chat — 30-memoria.js: 🧠 a memória que vai junto em TODA conversa. (era ferramentas/meu-chat/js/30-memoria.js)
js/98-contextos.js    ← Meu Chat — 33-contextos.js: 📌 CONTEXTOS — "cartões" de assunto que vo (era ferramentas/meu-chat/js/33-contextos.js)
js/98-guia.js         ← 🧭 Painel do Guia (16/11): o que é cada app do Maikon, a versão atual  (era ferramentas/meu-chat/js/34-guia.js)
js/98-jeito.js        ← Meu Chat — 35-jeito.js: 🎭 O JEITO DE CADA IA. Para não ter "mudança d (era ferramentas/meu-chat/js/35-jeito.js)
js/98-voz.js          ← Meu Chat — 40-voz.js: 🎤 falar (ditado) e 🔊 ouvir a resposta. 🔊 DOIS (era ferramentas/meu-chat/js/40-voz.js)
js/98-internet.js     ← Meu Chat — 50-internet.js: 🌐 pesquisar e 🔗 ler links. - Gemini e Cla (era ferramentas/meu-chat/js/50-internet.js)
js/98-previa.js       ← Meu Chat — 60-previa.js: 👁 ver o código funcionando, na hora. - HTML: (era ferramentas/meu-chat/js/60-previa.js)
js/98-texto.js        ← Meu Chat — 70-texto.js: mostra a resposta da IA bonitinha (negrito, li (era ferramentas/meu-chat/js/70-texto.js)
js/98-chat.js         ← Meu Chat — 80-chat.js: a conversa (mensagens, fotos, mandar, parar, li (era ferramentas/meu-chat/js/80-chat.js)
js/98-config.js       ← Meu Chat — 85-config.js: ⚙️ chaves das IAs, modelo, busca, voz, instru (era ferramentas/meu-chat/js/85-config.js)
js/98-cofre.js        ← Meu Chat — 87-cofre.js: 🔐 Cofre de chaves. Mostra cada chave guardada (era ferramentas/meu-chat/js/87-cofre.js)
js/98-backup.js       ← Meu Chat — 90-backup.js: 💾 backup de tudo (conversas + memória + ajus (era ferramentas/meu-chat/js/90-backup.js)
js/98-ponte-lab.js    ← 🔬 Ponte com o Laboratório: quando o Meu Chat está DENTRO do Laboratór (era ferramentas/meu-chat/js/95-ponte-lab.js)
js/98-cofre-arquivo.js← 🔐 Arquivo de chaves do Maikon — o MESMO formato no Mini SK, no Meu Ch (era ferramentas/meu-chat/js/lib/cofre-arquivo.js)
js/98-guia-maikon.js  ← 🧭 Guia das ferramentas do Maikon — o MESMO texto em todos os apps (Mi (era ferramentas/meu-chat/js/lib/guia-maikon.js)
js/98-guia-versoes.js ← 🧭 Guia das VERSÕES — o que é cada app do Maikon, qual a versão atual, (era ferramentas/meu-chat/js/lib/guia-versoes.js)
js/98-nuvem-neon.js   ← 🐘 Nuvem pelo NEON (17/11) — usada pelo Meu Chat e pelo SK Jurídico HT (era ferramentas/meu-chat/js/lib/nuvem-neon.js)
js/98-ia.js           ← Assistente Jurídico — 10-ia.js Fala com a IA. Principal: Google Gemini (era js/10-ia.js)
js/98-voz.js          ← Assistente Jurídico — 12-voz.js 🎤 Ditado (falar e virar texto) e 🔊 l (era js/12-voz.js)
js/98-nuvem.js        ← SK Jurídico HTML — 13-nuvem.js · ☁️ NUVEM (Supabase) — 17/11 - O MESMO (era js/13-nuvem.js)
js/98-importar.js     ← Assistente Jurídico — 15-importar.js Lê arquivos: PDF, Word (.docx), T (era js/15-importar.js)
js/98-internet.js     ← Assistente Jurídico — 16-internet.js 🌐 Pesquisa na internet para QUAL (era js/16-internet.js)
js/98-texto.js        ← Assistente Jurídico — 18-texto.js Transforma o texto que a IA devolve  (era js/18-texto.js)
js/98-processar.js    ← Assistente Jurídico — 20-processar.js ⚡ Processar: cole/abra o texto d (era js/20-processar.js)
js/98-motor.js        ← SK Jurídico HTML — 21-motor.js · ⚙️ O MOTOR DO SEU JURÍDICO (17/11) Os (era js/21-motor.js)
js/98-drive.js        ← Assistente Jurídico — 22-drive.js ☁️ GOOGLE DRIVE DIRETO: manda e busc (era js/22-drive.js)
js/98-regras.js       ← Assistente Jurídico — 25-regras.js 📜 O "cérebro" do seu escritório, q (era js/25-regras.js)
js/98-editor.js       ← Assistente Jurídico — 30-editor.js ✏️ Editor com formatação de verdade (era js/30-editor.js)
js/98-docx.js         ← Assistente Jurídico — 35-docx.js ⬇ Word de VERDADE (.docx), feito aqui (era js/35-docx.js)
js/98-conversa.js     ← Assistente Jurídico — 40-conversa.js 💬 Conversa com a IA sobre o caso (era js/40-conversa.js)
js/98-documentos.js   ← Assistente Jurídico — 50-documentos.js 📁 Documentos salvos no aparelh (era js/50-documentos.js)
js/98-biblioteca.js   ← Assistente Jurídico — 55-biblioteca.js 📐 Modelos (peças prontas com [ (era js/55-biblioteca.js)
js/98-codigos.js      ← Assistente Jurídico — 60-codigos.js 🧪 MEUS CÓDIGOS: playground que GU (era js/60-codigos.js)
js/98-ferramentas.js  ← Assistente Jurídico — 70-ferramentas.js 🧰 As ferramentas que já funci (era js/70-ferramentas.js)
js/98-config.js       ← Assistente Jurídico — 80-config.js ⚙️ Chave da IA (Gemini grátis + Gro (era js/80-config.js)
js/98-nuvem-neon.js   ← 🐘 Nuvem pelo NEON (17/11) — usada pelo Meu Chat e pelo SK Jurídico HT (era js/lib/nuvem-neon.js)
js/98-voz-francisco.js← !/usr/bin/env python3 -*- coding: utf-8 -*- (era kits/voz-francisco.py)
js/98-banco-neon.js   ← Banco de Dados (Neon) — 🗄 Banco de Dados (Neon) (era ferramentas/banco-neon.html)
js/98-cacabug.js      ← Caça-Bug (era ferramentas/cacabug/index.html)
js/98-calculadora-sentenca.js← Calculadora da Sentença — Memória de cálculo (era ferramentas/calculadora-sentenca.html)
js/98-colador.js      ← Colador de Links — 🔗 Colador de Links (era ferramentas/colador.html)
js/98-colecionador.js ← Colecionador de Comandos (era ferramentas/colecionador.html)
js/98-comparador.js   ← Comparador de Versões — ⚖️ Comparador de Versões (era ferramentas/comparador.html)
js/98-comunicacoes.js ← Comunicações Processuais — ⚖️ Comunicações Processuais (era ferramentas/comunicacoes.html)
js/98-extrator.js     ← Extrator de Sites — 🛠️ Extrator de Sites (era ferramentas/extrator.html)
js/98-juntador.js     ← Juntador de Arquivos — 🧩 Juntador de Arquivos (era ferramentas/juntador.html)
js/98-laboratorio.js  ← Laboratório HTML — Advocacia Previdenciária (era ferramentas/laboratorio.html)
js/98-limpador.js     ← Limpador de Processos — Limpador de Processos (era ferramentas/limpador.html)
js/98-meu-chat.js     ← Meu Chat (era ferramentas/meu-chat/index.html)
js/98-organizador.js  ← Organizador de Documentos — 📑 Organizador de Documentos (era ferramentas/organizador.html)
js/98-perito.js       ← Perito de Metadados — Perito de Metadados (era ferramentas/perito.html)
js/98-verificador-citacoes.js← Verificador de Citações (era ferramentas/verificador-citacoes.html)
js/98-inicio.js       ← SK Jurídico HTML (era index.html)
js/99-app.js          ← o último: monta a tela com o que embarcou
```

## 3. As partes, uma por uma

| # | Era | Vira | Tipo | O que faz | Usa |
|---|---|---|---|---|---|
| 1 | `ferramentas/cacabug/ferramentas/ai-code-studio.js` | `js/10-ai-code-studio.js` | logica | Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o origina | — |
| 2 | `ferramentas/cacabug/ferramentas/analisador-universal.js` | `js/15-analisador-universal.js` | logica | Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o origina | — |
| 3 | `ferramentas/cacabug/ferramentas/cirurgiao.js` | `js/20-cirurgiao.js` | logica | Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o origina | — |
| 4 | `ferramentas/cacabug/ferramentas/desembrulhar.js` | `js/25-desembrulhar.js` | logica | Ferramenta do Caça-Bug — vinda do Laboratório (16/11) | — |
| 5 | `ferramentas/cacabug/ferramentas/gerador-eas.js` | `js/30-gerador-eas.js` | logica | Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o origina | — |
| 6 | `ferramentas/cacabug/ferramentas/montar.py` | `js/35-montar.js` | logica | Monta ferramentas/*.js do Caça-Bug a partir dos HTML originais (sem mexer neles). Uso: pyt | — |
| 7 | `ferramentas/cacabug/ferramentas/projeto-lab.js` | `js/40-projeto-lab.js` | logica | Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o origina | — |
| 8 | `ferramentas/cacabug/ferramentas/raiox.js` | `js/45-raiox.js` | logica | Ferramenta do Caça-Bug — vinda do Laboratório (16/11) | — |
| 9 | `ferramentas/cacabug/ferramentas/triagem.js` | `js/50-triagem.js` | logica | Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o origina | — |
| 10 | `ferramentas/cacabug/js/00-core.js` | css/app.css | logica | Caça-Bug — 00-core.js (a mesma base do Mini SK, com banco próprio) Base de tudo: atalhos,  | — |
| 11 | `ferramentas/cacabug/js/20-zip.js` | `js/55-zip.js` | logica | Caça-Bug — 20-zip.js (o mesmo do Mini SK) Lê e cria arquivos .zip SEM biblioteca externa ( | — |
| 12 | `ferramentas/cacabug/js/30-projeto.js` | `js/60-projeto.js` | logica | Caça-Bug — 30-projeto.js Projetos: importar (.zip, arquivos soltos ou pasta), guardar no a | — |
| 13 | `ferramentas/cacabug/js/40-ferramentas.js` | `js/65-ferramentas.js` | logica | Caça-Bug — 40-ferramentas.js Abre cada ferramenta (Cirurgião, Projeto Lab, Triagem, Perito | — |
| 14 | `ferramentas/cacabug/js/45-organizar.js` | `js/70-organizar.js` | logica | Caça-Bug — 45-organizar.js Aba 🗂️ Organizar: pega o projeto em uso (aquela pasta "embolad | — |
| 15 | `ferramentas/cacabug/js/46-limpo.js` | `js/75-limpo.js` | logica | Caça-Bug 1.4 — 46-limpo.js · 🧼 ZIP LIMPO (16/11) Projeto baixado da Replit vem com tudo:  | — |
| 16 | `ferramentas/cacabug/js/50-relatorios.js` | `js/80-relatorios.js` | logica | Caça-Bug — 50-relatorios.js 📋 Relatórios guardados: cada análise fica salva no aparelho,  | — |
| 17 | `ferramentas/cacabug/js/60-comparar.js` | `js/85-comparar.js` | logica | Caça-Bug — 60-comparar.js ⚖️ Comparar versões: escolha 2 ou mais projetos guardados e veja | — |
| 18 | `ferramentas/cacabug/js/70-ia.js` | `js/90-ia.js` | logica | Caça-Bug — 70-ia.js · 🤖 IA O MEU CHAT aqui dentro: as suas chaves (Gemini, Groq, OpenRout | — |
| 19 | `ferramentas/cacabug/js/80-terminal.js` | `js/91-terminal.js` | logica | Caça-Bug 1.4 — 80-terminal.js · 💻 TERMINAL DE VERDADE (16/11) O mesmo terminal do Laborat | — |
| 20 | `ferramentas/cacabug/js/99-app.js` | css/app.css | logica | Caça-Bug — 99-app.js Liga tudo: abas de baixo, tela de Projetos e tela de Diagnóstico | — |
| 21 | `ferramentas/cacabug/js/lib/expo-core.js` | `js/92-expo-core.js` | logica | expo-core.js — ☁️ Consertar um projeto EXPO para gerar APK pelo EAS Usado pelo Caça-Bug (D | app.json |
| 22 | `ferramentas/cacabug/js/lib/organizar-core.js` | `js/93-organizar-core.js` | logica | base, dir, ext, norm | — |
| 23 | `ferramentas/cacabug/js/lib/plano-core.js` | `js/94-plano-core.js` | logica | ext, uniq, normRota, arvore | — |
| 24 | `ferramentas/meu-chat/js/00-base.js` | `js/95-base.js` | logica | Meu Chat — 00-base.js: peças comuns (MC) | — |
| 25 | `ferramentas/meu-chat/js/10-banco.js` | `js/96-banco.js` | logica | Meu Chat — 10-banco.js: onde tudo fica guardado (IndexedDB do aparelho — não some ao fecha | — |
| 26 | `ferramentas/meu-chat/js/12-nuvem.js` | `js/97-nuvem.js` | logica | Meu Chat — 12-nuvem.js · ☁️ NUVEM (Supabase) — 17/11 - O chat continua funcionando SEM int | — |
| 27 | `ferramentas/meu-chat/js/20-provedores.js` | `js/98-provedores.js` | logica | Meu Chat — 20-provedores.js: conversar com as IAs (Gemini, Groq, OpenRouter, OpenAI, DeepS | — |
| 28 | `ferramentas/meu-chat/js/30-memoria.js` | `js/98-memoria.js` | logica | Meu Chat — 30-memoria.js: 🧠 a memória que vai junto em TODA conversa. A IA guarda sozinha | — |
| 29 | `ferramentas/meu-chat/js/33-contextos.js` | `js/98-contextos.js` | logica | Meu Chat — 33-contextos.js: 📌 CONTEXTOS — "cartões" de assunto que você LIGA e DESLIGA. D | — |
| 30 | `ferramentas/meu-chat/js/34-guia.js` | `js/98-guia.js` | logica | 🧭 Painel do Guia (16/11): o que é cada app do Maikon, a versão atual e COMO USAR, passo a | — |
| 31 | `ferramentas/meu-chat/js/35-jeito.js` | `js/98-jeito.js` | logica | Meu Chat — 35-jeito.js: 🎭 O JEITO DE CADA IA. Para não ter "mudança drástica" quando troc | — |
| 32 | `ferramentas/meu-chat/js/40-voz.js` | `js/98-voz.js` | logica | Meu Chat — 40-voz.js: 🎤 falar (ditado) e 🔊 ouvir a resposta. 🔊 DOIS "motores" de voz (⚙ | — |
| 33 | `ferramentas/meu-chat/js/50-internet.js` | `js/98-internet.js` | logica | Meu Chat — 50-internet.js: 🌐 pesquisar e 🔗 ler links. - Gemini e Claude pesquisam sozinh | — |
| 34 | `ferramentas/meu-chat/js/60-previa.js` | `js/98-previa.js` | logica | Meu Chat — 60-previa.js: 👁 ver o código funcionando, na hora. - HTML: abre a página como  | — |
| 35 | `ferramentas/meu-chat/js/70-texto.js` | `js/98-texto.js` | logica | Meu Chat — 70-texto.js: mostra a resposta da IA bonitinha (negrito, listas, links, blocos  | — |
| 36 | `ferramentas/meu-chat/js/80-chat.js` | `js/98-chat.js` | logica | Meu Chat — 80-chat.js: a conversa (mensagens, fotos, mandar, parar, lista de conversas). C | — |
| 37 | `ferramentas/meu-chat/js/85-config.js` | `js/98-config.js` | logica | Meu Chat — 85-config.js: ⚙️ chaves das IAs, modelo, busca, voz, instruções, tema | — |
| 38 | `ferramentas/meu-chat/js/87-cofre.js` | `js/98-cofre.js` | logica | Meu Chat — 87-cofre.js: 🔐 Cofre de chaves. Mostra cada chave guardada (👁 ver, 📋 copiar) | — |
| 39 | `ferramentas/meu-chat/js/90-backup.js` | `js/98-backup.js` | logica | Meu Chat — 90-backup.js: 💾 backup de tudo (conversas + memória + ajustes) e restaurar SEM | — |
| 40 | `ferramentas/meu-chat/js/95-ponte-lab.js` | `js/98-ponte-lab.js` | logica | 🔬 Ponte com o Laboratório: quando o Meu Chat está DENTRO do Laboratório (aba 🤖 IA), o La | — |
| 41 | `ferramentas/meu-chat/js/99-app.js` | css/app.css | logica | Meu Chat — 99-app.js: liga tudo quando abre | — |
| 42 | `ferramentas/meu-chat/js/lib/cofre-arquivo.js` | `js/98-cofre-arquivo.js` | logica | 🔐 Arquivo de chaves do Maikon — o MESMO formato no Mini SK, no Meu Chat e no que vier dep | — |
| 43 | `ferramentas/meu-chat/js/lib/guia-maikon.js` | `js/98-guia-maikon.js` | logica | 🧭 Guia das ferramentas do Maikon — o MESMO texto em todos os apps (Mini SK, Meu Chat…). A | — |
| 44 | `ferramentas/meu-chat/js/lib/guia-versoes.js` | `js/98-guia-versoes.js` | logica | 🧭 Guia das VERSÕES — o que é cada app do Maikon, qual a versão atual, e COMO USAR (passo  | — |
| 45 | `ferramentas/meu-chat/js/lib/nuvem-neon.js` | `js/98-nuvem-neon.js` | logica | 🐘 Nuvem pelo NEON (17/11) — usada pelo Meu Chat e pelo SK Jurídico HTML. Você cola o ende | — |
| 46 | `js/00-core.js` | css/app.css | logica | Assistente Jurídico — 00-core.js  (A LOCOMOTIVA: vem primeiro) Cria o "caixa comum" J que  | — |
| 47 | `js/10-ia.js` | `js/98-ia.js` | logica | Assistente Jurídico — 10-ia.js Fala com a IA. Principal: Google Gemini (chave grátis, AIza | — |
| 48 | `js/12-voz.js` | `js/98-voz.js` | logica | Assistente Jurídico — 12-voz.js 🎤 Ditado (falar e virar texto) e 🔊 leitura em voz NATURA | — |
| 49 | `js/13-nuvem.js` | `js/98-nuvem.js` | logica | SK Jurídico HTML — 13-nuvem.js · ☁️ NUVEM (Supabase) — 17/11 - O MESMO LOGIN e o MESMO Sup | — |
| 50 | `js/15-importar.js` | `js/98-importar.js` | logica | Assistente Jurídico — 15-importar.js Lê arquivos: PDF, Word (.docx), TXT, MD, RTF, HTML. P | — |
| 51 | `js/16-internet.js` | `js/98-internet.js` | logica | Assistente Jurídico — 16-internet.js 🌐 Pesquisa na internet para QUALQUER IA (Ollama, Gro | — |
| 52 | `js/18-texto.js` | `js/98-texto.js` | logica | Assistente Jurídico — 18-texto.js Transforma o texto que a IA devolve (com ##, **negrito** | — |
| 53 | `js/20-processar.js` | `js/98-processar.js` | logica | Assistente Jurídico — 20-processar.js ⚡ Processar: cole/abra o texto do processo → escolha | — |
| 54 | `js/21-motor.js` | `js/98-motor.js` | logica | SK Jurídico HTML — 21-motor.js · ⚙️ O MOTOR DO SEU JURÍDICO (17/11) Os textos abaixo viera | — |
| 55 | `js/22-drive.js` | `js/98-drive.js` | logica | Assistente Jurídico — 22-drive.js ☁️ GOOGLE DRIVE DIRETO: manda e busca arquivos na SUA co | — |
| 56 | `js/25-regras.js` | `js/98-regras.js` | logica | Assistente Jurídico — 25-regras.js 📜 O "cérebro" do seu escritório, que cresce com o temp | — |
| 57 | `js/30-editor.js` | `js/98-editor.js` | logica | Assistente Jurídico — 30-editor.js ✏️ Editor com formatação de verdade (folha A4, padrão A | — |
| 58 | `js/35-docx.js` | `js/98-docx.js` | logica | Assistente Jurídico — 35-docx.js ⬇ Word de VERDADE (.docx), feito aqui no aparelho, sem in | — |
| 59 | `js/40-conversa.js` | `js/98-conversa.js` | logica | Assistente Jurídico — 40-conversa.js 💬 Conversa com a IA sobre o caso — por texto ou por  | — |
| 60 | `js/50-documentos.js` | `js/98-documentos.js` | logica | Assistente Jurídico — 50-documentos.js 📁 Documentos salvos no aparelho + 🕐 histórico do  | — |
| 61 | `js/55-biblioteca.js` | `js/98-biblioteca.js` | logica | Assistente Jurídico — 55-biblioteca.js 📐 Modelos (peças prontas com [CAMPOS]) e 📚 Ementa | — |
| 62 | `js/60-codigos.js` | `js/98-codigos.js` | logica | Assistente Jurídico — 60-codigos.js 🧪 MEUS CÓDIGOS: playground que GUARDA. Para os seus c | — |
| 63 | `js/70-ferramentas.js` | `js/98-ferramentas.js` | logica | Assistente Jurídico — 70-ferramentas.js 🧰 As ferramentas que já funcionam, cada uma no se | — |
| 64 | `js/80-config.js` | `js/98-config.js` | logica | Assistente Jurídico — 80-config.js ⚙️ Chave da IA (Gemini grátis + Groq de reserva), voz,  | — |
| 65 | `js/99-app.js` | css/app.css | logica | Assistente Jurídico — 99-app.js  (O ÚLTIMO VAGÃO: vem por último) Monta cada módulo na sua | — |
| 66 | `js/lib/nuvem-neon.js` | `js/98-nuvem-neon.js` | logica | 🐘 Nuvem pelo NEON (17/11) — usada pelo Meu Chat e pelo SK Jurídico HTML. Você cola o ende | — |
| 67 | `kits/voz-francisco.py` | `js/98-voz-francisco.js` | logica | !/usr/bin/env python3 -*- coding: utf-8 -*- | — |
| 68 | `ferramentas/banco-neon.html` | `js/98-banco-neon.js` | tela | Banco de Dados (Neon) — 🗄 Banco de Dados (Neon) | — |
| 69 | `ferramentas/cacabug/css/app.css` | css/app.css | estilo | Caça-Bug — aparência. Cores do Mini SK (escuro), letras legíveis no celular | — |
| 70 | `ferramentas/cacabug/index.html` | `js/98-cacabug.js` | tela | Caça-Bug | manifest.json, icon-192.png, app.css, 00-core.js |
| 71 | `ferramentas/calculadora-sentenca.html` | `js/98-calculadora-sentenca.js` | tela | Calculadora da Sentença — Memória de cálculo | — |
| 72 | `ferramentas/colador.html` | `js/98-colador.js` | tela | Colador de Links — 🔗 Colador de Links | manifest.json |
| 73 | `ferramentas/colecionador.html` | `js/98-colecionador.js` | tela | Colecionador de Comandos | — |
| 74 | `ferramentas/comparador.html` | `js/98-comparador.js` | tela | Comparador de Versões — ⚖️ Comparador de Versões | — |
| 75 | `ferramentas/comunicacoes.html` | `js/98-comunicacoes.js` | tela | Comunicações Processuais — ⚖️ Comunicações Processuais | — |
| 76 | `ferramentas/extrator.html` | `js/98-extrator.js` | tela | Extrator de Sites — 🛠️ Extrator de Sites | — |
| 77 | `ferramentas/juntador.html` | `js/98-juntador.js` | tela | Juntador de Arquivos — 🧩 Juntador de Arquivos | — |
| 78 | `ferramentas/laboratorio.html` | `js/98-laboratorio.js` | tela | Laboratório HTML — Advocacia Previdenciária | — |
| 79 | `ferramentas/limpador.html` | `js/98-limpador.js` | tela | Limpador de Processos — Limpador de Processos | — |
| 80 | `ferramentas/meu-chat/css/app.css` | css/app.css | estilo | — | — |
| 81 | `ferramentas/meu-chat/index.html` | `js/98-meu-chat.js` | tela | Meu Chat | manifest.json, icon-192.png, app.css, 00-base.js |
| 82 | `ferramentas/organizador.html` | `js/98-organizador.js` | tela | Organizador de Documentos — 📑 Organizador de Documentos | — |
| 83 | `ferramentas/perito.html` | `js/98-perito.js` | tela | Perito de Metadados — Perito de Metadados | — |
| 84 | `ferramentas/verificador-citacoes.html` | `js/98-verificador-citacoes.js` | tela | Verificador de Citações | — |
| 85 | `css/app.css` | css/app.css | estilo | Assistente Jurídico — visual: azul-tinta e papel. Feito para o celular primeiro | — |
| 86 | `index.html` | `js/98-inicio.js` | tela | SK Jurídico HTML | manifest.json, icon-192.png, app.css, jszip.min.js |

## 4. Montar passo a passo (cada bloco é um pedido pronto: 📋 Copiar → colar na IA)

### Passo 0 — combinar as regras com a IA

```text
Vamos recriar o app "Caça-Bug" como HTML MODULAR, que abre pelo index.html, sem servidor e sem nada da Replit.
Regras: (1) index.html chama os arquivos js/ na ordem, antes do </body>; (2) js/00-core.js cria window.APP com APP.registrar(modulo), APP.guardar(chave, valor) em IndexedDB/localStorage e APP.avisar(texto); (3) cada arquivo js/NN-nome.js cuida de UM assunto, começa com (function (APP) { e termina com })(window.APP); (4) js/99-app.js vem por último e monta a tela com os módulos registrados; (5) textos em português do Brasil.
Vou pedir UM arquivo por vez. Responda só com o arquivo completo, sem cortar nada. Primeiro: crie index.html, css/app.css e js/00-core.js.
```

### Passo 1 — `js/10-ai-code-studio.js` (era `ferramentas/cacabug/ferramentas/ai-code-studio.js`, 3 linhas)

```text
Crie js/10-ai-code-studio.js. Ele faz: Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o original e rode montar.py).
No app original ele tinha estas funções/partes: est, uid, isMobile, escapeHtml, copyText, activeConv, MODULE_Storage, save, saveSoon, load, normMemory, stamp, download, exportAll, importBackup, handleImport, MODULE_Provider, models.
Ele chamava estes endereços: https://api.anthropic.com/v1/messages, https://api.anthropic.com/v1/models?limit=100, https://google.serper.dev/search. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 2 — `js/15-analisador-universal.js` (era `ferramentas/cacabug/ferramentas/analisador-universal.js`, 3 linhas)

```text
Crie js/15-analisador-universal.js. Ele faz: Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o original e rode montar.py).
No app original ele tinha estas funções/partes: handleFileInput, importZip, handleFolderInput, tryDecodeText, renderTree, buildTree, renderNode, countFiles, toggleFolder, expandAll, collapseAll, filterFiles, getFileIcon, formatSize, openFile, closeTab, renderTabs, renderEditor.
O original usava as bibliotecas @capacitor/cli: em HTML puro, use a versão de CDN (ou faça sem ela, se for simples).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 3 — `js/20-cirurgiao.js` (era `ferramentas/cacabug/ferramentas/cirurgiao.js`, 3 linhas)

```text
Crie js/20-cirurgiao.js. Ele faz: Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o original e rode montar.py).
No app original ele tinha estas funções/partes: esc, fmtB, fmtN, usd, agora, pausa, tokensDe, extDe, decode, pareceBinario, inflate, lerZip, CRC, crc32, escreverZip, baixar, copiar, status.
Ele chamava estes endereços: ${c.base}/models/${encodeURIComponent(c.modelo)}:generateContent, ${c.base}/messages, ${c.base}/chat/completions, https://registry.npmjs.org/, https://registry.npmjs.org/-/v1/search?size=20&text=, https://pypi.org/pypi/. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 4 — `js/25-desembrulhar.js` (era `ferramentas/cacabug/ferramentas/desembrulhar.js`, 3 linhas)

```text
Crie js/25-desembrulhar.js. Ele faz: Ferramenta do Caça-Bug — vinda do Laboratório (16/11).
No app original ele tinha estas funções/partes: ehHTML, pareceB64, deB64, tituloDe, procurarNoJS, andar, procurar, rec, desembrulhar, add, tela, rodar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 5 — `js/30-gerador-eas.js` (era `ferramentas/cacabug/ferramentas/gerador-eas.js`, 3 linhas)

```text
Crie js/30-gerador-eas.js. Ele faz: Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o original e rode montar.py).
No app original ele tinha estas funções/partes: switchTab, autoId, atualizar, importarProjeto, preencherDados, gerarTudo, renderArquivos, copiar, exportarZip, fileIcon, esc, escHtml, loadJSZ.
O original usava as bibliotecas @capacitor/cli: em HTML puro, use a versão de CDN (ou faça sem ela, se for simples).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 6 — `js/35-montar.js` (era `ferramentas/cacabug/ferramentas/montar.py`, 81 linhas)

```text
Crie js/35-montar.js. Ele faz: Monta ferramentas/*.js do Caça-Bug a partir dos HTML originais (sem mexer neles). Uso: python3 montar.py   (os originais ficam em /home/claude/cacabug-fontes e /home/claude).
No app original ele tinha estas funções/partes: fim_body, inserir_antes, libs_locais, importFiles.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 7 — `js/40-projeto-lab.js` (era `ferramentas/cacabug/ferramentas/projeto-lab.js`, 3 linhas)

```text
Crie js/40-projeto-lab.js. Ele faz: Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o original e rode montar.py).
No app original ele tinha estas funções/partes: esc, tick, fmtSize, fmtDate, normPath, dirname, basename, extOf, joinPath, hex, inflate, mask, lineFinder, parseLenientJSON, langOf, sniff, zipEntries, parsePax.
Ele chamava estes endereços: https://api.anthropic.com/v1/messages, https://api.anthropic.com/v1/models?limit=100. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 8 — `js/45-raiox.js` (era `ferramentas/cacabug/ferramentas/raiox.js`, 3 linhas)

```text
Crie js/45-raiox.js. Ele faz: Ferramenta do Caça-Bug — vinda do Laboratório (16/11).
No app original ele tinha estas funções/partes: mascara, examinar, tam, tem, inflar, textoAscii, examinarExe, busca, temTexto, tela, mostrar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 9 — `js/50-triagem.js` (era `ferramentas/cacabug/ferramentas/triagem.js`, 3 linhas)

```text
Crie js/50-triagem.js. Ele faz: Ferramenta do Caça-Bug — gerada a partir do HTML original (não edite aqui; edite o original e rode montar.py).
No app original ele tinha estas funções/partes: renderLista, abrirConversa, conversaAtiva, renderMensagens, enviarMensagem, formatarHora, salvar, extOf, normPath, findPaths, compatible, sniffType, looksWindows, extForType, fnNames, computeSig, jaccard, speakerOf.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 10 — `js/55-zip.js` (era `ferramentas/cacabug/js/20-zip.js`, 120 linhas)

```text
Crie js/55-zip.js. Ele faz: Caça-Bug — 20-zip.js (o mesmo do Mini SK) Lê e cria arquivos .zip SEM biblioteca externa (funciona offline). Usa o descompactador que já vem no navegador (DecompressionStream).
No app original ele tinha estas funções/partes: CRC_TABLE, crc32, streamThrough, read, write.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 11 — `js/60-projeto.js` (era `ferramentas/cacabug/js/30-projeto.js`, 215 linhas)

```text
Crie js/60-projeto.js. Ele faz: Caça-Bug — 30-projeto.js Projetos: importar (.zip, arquivos soltos ou pasta), guardar no aparelho, escolher o projeto ativo e fazer o DIAGNÓSTICO RÁPIDO: - que tipo de projeto é (Replit, Vite/React, Expo, Capacitor, servidor, PWA);.
No app original ele tinha estas funções/partes: listar, pegar, entradasDe, guardar, escolher, apagar, arquivoZip, semExt, importarArquivos, texto, raizComum, mascara, examinarIndex, diagnostico, tem, consertarCaminhos.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 12 — `js/65-ferramentas.js` (era `ferramentas/cacabug/js/40-ferramentas.js`, 136 linhas)

```text
Crie js/65-ferramentas.js. Ele faz: Caça-Bug — 40-ferramentas.js Abre cada ferramenta (Cirurgião, Projeto Lab, Triagem, Perito…) DENTRO do app, sem mexer no jeito delas funcionarem: - entrega o projeto ativo automaticamente (não precisa importar de novo);.
No app original ele tinha estas funções/partes: REG, baixar, tenta, comKit, lista, porId, esperarHub, olha, criarFrame, noFrame, alimentar, abrir, abrirComparacao, guardarRelatorio, montarLista.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 13 — `js/70-organizar.js` (era `ferramentas/cacabug/js/45-organizar.js`, 54 linhas)

```text
Crie js/70-organizar.js. Ele faz: Caça-Bug — 45-organizar.js Aba 🗂️ Organizar: pega o projeto em uso (aquela pasta "embolada") e devolve tudo separado — usa js/lib/organizar-core.js.
No app original ele tinha estas funções/partes: montar, analisar, num, zipar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 14 — `js/75-limpo.js` (era `ferramentas/cacabug/js/46-limpo.js`, 92 linhas)

```text
Crie js/75-limpo.js. Ele faz: Caça-Bug 1.4 — 46-limpo.js · 🧼 ZIP LIMPO (16/11) Projeto baixado da Replit vem com tudo: node_modules, .git, .cache, .local, .upm, restos da Replit, logs… e às vezes senhas (.env). Aqui você escolhe o que tirar e o Caça-Bug guarda uma CÓPIA limpa. O original NUNCA muda.
No app original ele tinha estas funções/partes: raizDe, medir, abrir, marcados, conta, gerar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 15 — `js/80-relatorios.js` (era `ferramentas/cacabug/js/50-relatorios.js`, 50 linhas)

```text
Crie js/80-relatorios.js. Ele faz: Caça-Bug — 50-relatorios.js 📋 Relatórios guardados: cada análise fica salva no aparelho, com data, ferramenta e projeto. Não some quando você sai da ferramenta. Abrir · copiar · baixar · mandar (Drive/WhatsApp) · apagar.
No app original ele tinha estas funções/partes: guardar, listar, nomeArq, cabecalho, montar, zipTodos.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 16 — `js/85-comparar.js` (era `ferramentas/cacabug/js/60-comparar.js`, 244 linhas)

```text
Crie js/85-comparar.js. Ele faz: Caça-Bug — 60-comparar.js ⚖️ Comparar versões: escolha 2 ou mais projetos guardados e veja - a tabela de RECURSOS por versão (IA, voz, PDF, Word, DJEN…) ✓ / — - arquivos: só numa, só na outra, mudaram, iguais.
No app original ele tinha estas funções/partes: raizComum, indice, difLinhas, soEm, comparar, textoRelatorio, bloco, montar, html, det, ligar, verDiferenca, mostra.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 17 — `js/90-ia.js` (era `ferramentas/cacabug/js/70-ia.js`, 78 linhas)

```text
Crie js/90-ia.js. Ele faz: Caça-Bug — 70-ia.js · 🤖 IA O MEU CHAT aqui dentro: as suas chaves (Gemini, Groq, OpenRouter…), o 🦙 Ollama sozinho quando estiver ligado (no PC ou no Termux), voz, internet e fotos. Os botões 📎 colocam na caixa do chat o DIAGNÓSTICO, o PLANO, um RELATÓRIO.
No app original ele tinha estas funções/partes: quadro, mandar, esconderChaves, colar, precisaProjeto, acao, escolher, pintar, montar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 18 — `js/91-terminal.js` (era `ferramentas/cacabug/js/80-terminal.js`, 471 linhas)

```text
Crie js/91-terminal.js. Ele faz: Caça-Bug 1.4 — 80-terminal.js · 💻 TERMINAL DE VERDADE (16/11) O mesmo terminal do Laboratório (o que não cai): ▶ Ligar tudo · 🚀 Rodar · ⏹ Parar · 🦙 Ollama · 🗣 Voz Francisco · 🧰 Verificar e instalar · 🩺 Terminal parado? + 🔎 Análise (git log/diff, achar lixo, arquivos grandes, pacotes sem uso) e 🧼 Zip limpo.
No app original ele tinha estas funções/partes: espera, status, pst, carregarScript, carregarCss, prepararTela, escreverTela, enviar, tamanho, ligado, conectar, desconectar, copiar, nome, dentro, responder, corpo, andar.
O original usava as bibliotecas http, fs, path, os: em HTML puro, use a versão de CDN (ou faça sem ela, se for simples).
Ele chamava estes endereços: ferramentas/meu-chat/voz-francisco.py. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 19 — `js/92-expo-core.js` (era `ferramentas/cacabug/js/lib/expo-core.js`, 192 linhas)

```text
Crie js/92-expo-core.js. Ele faz: expo-core.js — ☁️ Consertar um projeto EXPO para gerar APK pelo EAS Usado pelo Caça-Bug (Diagnóstico) e pelo Mini SK (painel ☁️ EAS). Junta o que os geradores antigos faziam separado (app.json, eas.json, autorizações, receita do GitHub) + limpeza da Replit, numa passada só.
No app original ele tinha estas funções/partes: json, raizDe, slugDe, ler, permissoes, tem, consertar, existe, tirarImg, limpa, base.
O original usava as bibliotecas fs: em HTML puro, use a versão de CDN (ou faça sem ela, se for simples).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 20 — `js/93-organizar-core.js` (era `ferramentas/cacabug/js/lib/organizar-core.js`, 347 linhas)

```text
Crie js/93-organizar-core.js. Ele é uma parte de logica do app.
No app original ele tinha estas funções/partes: base, dir, ext, norm, slug, chaveConteudo, hash, assuntoDe, incompleto, ehModuloES, sintaxe, conversaColada, tentarConsertar, resumo, cortar, add, analisar, relatorio.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 21 — `js/94-plano-core.js` (era `ferramentas/cacabug/js/lib/plano-core.js`, 171 linhas)

```text
Crie js/94-plano-core.js. Ele é uma parte de logica do app.
No app original ele tinha estas funções/partes: ext, uniq, normRota, arvore, andar, gerar, chave, dedup, temRota, tem, markdown, tab.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 22 — `js/95-base.js` (era `ferramentas/meu-chat/js/00-base.js`, 43 linhas)

```text
Crie js/95-base.js. Ele faz: Meu Chat — 00-base.js: peças comuns (MC).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 23 — `js/96-banco.js` (era `ferramentas/meu-chat/js/10-banco.js`, 26 linhas)

```text
Crie js/96-banco.js. Ele faz: Meu Chat — 10-banco.js: onde tudo fica guardado (IndexedDB do aparelho — não some ao fechar).
No app original ele tinha estas funções/partes: abrir, req, loja.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 24 — `js/97-nuvem.js` (era `ferramentas/meu-chat/js/12-nuvem.js`, 280 linhas)

```text
Crie js/97-nuvem.js. Ele faz: Meu Chat — 12-nuvem.js · ☁️ NUVEM (Supabase) — 17/11 - O chat continua funcionando SEM internet: tudo fica no aparelho (IndexedDB). - Com a nuvem ligada, ele COPIA para o Supabase e traz de volta em qualquer aparelho (celular, PC, outro celular) entrando com o mesmo e-mail e senha.
No app original ele tinha estas funções/partes: cfg, sessao, ehNeon, neonConn, logado, ligada, auth, traduzir, guardarSessao, token, rest, mod, horaUnica, marcar, ganchos, marcarPrefs, prefsViajam, semFotos.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 25 — `js/98-provedores.js` (era `ferramentas/meu-chat/js/20-provedores.js`, 240 linhas)

```text
Crie js/98-provedores.js. Ele faz: Meu Chat — 20-provedores.js: conversar com as IAs (Gemini, Groq, OpenRouter, OpenAI, DeepSeek, Claude). - Várias chaves; quando uma acaba (limite/cota), passa sozinho para a próxima ("revezar"). - Busca a lista de modelos de verdade na hora de testar a chave (nada de nome velho chumbado). - As chaves ficam SÓ neste aparelho.
No app original ele tinha estas funções/partes: detectar, procurarOllama, chaves, salvarChaves, pontoGemini, listarModelos, pontoLivre, geracao, modeloDe, testarChave, erroLegivel, corsAviso, ehLimite, cabAnthropic, lerSSE, pedir, parcial, conversar.
Ele chamava estes endereços: http://127.0.0.1:11434/api/tags. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 26 — `js/98-memoria.js` (era `ferramentas/meu-chat/js/30-memoria.js`, 77 linhas)

```text
Crie js/98-memoria.js. Ele faz: Meu Chat — 30-memoria.js: 🧠 a memória que vai junto em TODA conversa. A IA guarda sozinha o que for importante escrevendo [[lembrar: …]] no fim da resposta (o app tira isso do texto, guarda e mostra "🧠 guardei"). [[esquecer: …]] apaga.
No app original ele tinha estas funções/partes: texto, salvar, lembrar, esquecer, aplicarMarcas, guiaParaPergunta, tamanhoTexto, sistema, abrir.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 27 — `js/98-contextos.js` (era `ferramentas/meu-chat/js/33-contextos.js`, 178 linhas)

```text
Crie js/98-contextos.js. Ele faz: Meu Chat — 33-contextos.js: 📌 CONTEXTOS — "cartões" de assunto que você LIGA e DESLIGA. Diferente da 🧠 memória (que vale para sempre e vai em tudo): um contexto é o resumo de um assunto ou de uma conversa (por exemplo, o que você vinha fazendo com o Claude), para a IA não começar do zero. Ligado = vai junto em toda conversa. Desligado = fica guardado, sem gastar.
No app original ele tinha estas funções/partes: lista, gravar, semear, esconder, tokens, ligados, texto, pintarChip, pintar, novo, clique.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 28 — `js/98-guia.js` (era `ferramentas/meu-chat/js/34-guia.js`, 39 linhas)

```text
Crie js/98-guia.js. Ele faz: 🧭 Painel do Guia (16/11): o que é cada app do Maikon, a versão atual e COMO USAR, passo a passo. 🔊 lê em voz alta (voz Francisco ou a do aparelho) · 🤖 Perguntar: o chat explica aquele app.
No app original ele tinha estas funções/partes: textoDe, pintar, iniciar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 29 — `js/98-jeito.js` (era `ferramentas/meu-chat/js/35-jeito.js`, 56 linhas)

```text
Crie js/98-jeito.js. Ele faz: Meu Chat — 35-jeito.js: 🎭 O JEITO DE CADA IA. Para não ter "mudança drástica" quando troca de IA: um jeito de conversar que vale para TODAS (parceiro, calmo, honesto) e, se quiser, um jeito só de uma (ex.: o Perplexity como pesquisador jurídico que sempre traz as fontes). Tudo editável em ⚙️ → 🎭 Jeito de cada IA.
No app original ele tinha estas funções/partes: geral, deUma, texto, pintar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 30 — `js/98-voz.js` (era `ferramentas/meu-chat/js/40-voz.js`, 227 linhas)

```text
Crie js/98-voz.js. Ele faz: Meu Chat — 40-voz.js: 🎤 falar (ditado) e 🔊 ouvir a resposta. 🔊 DOIS "motores" de voz (⚙️ → Voz): - 📱 "Voz do aparelho" (o padrão): funciona com QUALQUER IA (Gemini, Groq, Claude, Ollama…), grátis e sem limite. Você escolhe a voz (as ⭐ são as naturais), a velocidade e o tom.
No app original ele tinha estas funções/partes: podeOuvir, ouvir, parar, marcar, paraFala, pedacos, noPC, motor, temAndroid, temNavegador, natural, vozesAparelho, cfgVoz, falarFrase, enfileirar, verificarFim, pararAparelho, fluxo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 31 — `js/98-internet.js` (era `ferramentas/meu-chat/js/50-internet.js`, 58 linhas)

```text
Crie js/98-internet.js. Ele faz: Meu Chat — 50-internet.js: 🌐 pesquisar e 🔗 ler links. - Gemini e Claude pesquisam sozinhos (a busca vem embutida neles). - As outras IAs: usa a SUA chave de busca (Serper, Tavily ou Brave), se tiver, e manda os resultados junto. - Link na mensagem: o app lê a página (pelo leitor r.jina.ai, grátis) e manda o texto para a IA.
No app original ele tinha estas funções/partes: buscar, lerLink, preparar.
Ele chamava estes endereços: https://google.serper.dev/search, https://api.tavily.com/search, https://api.search.brave.com/res/v1/web/search?count=8&country=BR&search_lang=pt-br&q=, https://r.jina.ai/. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 32 — `js/98-previa.js` (era `ferramentas/meu-chat/js/60-previa.js`, 76 linhas)

```text
Crie js/98-previa.js. Ele faz: Meu Chat — 60-previa.js: 👁 ver o código funcionando, na hora. - HTML: abre a página como ela é. - TSX / JSX (React): monta com React + Babel + Tailwind (pela internet) e mostra o componente. Os erros aparecem embaixo, em vermelho.
No app original ele tinha estas funções/partes: paginaHTML, paginaReact, falha, req, App, tipoDe, abrir.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 33 — `js/98-texto.js` (era `ferramentas/meu-chat/js/70-texto.js`, 45 linhas)

```text
Crie js/98-texto.js. Ele faz: Meu Chat — 70-texto.js: mostra a resposta da IA bonitinha (negrito, listas, links, blocos de código com 📋 copiar, ⤓ baixar e 👁 ver funcionando).
No app original ele tinha estas funções/partes: inline, render, ligar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 34 — `js/98-chat.js` (era `ferramentas/meu-chat/js/80-chat.js`, 252 linhas)

```text
Crie js/98-chat.js. Ele faz: Meu Chat — 80-chat.js: a conversa (mensagens, fotos, mandar, parar, lista de conversas). Cada conversa fica guardada no aparelho. Vai para a IA: a memória + as últimas mensagens.
No app original ele tinha estas funções/partes: nova, abrirConversa, guardar, reduzir, anexar, pintarAnexos, htmlMsg, dedup, hora, pintar, mandar, responder, depois, comparar, juntar, tela, escolherComparar, resumirSePrecisar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 35 — `js/98-config.js` (era `ferramentas/meu-chat/js/85-config.js`, 115 linhas)

```text
Crie js/98-config.js. Ele faz: Meu Chat — 85-config.js: ⚙️ chaves das IAs, modelo, busca, voz, instruções, tema.
No app original ele tinha estas funções/partes: opcoesVoz, pintar, clique, mudou, aplicarTema, abrir.
Ele chamava estes endereços: voz-francisco.py. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 36 — `js/98-cofre.js` (era `ferramentas/meu-chat/js/87-cofre.js`, 94 linhas)

```text
Crie js/98-cofre.js. Ele faz: Meu Chat — 87-cofre.js: 🔐 Cofre de chaves. Mostra cada chave guardada (👁 ver, 📋 copiar) e leva SÓ as chaves para outro app/aparelho num arquivo trancado com senha — o mesmo arquivo do Mini SK (js/lib/cofre-arquivo.js).
No app original ele tinha estas funções/partes: todas, pintar, status, conteudo, baixar, trazer, selarTexto, trazerTexto.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 37 — `js/98-backup.js` (era `ferramentas/meu-chat/js/90-backup.js`, 44 linhas)

```text
Crie js/98-backup.js. Ele faz: Meu Chat — 90-backup.js: 💾 backup de tudo (conversas + memória + ajustes) e restaurar SEM APAGAR NADA.
No app original ele tinha estas funções/partes: gerar, baixar, restaurar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 38 — `js/98-ponte-lab.js` (era `ferramentas/meu-chat/js/95-ponte-lab.js`, 20 linhas)

```text
Crie js/98-ponte-lab.js. Ele faz: 🔬 Ponte com o Laboratório: quando o Meu Chat está DENTRO do Laboratório (aba 🤖 IA), o Laboratório pode mandar texto para a caixa de escrever (o plano do projeto, a memória, a comparação A × B). Só aceita mensagens da própria página (mesmo endereço).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 39 — `js/98-cofre-arquivo.js` (era `ferramentas/meu-chat/js/lib/cofre-arquivo.js`, 61 linhas)

```text
Crie js/98-cofre-arquivo.js. Ele faz: 🔐 Arquivo de chaves do Maikon — o MESMO formato no Mini SK, no Meu Chat e no que vier depois. Guarda SÓ as chaves (IA, GitHub, Expo, pesquisa e "Minhas chaves"), trancadas com uma senha sua (AES-GCM 256 + PBKDF2 com 250 mil voltas — sem a senha, o arquivo não abre). Assim dá para levar as chaves de um app/aparelho para outro sem passar pelo WhatsApp.
No app original ele tinha estas funções/partes: b64, deB64, chaveDaSenha, normal, selar, abrir, contar, mascara.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 40 — `js/98-guia-maikon.js` (era `ferramentas/meu-chat/js/lib/guia-maikon.js`, 118 linhas)

```text
Crie js/98-guia-maikon.js. Ele faz: 🧭 Guia das ferramentas do Maikon — o MESMO texto em todos os apps (Mini SK, Meu Chat…). A IA de cada app lê isto sozinha: assim ela já sabe o que ele tem, para que serve cada coisa, e quando é melhor mandar para outra ferramenta ou "levar para o Claude". Para atualizar: troque este arquivo nos apps (o Claude manda a versão nova junto).
No app original ele tinha estas funções/partes: resumoParaClaude, esconder.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 41 — `js/98-guia-versoes.js` (era `ferramentas/meu-chat/js/lib/guia-versoes.js`, 163 linhas)

```text
Crie js/98-guia-versoes.js. Ele faz: 🧭 Guia das VERSÕES — o que é cada app do Maikon, qual a versão atual, e COMO USAR (passo a passo). Uma fonte só: o painel 🧭 do Meu Chat mostra isto para ele ler, e a IA recebe o mesmo texto (junto do guia-maikon.js) para saber explicar. Atualizado pelo Claude a cada versão nova.
No app original ele tinha estas funções/partes: texto.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 42 — `js/98-nuvem-neon.js` (era `ferramentas/meu-chat/js/lib/nuvem-neon.js`, 73 linhas)

```text
Crie js/98-nuvem-neon.js. Ele faz: 🐘 Nuvem pelo NEON (17/11) — usada pelo Meu Chat e pelo SK Jurídico HTML. Você cola o endereço do banco (a "connection string" postgresql://…) e pronto: o app cria a tabela SOZINHO (não precisa rodar nada em inglês no site do Neon). ⚠ Esse endereço tem a SENHA do banco: fica só no seu aparelho (como uma chave de IA),.
No app original ele tinha estas funções/partes: traduzir, preparar, upsert, listar, conv.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 43 — `js/98-ia.js` (era `js/10-ia.js`, 208 linhas)

```text
Crie js/98-ia.js. Ele faz: Assistente Jurídico — 10-ia.js Fala com a IA. Principal: Google Gemini (chave grátis, AIza… ou AQ.…). Reserva: Groq (grátis, chave gsk_…) — se o Gemini der "limite", troca sozinho. O modelo antigo (gemini-1.5-flash) foi desligado pelo Google: era um dos.
No app original ele tinha estas funções/partes: cfg, salvar, sistemaBase, textoDeErro, gFetch, corpoGemini, gemini, groq, ollama, ollamaInfo, compat, claude, modelosOpenRouter, gerar, modelos.
Ele chamava estes endereços: https://api.anthropic.com/v1/messages, https://openrouter.ai/api/v1/models. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 44 — `js/98-voz.js` (era `js/12-voz.js`, 167 linhas)

```text
Crie js/98-voz.js. Ele faz: Assistente Jurídico — 12-voz.js 🎤 Ditado (falar e virar texto) e 🔊 leitura em voz NATURAL. A voz é a do Gemini (gente de verdade, não robô) — usa a mesma chave grátis. Voz "de robô" do aparelho NUNCA é usada. No navegador Edge, as vozes.
No app original ele tinha estas funções/partes: noPC, cfg, audioFrancisco, francisco, limpar, pedacos, wav, audioGemini, parar, vozesNaturais, nat, falar, fim, ditar, botaoDitado.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 45 — `js/98-nuvem.js` (era `js/13-nuvem.js`, 247 linhas)

```text
Crie js/98-nuvem.js. Ele faz: SK Jurídico HTML — 13-nuvem.js · ☁️ NUVEM (Supabase) — 17/11 - O MESMO LOGIN e o MESMO Supabase do 💬 Meu Chat (entrou num, entrou no outro). - Tudo continua no aparelho (funciona sem internet); a nuvem COPIA e leva para o celular, o PC, outro aparelho.
No app original ele tinha estas funções/partes: MCK, lerMC, gravarMC, cfg, sessao, tipoNuvem, neonConn, ehNeon, logado, ligada, traduzir, auth, guardarSessao, token, rest, mod, horaUnica, marcar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 46 — `js/98-importar.js` (era `js/15-importar.js`, 60 linhas)

```text
Crie js/98-importar.js. Ele faz: Assistente Jurídico — 15-importar.js Lê arquivos: PDF, Word (.docx), TXT, MD, RTF, HTML. PDF e Word usam bibliotecas que vêm da internet só na 1ª vez. Foto/escaneado (precisa de OCR): use a ferramenta 🧹 Limpador.
No app original ele tinha estas funções/partes: pdf, docx, rtf, htmlParaTexto, lerArquivo, escolher.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 47 — `js/98-internet.js` (era `js/16-internet.js`, 51 linhas)

```text
Crie js/98-internet.js. Ele faz: Assistente Jurídico — 16-internet.js 🌐 Pesquisa na internet para QUALQUER IA (Ollama, Groq, Claude, OpenAI…). O Gemini pesquisa sozinho. As outras usam a SUA chave de busca (Serper, Tavily ou Brave, todas com uso grátis) e recebem os resultados junto.
No app original ele tinha estas funções/partes: cfg, buscar, lerLink, preparar.
Ele chamava estes endereços: https://google.serper.dev/search, https://api.tavily.com/search, https://api.search.brave.com/res/v1/web/search?count=8&country=BR&search_lang=pt-br&q=, https://r.jina.ai/. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 48 — `js/98-texto.js` (era `js/18-texto.js`, 77 linhas)

```text
Crie js/98-texto.js. Ele faz: Assistente Jurídico — 18-texto.js Transforma o texto que a IA devolve (com ##, **negrito**, listas) em texto formatado de verdade — para mostrar na tela e para o Editor/Word.
No app original ele tinha estas funções/partes: inline, mdParaHtml, cel, htmlParaTexto, limparHtml, andar, textoParaHtml.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 49 — `js/98-processar.js` (era `js/20-processar.js`, 139 linhas)

```text
Crie js/98-processar.js. Ele faz: Assistente Jurídico — 20-processar.js ⚡ Processar: cole/abra o texto do processo → escolha o que fazer → resultado formatado → Editor, Word, ouvir, salvar ou conversar sobre ele. As ações vieram do "Assistente Jurídico Pro" antigo (mesmos pedidos).
No app original ele tinha estas funções/partes: montar, pintarAcoes, conta, receber, executar, andamento, podar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 50 — `js/98-motor.js` (era `js/21-motor.js`, 63 linhas)

```text
Crie js/98-motor.js. Ele faz: SK Jurídico HTML — 21-motor.js · ⚙️ O MOTOR DO SEU JURÍDICO (17/11) Os textos abaixo vieram PALAVRA POR PALAVRA do servidor do SK Jurídico 1.7.x (server/routes/ai.ts: SYSTEM_PROMPT_BASE, ACTION_PROMPTS e os níveis de esforço). Agora rodam aqui no aparelho, sem servidor: o texto vai direto para a IA que você escolheu.
No app original ele tinha estas funções/partes: montar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 51 — `js/98-drive.js` (era `js/22-drive.js`, 87 linhas)

```text
Crie js/98-drive.js. Ele faz: Assistente Jurídico — 22-drive.js ☁️ GOOGLE DRIVE DIRETO: manda e busca arquivos na SUA conta do Drive, numa pasta "Assistente Jurídico", sem precisar do app do Drive. Precisa de um "ID do cliente" (Client ID) do Google — é de graça, faz uma.
No app original ele tinha estas funções/partes: cfg, salvar, configurado, conectar, api, pasta, enviar, listar, baixar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 52 — `js/98-regras.js` (era `js/25-regras.js`, 115 linhas)

```text
Crie js/98-regras.js. Ele faz: Assistente Jurídico — 25-regras.js 📜 O "cérebro" do seu escritório, que cresce com o tempo, SEM mexer no código: - Regras: como a IA deve escrever e processar (cole quantas quiser; liga/desliga). - Memória: o que a IA deve saber (dados do escritório, preferências, casos).
No app original ele tinha estas funções/partes: adicionarPacote, carregar, paraIA, montar, exportar, pintar, clique.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 53 — `js/98-editor.js` (era `js/30-editor.js`, 133 linhas)

```text
Crie js/98-editor.js. Ele faz: Assistente Jurídico — 30-editor.js ✏️ Editor com formatação de verdade (folha A4, padrão ABNT): negrito, itálico, sublinhado, títulos, citação recuada, alinhamento, recuo da 1ª linha, listas, fonte e tamanho. Baixa em Word (.docx) de verdade.
No app original ele tinha estas funções/partes: montar, voltarSelecao, estilizar, marcarMudou, html, texto, nomeArquivo, paginaHtml, abrir, salvar, iaNaSelecao.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 54 — `js/98-docx.js` (era `js/35-docx.js`, 154 linhas)

```text
Crie js/98-docx.js. Ele faz: Assistente Jurídico — 35-docx.js ⬇ Word de VERDADE (.docx), feito aqui no aparelho, sem internet. Folha A4, margens ABNT (3/3/2/2 cm), Times 12, espaçamento 1,5, recuo de 2,5 cm na 1ª linha, citação recuada 4 cm em 10 pt,.
No app original ele tinha estas funções/partes: tamanhoMeioPonto, run, runs, paragrafo, alinhamento, corpo, bloco, filhos, despeja, gerar, parTimbre, baixar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 55 — `js/98-conversa.js` (era `js/40-conversa.js`, 128 linhas)

```text
Crie js/98-conversa.js. Ele faz: Assistente Jurídico — 40-conversa.js 💬 Conversa com a IA sobre o caso — por texto ou por VOZ. 📎 Contexto: o documento do Editor, o texto do Processar ou um arquivo. 🔁 Modo voz: você fala → a IA responde em voz natural → escuta de novo.
No app original ele tinha estas funções/partes: nova, montar, definirContexto, pintarContexto, listar, pintar, guardar, enviar, escutar, alternarModoVoz, pintarModo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 56 — `js/98-documentos.js` (era `js/50-documentos.js`, 80 linhas)

```text
Crie js/98-documentos.js. Ele faz: Assistente Jurídico — 50-documentos.js 📁 Documentos salvos no aparelho + 🕐 histórico do que a IA fez. Abrir no Editor, baixar em Word, mandar ao Drive, duplicar, apagar. 💾 Backup de tudo num arquivo só (e restaurar em outro aparelho).
No app original ele tinha estas funções/partes: nomeArq, montar, casa, pintar, item, acao, backup, restaurar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 57 — `js/98-biblioteca.js` (era `js/55-biblioteca.js`, 87 linhas)

```text
Crie js/98-biblioteca.js. Ele faz: Assistente Jurídico — 55-biblioteca.js 📐 Modelos (peças prontas com [CAMPOS]) e 📚 Ementas (jurisprudência que VOCÊ guarda — a IA só usa as que você marcar; nada inventado). 🪄 Preencher modelo com o caso: a IA completa os [CAMPOS] com o texto do ⚡ Processar.
No app original ele tinha estas funções/partes: montar, pintarModelos, pintarEmentas, acao.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 58 — `js/98-codigos.js` (era `js/60-codigos.js`, 104 linhas)

```text
Crie js/98-codigos.js. Ele faz: Assistente Jurídico — 60-codigos.js 🧪 MEUS CÓDIGOS: playground que GUARDA. Para os seus códigos jurídicos (calculadoras, modelos em HTML, ferramentas antigas…). Cole ou importe (vários de uma vez, inclusive .zip), rode ao vivo.
No app original ele tinha estas funções/partes: humano, tipoDe, montar, carregar, pintar, abrir, modo, rodar, fechar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 59 — `js/98-ferramentas.js` (era `js/70-ferramentas.js`, 62 linhas)

```text
Crie js/98-ferramentas.js. Ele faz: Assistente Jurídico — 70-ferramentas.js 🧰 As ferramentas que já funcionam, cada uma no seu arquivo (ferramentas/), abertas aqui dentro. Ficam "vivas": trocar de aba não apaga o que estava sendo feito nelas.
No app original ele tinha estas funções/partes: montar, passarChave, abrir.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 60 — `js/98-config.js` (era `js/80-config.js`, 196 linhas)

```text
Crie js/98-config.js. Ele faz: Assistente Jurídico — 80-config.js ⚙️ Chave da IA (Gemini grátis + Groq de reserva), voz, seus dados e regras do escritório (a IA segue sempre). Tudo fica só neste aparelho.
No app original ele tinha estas funções/partes: montar, pintarOutra, salvarO, pintarProv, salvarDr, preencherOl, olMsg, pintarCat, guardarChave, linkBusca, pintarVoz, guardarVoz.
Ele chamava estes endereços: kits/voz-francisco.py. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 61 — `js/98-nuvem-neon.js` (era `js/lib/nuvem-neon.js`, 73 linhas)

```text
Crie js/98-nuvem-neon.js. Ele faz: 🐘 Nuvem pelo NEON (17/11) — usada pelo Meu Chat e pelo SK Jurídico HTML. Você cola o endereço do banco (a "connection string" postgresql://…) e pronto: o app cria a tabela SOZINHO (não precisa rodar nada em inglês no site do Neon). ⚠ Esse endereço tem a SENHA do banco: fica só no seu aparelho (como uma chave de IA),.
No app original ele tinha estas funções/partes: traduzir, preparar, upsert, listar, conv.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 62 — `js/98-voz-francisco.js` (era `kits/voz-francisco.py`, 134 linhas)

```text
Crie js/98-voz-francisco.js. Ele faz: !/usr/bin/env python3 -*- coding: utf-8 -*-.
No app original ele tinha estas funções/partes: _listar, _falar, Voz, _cabecalhos, do_OPTIONS, _json, _pedido, do_GET, do_POST, _tratar, log_message.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 63 — `js/98-banco-neon.js` (era `ferramentas/banco-neon.html`, 250 linhas)

```text
Crie js/98-banco-neon.js. Ele faz: Banco de Dados (Neon) — 🗄 Banco de Dados (Neon).
No app original ele tinha estas funções/partes: mostrarModelo, traduzir, listar, grade, cel, nomeSeguro, ver, baixar, csv, tudoDe, confirmar, rodar, limpo, campo, sqlNova, pintarNc.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 64 — `js/98-cacabug.js` (era `ferramentas/cacabug/index.html`, 76 linhas)

```text
Crie js/98-cacabug.js. Ele faz: Caça-Bug.
Ele usa o que já foi criado em: js/55-zip.js, js/60-projeto.js, js/20-cirurgiao.js, js/40-projeto-lab.js, js/15-analisador-universal.js, js/50-triagem.js, js/30-gerador-eas.js, js/10-ai-code-studio.js, js/45-raiox.js, js/25-desembrulhar.js, js/65-ferramentas.js, js/80-relatorios.js, js/85-comparar.js, js/94-plano-core.js, js/92-expo-core.js, js/93-organizar-core.js, js/70-organizar.js, js/75-limpo.js, js/90-ia.js, js/91-terminal.js (pelo APP).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 65 — `js/98-calculadora-sentenca.js` (era `ferramentas/calculadora-sentenca.html`, 514 linhas)

```text
Crie js/98-calculadora-sentenca.js. Ele faz: Calculadora da Sentença — Memória de cálculo.
No app original ele tinha estas funções/partes: num, brl, pct, ymDe, ymMais, ymLista, ymBR, dataBR, mesesEntre, esc, lerTela, porNaTela, salvar, carregar, mostrarCaixas, codigoJuros, pintarDados, periodo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 66 — `js/98-colador.js` (era `ferramentas/colador.html`, 797 linhas)

```text
Crie js/98-colador.js. Ele faz: Colador de Links — 🔗 Colador de Links.
No app original ele tinha estas funções/partes: uid, ler, gravar, nomeLista, nomeDe, pintar, fixar, tirar, mover, recarregar, pintarJanela, iniciar, montar, salvar, daLista, contar, pintarListas, caixaDe.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 67 — `js/98-colecionador.js` (era `ferramentas/colecionador.html`, 1672 linhas)

```text
Crie js/98-colecionador.js. Ele faz: Colecionador de Comandos.
No app original ele tinha estas funções/partes: req, QR8bitByte, QRBitBuffer, QRPolynomial, QRRSBlock, QRCode, esc, semAcento, uid, toast, ler, salvar, copiar, adivinhar, desenharFiltros, desenhar, cartao, lembrete.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 68 — `js/98-comparador.js` (era `ferramentas/comparador.html`, 389 linhas)

```text
Crie js/98-comparador.js. Ele faz: Comparador de Versões — ⚖️ Comparador de Versões.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 69 — `js/98-comunicacoes.js` (era `ferramentas/comunicacoes.html`, 287 linhas)

```text
Crie js/98-comunicacoes.js. Ele faz: Comunicações Processuais — ⚖️ Comunicações Processuais.
No app original ele tinha estas funções/partes: esc, carregarDados, iso, periodo, limpar, fData, parse, chave, status, montarParams, buscar, render, baixar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 70 — `js/98-extrator.js` (era `ferramentas/extrator.html`, 265 linhas)

```text
Crie js/98-extrator.js. Ele faz: Extrator de Sites — 🛠️ Extrator de Sites.
No app original ele tinha estas funções/partes: esc, LEITOR, hist, salvarHist, renderHist, status, buscar, absoluto, analisar, addRec, extrair, realce, conteudoAba, mostrar, copiar, baixar, nomeBase, CRC.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 71 — `js/98-juntador.js` (era `ferramentas/juntador.html`, 437 linhas)

```text
Crie js/98-juntador.js. Ele faz: Juntador de Arquivos — 🧩 Juntador de Arquivos.
No app original ele tinha estas funções/partes: esc, uid, toast, ext, lang, isTexto, bytesFmt, linhas, decode, pareceBinario, b64, unb64, inflate, lerZip, CRC, crc32, escreverZip, textoDocx.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 72 — `js/98-laboratorio.js` (era `ferramentas/laboratorio.html`, 823 linhas)

```text
Crie js/98-laboratorio.js. Ele faz: Laboratório HTML — Advocacia Previdenciária.
No app original ele tinha estas funções/partes: separar, ler, cssDosAjustes, regra, completo, guardar, caminho, limpo, info, marcar, pagina, quemE, hex, transparente, num, montar, carregar, enviar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 73 — `js/98-limpador.js` (era `ferramentas/limpador.html`, 665 linhas)

```text
Crie js/98-limpador.js. Ele faz: Limpador de Processos — Limpador de Processos.
No app original ele tinha estas funções/partes: esc, fmt, linhasDaPagina, lerPdf, lerTxt, progresso, adicionar, regrasAtivas, minhasRegras, normLinha, acharRepetidas, limparPagina, processar, montarRegras, montarRepetidas, aplicar, faixas, verPagina.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 74 — `js/98-meu-chat.js` (era `ferramentas/meu-chat/index.html`, 116 linhas)

```text
Crie js/98-meu-chat.js. Ele faz: Meu Chat.
Ele usa o que já foi criado em: js/95-base.js, js/96-banco.js, js/98-nuvem-neon.js, js/97-nuvem.js, js/98-provedores.js, js/98-memoria.js, js/98-contextos.js, js/98-guia.js, js/98-jeito.js, js/98-voz.js, js/98-internet.js, js/98-previa.js, js/98-texto.js, js/98-chat.js, js/98-cofre-arquivo.js, js/98-guia-versoes.js, js/98-guia-maikon.js, js/98-config.js, js/98-cofre.js, js/98-backup.js, js/98-ponte-lab.js (pelo APP).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 75 — `js/98-organizador.js` (era `ferramentas/organizador.html`, 558 linhas)

```text
Crie js/98-organizador.js. Ele faz: Organizador de Documentos — 📑 Organizador de Documentos.
No app original ele tinha estas funções/partes: esc, tipoDe, compDe, numDe, moedaPorData, lerPdf, organizar, deTexto, moldeDe, bate, aplicar, camposUsados, status, tudo, renderLinhas, escolherRegra, renderRegras, fmtComp.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 76 — `js/98-perito.js` (era `ferramentas/perito.html`, 1142 linhas)

```text
Crie js/98-perito.js. Ele faz: Perito de Metadados — Perito de Metadados.
No app original ele tinha estas funções/partes: EMBUTIDO, esc, latin1, deLatin1, juntar, utf8, decTexto, tamanhoTxt, sha256js, sha256, inflar, inflarZlib, mkData, dataPdf, dataExif, dataIso, difTxt, num.
Ele chamava estes endereços: https://nominatim.openstreetmap.org/search?format=json&limit=1&countrycodes=br&q=. Em HTML, ligue cada um à função equivalente do módulo certo.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 77 — `js/98-verificador-citacoes.js` (era `ferramentas/verificador-citacoes.html`, 256 linhas)

```text
Crie js/98-verificador-citacoes.js. Ele faz: Verificador de Citações.
No app original ele tinha estas funções/partes: esc, linksPara, numeroEstranho, cnjConfere, verificar, add, temLinkPerto, pintar, aviso, carregarScript, tenta, lerDocx, lerPdf, rodar.
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 78 — `js/98-inicio.js` (era `index.html`, 71 linhas)

```text
Crie js/98-inicio.js. Ele faz: SK Jurídico HTML.
Ele usa o que já foi criado em: js/98-ia.js, js/98-nuvem-neon.js, js/98-nuvem.js, js/98-voz.js, js/98-internet.js, js/98-drive.js, js/98-importar.js, js/98-texto.js, js/98-regras.js, js/98-motor.js, js/98-processar.js, js/98-editor.js, js/98-docx.js, js/98-conversa.js, js/98-documentos.js, js/98-biblioteca.js, js/98-codigos.js, js/98-ferramentas.js, js/98-config.js (pelo APP).
Registre com APP.registrar({ nome, icone, abrir }). Devolva só o arquivo completo.
```

### Passo 79 — `js/99-app.js` e conferir

```text
Crie js/99-app.js: ele olha APP.modulos e monta o menu/abas com um botão para cada módulo. Depois, me mande o index.html atualizado com todos os <script src="js/…"> na ordem certa: js/00-core.js, js/10-ai-code-studio.js, js/15-analisador-universal.js, js/20-cirurgiao.js, js/25-desembrulhar.js, js/30-gerador-eas.js, js/35-montar.js, js/40-projeto-lab.js, js/45-raiox.js, js/50-triagem.js, js/55-zip.js, js/60-projeto.js, js/65-ferramentas.js, js/70-organizar.js, js/75-limpo.js, js/80-relatorios.js, js/85-comparar.js, js/90-ia.js, js/91-terminal.js, js/92-expo-core.js, js/93-organizar-core.js, js/94-plano-core.js, js/95-base.js, js/96-banco.js, js/97-nuvem.js, js/98-provedores.js, js/98-memoria.js, js/98-contextos.js, js/98-guia.js, js/98-jeito.js, js/98-voz.js, js/98-internet.js, js/98-previa.js, js/98-texto.js, js/98-chat.js, js/98-config.js, js/98-cofre.js, js/98-backup.js, js/98-ponte-lab.js, js/98-cofre-arquivo.js, js/98-guia-maikon.js, js/98-guia-versoes.js, js/98-nuvem-neon.js, js/98-ia.js, js/98-voz.js, js/98-nuvem.js, js/98-importar.js, js/98-internet.js, js/98-texto.js, js/98-processar.js, js/98-motor.js, js/98-drive.js, js/98-regras.js, js/98-editor.js, js/98-docx.js, js/98-conversa.js, js/98-documentos.js, js/98-biblioteca.js, js/98-codigos.js, js/98-ferramentas.js, js/98-config.js, js/98-nuvem-neon.js, js/98-voz-francisco.js, js/98-banco-neon.js, js/98-cacabug.js, js/98-calculadora-sentenca.js, js/98-colador.js, js/98-colecionador.js, js/98-comparador.js, js/98-comunicacoes.js, js/98-extrator.js, js/98-juntador.js, js/98-laboratorio.js, js/98-limpador.js, js/98-meu-chat.js, js/98-organizador.js, js/98-perito.js, js/98-verificador-citacoes.js, js/98-inicio.js, js/99-app.js.
```

## 5. Conferir no final

- [ ] Abrir o index.html na prévia: aparece a tela sem erro (▤ console vazio)?
- [ ] Cada botão abre a sua parte?
- [ ] Fechar e abrir de novo: os dados continuam?
- [ ] Nada com "replit", "REPL_", "@workspace" no código (🏗️ Preparar confere).
- [ ] 📱 PWA → deixar instalável; 📦 APK ou 🖥️ .exe.
