\# Détection et lecture de plaques d'immatriculation



Pipeline de détection et lecture automatique de plaques d'immatriculation :

\- \*\*Détection\*\* : YOLOv8 (entraîné sur 433 images annotées, dataset Kaggle "Car License Plate Detection")

\- \*\*Prétraitement\*\* : découpe, super-résolution (Lanczos), débruitage, netteté, seuillage adaptatif

\- \*\*Lecture (OCR)\*\* : EasyOCR



\## Dataset

\[Car License Plate Detection (Kaggle)](https://www.kaggle.com/datasets/andrewmvd/car-plate-detection)



\## Pipeline

1\. Conversion des annotations XML (Pascal VOC) vers le format YOLO

2\. Entraînement YOLOv8 (50 époques, GPU)

3\. Détection de la plaque sur une nouvelle image

4\. Nettoyage de l'image de la plaque (débruitage, netteté, seuillage)

5\. Lecture du texte avec EasyOCR



\## À propos du modèle

Le fichier best.pt include dans ce dépôt est mon modèle personalisé entraîné pour la déection de plaques d'immatriculation.

