Projeto Individual Módulo 4 - Formação em Análise de Dados

Este notebook foi desenvolvido como parte do Projeto Individual do Módulo 4 do curso de Análise de Dados. 
O objetivo é gerar um relatório de progresso diário para avaliar a produtividade dos funcionários de uma empresa de desenvolvimento de softwares.

Dados Fornecidos
O conjunto de dados utilizado no projeto inclui informações sobre as horas trabalhadas, bugs corrigidos e tarefas concluídas em diferentes datas.

dados = {
    'Data': ['21 de Janeiro 2024', '13 de Janeiro 2024', '17 de Janeiro 2024', '24 de Janeiro 2024'],
    'Horas Trabalhadas': [8, 7, 9, 8],
    'Bugs Corrigidos': [2, 1, 3, 0],
    'Tarefas Concluidas': [10, 8, 12, 7]
}

df = pd.DataFrame(dados)
Análise e Relatório de Progresso Diário

Produtividade Diária:
A produtividade diária é calculada dividindo o número de tarefas concluídas pelas horas trabalhadas.

df['Produtividade'] = df['Tarefas Concluidas'] / df['Horas Trabalhadas']

Relatório:

O relatório inclui as seguintes métricas:
Total de Horas Trabalhadas
Média Diária de Horas Trabalhadas
Total de Bugs Corrigidos
Média Diária de Bugs Corrigidos
Total de Tarefas Concluídas
Média Diária de Tarefas Concluídas
Produtividade Diária (Tarefas por Hora)

relatorio = pd.DataFrame({
    'Total de Horas Trabalhadas': [df['Horas Trabalhadas'].sum()],
    'Média Diária de Horas Trabalhadas': [df['Horas Trabalhadas'].mean()],
    'Total de Bugs Corrigidos': [df['Bugs Corrigidos'].sum()],
    'Média Diária de Bugs Corrigidos': [df['Bugs Corrigidos'].mean()],
    'Total de Tarefas Concluídas': [df['Tarefas Concluidas'].sum()],
    'Média Diária de Tarefas Concluídas': [df['Tarefas Concluidas'].mean()],
    'Produtividade Diária (Tarefas por Hora)': [df['Produtividade'].mean()]
})

Utilização do Código:
Certifique-se de ter o ambiente do Google Colab configurado.
Copie e cole o código no seu notebook do Google Colab.
Execute cada célula sequencialmente para visualizar os resultados.
Este notebook fornece uma análise básica e pode ser expandido conforme necessário para atender aos requisitos específicos do projeto. Lembre-se de personalizar os dados conforme a estrutura real do seu conjunto de dados.






