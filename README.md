# TCC
Projeto do TCC - MBA

----------------------------------------------------------------------

Features:

  - porto : ["Aratu - Salvador", "Manaus", "Natal", "Pecém - Fortaleza", "Porto Velho", "Suape - Recife", "Vila do Conde"]
  
  - mes : ["jan", "fev", "mar", "abr", "mai", "jun", "jul", "ago", "set", "out", "nov", "dez"]
    
  - tipo_navegação : ["Cabotagem", "Longo Curso", "Interior"]
    
  - tipo_operacao : ["Interior", "Longo Curso Importação", "Cabotagem", "Baldeação de Carga Estrangeira de Passagem", "Baldeação de Carga Nacional", "Longo Curso Exportação", "Longo Curso Exportação com Baldeação de Carga Estrangeira", "Longo Curso Importação com Baldeação de Carga Estrangeira", "Movimentação de Carga"]
    
  - mercadoria : ["Maquinário", "Alumínio", "Cereais", "Ferro", "Frutas", "Madeira e Carvão", "Materiais de Construção", "Materiais e aparelhos elétricos", "Papel e seus derivados", "Plásticos", "Produtos Químicos Orgânicos"]
    
  - peso_carga : float64()


Target:


  - nivel_atraso : ["Bom", "Moderado", "Ruim"]


Onde as classificações da Target são:

  - Bom: Tempo de espera < 10 minutos
  - Moderado: Tempo de espera entre 10 minutos e 2 horas
  - Ruim: Tempo de espera maior do que 2 horas


-----------------------------------------------------------------------------

Modelo escolhido com base na maior acurácia:

XGBClassifier(verbosity=0, n_estimators=950, learning_rate=0.01, max_depth=8)

-----------------------------------------------------------------------------

Resultado do gráfico da área abaixo da curva ROC para o modelo escolhido:

![roc_xgb](https://github.com/user-attachments/assets/92732b72-42de-4140-9d24-8ef5517f160b)

----------------------------------------------------------------------------

Endpoint da API que recebe as features, no formato JSON, para previsão do modelo XGB treinado:

  - https://vps.butturi.com.br/predict

--------------------------------------------------------------------------

Site que envia as features em JSON para a API, evitando erros de digitação e dispensando conhecimento em programação:

  - https://butturi.com.br/analise_atraso
