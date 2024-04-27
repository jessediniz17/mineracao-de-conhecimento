# Mineração de Conhecimento
Projeto de mineração de conhecimento utilizando Azure Cognitive Search



O objetivo, o qual descreverei passo a passo nesse arquivo readme, foi utilizar ferramentas do Microsoft Azure para realizar buscas cognitivas. A utilização em conjunto dessas ferramentas é muito poderosa, e pode ser usada diretamente no Microsoft Azure ou implantada em outros softwares, para se obter uma quantidade massiva de dados e insights para tomada de decisão.

Um exemplo de utilização dessas ferramentas poderia ser um renomado restaurante de uma cidade. Eles podem realizar um post em uma rede social para obter comentários e avaliações de seus clientes, para saber seus pontos fracos e fortes. Também podem fazer uma busca por dados em uma planilha ou software, para saber quais os produtos mais vendidos em um determinado mês, qual o horário e dia de maior movimentação, etc. 

A princípio, podem parecer coisas simples, mas são informações valiosíssimas para quem utiliza as ferramentas com o intuito de obter insights e tomar decisões baseadas em dados.



O primeiro passo é criar um novo serviço de pesquisa, lembrando de colocar um nome que faça sentido e alterar o preço para *Basic*. 

O próximo passo é criar um recurso de IA, seguindo o caminho *Criar um recurso* >> *Ia + Machine Learning* >> *Serviços Cognitivos*. Após criar o recurso, o próximo passo é criar uma conta de armazenamento, seguindo os passos *Storage account* >> *Create a storage account*, lembrando de preencher os dados corretamente.

	* Performance: Standard
	* Redundancy: GRS



Depois que nosso storage for criado, precisamos fazer uma configuração antes de seguir para a próxima etapa. No menu lateral, vá em *Configurações* e mude a opção *Permitir Blobs de acesso anônimo* para "Habilitado". Ainda no menu lateral, vá na opção *Data Storage* e crie um novo contâiner, nomeando-o e escolhendo a opção *Container*.

Abra o contâiner criado e faça upload dos arquivos que você precisará baixar nesse link (https://aka.ms/mslearn-coffee-reviews).

Voltamos para o mecanismo de busca (AI Search) para fazer as configurações necessárias. Clicamos na opção *Armazenamento de Blob do Azure* e seguimos para os passos seguintes, preenchendo os campos que são necessários, e escolhendo o arquivo de *coffee reviews*, o qual fizemos o download. Ele será a base para nossa pesquisa.

Ainda no AI Search, vamos em *Gerenciador de pesquisas*. Note que, no campo *Índice*, vai estar o índice que acabamos de criar, com base no contâiner *coffee reviews*
