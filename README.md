________________________________________
🕵️ Sherlock: Detecção de Phishing com Machine Learning
📋 Sobre o Projeto
Sherlock é um modelo de aprendizado de máquina desenvolvido para identificar URLs maliciosas, também conhecidas como phishing. O modelo analisa diversas características das URLs, como o comprimento, a estrutura e a presença de anormalidades, para prever se um link é seguro ou suspeito.
________________________________________
👥 Equipe
•	Ester
•	Gabriela
•	Gustavo
•	Mariana
________________________________________
🛠️ Tecnologias
•	Linguagem: Python
•	Bibliotecas: 
o	Pandas
o	NumPy
o	Scikit-learn
o	tld
o	re
o	urllib
o	joblib
________________________________________
📊 Etapas do Projeto
1.	Carregamento e Exploração dos Dados
O projeto utiliza um dataset com URLs classificadas como legítimas ou maliciosas. O dataset contém 549.346 registros com 2 colunas principais: a URL e o rótulo (legítima ou maliciosa).
2.	Pré-processamento dos Dados
o	Limpeza das URLs (remoção de padrões como 'www.')
o	Extração de características como comprimento da URL, presença de IP, uso de HTTPS, etc.
o	Criação de novas colunas para armazenar essas características.
3.	Treinamento do Modelo
o	O modelo foi treinado utilizando o Random Forest Classifier.
o	A precisão do modelo foi avaliada e atingiu 79,04%.
4.	Classificação de URLs
o	A partir das características extraídas, o modelo pode prever se uma URL é confiável ou não.
o	O modelo foi validado utilizando URLs de exemplo e produziu previsões precisas.
________________________________________
🚀 Como Executar
1.	Instale as dependências:
Crie um ambiente virtual e instale as dependências necessárias.
2.	pip install -r requirements.txt  
3.	Pré-processamento e Extração de Características:
Use o script preprocessing.py para processar os dados e gerar as características necessárias.
4.	Treinamento do Modelo:
Execute o script model.py para treinar o modelo utilizando o Random Forest Classifier.
5.	python src/model.py  
6.	Teste do Modelo:
Para testar o modelo com novas URLs, execute o script predict.py com o arquivo contendo as URLs de teste.
7.	python src/predict.py --input data/test_urls.csv  
________________________________________
📈 Resultados
Treinamento e Teste do Modelo
•	Acurácia: O modelo obteve uma precisão de 79,04% no conjunto de teste, utilizando o algoritmo Random Forest Classifier.
Previsão de Classe de URL
•	Exemplo de URL: "super1000.info/docs"
•	Características extraídas:
o	Comprimento da URL: 19
o	Contagem de letras: 13
o	Contagem de dígitos: 4
o	Contagem de caracteres especiais: 1
o	URL encurtada: Não
o	URL anormal: Não
o	HTTPS: Não
o	IP na URL: Não
o	Indexação no Google: Sim
•	Resultado da Previsão:
o	CUIDADO! Link suspeito
Modelo Salvo
O modelo treinado foi salvo como um arquivo joblib chamado modelo_treinado_joblib.sav. Esse arquivo pode ser carregado em futuras implementações para realizar previsões em novos dados.
________________________________________
📂 Estrutura do Projeto
sherlock/  
│  
├── data/                # Dados brutos e processados  
├── notebooks/           # Notebooks de análise  
├── src/                 # Código-fonte  
├── README.md            # Documentação do projeto  
├── requirements.txt     # Lista de bibliotecas necessárias  
└── .gitignore           # Arquivos ignorados pelo Git  
________________________________________
🎓 Trabalho Acadêmico
Este trabalho foi desenvolvido como parte da disciplina Processamento de Linguagem Natural, ministrada pelo Professor Mateus Fuini, no curso Desenvolvimento de Software e Multiplataforma, da FATEC Itapira.
________________________________________

