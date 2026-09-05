# Pregador Excellington — GitHub Pages

Projeto estático preparado para publicação direta no GitHub Pages.

## Arquivos

- `index.html` — aplicativo
- `bible_arc.json` — Bíblia Almeida Revista e Corrigida (ARC), completa, com 66 livros
- `sw.js` — suporte a cache/offline
- `.nojekyll` — evita processamento Jekyll
- `LEIA-ME.txt` — observações do projeto

## Publicação

1. Crie um repositório no GitHub.
2. Envie TODOS os arquivos deste pacote para a raiz da branch `main`.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/(root)`.
6. Clique em **Save**.
7. Aguarde a publicação e abra a URL informada pelo GitHub.

O `index.html` está na raiz e o `bible_arc.json` é carregado por caminho relativo, portanto o projeto funciona tanto em um site de usuário quanto em um site de projeto do GitHub Pages.

## Funcionamento offline

No primeiro acesso, o aplicativo baixa o `bible_arc.json` e grava os versículos no IndexedDB do navegador. O Service Worker também armazena os arquivos necessários para que os acessos seguintes possam funcionar sem internet.

É importante fazer o primeiro carregamento com internet e aguardar a mensagem de que a Bíblia ARC foi carregada.

## Observação sobre a ARC

O arquivo ARC deste projeto foi obtido dos arquivos fornecidos pelo usuário. O metadado da fonte identifica a tradução como "Almeida Revista e Corrigida", ano 1995, editora SBB e licença "copyright". A publicação/distribuição pública do texto deve ser feita somente se você tiver os direitos ou autorização necessários.
