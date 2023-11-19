# Notes-de-cours-algo
Simples notes perso de cours d'algo, ne regardez pas les fautes d'orthographes lol.


# Linear Search List :
    Objectif : faire une recherche linéaire simple
    O(n)

# Binary Search Algorithm
    Il est toujours important de se demander si les informations sont ordonnées ou non
    [####################################]
     o                                  N
     |                 |                  
     -------------------
        ici on vérifie si
        N est présent
        si oui, on supprime 
        le reste. sinon on prends le reste
    
    le but est de toujours supprimer la moitié tant que la valeur n'est pas trouvée jusqu'à trouver la valeur demandée.
    La position est donc log(N)
    Si on scanne en même temps, la position est alors N log(N)

## En pseudo code, cela donne ça :
    Search(array, low, High, needle) {
        // ici le but est trouver le milieu
        millieu = low + (high - low) /2
        value = array[millieu]

        // il faut maintenant trois conditions : 
        // 1- on cherche la valeur
        // 2- si la valeur est plus grande
        // 3- si la valeur est moins grande
        do {
            if (value == needle) {
                return true
            } else if(valeur > millieu){
                low = millieu + 1
            } else {
                high = millieu 
            }
        } while (low < high){
            return false;
        } // ici on dit que tant que low n'est pas égal a while, on continue la boucle. si on arrive à ce point, c'est qu'on a pas trouvé la valeur
        
    }

# Bubble sort
L'idée : On prends un tableau, on prends une valeur [i], si cette valeur est plus grande que la suivante, on l'échange de place avec celle-ci.

    Ce que ça produit, c'est que lors de la première itération, la dernière valeur qui est passée est forcément la plus grande. Donc pas besoin de réitérer cette valeur ensuite.

    Cette algo est noté : o(N²)
    
