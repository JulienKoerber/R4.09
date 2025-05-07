FROM python:3.11-slim

RUN apt-get update && apt-get install -y unzip && apt-get clean

# Étape 3 : Créer et définir le répertoire de travail
WORKDIR /app

# Étape 4 : Copier l’archive Django et le fichier des dépendances
COPY django-model-master.zip .
COPY requirements.txt .

# Étape 5 : Extraire l’archive et supprimer le zip
RUN unzip django-model-master.zip && rm django-model-master.zip

# Étape 6 : Installer les dépendances Python (comme Django)
RUN pip install --no-cache-dir -r requirements.txt

# Étape 7 : Définir le répertoire contenant manage.py (adapter si nécessaire)
WORKDIR /app/django-model-master/modele

# Étape 8 : Exposer le port 8000 utilisé par le serveur Django
EXPOSE 8000

# Étape 9 : Démarrer le serveur Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
