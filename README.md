# 🎹 Virtual Piano — Partitura Interativa

Um piano virtual para navegador com suporte a **autoplay por partitura de texto**, polifonia (acordes), múltiplos timbres e teclado clicável. Sem instalação, sem dependências — basta abrir o arquivo HTML em qualquer navegador moderno.

---

## ✨ Funcionalidades

| Recurso | Descrição |
|---|---|
| **Autoplay** | Toca automaticamente a partir de uma partitura em texto |
| **Acordes** | Múltiplas notas simultâneas com `[ ]` |
| **4 Oitavas** | Teclado visual de C2 a B5 |
| **4 Timbres** | Piano, Flauta, Órgão, Sintetizador |
| **BPM ajustável** | De 40 a 280 batimentos por minuto |
| **Volume** | Controle deslizante |
| **Loop** | Repete a partitura indefinidamente |
| **Seek** | Clique na barra de progresso para pular para qualquer ponto |
| **Teclado físico** | Toque notas com o teclado do computador |
| **Teclado clicável** | Clique nas teclas do piano com o mouse ou toque na tela |
| **Preview de tokens** | Destaque visual do token sendo tocado em tempo real |

---

## 🚀 Como usar

### Opção 1 — Abrir localmente

Baixe o arquivo `piano-virtual.html` e abra diretamente no navegador. Nenhuma instalação necessária.

### Opção 2 — Acesse online

https://effervescent-licorice-3a343b.netlify.app/
---

## 🎵 Guia de Notação

A partitura é uma sequência de **tokens** separados por espaços ou traços. Cada token representa uma nota ou um acorde.

---

### Estrutura de uma nota

```
[Nome da nota][Acidental][Oitava]
```

| Parte | O que é | Exemplos |
|---|---|---|
| Nome da nota | Letra de A a G | `C`, `D`, `E`, `F`, `G`, `A`, `B` |
| Acidental | Sustenido ou bemol (opcional) | `#` = sustenido, `b` = bemol |
| Oitava | Número de 0 a 8 | `C4` = Dó central |

**Exemplos de notas simples:**

```
C4   D4   E4   F4   G4   A4   B4
C#4  D#4  F#4  G#4  A#4
Db4  Eb4  Gb4  Ab4  Bb4
```

---

### Oitavas — Referência

| Oitava | Notas | Faixa sonora |
|---|---|---|
| 2 | C2 – B2 | Grave (baixo) |
| 3 | C3 – B3 | Médio-grave |
| 4 | C4 – B4 | Médio (região do Dó central) |
| 5 | C5 – B5 | Médio-agudo |

> **Dica:** C4 é o **Dó central** — a referência mais comum em partituras.

---

### Acordes

Para tocar várias notas ao mesmo tempo, coloque-as entre colchetes `[ ]`:

```
[C4E4G4]        → Dó maior (C maior)
[A3C4E4]        → Lá menor (Am)
[C3E3G3B3]      → Dó maior com sétima maior (Cmaj7)
[G2D3G3B3]      → Sol maior (G)
[F2C3F3A3]      → Fá maior (F)
```

As notas dentro do acorde podem ser de oitavas diferentes:

```
[C2G4]          → Baixo (C2) + agudo (G4) juntos
[A2E3A3C4E4]    → Acorde aberto em 5 notas
```

---

### Separadores

Espaços e traços entre tokens são ignorados. Use como preferir para melhorar a leitura:

```
C4 E4 G4              ← com espaços
C4-E4-G4              ← com traços
C4E4G4                ← colados
[C4E4G4] A4 [F3A3C4]  ← misturado
```

---

### Sustenidos e Bemóis — Equivalências

O piano usa apenas sustenidos internamente. Bemóis são convertidos automaticamente:

| Bemol | Equivalente | Nota |
|---|---|---|
| `Db` | `C#` | Ré bemol |
| `Eb` | `D#` | Mi bemol |
| `Fb` | `E` | Fá bemol |
| `Gb` | `F#` | Sol bemol |
| `Ab` | `G#` | Lá bemol |
| `Bb` | `A#` | Si bemol |
| `Cb` | `B` | Dó bemol |

---

### Exemplos completos

**Escala de Dó maior (C4 a C5):**
```
C4 D4 E4 F4 G4 A4 B4 C5
```

**Progressão simples I–V–vi–IV (em Dó):**
```
[C4E4G4] [G3B3D4] [A3C4E4] [F3A3C4]
```

**Melodia com acompanhamento de baixo:**
```
[C2C3] E4 G4 [G2D3] F4 A4 [A2E3] E4 C4 [F2C3] D4 F4
```

**Com notas rápidas e acordes misturados:**
```
C4 E4 G4 [C4E4G4] A4 C5 [A3E4A4] G4 F4 [F3A3C4]
```

**Exemplo do arquivo original (Animal Crossing style):**
```
[C3G4] E4 C4[G#2D4] [A2E4] [G#3E3B4] [A3A4][A2F4]-F3-C5A4 F4
[G2F3A3] G#3 [G2G3B3G4]A#4 B4 [C2C5] G4 G2 G4
[F2G5] [G4E5] [C3E5] [G4D5][A2C5] A4 E2 A4
```

---

### Teclado físico (atalhos)

Quando o foco não está no campo de texto, você pode tocar com o teclado:

| Tecla | Nota |
|---|---|
| `A` | C4 |
| `W` | C#4 |
| `S` | D4 |
| `E` | D#4 |
| `D` | E4 |
| `F` | F4 |
| `T` | F#4 |
| `G` | G4 |
| `Y` | G#4 |
| `H` | A4 |
| `U` | A#4 |
| `J` | B4 |
| `K` | C5 |
| `O` | C#5 |
| `L` | D5 |
| `P` | D#5 |
| `Espaço` | Play / Pausar |

---

## 🎨 Timbres disponíveis

| Timbre | Onda | Som |
|---|---|---|
| **Piano** | Triangular | Suave, próximo de piano acústico |
| **Flauta** | Senoidal | Puro, suave, sem harmônicos |
| **Órgão** | Quadrada | Rico em harmônicos, brilhante |
| **Sintetizador** | Dente de serra | Eletrônico, encorpado |

---

## ⚙️ Tecnologias

- **HTML5 / CSS3 / JavaScript** puro — zero dependências de framework
- **Web Audio API** — síntese de som em tempo real no navegador
- **Google Fonts** — tipografia (Playfair Display + IBM Plex Mono)
- **Tabler Icons** — ícones via webfont

---

## 📄 Licença

Livre para uso pessoal e educacional.

---

*Feito com ♪ — basta um navegador para tocar.*
