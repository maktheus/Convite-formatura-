# Convite de Formatura ✦ Matheus Serrão Uchôa

Convite de formatura em página única (`index.html`), implementação fiel do
design **Convite Formatura.dc.html** criado no Claude Design — paleta clara
estilo papel, tipografia Garamond e ilustração de capa em tela cheia.

**No ar:** https://maktheus.github.io/Convite-formatura-/

## Estrutura (do design)

- **Hero** — ilustração de capa, "O fim de uma jornada. O início de muitas
  outras." e a data 11 · 08 · 2026;
- **História** — texto de convite;
- **Formando** — Matheus Serrão Uchôa, Engenharia da Computação — UFAM;
- **Detalhes** — data, horário (19h) e local (Auditório Eulálio Chaves,
  UFAM) com botão "Ver no mapa";
- **RSVP** — botões "Confirmo minha presença" / "Não poderei comparecer"
  com mensagem de resposta;
- **Citação final** com assinatura.

## Camadas extras (sobre o design)

- **Tela de abertura** — instrui a aumentar o som e a tocar nas pétalas;
  o clique em "Abrir convite" libera o áudio (exigência dos navegadores).
- **Trilha da jornada** — playlist do YouTube tocando num mini-player
  oficial e discreto (canto inferior esquerdo). Se o player não carregar,
  entra o som ambiente sintetizado do próprio design (vento + sinos, via
  Web Audio API). Nenhum arquivo de áudio é distribuído no repositório.
- **Pétalas interativas** — a física de queda é a do design; cada pétala
  ganha um gradiente pastel de matiz aleatório, o cursor/dedo sopra as
  pétalas e o toque as desfaz em fagulhas.
- **Botões de ligar/desligar** som e animações (canto inferior direito),
  persistidos em `localStorage`; a página respeita `prefers-reduced-motion`.
- **Versão mobile dedicada** — tipografia, espaçamentos, enquadramento da
  capa, botões em largura total e áreas seguras (notch) ajustados para
  telas estreitas.
- **Revelação suave das seções** ao rolar.

## Personalização

- Playlist, densidade de pétalas e volume: objeto `CONFIG` no início do
  `<script>` do `index.html`;
- Textos e datas: direto nas seções do HTML.

## Deploy

Todo push na `main` dispara `.github/workflows/deploy-pages.yml`, que
publica o site no GitHub Pages.
