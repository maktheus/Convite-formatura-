# Convite de Formatura ✦

Convite de formatura em página única (`index.html`), com estética inspirada na
atmosfera de *Frieren: Beyond Journey's End* — céu crepuscular, magia, jornada.

**Deploy:** https://maktheus.github.io/Convite-formatura-/

## Recursos

- **Tela de abertura com selo mágico** — instrui a aumentar o som e a tocar
  nas pétalas; o convite abre com um clique no selo (o gesto também libera o
  áudio, exigência dos navegadores).
- **Animações**: estrelas piscando, pétalas ao vento, vaga-lumes dourados,
  estrelas cadentes, círculos mágicos girando, auroras ao fundo, título com
  brilho, revelação das seções ao rolar e contagem regressiva ao vivo.
- **Pétalas interativas** — cada pétala cai pintada com um gradiente de matiz
  aleatório; passar o dedo/cursor perto sopra as pétalas para o lado, e tocar
  em uma faz com que ela exploda em fagulhas das próprias cores.
- **Som ambiente sintetizado** — vento, acordes etéreos e sinos mágicos gerados
  ao vivo com Web Audio API. É uma paisagem sonora **original**, inspirada no
  clima contemplativo do anime (nenhuma faixa da trilha sonora é usada — a
  trilha original é protegida por direitos autorais).
- **Botões de ligar/desligar** (canto inferior direito): um para as animações e
  outro para o som. As escolhas ficam salvas no navegador (`localStorage`) e a
  página respeita `prefers-reduced-motion`.
- **Exibição sempre na horizontal** — em aparelhos na vertical o layout é
  girado 90° via CSS (e, onde o navegador permite, `screen.orientation.lock`
  trava a orientação em paisagem).

## Como personalizar

Procure pelos comentários `<!-- EDITE AQUI -->` no `index.html`:

- Nome do formando e curso (seção *hero*);
- Data, horário, local da cerimônia e da recepção (cards de *Detalhes*);
- E-mail/link de confirmação de presença (botão *RSVP*);
- Data-alvo da contagem regressiva (objeto `CONFIG` no início do `<script>`).

## Deploy

O deploy é automático: todo push na branch `main` dispara o workflow
`.github/workflows/deploy-pages.yml`, que publica o site no GitHub Pages.
