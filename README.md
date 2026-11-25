# Inventário de Dados da SRE – ANPD

Página do Plano de Dados Abertos da Superintendência de Regulação, feita para ser embutida (iframe) no portal da ANPD.

- Página: https://tsouto.github.io/anpd-inventario-sre/?embed=1
- `?embed=1` esconde a barra gov.br, o cabeçalho e o rodapé (a página já fica dentro do portal).

## Como atualizar os dados

1. Gere o novo HTML do inventário a partir da planilha "Inventário de Dados SRE — Plano de Dados Abertos".
2. Renomeie o arquivo para **`index.html`** (exatamente esse nome).
3. Neste repositório, clique em **Add file → Upload files**.
4. Arraste o `index.html`. O GitHub substitui o arquivo antigo.
5. Em "Commit changes", descreva a atualização (ex.: `Dados de dezembro de 2026`) e clique em **Commit changes**.
6. Aguarde cerca de 1 minuto e abra a página acima para conferir. Se ainda mostrar a versão antiga, recarregue com Ctrl+F5.

O andamento da publicação aparece na aba **Actions** (ícone verde = publicado).

## Código para o portal (Plone)

```html
<iframe src="https://tsouto.github.io/anpd-inventario-sre/?embed=1"
        width="100%" height="2600" style="border:0;"
        title="Inventário de Dados da SRE – ANPD" loading="lazy"></iframe>
```

A altura é fixa porque a página está em outro domínio; o ajuste automático só funciona no mesmo domínio do portal.
O domínio precisa estar na lista de domínios permitidos para iframe do portal gov.br.
