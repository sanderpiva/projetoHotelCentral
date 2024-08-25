<h1>Projeto Hotel Central</h1>
<div>
  <p>O projeto Hotel Central trata-se de um exemplo de ChatBot, baseado em Processamento de Linguagem Natural, que visa proporcionar ao usuário uma interação de um chatbot
  sobre o tema 'Hotel Central'. O Hotel Central é um caso de um hotel bem estruturado, confortável e com boas opções de lazer e entreterimento que fica na cidade fictícia de Rio Preto SP
  perto da praça Dom Udarico Rechiel, permitindo aos seus hóspedes uma excelente estadia, descanso e acesso aos principais centros comerciais e empresariais.</p>
</div>
<div>
  <p>
    Em termos de codifificação, em linhas gerais, foi implementado um código no Google Colab 'Hotel_Central_ChatbotBackend.ipynb' cujo dataframe (base de dados)
    é 'dados2_pln_sem_acento'. Após o correto carregamento do dados, bem como do modelo: 'model = 'models/text-embedding-004', é chamado o método 'gerarEmbeddings' para gerar 
    embeddings aos registros ou linhas do dataframe cujas colunas são 'Titulo' e 'Conteudo'. Os embeddings são representações numéricas dos tokens processados na rede neural (768 camadas), porém essa numeração não representa diretamente o respectivo token em si, mas sim suas caracteristicas abstratas como significado, contexto, sintaxe e semântica.
  </p>
</div>
<div>
  <p>
    Na prática, será obtido um novo dataframe com uma coluna adicional 'Embeddings', correspondente a cada registro. Quando o método 'gerarBuscaConsulta' for chamado,
    passando os parametros 'consulta' e o 'dafaframe' novo, será possível realizar testes de consulta onde a pergunta ou consulta será um 'embedding' que será mapeado dentro 
    do dataframe com seus embeddings. A resposta, cuja probabilidade varia entre 0 - 100%, deverá ser o resultado com probabilidade mais perto de 100%. Isso significa que a resposta
    fornecida é a que mais se aproxima daquilo que foi consultado ou perguntado.
    Supondo que tenha funcionado, o próximo passa será pegar o dataframe e salva-lo em um arquivo chamado datasetEmbeddings.pkl. 
    Ao salvar o DataFrame, ele é convertido em uma representação binária
    que pode ser facilmente armazenada e carregada posteriormente. O código no Google Colab, seu dataframe, incluindo fotos de testes no Postman estão disponíveis nesse repositório
    para download. 
  </p>
</div>
<div>
  <p>
    O arquivo exportado servirá como base para um projeto Flask, testado localmente e com o Postman. Em seguida, o backend Flask será hospedado na Azure Students. Após a configuração do      frontend React para consumir a API Flask, um chatbot será desenvolvido exclusivamente para o Hotel Central. Os repositórios dos projetos Flask, React e da aplicação final na Vercel       estão disponíveis nos links a seguir:
  </p>
  <ol>
    <li>Flask: https://github.com/sanderpiva/flask_hotel2.git</li>
    <li>React: https://github.com/sanderpiva/react_hotel_central.git</li>
    <li>Vercel: https://react-hotel-central.vercel.app/</li>
  </ol>
</div>
<div>
  <p>Integrantes do projeto: </p>
  <ul>
    <li>Darlene Silva Leão De Souza</li>
    <li>Renan Feliciano Rocha</li>
    <li>Sander Gustavo Piva</li>
  </ul>
</div>
<div>
  <h2>Algumas fotos do resultado dos testes no Postman:</h2>
  
  <img src="https://github.com/sanderpiva/projetoHotelCentral/blob/main/Imgs_Testes_Postman_Flask_Local_rodando/1.png" alt="Foto 1: Teste Postman nº 1">
  <p>Foto 1: Teste Postman nº 1</p><br><br>
  <img src="https://github.com/sanderpiva/projetoHotelCentral/blob/main/Imgs_Testes_Postman_Flask_Local_rodando/2.png" alt="Foto 2: Teste Postman nº 2">
  <p>Foto 2: Teste Postman nº 2</p><br><br>
  <img src="https://github.com/sanderpiva/projetoHotelCentral/blob/main/Imgs_Testes_Postman_Flask_Local_rodando/1.png" alt="Foto 3: Teste Postman nº 3">
  <p>Foto 3: Teste Postman nº 3</p><br><br>
  <p>- - - - - - </p>
  <p>Algumas fotos da aplicação final: </p>
  <img src="https://github.com/sanderpiva/projetoHotelCentral/blob/main/fotos_hotel_central_vercel/foto1_app_hotel_central.png" alt="Foto 4: ChatBot Hotel Central">
  <p>Foto 4: ChatBot Hotel Central</p><br><br>
  <img src="https://github.com/sanderpiva/projetoHotelCentral/blob/main/fotos_hotel_central_vercel/foto2_app_hotel_central.png" alt="Foto 5: Consulta sobre lazer e atrações do Hotel Central">
  <p>Foto 5: Consulta sobre lazer e atrações do Hotel Central</p><br><br>
  <img src="https://github.com/sanderpiva/projetoHotelCentral/blob/main/fotos_hotel_central_vercel/foto3_app_hotel_central.png" alt="Foto 6: As opções de lazer e atrações do Hotel Central">
  <p>Foto 6: As opções de lazer e atrações do Hotel Central</p><br><br>
  <h2>FIM</h2>
</div>
