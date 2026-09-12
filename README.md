# Beira-Campo

Simulador de carreira de técnico no futebol brasileiro. Série A e B, partida ao vivo com
decisões de banco, mercado, contratos, estádio e carreira entre clubes.

Um arquivo só, sem build e sem dependência de servidor: `index.html`.

## Publicar

**GitHub Pages** — Settings → Pages → Source: `Deploy from a branch`, branch `main`, pasta `/ (root)`.
Em um ou dois minutos o jogo está em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

**Render** — New → Static Site → conecte o repositório →
Build Command: deixe vazio · Publish Directory: `.`

## Escudos personalizados

Os escudos que você sobe no Editor ficam no navegador de quem jogou. Para que **todo mundo**
veja os seus escudos ao abrir o link:

1. No jogo: Editor → Clubes → "Enviar vários escudos de uma vez"
2. Editor → "Exportar / importar pacote" → clique na caixa de cima e copie
3. Neste arquivo `index.html`, procure `const IDENTIDADE_PADRAO = {};`
   e troque o `{}` pelo texto copiado. Salve e faça commit.

## Saves

Cada jogador tem a própria carreira, guardada no navegador dele (`localStorage`).
Nada é enviado para servidor nenhum. Dentro do jogo, "Backup da carreira" exporta
e restaura, e o jogo guarda pontos de retorno antes de cada virada de temporada.
