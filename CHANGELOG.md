# Changelog

Todas as mudanças relevantes deste projeto serão documentadas aqui.

Formato inspirado em [Keep a Changelog](https://keepachangelog.com/pt-BR/).

## [v2] - Versão atual

### Adicionado

- Reordenação manual dos blocos de zonas nas seleções confirmadas por arrastar e soltar.
- Preservação da ordem personalizada dos blocos na exportação/PDF.
- Manutenção da ordem crescente das zonas como padrão inicial.
- Ícone visual de arraste nos títulos das zonas.
- Exclusão de grupos de zonas selecionadas com botão `×`.
- Confirmação antes de excluir um grupo de zonas.
- Zoom máximo do mapa ampliado para 400%.
- Padronização do bloco de observações na exportação:
  - título em negrito;
  - texto em peso normal;
  - mesmo padrão visual dos demais blocos.
- Créditos atualizados:
  - mapa-base atribuído a Sailoratlantis, Avrelianvs Magnvs e demais colaboradores do Wikimedia Commons;
  - adaptação interativa atribuída a netunoflex.

### Alterado

- Exportação em PDF ajustada para melhorar o encaixe dos blocos logo abaixo do mapa.
- Exportação configurada em A4 retrato.
- Blocos de métricas no PDF organizados em grade:
  - linha superior: votos do candidato e eleitores;
  - linha inferior: estimativa de votos válidos e eleitores alvo;
  - observações abaixo, exibidas apenas quando preenchidas.
- Edição de seleções agora preserva a ordem customizada sempre que possível.
- Novas zonas adicionadas durante edição entram ao final da seleção, mantendo a ordenação crescente entre elas.
- Visual dos blocos exportados refinado para leitura mais limpa.

### Corrigido

- Corrigido o salto de página que fazia os blocos das zonas começarem apenas na página seguinte ao mapa.
- Corrigido comportamento de exportação para preservar melhor a cor das seleções no mapa.
- Corrigida a diferença visual do título de observações em relação aos demais títulos de blocos.

## [v1] - Versão anterior

### Recursos existentes

- Mapa SVG interativo standalone.
- Seleção de zonas eleitorais por grupo.
- Escolha de cor por seleção.
- Painel lateral com seleções confirmadas.
- Campos editáveis por zona:
  - votos do candidato;
  - eleitores;
  - estimativa de votos válidos;
  - eleitores alvo;
  - observações.
- Título editável do PDF.
- Exportação para impressão/PDF em A4 retrato.
- Exportação preservando o enquadramento atual do mapa.
- Zoom vetorial do mapa.
- Controle de deslocamento nos eixos X e Y.
- Salvamento local via `localStorage`.

### Limitações conhecidas

- Blocos das zonas não eram reordenáveis manualmente.
- Grupos de zonas não tinham botão direto de exclusão com confirmação.
- Zoom máximo limitado a 300%.
- Observações no PDF tinham diferença visual em relação aos demais blocos.
- Quebra de página podia empurrar os blocos para depois do mapa, deixando área branca excessiva.
