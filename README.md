# Portfólio — Kariny Alpiano

Portfólio **100% estático** (apenas `index.html`) com **tema de desenvolvedora**, seletor de **idioma PT‑BR/EN**, alternância **dark/light** e cards de **projetos**.  
Feito para ser hospedado no **GitHub Pages** sem build.

## ✨ Destaques
- **Design dev**: tema escuro por padrão, grade técnica, tipografia monoespaçada e “janela de terminal” no herói.
- **i18n PT‑BR/EN**: seletor no topo. O PT‑BR do HTML é a **fonte de verdade**; ao trocar para EN o script aplica traduções. Ao voltar para PT‑BR, o texto original é restaurado.
- **Tema**: botão 🌙/☀️ alterna entre *dark* e *light* (salvo em `localStorage`).
- **Stack com ícones SVG**: Python, JavaScript, TypeScript, React, Vue, Node.js, NestJS, MongoDB, GCP, Power BI, Django, Flask, TensorFlow, Gradio, SQLite.
- **Metodologias**: badge de **Kanban**.
- **SEO básico**: `meta description`, Open Graph e `lang` dinâmico.

## 🗂 Estrutura
```
.
├── index.html      # Único arquivo necessário
├── README.md       # Este arquivo
├── LICENSE         # MIT
└── .nojekyll       # Necessário para GitHub Pages não rodar Jekyll
```

## 🚀 Executar localmente
- **Sem servidor**: dê duplo clique em `index.html` e abra no navegador.
- **Com servidor (recomendado)**: use a extensão “Live Server” do VS Code ou rode qualquer servidor estático (ex.: `python -m http.server`).

## 🌐 Publicar no GitHub Pages
1. Crie um repositório no GitHub (ex.: `karinyalpiano/portfolio`).  
2. Faça upload de todos os arquivos (branch **main**).
3. Vá em **Settings → Pages → Build and deployment**:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` / **Folder**: `/root`
4. Acesse a URL gerada (ex.: `https://<seu-usuario>.github.io/<repo>/`).

> **Importante:** mantenha o arquivo `.nojekyll` na raiz para evitar que o GitHub Pages processe o site com Jekyll.

## 🧩 Personalização
### “Sobre mim”
- Edite diretamente o parágrafo dentro da seção **SOBRE MIM** no `index.html` (PT‑BR).  
- O script faz um _snapshot_ do conteúdo PT‑BR e **só aplica tradução** quando o idioma for EN.  
- Quer alterar também em inglês? Mude a chave `"about-long"` dentro de `translations.en`.

### Cores e tema
- A cor de destaque vem da variável CSS `--accent` no `<style>`.  
- O botão de tema salva a preferência em `localStorage` (`theme` = `"dark"` ou `"light"`).

### Foto de perfil e links
- Troque o avatar alterando a URL `https://github.com/karinyalpiano.png`.
- Atualize os links de **GitHub**, **LinkedIn** e **e‑mail** no topo e no rodapé/contato.

### Projetos
- Cada card fica na seção **PROJETOS**. Copie/cole um card e ajuste:
  - `href` do repositório,
  - título/descrição (`data-i18n`),
  - tags (tecnologias).

### Stack & Metodologias
- Os ícones SVG são inline (fáceis de editar).  
- Para adicionar/remover itens, duplique um bloco `.panel` na seção **SKILLS** e ajuste o SVG + texto.

### SEO
- As metatags `description` e `og:description` também são atualizadas conforme o idioma selecionado.

## 🧠 Como funciona o i18n
- Elementos com `data-i18n="..."` são candidatos a tradução.  
- No carregamento, o script salva o **conteúdo original PT‑BR** em `data-i18n-original`.  
- `applyLang("en")` substitui o conteúdo pelas traduções de `translations.en`.  
- `applyLang("pt")` **restaura o HTML original**, garantindo que suas edições (ex.: “Sobre mim”) não sejam perdidas.

## 🧯 FAQ — Problemas comuns
**“O tema não alterna.”**  
Verifique se o `<html>` recebe/tira a classe `dark`. Apague `localStorage.theme` no DevTools e teste novamente.

**“O ‘Sobre mim’ não atualiza.”**  
Esta versão usa o snapshot PT‑BR. Se ainda assim não atualizar, limpe `localStorage.lang` e recarregue.  
Alternativa: remova `data-i18n="about-long"` do parágrafo (ele para de ser traduzido).

**“Mistura PT com EN.”**  
Use o seletor de idioma para **PT‑BR** e recarregue. Confirme as chaves em `translations.en` se tiver editado.

## 📝 Licença
[MIT](./LICENSE)

---
Feito por **Kariny Alpiano** — código, café e curiosidade.  
Gerado em 2025-11-06 15:03 UTC.