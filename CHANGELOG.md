## [v2.1.0] - Organização avançada, campos dinâmicos e progresso importável

### Adicionado

- Botão **Salvar progresso**, exportando o estado atual da aplicação em arquivo `.json`.
- Botão **Importar progresso**, permitindo restaurar seleções, campos, ordem dos blocos e enquadramento visual.
- Salvamento/importação de:
  - seleções confirmadas;
  - cores das seleções;
  - dados preenchidos nas zonas;
  - campos personalizados;
  - campos ocultos/removidos;
  - ordem manual dos blocos de seleção;
  - ordem manual das boxes de zonas;
  - título do relatório;
  - zoom;
  - eixo X;
  - eixo Y;
  - escala dos rótulos.
- Botão `+` em cada box de zona para adicionar novos campos de texto.
- Campos personalizados com label editável, valor editável e botão de remoção.
- Botão `×` para remover/ocultar campos padrão dentro de cada box de zona.
- Reordenação manual dos blocos de seleção por arrastar e soltar.
- Alça visual de arraste nos títulos dos blocos de seleção.
- Painel de ordenação opcional.
- Ordenação automática opcional de blocos de seleção por título.
- Ordenação automática opcional de boxes de zonas por:
  - número da zona;
  - valor de uma caixa de texto;
  - direção crescente ou decrescente.
- Seleção de escopo para ordenar boxes em todas as seleções ou em uma seleção específica.
- Suporte a ordenação por campos como “votação”, “eleitores”, “votos” ou campos personalizados.

### Alterado

- Boxes de zonas passaram a funcionar como fichas configuráveis, com campos padrão, campos ocultáveis e campos personalizados.
- Relatório/exportação passou a renderizar campos dinamicamente, respeitando campos removidos e campos adicionados.
- Ordem manual dos blocos de seleção passou a ser preservada no painel e no relatório.
- Ordem manual das boxes de zonas passou a ser preservada no painel e no relatório.
- A ordenação automática passou a ser complementar, sem substituir o controle manual por arraste.
- O estado da aplicação passou a ser exportável e importável por JSON, reduzindo dependência exclusiva do `localStorage`.
- Controles de deslocamento dos eixos X e Y foram ampliados para permitir maior ajuste visual do mapa.

### Corrigido

- Corrigida a limitação de poder remover campos das boxes sem conseguir adicionar novos campos.
- Corrigida a ausência de ordenação manual dos blocos principais de seleção.
- Corrigida a perda de contexto ao recarregar ou transferir trabalho entre sessões, com a introdução de salvar/importar progresso.
- Corrigida a inconsistência entre campos editados no painel e campos exibidos no relatório.
- Melhorada a usabilidade para análises em que a ordem narrativa dos blocos é mais importante que a ordem numérica das zonas.
