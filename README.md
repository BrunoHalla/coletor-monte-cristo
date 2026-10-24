# Controle Safra — Coletor John Deere

Página institucional pública de apresentação do módulo de integração do Controle Safra com o John Deere Operations Center.

## Estrutura
- `coletor-johndeere/index.html`: página atual e principal do Coletor John Deere
- `index.html`: redirecionamento da antiga raiz para a nova página, com `noindex`

## URLs
- URL de pré-visualização no GitHub Pages: `https://brunohalla.github.io/coletor-monte-cristo/coletor-johndeere/`
- URL pública solicitada: `https://www.controlesafra.com.br/coletor-johndeere/`

**A publicação no endereço personalizado requer configuração da hospedagem efetiva do domínio.** Este repositório não ativa automaticamente uma subpasta em um domínio já hospedado por outro servidor/Cloudflare. Não mudar A/AAAA/CNAME do domínio raiz ou `www` sem verificar o frontend e as APIs existentes.

Se o domínio estiver no GitHub Pages, use o repositório que serve a raiz de `www.controlesafra.com.br` e adicione a pasta `coletor-johndeere/` nesse repositório. Se o frontend estiver em Cloudflare Pages, publicar a pasta na build/site, ou configurar roteamento do caminho. Se o site usar servidor web/reverse proxy, disponibilizar o conteúdo estático apenas nessa rota. Não proxyar ou tornar públicos os endpoints internos.

## Cadastro John Deere Developer Portal
Application Name: `Controle Safra - Coletor John Deere`

Website Link, quando acessível e com certificado HTTPS válido: `https://www.controlesafra.com.br/coletor-johndeere/`

Short Description (186 caracteres):
> Integração do Controle Safra com o John Deere Operations Center para coletar dados de plantio, colheita e aplicações, gerar relatórios operacionais e enviar planejamentos via Work Plans.

**Website Link não é Redirect URI do OAuth.** Manter e conferir as URLs de callback da integração antes de alterá-las.

A aplicação é independente. A página não contém dados reais, credenciais ou afirmação de vínculo comercial com a John Deere.
