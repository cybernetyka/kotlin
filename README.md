# kotlin
modele cybernetyczne napisane w kotlin skrypty z przykladami, kotlin, groovy



## CoBIT


### Podstawowe:

  + organizm
  + waga podziału - pochodna energii i czasu, skutek
  + energia
  + datownik
  

## Cecha, własciwość
  + typ
  + relacja
  + proporcja


### zdarzenie 

  + Datownik
  + Akcja
  + Wiązanie

  
### Akcja

  //+ waga => Intencja = informacja wyjściowa - jaki chcielibyśmy widzieć układ, jaką zmianę chcielibyśmy zainicjować   
  //+ Waga - sposób podziału energii pomiędzy 1 i 2 np. 1/2 2/3 3/4 dotyczy pierwszego elementu  
  //+ Informacja/intencja: 
  //+ Energia = energia wyjściowa, siła intencji
  //+ Czas trwania
  Biton
  Waga(3/4)


### InterAkcja, Transakcja, Wiązanie
  
    aplikacja( Akcja( Biton, Waga(3/4) ) ){
      
      Biton1->setWaga(3/4)
      Biton1->setInfo(Biton)
      
      Biton1->setWaga(1/4)
      Biton1->setInfo(Biton)
    }
    
  + Akcja - otrzymana energia i informacja dla każdego elementu  
  + Biton 1, waga 2/3
  + Biton 2, waga 1/3
  
  

### Biton - Materia (proporcje informacji i energii)
  
  cechy[]
    
    typ:  wygląd
    relacja: czarny/biały
    proporcja: 1/2
    
    typ: energia:
    relacja: akumulacja/konsumpcja
    proporcja: 1/2
  
  


### CoBIT - świadomy organizm, składa się z materii z Bitonów
  
  //getWaga()
  //getAkumulacja()
  //getKonsumpcja()
  
  + transakcje, zdarzenia wiązań: 
    InterAkcja(Akcja, Waga, Biter1, Biter2)
  
  
  
  
  
CoBIT

  Wartości pobranej energii i zdobytej informacji
  
  getCecha()->filtrowanie(energia)
  sprawdzanie proporcji dla już sitniejących
  jesli nie istnieje, to przyjmuje się 1 o ile nie zadecyduje waga
  

  Interakcja

    aplikacjaEnergii(
      Biton, // Akcja(czarny, 10J, 10s)
      Waga(3/4), - intencja podziału energii
      Biton1
      Biton2
    )
    
    
```python


class Property:

    //typ:  wygląd
    //relacja: czarny/biały
    //proporcja: 1/2
    
    def __init__(self, type, relation, proportion):
        self.type = type        
        self.relation = relation
        self.proportion = proportion



class Biton:

    def __init__(self, Property):        
        self.property = [ Property ]

    def addProperty(self, Property):
        self.property.append(Property)
        
    
    def listProperty(self):
        return self.property
        
    def filter(self, key)
      //properties()->filtrowanie(energia)


class Cobit:    

    def __init__(self, Biton):
        self.Biton = Biton
        self.transaction = []

    def addBiton(self, Biton):
        self.transaction.append(Biton)
        // sprawdz czy zawiera typ, sumowanie proporcji i relacji
        // przy powolywaniu instancji Biton jest wymagany
    
    def listBiton(self):
        return self.transaction
        
    def values(self, key)
      //getCecha()->filtrowanie(energia)
        
```        
  
