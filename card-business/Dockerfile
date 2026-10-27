# Utiliza a imagem oficial do Python 3.11 (versão slim, ideal para produção)
FROM python:3.11-slim

# Define o diretório de trabalho dentro do container
WORKDIR /app

# Copia primeiro apenas o arquivo de dependências
# Isso aproveita o cache do Docker se as dependências não mudarem
COPY requirements.txt .

# Instala as dependências do Flask listadas no seu requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copia o restante dos arquivos do seu projeto para o container
COPY . .

# Informa a porta que o container escuta
EXPOSE 8080

# Comando para rodar a aplicação Flask
CMD ["python", "app.py"]
