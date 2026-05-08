# Mapa Interativo das Zonas Eleitorais da Cidade de São Paulo

Aplicação HTML standalone para visualizar, selecionar, organizar e exportar análises territoriais das zonas eleitorais da cidade de São Paulo.

O projeto foi pensado para ser simples de compartilhar: basta baixar o arquivo `.html` e abrir no navegador. Não requer instalação, servidor, backend ou dependências. O mapa, os controles, as seleções, os campos editáveis e a exportação ficam dentro de um único arquivo.

## Versão atual

**v2.1.0 - Organização avançada, campos dinâmicos e progresso importável**

Esta versão mantém o foco exclusivo no mapa das zonas eleitorais da cidade de São Paulo e adiciona recursos para organizar melhor as seleções, personalizar as informações de cada zona e salvar/restaurar o progresso do trabalho.

## Principais recursos

- Mapa SVG interativo das zonas eleitorais da cidade de São Paulo.
- Seleção de zonas por grupo com título obrigatório.
- Escolha de cor para cada grupo selecionado.
- Destaque visual das zonas selecionadas no mapa.
- Zoom vetorial do mapa, sem perda de qualidade.
- Zoom máximo ampliado para 400%.
- Controle de deslocamento nos eixos X e Y.
- Redimensionamento dos rótulos das zonas.
- Título editável do relatório/PDF.
- Campos editáveis por zona:
  - votos do candidato;
  - eleitores;
  - estimativa de votos válidos;
  - eleitores alvo;
  - observações.
- Títulos dos campos editáveis.
- Botão `+` para adicionar novos campos de texto em cada box de zona.
- Botão `×` para remover/ocultar campos padrão ou personalizados das boxes.
- Reordenação manual dos blocos de seleção por arrastar e soltar.
- Reordenação manual das boxes de zonas dentro de cada seleção.
- Arraste restrito às áreas de título, evitando conflito com campos editáveis.
- Painel de ordenação opcional para ordenar blocos ou boxes automaticamente.
- Ordenação por número da zona, título da seleção ou valor de campos preenchidos, como “votação” ou “eleitores”.
- Exclusão de grupos de zonas com confirmação.
- Exportação para impressão/PDF em A4 retrato.
- Exportação preservando o enquadramento atual do mapa: zoom, X e Y.
- Exportação dos campos personalizados no relatório.
- Ocultação de campos removidos também no relatório.
- Salvamento local automático via `localStorage`.
- Botão **Salvar progresso** para exportar o estado atual em `.json`.
- Botão **Importar progresso** para restaurar seleções, campos, ordem manual e enquadramento visual.

## Como usar

### 1. Abrir a aplicação

Baixe o arquivo HTML do projeto e abra no navegador.

Navegadores recomendados:

- Google Chrome
- Microsoft Edge
- Brave
- Firefox atualizado

Não é necessário instalar nada.

### 2. Ajustar o mapa

No cabeçalho, use os controles:

- **Rótulos**: altera o tamanho dos números das zonas.
- **Zoom**: aproxima ou afasta o mapa.
- **X**: move o enquadramento para esquerda ou direita.
- **Y**: move o enquadramento para cima ou para baixo.
- **Resetar visão**: volta o enquadramento ao padrão.

A exportação usa o enquadramento atual do mapa. Antes de gerar o relatório, ajuste o zoom e a posição. Parece detalhe, mas é exatamente onde relatório bonito vira print torto.

### 3. Criar uma seleção de zonas

No painel lateral:

1. Digite um título para a seleção.
2. Escolha uma cor.
3. Clique nas caixinhas das zonas no mapa.
4. Confira a lista de zonas selecionadas.
5. Clique em **Confirmar seleção**.

Cada seleção confirmada aparece no painel de **Seleções confirmadas**.

### 4. Editar informações das zonas

Em cada zona selecionada, preencha ou edite os campos:

- `VOTOS [CANDIDATO]:`
- `ELEITORES:`
- `ESTIMATIVA DE VOTOS VÁLIDOS:`
- `ELEITORES ALVO:`
- observações adicionais.

Os títulos dos campos também são editáveis. Isso permite trocar, por exemplo, `VOTOS [CANDIDATO]:` por `VOTOS DRA. SANDRA TADEU - 2024:`.

### 5. Adicionar ou remover campos nas boxes

Cada box de zona possui controles próprios:

- use o botão `+` para adicionar uma nova caixa de texto;
- edite o título do novo campo;
- preencha o valor desejado;
- use o botão `×` para remover campos padrão ou personalizados.

