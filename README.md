# Controle Safra — Coletor John Deere

Página institucional do **Controle Safra** e de seu componente de integração com o **John Deere Operations Center** para uso interno da Fazenda Monte Cristo.

## Página atual
O conteúdo público está em `index.html`, publicado via GitHub Pages neste repositório. A apresentação descreve o sistema, o módulo Coletor John Deere, os dados agrícolas tratados e a finalidade privada da integração.

## Domínio planejado
`https://controlesafra.com.br`

**Não apontar o cadastro John Deere para o novo endereço antes de o domínio estar registrado, apontado via DNS, publicado no GitHub Pages e com HTTPS funcionando.**

Para migrar o domínio:
1. Verifique a titularidade ou registre `controlesafra.com.br` no Registro.br.
2. Em **Settings → Pages → Custom domain**, configure `controlesafra.com.br`. Isso cria/configura o arquivo `CNAME` para publicação por branch.
3. No provedor DNS do domínio, configure 4 registros `A` para o host `@` apontando para:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
4. Configure também `CNAME` de `www` para `brunohalla.github.io` (sem `/coletor-monte-cristo`).
5. Após propagação e emissão do certificado, ative **Enforce HTTPS**. Verifique ambos: `https://controlesafra.com.br` e `https://www.controlesafra.com.br`.
6. Somente então edite o Website Link no John Deere Developer Portal.

Fonte: documentação oficial GitHub Pages sobre domínio personalizado e HTTPS.

## Dados de cadastro para John Deere Developer Portal
- **Application Name**: Controle Safra - Coletor John Deere
- **Website Link**: https://controlesafra.com.br (após ativação)
- **Short Description (150–200 caracteres)**:
  > Aplicação privada do Controle Safra para integrar dados autorizados do John Deere Operations Center, consolidando operações agrícolas, máquinas, áreas e mapas da Fazenda Monte Cristo.
- **Modalidade**: aplicação privada para integração interna da Fazenda Monte Cristo.

Não crie outra aplicação apenas por mudança de marca. Preserve o cadastro existente e confira **Security / Redirect URIs**, **API access** e **Connected Organizations**. Website Link e Redirect URI são informações distintas; não altere o callback do OAuth sem conferir o endereço efetivamente usado pelo Coletor.

Este repositório contém apenas a página institucional; **não inclua tokens, Client Secret, credenciais, dados da fazenda ou arquivos operacionais**.
