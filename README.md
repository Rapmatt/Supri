# Supri

**Abasteça sem adivinhação.**

App de **controle de estoque e requisições diárias** que roda 100% no navegador —
funciona **offline**, guarda os dados **no próprio aparelho** e pode ser
**instalado como app** no celular (PWA), sem loja de aplicativos e sem servidor.

Protótipo pensado para restaurantes, mas serve a qualquer ramo (comércio,
clínicas, oficinas, eventos) — é só cadastrar as categorias e itens do seu negócio.

---

## ✨ Funcionalidades

- **Requisição diária** por categoria, com os campos **Est.** (estoque conferido),
  **M** (manhã) e **T** (tarde).
- **Baixa automática**: ao consolidar, o consumo (M + T) é descontado do estoque.
- **Estoque geral** com entrada/reposição, ajuste de inventário e alerta de mínimo.
- **Cadastro** próprio de categorias e produtos (adicionar, editar, excluir).
- **Impressão** da requisição, da guia de separação e da folha de contagem (ou salvar em PDF).
- **Backup**: exportar/importar os dados em arquivo `.json`.
- **Funciona offline** e **instala no celular** como aplicativo.

> Já vem com um catálogo de exemplo carregado (128 itens em 4 categorias). Para
> começar do zero, use **Cadastro → Apagar tudo** e cadastre os seus itens.

---

## 🌐 Publicar e instalar (GitHub Pages)

1. Suba todos os arquivos deste projeto para o repositório (`index.html`,
   `manifest.webmanifest`, `sw.js`, os ícones `.png`, este `README.md` e o `.nojekyll`).
2. No repositório, vá em **Settings → Pages**.
3. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
4. Selecione a branch **main** e a pasta **/ (root)** e clique em **Save**.
5. Aguarde cerca de 1 minuto. O site ficará disponível em:
   **https://rapmatt.github.io/Supri/**

### 📲 Instalar no celular

1. Abra o endereço acima no **Chrome (Android)** ou **Safari (iPhone)**.
2. **Android:** menu **⋮ → Instalar app / Adicionar à tela inicial**.
   **iPhone:** **Compartilhar → Adicionar à Tela de Início**.
3. Pronto: o **Supri** vira um ícone na tela inicial, abre em tela cheia e
   funciona offline. Os dados ficam salvos no aparelho.

---

## 🔒 Privacidade

Nenhum dado sai do aparelho — não há servidor nem nuvem. Faça **backup**
periódico (Cadastro → Exportar) para não perder os dados ao trocar de celular
ou limpar o navegador.

---

## 🛠️ Tecnologia

HTML + Tailwind CSS + JavaScript puro, com armazenamento local (localStorage) e
service worker para funcionamento offline. Sem dependências externas em tempo de execução.
