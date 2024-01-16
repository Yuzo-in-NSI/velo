# Sujet de Bac Terminale NSI Exercice 2 
# 1) a)
flotte[26] renvoie {'type' : 'classique', 'etat' : 1, 'station' : 'Coliseum'}
# 1) b)
flotte[80]['etat'] renvoie la valeur 0.
# 1) c)
flotte[99]['etat'] renverra une erreur car la clé 99 n'existe pas.


# 4
def station(coord):
  d = {}
  for num,info in flotte.items() :
    nom_station = info['station']
    distance_station = distance(stations[nom_station],coord)
    if info['etat'] == 1 and distance_station < 800:
      if nom_station not in d :
        d[nom_station] = [distance_station, [num]]
      else :
        d[nom_station][1].append(num)
  return d




