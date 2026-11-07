# ISSD - Charmoso Gauchão 2026/27 Deluxe (SNES Web Player)

Site estático ultra-performático para rodar **International Superstar Soccer Deluxe - Charmoso Gauchão 2026-27 Deluxe** automaticamente no navegador em 60 FPS via WebAssembly (`snes9x` / EmulatorJS).

- **Subdomínio configurado:** `https://charmosogauchao.martynfigueiredo.com`
- **ROM:** `rom/ISSD - Charmoso Gauchão 2026-27 Deluxe.smc`

## Como rodar localmente

Basta executar o servidor Node incluso (sem precisar instalar pacotes):

```bash
node server.js
```

Depois acesse `http://localhost:8080`.

## Deploy automático via GitHub Actions

O projeto já possui o workflow `.github/workflows/deploy.yml` configurado para publicar automaticamente no **GitHub Pages** a cada `push` na branch `main`:

1. No seu repositório do GitHub, acesse **Settings → Pages**.
2. Em **Build and deployment → Source**, selecione **GitHub Actions**.
3. No painel de DNS do domínio `martynfigueiredo.com`, adicione um registro:
   - **Tipo:** `CNAME`
   - **Nome / Host:** `charmosogauchao`
   - **Destino / Valor:** `martynrangelfigueiredo.github.io`
4. Faça o push para a branch `main` — a Action vai validar o `index.html`, o `CNAME` e a ROM na pasta `rom/` e publicar o site automaticamente.
