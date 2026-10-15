---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

# Surface: Cruzador de Placas (index.html)

Mode: operate. Audience: alunos policiais em aula, página projetada no telão pelo professor; depois repetem no laboratório. Job: entender o método de análise de rota vendo o raciocínio (janela → consulta → passagens → cruzamento). Constraints: arquivo único, offline, nada sai do computador, WCAG AA, legível no fundo da sala.

## Direction contract

THESIS: A rota no tempo. Um gráfico de Marey (o gráfico de circulação dos despachantes de trem) é o palco da página: km da rota no eixo vertical, tempo no horizontal, janelas como faixas, cada placa como uma linha que atravessa ou não as faixas. Recusa o painel de cards com funil em barras e abas separadas.

OWN-WORLD: papel branco do gráfico de circulação sobre fundo cinza-azulado; tinta azul-marinho; azul de despacho forte no cabeçalho, nos botões primários e nas faixas de janela (translúcidas); lápis vermelho só para a placa em foco; linhas eliminadas em grafite claro; âmbar para avisos. Atkinson Hyperlegible Next (feita para leitura difícil) em caixa normal, Atkinson Hyperlegible Mono só para horários. Sem cards iguais, sem rótulos em caixa alta, sem pílulas.

STORY: o aluno vê as janelas da rota desenhadas antes de qualquer arquivo; carrega os CSVs e vê as passagens caírem dentro (ou fora) das faixas; avança ponto a ponto e vê as linhas das placas pararem até sobrar a linha vermelha. Conclui conferindo antes de afirmar.

FIRST VIEWPORT: faixa azul com o nome, uma frase do método e o estado (exemplo Caso 1, começar do zero). Logo abaixo, o gráfico em largura total (~60% da altura), estações à esquerda com nome e km, contagem "restam N" à direita de cada estação, controle "Mostrar até: P1 P2 P3 P4 P5" acima do gráfico, legenda curta. A frase-resultado ("1 placa passou pelos 5 pontos, na ordem") fica sobre o gráfico. Ação primária: avançar ponto a ponto.

FORM: assinatura = diagrama tempo × distância com eliminação passo a passo (candidato 1 da lista ordenada: Marey, mapa rodoviário, mapa de metrô, quadro de horários, sinalização DNIT, lousa, dossiê); escolhido pelo usuário sobre o sorteado (quadro de horários). seed:0ca53f8840cc18b1 (rolagem degradada, sem desafiantes: serviço bloqueado pelo proxy).

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance

## Unresolved
- Ordem da rota: declarada pela rota da calculadora; arquivos sem janela caem na ordem dos horários.