Campos removidos deixam de aparecer no painel e também não são exibidos no relatório exportado.

### 6. Reordenar blocos e zonas manualmente

Nas seleções confirmadas, a ordem pode ser ajustada manualmente.

Para reordenar blocos de seleção:

1. Clique e segure no título do bloco de seleção.
2. Arraste o bloco inteiro para a posição desejada.
3. Solte.

Para reordenar zonas dentro de uma seleção:

1. Clique e segure no título da zona ou no ícone de arraste.
2. Arraste a box para a posição desejada.
3. Solte.

A ordem personalizada é preservada no painel, no salvamento de progresso e na exportação/PDF.

### 7. Usar o painel de ordenação

Além da ordenação manual, a aplicação possui um painel de ordenação opcional.

Ele permite ordenar:

- blocos de seleção;
- boxes de zonas dentro das seleções.

Critérios disponíveis:

- título da seleção;
- número da zona;
- valor de uma caixa de texto, como “votação”, “eleitores”, “votos” ou qualquer campo personalizado;
- ordem crescente ou decrescente.

### 8. Editar ou excluir uma seleção

Para editar:

1. Use o campo **Editar seleção existente**.
2. Escolha o grupo.
3. Altere título, cor ou zonas.
4. Confirme novamente.

Para excluir:

1. Clique no botão `×` no canto superior do grupo.
2. Confirme a exclusão.

A exclusão remove o grupo e os dados preenchidos nele.

### 9. Salvar e importar progresso

A aplicação salva automaticamente no navegador usando `localStorage`, mas também permite exportar um arquivo de progresso.

Use:

- **Salvar progresso**: baixa um arquivo `.json` com o estado atual do trabalho.
- **Importar progresso**: restaura um arquivo `.json` salvo anteriormente.

O arquivo de progresso preserva:

- seleções criadas;
- cores;
- campos preenchidos;
- campos personalizados;
- campos removidos/ocultos;
- ordem manual dos blocos de seleção;
- ordem manual das boxes de zonas;
- título do relatório;
- tamanho dos rótulos;
- zoom;
- posição X e Y do mapa.

Use o arquivo `.json` quando precisar continuar o trabalho em outro navegador, outro computador ou depois de limpar dados locais.

### 10. Gerar PDF ou relatório

Use:

- **Gerar impressão**: abre uma aba com o relatório pronto para imprimir ou salvar em PDF.
- **Exportar HTML do relatório**: baixa um HTML separado com o relatório.

Na tela de impressão, escolha **Salvar como PDF**.

Configuração recomendada:

- Papel: A4
- Orientação: retrato
- Escala: padrão ou ajustar à página
- Gráficos de plano de fundo: ativado, se o navegador oferecer essa opção

## Salvamento dos dados

A aplicação salva dados no próprio navegador usando `localStorage`.

Isso inclui:

- seleções criadas;
- cores;
- campos preenchidos;
- campos personalizados;
- campos ocultos/removidos;
- ordem dos blocos de seleção;
- ordem das boxes de zonas;
- título do relatório;
- tamanho dos rótulos;
- zoom e posição do mapa.

Atenção: os dados salvos em `localStorage` ficam no navegador e no dispositivo usados. Se abrir o arquivo em outro computador ou outro navegador, os dados não vão junto automaticamente.

Para transportar o trabalho, use **Salvar progresso** e depois **Importar progresso**.

## Arquivos recomendados no repositório

- `Mapa Interativo - ZONAS ELEITORAIS da Cidade de São Paulo.html`
- `README.md`
- `CHANGELOG.md`
- `LICENSE`

## Créditos

Mapa-base: Sailoratlantis, Avrelianvs Magnvs e demais colaboradores do Wikimedia Commons, licenciado sob CC BY-SA 4.0.

Adaptação interativa: netunoflex.

## Licença

Este projeto é uma adaptação interativa baseada em mapa licenciado sob CC BY-SA 4.0.

Ao redistribuir, adaptar ou publicar versões derivadas, mantenha:

- atribuição aos autores do mapa-base;
- atribuição da adaptação interativa;
- indicação de que se trata de obra derivada;
- licença compatível com CC BY-SA 4.0.

## Observações importantes

Este projeto é uma ferramenta de apoio visual e estratégico. Ele não substitui bases oficiais da Justiça Eleitoral, cartórios eleitorais, TRE-SP ou demais fontes institucionais.

Antes de usar em apresentação pública, campanha, estudo técnico ou material institucional, valide os dados eleitorais com fontes oficiais.
