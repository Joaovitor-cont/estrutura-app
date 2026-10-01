# Atalho do app — Estrutura Contábil

Página de atalho para o sistema de gestão da **Estrutura Contábil** (Kanban Fiscal).

## Para que serve

O sistema roda no Google Apps Script, cuja página pertence ao Google. Por isso não é possível
definir ali o `apple-touch-icon` nem um `manifest` — e o celular acaba usando o ícone genérico do
Google ao adicionar o sistema à tela de início.

Esta página resolve isso: ela declara o ícone correto e redireciona para o sistema. Quem adiciona
**esta** página à tela de início recebe o ícone da Estrutura e, ao tocar nele, cai direto no
sistema. Aberta pelo navegador, ela mostra as instruções de instalação — útil para enviar à equipe
no lugar do endereço longo do Apps Script.

## O que existe aqui

| Arquivo | Para que serve |
|---|---|
| `index.html` | A página: ícone, botão de abrir e instruções. Redireciona sozinha quando aberta pelo ícone |
| `manifest.webmanifest` | Nome, cores e ícones para o Android instalar como aplicativo |
| `icone-512.png`, `icone-192.png`, `icone-180.png`, `favicon.ico` | Ícones, gerados a partir do monograma do próprio sistema |

Os ícones são gerados por `scripts/gen_icone_app.py`, no repositório do sistema, a partir do
mesmo SVG embutido no app.

## Sobre o conteúdo ser público

Este repositório precisa ser público porque o GitHub Pages só é gratuito assim. Ele contém
**apenas o ícone e o redirecionamento** — nenhum dado de cliente, nenhuma senha, nenhuma planilha.

O endereço do sistema aparece no código, mas o acesso continua restrito ao domínio
`estruturacontabilba.com.br`: quem não tem conta do escritório não entra, mesmo com o endereço.
O sistema em si é privado e segue em outro repositório.
