# LaboratorioMLBicicletas
Um projeto de estudo usando o Azure ML.
Esse projeto vem de um curso ministrado pela Digital Innovation One, onde nos ensinou a fazer e configurar a nossa conta no Azure e então dar inicio ao projeto.
Primeiramente iniciamos o Azure Machine Learning studio através do portal do Azure.
Depois escolhemos criar novo trabalho de ML automatizado e ajustamos as definições , assim como nome do trabalho, nome do experimento e a descrição.
Então escolhemos o tipo de tarefa (a qual escolhemos regressão) e selecionamos o conjunto de dados a qual demos o nome, descrição e definimos o tipo como tabular.
Escolhemos a fonte de dados a qual alimentamos a ML. Esse fonte de um arquivo web a qual definimos uma url que peguei da documentação da microsoft.
Após esse processo foi a hora de alterar as configurações. Escolhemos a tarefa de regressão e demos os nomes aos conjuntos de dados e as colunas de destino. Definimos então a métrica primária como Normalized root mean squared error e escolhemos como modelos permitidos os RamdomForest e o LightGMB.
Então foi a hora de definir os limites. O máximo de testes, o máximo de testes simultâneos e o máximo de nós definimos em 3. O limite de pontuação da métrica foi definido em 0.085. O tempo limite e o tempo limite de interação ambos foram definidos em 15 e deixamos o Habilitar rescisão antecipada selecionado.
Em validação e teste definimos o tipo de validação em Train-validation split. Já na porcentagem de dados de validação demos o valor de 10 e não selecionamos nenhum conjunto de dados de teste.
Por fim fomos para as definições de calculo, onde em tipo de computação escolhemos em não usar um servidor e definimos a CPU como tipo de maquina virtual tendo uma chamada dedicada, com o tamanho Standart_DS3_V2 e de apenas uma instâcia.
Depois enviamos o trabalho para treinamento e o tempo que durou foram 8 minutos.
