# 🎵 Funky Friday Autoplayer

Autoplayer para **Funky Friday** (Roblox) com UI em [Rayfield Gen2](https://sirius.menu), timing baseado na velocidade real das notas, humanização, suporte a hold notes e filtro de notas especiais (Death / Poison).

> **Autor:** fal

---

## ✨ Recursos

- **Timing velocity-aware (modo Auto):** mede a velocidade real das setas e dispara quando cruzam a judgment line — funciona em qualquer scroll speed.
- **Modo Fixed:** delay fixo configurável (comportamento clássico).
- **Hold notes:** segura a tecla até o fim da nota (tempo máximo configurável).
- **Humanização:** jitter gaussiano, qualidades Perfect/Great/Ok e chance de miss forçado com cooldown.
- **Notas especiais:** detecta e ignora notas Death e Poison (cache das skins lido da UI do jogo).
- **Suporte 4K–12K:** até 12 lanes.
- **Múltiplos métodos de input:** `firesignal`, `Scriptable Input` e `Virtual Input` (conforme o executor).
- **Auto-rebind:** reconecta sozinho quando uma música começa/termina.
- **Painel de status:** hits, qualidades, misses e skips em tempo real.
- **Keybinds configuráveis** e **Unload** robusto.
- **Salvamento automático** de configurações (Rayfield).

---

## 📦 Requisitos

- Um executor de scripts Roblox com suporte a `loadstring`, `game:HttpGet` e, idealmente, `firesignal` / `getgenv`.
- Acesso à internet (o script baixa o Rayfield Gen2 e o Service Resolver).

---

## 🚀 Uso

Execute no seu executor:

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPO/main/FunkyFridayAutoplayer.lua"))()
```

> Troque `SEU_USUARIO` e `SEU_REPO` pelos seus dados.

---

## 🎮 Controles padrão

| Ação | Tecla |
|------|-------|
| Ligar/desligar autoplay | `Right Shift` |
| Esconder/mostrar UI | `Right Control` |

As teclas podem ser alteradas na aba **Config**.

---

## ⚙️ Valores padrão (Timing)

| Opção | Padrão |
|-------|--------|
| Timing Offset | `-139 ms` |
| Fixed Delay | `80 ms` |
| Tap Hold | `5 ms` |
| Release Delay | `0 ms` |
| Max Hold | `1 s` |
| Min Velocity | `50 px/s` |
| Velocity Smoothing | `0 %` |

Se as notas estiverem sendo acertadas cedo/tarde demais, ajuste o **Timing Offset** na aba *Timing*.

---

## 🗂️ Abas da UI

- **Autoplay** — liga/desliga, holds, precisão, modo de input.
- **Timing** — modo Auto/Fixed, offsets, tempos de tap/hold, velocidade.
- **Humanização** — jitter e miss forçado.
- **Notas Especiais** — filtros Death/Poison e refresh das skins.
- **Status/Debug** — estatísticas ao vivo e modo debug.
- **Config** — keybinds, rebind manual e unload.

---

## 🛠️ Solução de problemas

- **Não acerta nada:** troque o *Input Mode* na aba Autoplay; alguns executores só suportam um método.
- **Timing errado:** ajuste o *Timing Offset*; teste alternando entre *Auto* e *Fixed*.
- **Não detectou a música:** use *Rebind Song* na aba Config.
- **Death/Poison não filtram:** use *Refresh Special Skins* (abre a tela de Configuração do jogo brevemente).
- **Para de funcionar ao trocar de janela (PC):** o jogo para de ler inputs quando perde o foco.

---

## ⚠️ Aviso

Este projeto é fornecido **apenas para fins educacionais**. Usar scripts de terceiros em Roblox viola os [Termos de Uso](https://en.help.roblox.com/hc/en-us/articles/115004647846) e pode resultar em banimento da conta. Use por sua conta e risco; o autor não se responsabiliza por quaisquer consequências.

---

## 📄 Licença

Distribuído sob a licença MIT. Veja [`LICENSE`](LICENSE).
