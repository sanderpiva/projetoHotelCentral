<h1>Projeto Hotel Central</h1>
<div>
  <p>O projeto Hotel Central trata-se de um exemplo de ChatBot, baseado em Processamento de Linguagem Natural, que visa proporcionar ao usuário uma interação de um chatbot
  sobre o tema 'Hotel Central'. O Hotel Central é um caso de um hotel bem estruturado, confortável e com boas opções de lazer e entreterimento que fica na cidade fictícia de Rio Preto SP
  perto da praça Dom Udarico Rechiel, permitindo aos seus hóspedes uma excelente estadia, descando e acesso aos principais centros comerciais e empresariais.</p>
</div>
<div>
  <p>
    Em termos de codifificação, em linhas gerais, foi implementado um código no Google Colab 'Hotel_Central_ChatbotBackend.ipynb' cujo dataframe (base de dados)
    é 'dados2_pln_sem_acento', onde após o correto carregamento do dados, do 'model = 'models/text-embedding-004', é chamado o método 'gerarEmbeddings' para gerar 
    embeddings aos registros ou linhas do dataframe cujas colunas são 'Titulo' e 'Conteudo'. Os embeddings são representações numéricas dos tokens processados na rede neural (768 camadas), porém essa numeração não representa diretamente o respectivo token em si, mas sim suas caracteristicas abstratas como significado, contexto, sintaxe e semântica.
  </p>
</div>
<div>
  <p>
    Na prática, será obtido um novo dataframe com uma coluna adicional 'Embeddings', correspondente a cada registro. Quando o método 'gerarBuscaConsulta' for chamado,
    passando os parametros 'consulta' e o 'dafatframe' novo, será possível realizar testes de consulta onde a pergunta, consulta será um 'embedding' que será mapeado dentro 
    do dataframe com os seus embeddings. A resposta, cuja probabilidade varia entre 0 - 100%, deverá ser o resultado com probabilidade mais perto de 100%. Isso significa que a resposta
    fornecida é a que mais se aproxima daquilo que foi consultado ou perguntado.
    Supondo que tenha funcionado, o próximo passa será pegar o dataframe e salva-lo em um arquivo chamado datasetEmbeddings.pkl. 
    Ao salvar o DataFrame, ele é convertido em uma representação binária
    que pode ser facilmente armazenada e carregada posteriormente. O código no Google Colab, seu dataframe, incluindo fotos de testes no Postman estão disponíveis nesse repositório
    para download. 
  </p>
</div>
<div>
  <p>
    O arquivo exportado será utilizado para uma implementação em Flask, testado em máquina local e com a ferramenta Postman. Na sequencia o codigo em Flask é hospedado em uma
    conta da Azure (Azure Students) para ser o 'backend' da aplicação. Uma vez que tudo tenha funcionado, é implementada uma aplicação em React para funcionar como 'frontend' 
    e, com o endereço do projeto em Flask da Azure configurado, utilizar esse Flask para realizar consultas em um chatbot desenvolvido em React exclusivamente para a 
    proposta do Hotel Central. Os repositórios para consulta do código em Flask, hospedado na Azure Students, do React e ainda do código da aplicação final hospedado na Vercel, 
    são disponibilidados a seguir:
  </p>
  <ol>
    <li>Flask: https://github.com/sanderpiva/flask_hotel2.git</li>
    <li>React: https://github.com/sanderpiva/react_hotel_central.git</li>
    <li>Vercel: https://react-hotel-central.vercel.app/</li>
  </ol>
</div>
<div>
  <p>Integrantes do projeto: </p>
</div>
<div>
  <p>Algumas fotos da aplicação final: </p>
  <img src="https://github.com/sanderpiva/projetoHotelCentral/blob/main/fotos_hotel_central_vercel/foto1_app_hotel_central.png" alt="Foto 1: ChatBot Hotel Central">
  <p>Foto 1: ChatBot Hotel Central</p><br><br>
  <img src="https://github.com/sanderpiva/projetoHotelCentral/blob/main/fotos_hotel_central_vercel/foto2_app_hotel_central.png" alt="Foto 2: Consulta sobre lazer e atrações do Hotel Central">
  <p>Foto 2: Consulta sobre lazer e atrações do Hotel Central</p><br><br>
  <img src="https://github.com/sanderpiva/projetoHotelCentral/blob/main/fotos_hotel_central_vercel/foto3_app_hotel_central.png" alt="Foto 3: As opções de lazer e atrações do Hotel Central">
  <p>Foto 3: As opções de lazer e atrações do Hotel Central</p><br><br>

</div>
