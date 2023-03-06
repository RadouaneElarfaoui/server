import requests
import datetime

access_token = 'EAAFXA8ohwZA4BAH2kPx2vn0uh0KeZBiAWmZBuAj9Cmvgp7NwdViklZBwnN5ZBqDfE9VBEOERcbEZBls5ios639NjcyJZC8dXJP63i0IJhdnJUoLwsQWvpZADpaTiNRLDy5qE0BWu84RP4QKRWf17J2TC8XNOfzYfPkGqUVHUjO0JWtUApeDufo8O'

post_id = '109885885096358_179530931489956'

# Envoyer une requête GET à l'API Graph pour accéder au post
response = requests.get('https://graph.facebook.com/v16.0/' + post_id, params={'access_token': access_token})

# Extraire les données JSON de la réponse
data = response.json()

# Obtenir l'heure actuelle
current_time = datetime.datetime.now().strftime('%Y-%m-%d %H:%M:%S')

# Modifier le message du post en ajoutant l'heure actuelle
data['message'] = f"The current time is : ({current_time})\nby a.r.f"

# Envoyer une requête POST pour éditer le post
response = requests.post('https://graph.facebook.com/v16.0/' + post_id, params={'access_token': access_token}, data=data)

# Vérifier le statut de la réponse
if response.status_code == 200:
    print('Le post a été modifié avec succès.')
else:
    print('Une erreur est survenue lors de la modification du post.')
