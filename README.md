# Villa Courses — Laravel na prática

Mini-site estático (HTML puro, sem build) pronto para publicar no GitHub Pages. Serve como alternativa ao Moodle: a página inicial (`index.html`) lista o curso de Laravel e linka para as 6 aulas em `aulas/`.

## Estrutura

```
site/
├── index.html        # página inicial (landing da "plataforma de cursos")
└── aulas/
    ├── aula1.html
    ├── aula2.html
    ├── aula3.html
    ├── aula4.html
    ├── aula5.html
    └── aula6.html
```

Cada arquivo é autocontido (CSS inline, sem dependências externas) — funciona abrindo direto no navegador, sem servidor.

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (pode ser público), por exemplo `curso-laravel`.
2. Suba **o conteúdo desta pasta `site/`** para a raiz do repositório (não a pasta `laravel/` inteira — só o que está dentro de `site/`):

   ```bash
   cd D:\duvidas\laravel\site
   git init
   git add .
   git commit -m "Publica curso de Laravel"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/curso-laravel.git
   git push -u origin main
   ```

3. No GitHub, abra o repositório → **Settings → Pages**.
4. Em "Build and deployment", selecione **Deploy from a branch**, branch `main`, pasta `/ (root)`.
5. Salve. Em alguns minutos o site fica disponível em:
   `https://SEU-USUARIO.github.io/curso-laravel/`

## Atualizando o conteúdo

Os arquivos em `site/aulas/` são cópias independentes dos originais em `D:\duvidas\laravel\aulaN.html` (usados para eventual upload direto no Moodle). Se editar um dos dois, replique a mudança no outro manualmente, ou decida qual dos dois vira a fonte única do conteúdo.
