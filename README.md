## Trabalhando com Machine Learning na Prática no Azure ML

Este é passo a passo do projeto sobre Machine Learning na Prática utilizando o Azure ML da DIO.

### Passo 1: Criação do recurso do Azure Machine Learning

1. Clique em "Criar recurso" e pesquise por "Azure Machine Learning" no marketplace.
2. Forneça a assinatura para cobrança e especifique o Grupo de recursos.
3. Configure os detalhes do workspace, mantendo as configurações mínimas para um laboratório.
4. Crie o recurso após a validação ser aprovada.

### Passo 2: Configuração do recurso do Azure Machine Learning

1. Acesse a página do recurso clicando em "Ir para o recurso".
2. Na aba Básico > Detalhes do recurso, forneça a assinatura e o Grupo de recursos.
3. Em Detalhes da área de trabalho, especifique os detalhes do workspace e clique em "Criar".

### Passo 3: Criação do modelo

1. No estúdio, na página do workspace, acesse ML automatizado e clique em "Novo trabalho de ML automatizado".
2. Preencha os campos básicos e selecione o tipo de tarefa como Regressão.
3. Configure e selecione os dados, avançando através dos passos necessários.
4. Revisando as configurações, crie o modelo.

### Passo 4: Métricas do modelo

1. Acesse as métricas do modelo treinado através do link fornecido na página do modelo ou pela opção "Tarefas (jobs)" no menu.

### Passo 5: Teste do modelo

1. Na página do modelo, acesse a aba "Pontos de extremidade" e tente implantar o modelo.
2. Caso o botão não funcione, crie manualmente o ponto de extremidade em "Pontos de extremidade" no menu lateral.
3. Após a implantação, acesse a aba "Testar" do ponto de extremidade criado para realizar o teste do modelo com o seguinte JSON:

```json
{
  "input_data": {
    "data": [
       {
         "day": 1,
         "mnth": 1,   
         "year": 2022,
         "season": 2,
         "holiday": 0,
         "weekday": 1,
         "workingday": 1,
         "weathersit": 2, 
         "temp": 0.3, 
         "atemp": 0.3,
         "hum": 0.3,
         "windspeed": 0.3 
       }
     ]
  },
	"GlobalParameters": 1.0
}

O resultado do teste foi de 353.08.





