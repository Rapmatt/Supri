# Supri

**Abasteça sem adivinhação.**

_Desenvolvido por Raphael Silveira._

App de **controle de estoque e requisições diárias** que roda 100% no navegador —
funciona **offline**, guarda os dados **no próprio aparelho** e pode ser
**instalado como app** no celular (PWA), sem loja de aplicativos e sem servidor.

Protótipo pensado para restaurantes, mas serve a qualquer ramo (comércio,
clínicas, oficinas, eventos) — é só cadastrar as categorias e itens do seu negócio.

---

## ✨ Funcionalidades

- **Requisição diária** por categoria, com os campos **Est.** (estoque conferido),
  **M** (manhã) e **T** (tarde).
- **Requisição por arquivo**: o celular **exporta** a requisição (`.json`) e envia
  por WhatsApp/e-mail; o PC **importa** o arquivo — não precisa estar na mesma rede.
- **Baixa automática** no estoque geral: ao dar baixa, o consumo (M + T) é descontado.
- **Estoque geral** com entrada/reposição, ajuste de inventário e alerta de mínimo.
- **Relatório e histórico**: toda entrada e saída fica registrada com data/hora;
  veja por período, com **resumo por produto** (quanto entrou/saiu de cada item),
  imprima, ou **exporte em CSV** para abrir no Excel.
- **Cadastro** próprio de categorias e produtos (adicionar, editar, excluir).
- **Impressão** da requisição, da guia de separação, da contagem e do relatório (ou PDF).
- **Backup**: exportar/importar todos os dados em arquivo `.json`.
- **Funciona offline** e **instala no celular** como aplicativo.

### Novidades (Bloco A)
- **Tela inicial** com cada função em seu próprio cartão (sem telas poluídas).
- **Senha de acesso** (padrão `supri9832`, trocável em Cadastro/Configurações) nas abas restritas: Contagens, Estoque, Relatório, Importar, Recebidas e Cadastro.
- **Contagem** (Bebidas, Secos, Mat. Limpeza) com Ideal/Contagem/**Pedido** (= Ideal − Contagem) e **unidade** por item; botão **Lançar no estoque G4** (marco inicial).
- **Contagem Vinhos** com **G3 / G4 / Total**: o BAR preenche só o G3; o **G4** é liberado só pelo admin; o Total soma os dois.

### Novidades (Bloco B)
- **Requisição Bebidas (Bar)** e **Requisição Vinhos/Espumantes** com turnos **Dia/Noite** e campo de **Observação**, organizadas por seção.
- A **baixa (Dia + Noite)** acontece no estoque **G4** ao dar baixa em Recebidas; os produtos são criados no banco automaticamente.
- Cada requisição grava **data e horário** do ato e pode ser **enviada por arquivo** (celular → PC) e **impressa**.
- _Em construção (Bloco C):_ Importar XML (NF‑e) / Excel / PDF.

### v2.0
- **Bebidas alinhadas:** os 8 nomes divergentes da Requisição Bebidas passaram a usar o nome padrão da lista (ex.: CHIVAS REGAL → WHISKY CHIVAS REGAL; cafés → _pack 50un), casando com a Contagem para a baixa.

### v1.9
- **Secos e Limpeza** com nomenclatura + **fator** (un por pack) aplicados: 16 itens de Secos em pack (açúcar, sal, arroz…) mostram **Total un** na contagem; Limpeza é avulso.

### v1.8
- **NF‑e: categoria por produto.** Na prévia da importação, cada produto tem um **seletor com todas as categorias** (+ "nova categoria" e "ignorar"), para você colocar cada item no lugar certo. Produto já existente é movido se você trocar a categoria.

### v1.7
- **Importar Excel (.xlsx)** de verdade (lê a primeira aba), além de CSV e NF‑e (XML). PDF fica para depois.

### v1.6 (Auditoria)
- **Registro de atividades** (admin, em Cadastro/Configurações): grava **acessos** ao app e todas as ações — impressões, requisições salvas/enviadas/exportadas/importadas, **baixas**, contagens, importações (NF‑e/CSV) e **alterações de cadastro** (produtos, categorias, senha), cada uma com **data e hora**. Filtro por dia, impressão e inclusão no backup.

### v1.5 (Bloco C — Importar)
- **Importar NF‑e (XML)** do fornecedor: lê os produtos da nota e lança **entrada** no estoque G4 (cria os novos na categoria escolhida; guarda o valor unitário).
- **Importar planilha (CSV)**: colunas nome, categoria, quantidade, unidade → entrada no G4.
- _Próximo:_ Excel (.xlsx) e PDF.

### v1.4
- **Vinhos unificados**: a Requisição Vinhos e a Contagem Vinhos usam a **mesma lista** (104 vinhos, união das duas) — uma completa a outra.
- **Ocultar / re-exibir** vinho (🙈 / ↩): sai das duas telas e volta quando quiser; fica salvo no aparelho.

### v1.3
- Versão visível na tela inicial; cada pacote de release vai numerado.
- Nomenclatura das **bebidas** com o **pack** no nome (ex.: `COCA NORMAL 350ML_pack 12un`) e **fator** (un por pack) guardado — a Contagem Bebidas mostra o **Total em unidades**.

> Já vem com o catálogo Sushi Rio 2026 carregado (128 itens em 4 categorias). Para
> começar do zero, use **Cadastro → Apagar tudo** e cadastre os seus itens.

## 🔄 Como funciona (celular × PC)

1. **Celular (colaborador):** abre o app, preenche a requisição (Est./M/T) e toca
   em **Salvar**. Em **Recebidas**, abre a requisição e toca em **📤 Enviar** para
   gerar o arquivo e mandar para você (WhatsApp, e-mail etc.). Funciona mesmo em
   outra rede ou nos dados móveis.
2. **PC (estoque geral):** mantém o estoque atualizado no dia a dia. Em **Recebidas**,
   toca em **📥 Importar requisição (arquivo)**, escolhe o arquivo recebido, confere
   e toca em **⬇️ Dar baixa** — o consumo é descontado do estoque central.
3. **Relatório:** consulte em **📊 Relatório** o que entrou e saiu no período, com
   histórico completo; imprima ou salve em PDF.

> Cada aparelho guarda os próprios dados. O PC é quem mantém o **estoque geral**
> (a baixa acontece nele). O celular serve para montar e enviar a requisição.

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
