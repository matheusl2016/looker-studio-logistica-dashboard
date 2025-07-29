# looker-studio-logistica-dashboard
Dashboard logístico interativo criado com Looker Studio, com foco em análise de desempenho operacional

1. Conexão com Google Sheets via Looker Studio, utilizando quatro fontes de dados:

Produtos
Estoque
Veículos
Pedidos

2. Criação de métricas logísticas personalizadas, com lógica de negócios

  Algumas das fórmulas usadas no projeto:
  -- Média de dias para entrega (Ship-to-Door)
AVG(DATE_DIFF(Data de entrega, Data da compra))

-- Tempo de espera da entrega
DATE_DIFF(Data previsão, Data de entrega)

3. Cálculos com filtros lógicos no Looker Studio:

    Entregas no prazo:
  Filtro → Tempo de espera >= 0
  Agregação → COUNT()

    Entregas em atraso:
  Filtro → Tempo de espera < 0
  Agregação → COUNT()

    Veículos disponíveis:
  Filtro → Status = "Disponível"
  Agregação → COUNT(ID Veículos)

4. Visualizações criadas:
Cartões de Visão Geral: Entregas no prazo, em atraso e veículos disponíveis
Gráfico de Barras: Média de estoque por ano
Gráfico de Linhas: Média de dias de entrega (S2D) ao longo do tempo
Mapa Coroplético (Heatmap): Pedidos por estado (BR)
Relatório Mobile: Dashboard responsivo 100% ajustado para celulares
