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
    
    

Intencja -  to możliwość poukładania w odpowiednim porzadku nadchodzacych Bitonów do Cobitu, zmieniając jego wrażliwosć na kolejne wiadomosci (Bitony)
Jako pętla spreparowanych Bitonów dla Cobitu

### EXAMPLE

```python

ListBiton = [Biton1([Property1, Property2]), Biton2[Property3], Biton3[Property4]]

myCobit = new CoBit()
myCobit.addBiton(Biton1)
print( CoBit.values() )

for Biton as ListBiton:
  CoBit.addBiton(Biton)

print( CoBit.listProperty() )

```


### CORE

```python


# Materia (proporcje relacji cech)
class Property:

    # typ:  wygląd
    # relacja: czarny/biały
    # proporcja: 2/3 dotyczy pierwszego elementu relacji, drugi ma 1/3
    
    def __init__(self, type, relation, proportion):
        self.type = type        
        self.relation = relation
        self.proportion = proportion

    # sprawdz czy zawiera typ, sumowanie proporcji i relacji
    # dodaj jesli nie ma typu i relacji
    # jesli istnieje to zmien wagi proporcji
    def add(self, Property):
        if(Property.relation != self.relation) {
          self.type = Property.type
          self.relation = Property.relation
          self.proportion = Property.proportion
        } else {
          self.type = Property.type
          self.relation = Property.relation
          self.proportion = Property.proportion
        }


# Biton - Zbiór relacji
class Biton:

    def __init__(self):        
        self.property = []        

    def addProperty(self, Property):
        self.property.append(Property)

    # sprawdz czy zawiera typ, sumowanie proporcji i relacji
    # dodaj jesli nie ma typu i relacji
    # jesli istnieje to zmien wagi proporcji
    
    ## Jeśli znajdzie już istniejące, to nie zastępuje, tylko dopisuje i potem liczy wagę dynamicznie
    
    def sum(self, Property):
      list_similiar_types = self.property.find(Property.type)
   
      for Property2 as list_similiar_types:
        if(Property2.relation === self.property.find(Property.relation).relation){ // if TYPE && RELATION
           self.property.find(Property.type).sum(Property)        
        else {
          self.property.find(Property.type).
        }
        
        
    def listProperty(self):
        ## calculate the proportions dynamic        
        return self.property
        
    def calcProperty(self):
        ## calculate the proportions dynamic,
        # za każdym razem, gdy już istnieje porperty z tym samym typem i relacją, zmieniaj proporcje biorąc pod uwagę ilośc prób, porporcja = nowa proporcja  = jeśli proporcja mniejsza to odejmij, jeśli większa to zwiększ, ale wczesniej podziel przez ilość prób 
        return self.property
        
    def filter(self, key)
      #properties()->filtrowanie(energia)
      

    # find array of Objects another object with param 
    def filter(self, key)
      #properties()->filtrowanie(energia)      



# CoBit - świadomy organizm, składa się z materii z Bitonów
class Cobit:    

    def __init__(self):        
        self.biton = []        

    def addBiton(self, Biton):
        self.biton.append(Biton)
        # sprawdz czy zawiera typ, sumowanie proporcji i relacji
        # dodaj jesli nie ma typu i relacji
        # jesli istnieje to zmien wagi proporcji
        
    
    def listBiton(self):
        return self.biton
    
    
    def listType(self):
        return self.biton.filter() // get all types of biton
        
    def listProperty(self, key)
      return self.biton.filter()->filtrowanie(energia) // return grupuj po typach, zmien proporcje, jesli typy i relacje są te same
        
```        
  

