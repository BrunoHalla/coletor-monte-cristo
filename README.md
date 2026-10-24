# Controle Safra — Coletor John Deere

Página institucional da integração **Controle Safra - Coletor John Deere**, preparada para Cloudflare Pages, sem dependência do Worker do portal.

## Publicação pretendida

- **URL final:** https://www.controlesafra.com.br/coletor-johndeere/
- **Conteúdo:** `coletor-johndeere/index.html`
- **Página raiz:** `index.html` (redireciona para o novo endereço relativo).
- **Branch:** `main`
- **Framework:** None
- **Build command:** `exit 0`
- **Build output directory:** `.` (raiz do repositório)

## Cloudflare: implantação com baixo risco

**Importante:** o domínio `controlesafra.com.br` e `portal.controlesafra.com.br` já atendem o Worker `controle-safra-portal`. Não remover nem mudar seus Custom Domains, rotas ou registros DNS.

1. Abra **Cloudflare → Workers & Pages → Create application → Pages → Connect to Git**.
2. Selecione este repositório GitHub e branch `main`.
3. Nome sugerido do projeto: `controle-safra-coletor`.
4. Configure **Framework preset: None; Build command: `exit 0`; Build output directory: `.`**.
5. Publique primeiro no domínio padrão `*.pages.dev` do projeto. Verifique o caminho `/coletor-johndeere/` e conteúdo.
6. Em **Pages project → Custom domains → Set up a domain**, informe `www.controlesafra.com.br`. Como a zona já está na Cloudflare, o painel deve oferecer a configuração correspondente de DNS/certificado para o subdomínio; confira conflitos com registros ou rotas existentes antes de confirmar.
7. Teste `https://www.controlesafra.com.br/coletor-johndeere/` em navegador anônimo, incluindo HTTPS, sem autenticação Cloudflare Access.
8. No John Deere Developer Portal, atualize **Website Link** para o endereço completo com `https://`. **Não altere Client ID, Client Secret, Redirect URI ou Connected Organizations** por causa da mudança do endereço institucional.

### Preservação de serviços existentes

- `controlesafra.com.br` → Worker `controle-safra-portal`: permanece.
- `portal.controlesafra.com.br` → mesmo Worker: permanece.
- `controle-safra-sync` e D1: permanecem.
- `www.controlesafra.com.br` → novo Pages exclusivo do site institucional.
- `coletor-johndeere/index.html` não realiza chamadas a APIs internas e não requer autenticação.

O endereço `www` ainda não foi confirmado como publicado. Evite anunciar sucesso antes de validar o domínio/certificado.

## Situação do endereço GitHub Pages antigo

O conteúdo da raiz antiga foi substituído por uma página de redirecionamento para `/coletor-johndeere/`, sem texto de marca anterior. Após a publicação no Cloudflare, é possível desativar o GitHub Pages antigo em **GitHub → Settings → Pages**, mantendo este repositório apenas como fonte do Cloudflare Pages. Não exclua o repositório se o Cloudflare Pages continuar ligado a ele.

## Cadastro John Deere

- **Application Name:** `Controle Safra - Coletor John Deere`
- **Website Link:** `https://www.controlesafra.com.br/coletor-johndeere/` (após publicar)
- **Descrição curta:**

> Integração do Controle Safra com o John Deere Operations Center para coletar dados de plantio, colheita e aplicações, gerar relatórios operacionais e enviar planejamentos via Work Plans.

O site é institucional e independente. As marcas de terceiros são usadas apenas para identificar a integração. Não adicionar dados reais de clientes, credenciais ou endpoints internos.

Referências técnicas: [Cloudflare Pages - Git integration](https://developers.cloudflare.com/pages/get-started/git-integration/), [Static HTML](https://developers.cloudflare.com/pages/framework-guides/deploy-anything/), [Custom domains](https://developers.cloudflare.com/pages/configuration/custom-domains/).
