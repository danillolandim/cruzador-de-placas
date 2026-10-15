# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Alunos da disciplina Ferramentas Tecnológicas e Plataformas de Apoio (CIAR), policiais em formação. O uso principal é em aula: o professor projeta a página e conduz o exercício, e a turma acompanha à distância. A página precisa ser lida no telão por quem está no fundo da sala.

## Product Purpose

Ensinar a análise de rota com câmeras OCR. O aluno calcula a janela de horário de cada ponto da rota para consultar no Córtex, depois cruza os CSVs exportados do Consulta Radares (um por ponto) e vê quais placas passaram em todos os pontos, na ordem. Sucesso é o aluno entender o raciocínio vendo-o acontecer: a rota, as janelas no tempo e a lista de placas encolhendo a cada ponto até sobrar quem fez o trajeto.

## Positioning

Não é um sistema de consulta: é a aula de análise de rota em forma de ferramenta. Mostra o método (janela, consulta, cruzamento, qualificação), não só a resposta.

## Operating Context

- Aula expositiva com projetor; depois os alunos repetem no laboratório.
- Fluxo real: Google Maps (tempo de trajeto) → Córtex 1.0 (uma data por consulta, hora de Brasília em todos os pontos, inclusive MS, passagens chegam com 1 a 2 h de atraso) → exportação CSV do Consulta Radares (colunas Placa, MarcaModelo, Cor, UfEmplacamento, DataHoraPassagem, Local) → cruzamento → qualificação da placa (dono, quem dirige, locadora, passagens).
- Janela que passa da meia-noite vira duas consultas na mesma câmera; o Cruzador junta consultas emendadas num ponto só.

## Capabilities and Constraints

- Página única, HTML/CSS/JS, sem build, sem servidor: os arquivos são lidos só no navegador de quem usa e nada é enviado. Funciona offline (fontes embutidas).
- Duas tarefas: calcular janelas (saída + tempo do Maps + 1 h de parada a cada 3 h + folga de 1/3) e cruzar placas (2 a 10 pontos, exigir ordem opcional, mínimo de pontos, máscara de placa para projeção, exportação CSV com placa completa).
- Repositório público: só a página e dados fictícios entram nele.
- Em aberto: se a ordem da rota é declarada pelo analista ou deduzida pelos horários (hoje é deduzida).

## Brand Commitments

Nome: Cruzador de Placas. Interface em português do Brasil.

## Evidence on Hand

- Caso 1 "Bate e volta": base fictícia de 5 pontos no corredor DF ↔ Ponta Porã (BR-060, Rio Verde, BR-463), embutida em `index.html` (`const DEMO`). Resultado: 82 → 4 → 3 → 1 → 1, placa SGX4D17, 14h35 na fronteira.
- Não há fotos, logotipo, depoimentos nem dados reais; nada disso deve ser inventado.

## Product Principles

1. Mostrar o raciocínio, não só a resposta: cada etapa do método fica visível.
2. Legível no telão: quem está no fundo da sala precisa ler o que importa.
3. Dados do aluno nunca saem do computador.
4. Antes de concluir, conferir: o resultado sempre lembra o que pode estar errado.

## Accessibility & Inclusion

WCAG 2.1 AA. Uso com teclado e leitor de tela; contraste pensado para projetor (luz ambiente, imagem lavada).
