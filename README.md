Aqui está a versão do README com alguns emojis para deixar o texto mais visual e envolvente:

---

# Sherlock Phishing - Machine Learning 🕵️‍♂️💻

## Sobre o Projeto 🌐

O **Sherlock Phishing - Machine Learning** é uma solução desenvolvida para detectar links maliciosos (phishing) na web, utilizando técnicas de aprendizado de máquina 🤖. O projeto busca analisar e classificar URLs com base em características como comprimento, presença de caracteres especiais, uso de serviços de encurtamento de links e segurança do protocolo (HTTPS) 🔒, com o objetivo de identificar links suspeitos e proteger os usuários.

Utilizando um modelo treinado com dados de URLs reais, nosso sistema consegue identificar padrões comuns em ataques de phishing e alertar o usuário sobre links potencialmente perigosos ⚠️.

## Equipe 👩‍💻👨‍💻

Este projeto foi desenvolvido por:

- **Ester Carlos**
- **Gabriela Florencio**
- **Gustavo Ornaghi**
- **Mariana Cardoso**

## Objetivos 🎯

O projeto tem como principais objetivos:

- **Identificar URLs Suspeitas**: Utilizar técnicas de Machine Learning para classificar URLs como seguras ou suspeitas.
- **Educar sobre Phishing**: Ajudar os usuários a entender os riscos de links maliciosos e como se proteger 🛡️.
- **Implementar um Sistema Inteligente**: Criar uma solução autônoma que utilize modelos de aprendizado para analisar links e dar uma resposta em tempo real ⏱️.

## Como Funciona ⚙️

### Coleta e Extração de Características 🔍

A primeira etapa do processo é a coleta de URLs e a extração de diversas características, incluindo:

- Comprimento do URL 📏
- Contagem de caracteres alfanuméricos e especiais 🔤
- Uso de serviços de encurtamento de links ⬇️
- Presença de IP no link 🌐
- Utilização de HTTPS 🔐
- Verificação da URL no índice de busca do Google 🔍

Essas características são então utilizadas como input para o modelo de aprendizado de máquina.

### Treinamento do Modelo 🧠

Usando o conjunto de dados, um modelo de **Random Forest** é treinado para classificar links como "Confiáveis" ou "Suspeitos", com base nas características extraídas.

### Realização de Predições 🔮

Após o modelo ser treinado, ele pode ser usado para classificar URLs em tempo real. Quando o usuário insere um link, o sistema analisa as características e retorna se o link é seguro ou apresenta risco de phishing.

## Tecnologias Utilizadas 🛠️

- **Python**: Linguagem principal para desenvolvimento do projeto 🐍.
- **Scikit-learn**: Biblioteca para criação e treinamento do modelo de aprendizado de máquina 📚.
- **Pandas**: Para manipulação de dados 🗃️.
- **Numpy**: Para operações matemáticas ➗.
- **Joblib**: Para salvar e carregar o modelo treinado 💾.
- **BeautifulSoup & Requests**: Para scraping e verificação de links 🌐.

## Como Usar 🚀

### 1. Instalar as Dependências 📦

Para rodar o projeto, é necessário instalar as bibliotecas do Python listadas em `requirements.txt`. Utilize o seguinte comando para instalá-las:

```bash
pip install -r requirements.txt
```

### 2. Treinar o Modelo 🏋️‍♀️

Utilize o código abaixo para treinar o modelo de Machine Learning:

```python
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier

# Preparando os dados
X = dataset.drop(['URL', 'Label', 'class_url', '@', '?', '-', '=', '.', '#', '%', '+', '$', '!', '*', ',', '//'], axis=1)
y = dataset['class_url']

# Dividindo os dados em treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, shuffle=True, random_state=5)

# Treinando o modelo
classifier = RandomForestClassifier(n_estimators=200, max_features='sqrt')
classifier.fit(X_train, y_train)

# Avaliando o modelo
accuracy = classifier.score(X_test, y_test)
print(f"Acurácia: {accuracy}")
```

### 3. Salvar e Carregar o Modelo Treinado 💾

Após treinar o modelo, você pode salvá-lo para reutilização futura com o **Joblib**:

```python
import joblib

# Salvando o modelo treinado
joblib.dump(classifier, 'modelo_treinado_joblib.sav')

# Carregando o modelo
classifier = joblib.load('modelo_treinado_joblib.sav')
```

### 4. Realizando Previsões 🔮

Para realizar a predição de um novo link, use o seguinte código:

```python
url = "exemplo.com"

# Função para extrair as características do URL
def get_url(url):
    url_len = len(url)
    letters_count = letter_count(url)
    digits_count = digit_count(url)
    special_chars_count = sum_count_special_characters(url)
    shortened = Shortining_Service(url)
    abnormal = abnormal_url(url)
    secure_https = httpSecured(url)
    have_ip = having_ip_address(url)
    index_google = google_index(url)

    return {
        'url_len': url_len,
        'letters_count': letters_count,
        'digits_count': digits_count,
        'special_chars_count': special_chars_count,
        'shortened': shortened,
        'abnormal': abnormal,
        'secure_http': secure_https,
        'have_ip': have_ip,
        'GoogleIndex' : index_google
    }

# Função de previsão
def model_predict(url):
    numerical_values = get_url(url)
    prediction = classifier.predict([list(numerical_values.values())])
    if prediction == 0:
        print("CUIDADO! Link suspeito ⚠️")
    else:
        print("Link Confiável ✅")

model_predict(url)
```

## Resultados 📊

Com o modelo treinado, conseguimos uma **acurácia de 79%** na classificação de URLs, o que demonstra um bom desempenho na detecção de phishing:

```
Acurácia: 0.7903704377901156
```

## Conclusão 🎉

O **Sherlock Phishing - Machine Learning** oferece uma ferramenta eficaz para a detecção de links de phishing, utilizando aprendizado de máquina para analisar URLs e alertar os usuários sobre possíveis riscos 🔐. A aplicação de técnicas de **Processamento de Linguagem Natural** e aprendizado de máquina tem se mostrado promissora na luta contra ataques cibernéticos 🛡️.

---

### Trabalho acadêmico para a matéria **Processamento de Linguagem Natural**, ministrada pelo professor **Mateus Fuini**, curso **Desenvolvimento de Software e Multiplataforma**, **FATEC Itapira** 🎓.

--
