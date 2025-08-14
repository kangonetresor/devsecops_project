# Étape 1 : Base image Azure Functions pour Python 4.x
FROM mcr.microsoft.com/azure-functions/python:4-python3.11

# Définir le dossier de travail dans le container
WORKDIR /home/site/wwwroot

# Copier le fichier requirements.txt pour installer les dépendances
COPY requirements.txt /requirements.txt

# Installer les dépendances Python
RUN pip install --no-cache-dir -r /requirements.txt

# Copier tout le code de la fonction dans le container
COPY . /home/site/wwwroot

# Azure Functions lance automatiquement le host à partir de cette image
