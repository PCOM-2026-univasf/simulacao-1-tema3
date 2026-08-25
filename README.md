# Tema 3 — Algoritmo automático de verificação de sobremodulação

Esse repositório contém o código necessário para decidir programaticamente se um sinal AM pode ser demodulado por detecção de envoltório, e sugere o valor mínimo de portadora necessário.

---

## Estrutura

- `test_cases.json`: Arquivo de configuração flexível contendo os dados dos casos de teste (seno simples, soma de senos, dente de serra, ruído aleatório e arquivo de áudio real) e as amplitudes $A$ a serem testadas.
- `signal_generator.py`: Módulo responsável por converter as definições de sinais do JSON em vetores de dados.
- `overmodulation_checker.py`: Script principal contendo a função de verificação matemática `verifica_envelope()` e a geração dos plots de análise.
- `run.py`: Script portátil utilitário de bootstrap

---

## 🌐 Simulador Web Interativo (GitHub Pages)

Além dos scripts Python, o repositório conta com uma **Aplicação Web Interativa em Tempo Real** pronta para publicação no **GitHub Pages**.

### Funcionalidades do Simulador Web:
- 🎛️ **Seletor dos 5 Casos de Teste** (Seno simples, Soma de senos, Sinal triangular simétrico, Ruído aleatório e Áudio real do Xaropinho).
- 📈 **Osciloscópio Animado (Tempo Real)**: Renderização no HTML5 Canvas do sinal modulante $m(t)$, das envoltórias $\pm[A + m(t)]$, da portadora $s(t)$ e destaque visual em vermelho da **zona de sobremodulação** ($A + m(t) < 0$).
- 🚥 **Badge Semáforo e Diagnóstico**: Recálculo instantâneo de $a_{\text{min}}$ e indicação visual imediata (Verde = OK / Vermelho = Sobremodulado).
- 🔊 **Tocador de Áudio Real**: Decodificação via Web Audio API para audição e análise do sinal de áudio real (`xaropinho-rapaz.wav`).
- 💾 **Exportação de Dados**: Download dos gráficos em imagem **PNG** e da tabela resumo em **CSV** e **JSON**.

### Como Ativar no GitHub Pages:
1. Faça o commit e push das alterações para a branch `main` do seu repositório no GitHub.
2. No GitHub, navegue até **Settings** > **Pages**.
3. Em **Build and deployment** > **Source**, selecione `Deploy from a branch`.
4. Em **Branch**, selecione `main` e a pasta `/ (root)`. Clique em **Save**.
5. Em instantes, a aplicação estará online no link: `https://<seu-usuario>.github.io/simulacao-1-tema3/`

---

## Discentes

- Paulo Henrique de Farias Martins
- Caua Tavares Nunes
- Vitor Rocha Machado
- Vitor Gonçalves dos Santos
- José Victor Cruz Rebouças
