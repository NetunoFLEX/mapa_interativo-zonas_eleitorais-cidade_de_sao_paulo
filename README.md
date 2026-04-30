# Mapa Interativo das Zonas Eleitorais da Cidade de São Paulo

Aplicação HTML standalone para visualizar, selecionar, organizar e exportar análises territoriais das zonas eleitorais da cidade de São Paulo.

O projeto foi pensado para ser simples de compartilhar: basta abrir o arquivo `.html` no navegador. Sem instalação, sem servidor, sem backend, sem dependências. O mapa, os controles e a exportação ficam dentro de um único arquivo.

## Principais recursos

- Mapa SVG interativo das zonas eleitorais de São Paulo.
- Seleção de zonas por grupo com título obrigatório.
- Escolha de cor para cada grupo selecionado.
- Destaque visual das zonas selecionadas no mapa.
- Zoom vetorial do mapa, sem perda de qualidade.
- Controle de deslocamento nos eixos X e Y.
- Redimensionamento dos rótulos das zonas.
- Campos editáveis por zona:
  - votos do candidato;
  - eleitores;
  - estimativa de votos válidos;
  - eleitores alvo;
  - observações.
- Reordenação manual dos blocos das zonas por arrastar e soltar.
- Exclusão de grupos de zonas com confirmação.
- Título editável do relatório/PDF.
- Exportação para impressão/PDF em A4 retrato.
- Exportação preservando o enquadramento atual do mapa: zoom, X e Y.
- Salvamento local automático via `localStorage`.

## Como usar

### 1. Abrir a aplicação

Baixe o arquivo HTML do projeto e abra no navegador.

Recomendado:

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
- **Y**: move o enquadramento para cima ou baixo.
- **Resetar visão**: volta o enquadramento ao padrão.

A exportação usa o enquadramento atual do mapa. Então ajuste o zoom e a posição antes de gerar o relatório.

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

### 5. Reordenar zonas

Nas seleções confirmadas, os blocos das zonas aparecem em ordem crescente por padrão.

Para alterar a ordem:

1. Clique e segure no bloco da zona ou no ícone de arraste.
2. Arraste para a posição desejada.
3. Solte.

A ordem personalizada é salva e também será usada na exportação/PDF.

### 6. Editar ou excluir uma seleção

Para editar:

1. Use o campo **Editar seleção existente**.
2. Escolha o grupo.
3. Altere título, cor ou zonas.
4. Confirme novamente.

Para excluir:

1. Clique no botão `×` no canto superior do grupo.
2. Confirme a exclusão.

A exclusão remove o grupo e os dados preenchidos nele.

### 7. Gerar PDF ou relatório

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
- ordem dos blocos;
- título do relatório;
- tamanho dos rótulos;
- zoom e posição do mapa.

Atenção: os dados ficam salvos no navegador e no dispositivo usados. Se abrir o arquivo em outro computador ou outro navegador, os dados não vão junto automaticamente. Tecnologia local é assim: fiel, mas caseira.

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
