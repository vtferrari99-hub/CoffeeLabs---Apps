# CoffeeLabs Apps

Vitrine pública dos apps da CoffeeLabs. Aqui ficam **só** o catálogo e os APKs prontos — o código de cada app fica num repositório privado.

## Como funciona
- `catalogo.json` — lista de apps (nome, versão, tamanho, ícone, link do APK e `sha256`). O instalador CoffeeLabs lê este arquivo para montar a vitrine e avisar de atualizações.
- **Releases** — cada app tem uma release com o nome do seu `id` (ex.: `zeus`) contendo o APK mais recente. Link fixo:
  `https://github.com/vtferrari99-hub/CoffeeLabs---Apps/releases/download/<id>/<Arquivo>.apk`
- `icones/` — ícone de cada app (PNG 512×512).

O build de cada app (GitHub Actions no repositório privado dele) publica o APK aqui e atualiza o `catalogo.json` sozinho.

## Segurança
- Nunca coloque código, senhas ou tokens neste repositório.
- O instalador confere o `sha256` antes de instalar: se o arquivo baixado não bater, ele recusa.
- Todos os APKs são assinados sempre com a mesma chave de cada app, então só atualizações legítimas instalam por cima.
