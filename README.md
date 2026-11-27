Capsules sur les trajets de marches et de course
  
  Le fichiers csv "Minutes_historiques.csv" contient les informations nécessaires pour produire le code HTML des capsules pour chaque trajet :
    Url de la page du trajet
    Préfixe du lieu (numéro d'étape)
    Nom du lieu
    Lien hyertexte vers la MH (URL)
    Précision (texte entre parenthèse)
    URL vers le fichier MP3 hébergés sur Github

  Le programme python "Générer_parcours.py" utilise le fichiers "Minutes_historiques.csv" pour créer les fichier JSON de chaque trajet.
  Le programme utilise aussi le fichier "Style.json" qui permet de définir le style qui sera appliqué pour produire le code html des étapes du trajet :
    Style pour le Préfixe
    Style pour le nom de lieu
    Style pour la précision qui est entre parenthèse
    Style pour le texte de la durée audio.
  Les fichiers JSON des trajets qui sont produit intègrent ces styles ainsi que le détail de chaque étape du trajet. Donc pour changer le style pour tous les trajets, il suffit de modifier ce fichier.
  Le programme produit aussi le fichier "url_parcours.csv" qui liste les différents lien à intégrer dans chaque page de trajet.

  Le fichier Parcours.html est utilisé pour produire le code HTML à intégrer au site, en lui passant en paramètre le nom du fichier JSON du trajet en question.
  Par exemple, dans Google Site, en utilisant Insérer → Intégrer → Par URL, on peux passer l'URL suivante:
    https://dubluc.github.io/MinutesHistoriques/parcours.html?trajet=3k-a-la-marche-vieux-quebec
  Et le résultat fourni le bloc HTML des différentes étapes du parcours avec les lien vers les page de MH ainsi que les contrôles audio pour faire jouer l'audio directement dans la page.
    
Enfin, le fichier "../Parcours/url_parcours.csv" fourni le lien URL de chaque page à intégrer au site, exemple:
  https://dubluc.github.io/MinutesHistoriques/parcours.html?trajet=95-km-parc-lineaire-st-charles
  https://dubluc.github.io/MinutesHistoriques/parcours.html?trajet=105k-a-la-course-montcalm-vieux-quebec-place-royale-sillery
