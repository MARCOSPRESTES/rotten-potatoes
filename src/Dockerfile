
### Imagem base utilizada.
FROM python:3.8-slim-buster

### Diretório padrão de trabalho dentro do container.
WORKDIR /app

### Copiando arquivos para serem instalados.
COPY /requirements.txt .

### Instalando pacotes e dependências.
RUN pip install -r requirements.txt

### Copiando projeto.
COPY . /app

### Expondo porta 5000.
EXPOSE 5000

### Principal processo de execução do container.
CMD ["gunicorn", "--workers=3", "--bind", "0.0.0.0:5000", "-c", "config.py", "app:app"]