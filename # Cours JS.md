# Cours JS


## Corrections exercices Tableau

### exercice 1,2,3 :

```javascript
const monTab =[1,2,3,4,5]

monTab.forEach((numero,index)=>{
    console.log(numero)
    console.log(index)
})

```

### suite :

```javascript
const birds = ["pigeon","messange","colombe","corbeau"]
for (let i = 0; i<birds.length;i++){
    if (tab[i] === "corbeau"){
        console.log("trouve")
    }
}
```

## Correction exercices fonction :

### exercice 1 :

```javascript
function sum (nombre1,nombre2){
    return nombre1 + nombre2;
}

//appel de fonction 
const result = sum (4,5);

console.log(result)
```

### exercice 9 :

```javascript
const randomNumber = [3254,89657,82233335,461222,78,9156]
const getRandInt =(num)=> {
    return math.floor(math.random()*num);
}
const tabNine =[]

for (let index = 0; index < 7; index++){
    tabNine.push(getRandInt(index * 10))
}

console.log(tabNine)

```
### exercice () :

```javascript

function Nombre (num){
    const ones = [' ', 'one' ,'two','tree','four','five','six','seven','eight','nine','ten']
    const tens = [' ',' ','twenty','thirty','fourty','fifty','sixty','seventy','eighty','ninety']
    const teens =  ['ten','eleven', 'twelve', 'thirteen', 'fourteen', 'fifteen', 'sixteen', 'sevnteen', 'eighteen', 'nineteen']
    if (num<10){
      return ones[num];
    }
      else if (num <20){
        return teens [num-10];
      }
      else {
        return tens[Math.floor(num/10)] + '-' + ones[num%10];
      }
    }
   console.log(Nombre(42))
```

### exercice :

```javascript
const someObject = {
    firstname: "erwan",
    lastname: "Le Gal",
    age: 23,
    hasdriverlicence: true,
    placeOfbirth: "L'isle-Adam"
}
const tabKey = [
    {firstname : "erwan"}
       {firstname : "erwan"}
          {firstname : "erwan"}
             {firstname : "erwan"}
                {firstname : "erwan"}
]
const getPropertyValues = (arr,str) =>
{
    return objectArray.map((obj) => obj[str])
}

const testArray = [1,2,3,4568,9887]

testarray.map((element) =>{
    console;log(element)
})
```
## spread operator :

- En JavaScript, le spread operator  est utilisé pour décomposer un objet itérable (par exemple un tableau ou un objet) en ses éléments individuels. Le spread operator est représenté par trois points "..." et peut être utilisé dans les contextes suivants:

1. Pour étendre les éléments d'un tableau ou d'un objet:

Par exemple, si vous avez deux tableaux et que vous souhaitez les fusionner en un seul, vous pouvez utiliser le spread operator pour étendre les éléments de chaque tableau et les combiner en un seul tableau:

```javascript
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const combinedArray = [...array1, ...array2];
console.log(combinedArray); // Output: [1, 2, 3, 4, 5, 6]
```



De même, vous pouvez également utiliser le spread operator pour étendre les propriétés d'un objet et les combiner avec d'autres objets:

```javascript
const object1 = { x: 1, y: 2 };
const object2 = { z: 3 };
const combinedObject = { ...object1, ...object2 };
console.log(combinedObject); // Output: { x: 1, y: 2, z: 3 }
``` 
2. Pour passer des arguments à une fonction:

Le spread operator peut également être utilisé pour passer des arguments à une fonction de manière dynamique. Par exemple, si vous avez une fonction qui prend plusieurs arguments, vous pouvez utiliser le spread operator pour passer un tableau d'arguments à la fonction:

```javascript
function sum(a, b, c) {
  return a + b + c;
}
const numbers = [1, 2, 3];
console.log(sum(...numbers)); // Output: 6
```



Dans cet exemple, le spread operator décompose les éléments du tableau "numbers" et les passe à la fonction "sum" comme des arguments individuels.

Le spread operator est donc utile pour décomposer des tableaux, des objets et d'autres structures de données en éléments individuels et pour passer des arguments à des fonctions de manière dynamique.


## regexp

```javascript
const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

// Test si un email est valide
const isValidEmail = emailPattern.test("monemail@example.com"); //true
```



Dans cet exemple, nous avons défini une expression régulière appelée `emailPattern` qui valide un format d'adresse e-mail. Cette expression régulière est composée de trois parties: 
- `^[^\s@]+`: Le début de la chaîne de caractères doit contenir un ou plusieurs caractères qui ne sont ni des espaces ni des symboles @. 
- `@[^\s@]+\.`: La chaîne de caractères doit contenir un symbole @, suivi d'un ou plusieurs caractères qui ne sont ni des espaces ni des symboles @, suivi d'un point. 
- `[^\s@]+$`: La fin de la chaîne de caractères doit contenir un ou plusieurs caractères qui ne sont ni des espaces ni des symboles @.

Nous avons ensuite utilisé la méthode `test()` de l'objet RegExp pour vérifier si une adresse e-mail est valide en utilisant cette expression régulière. La méthode `test()` renvoie `true` si l'adresse e-mail est valide et `false` sinon.

##  Button / Function avec DOM :

```javascript
<script>
    alert('hello');
    const myElement = document.getElementById('toto')
    console.log("myElement content :",myElement)
    const myButton = document.getElementById('click')
    const myParagraphe = document.getElementById('paragraphe')
    myButton.addEventListener('click',function(){
      myParagraphe.innerHTML ="Bonjour les B1";
    })
   
  </script>
```
##   promise / fetch :

```javascript
const promise = new Promise((resolve, reject) =>{
    setTimeout(() => {
        const randomNumber = Math.floor(Math.random() * 10)
        if (randomNumber % 2 === 0) {
            resolve(randomNumber)
           
        } else {
            reject(new Error('Le nombre est impair.'))
        }
        
    
    }, 1000)
    
})
promise 
    .then(result => console.log(result))
    .catch(error => console.error(error.message))

```

2. Un deuxieme exemple  :

```Javascript
<script>
    function fetchSomePokemons(){
      return fetch('https://pokeapi.co/api/v2/pokemon?limit=150');
    }
    const pokemons = fetchSomePokemons()
                .then((httpResponse) =>{
                    console.log('httpResponse: ', httpResponse)
                    return httpResponse.json()
            })
            .then((pokemonList) => {
                console.log(pokemonList)
            })

  </script>
```

## Commandes utiles :

1. Déclarer une variable :

```javascript
let variableName = value;
``` 
2. Afficher un message dans la console :

```javascript
console.log('Hello World!');
``` 
3. Afficher une boîte de dialogue modale :

```javascript
alert('Hello World!');
``` 
4. Demander une saisie à l'utilisateur :

```javascript
let input = prompt('Entrez votre nom :');
``` 
5. Manipuler des éléments HTML :

```javascript
let element = document.querySelector('selector');
element.style.color = 'red';
element.innerHTML = 'Nouveau contenu';
``` 
6. Écouter un événement :

```javascript
element.addEventListener('click', function() {
  // Fonction à exécuter lors du clic sur l'élément
});
``` 
7. Conditionner l'exécution d'un bloc de code :

```javascript
if (condition) {
  // Code à exécuter si la condition est vraie
} else {
  // Code à exécuter si la condition est fausse
}
``` 
8. Boucler sur une liste d'éléments :

```javascript
let elements = document.querySelectorAll('selector');
for (let i = 0; i < elements.length; i++) {
  // Code à exécuter pour chaque élément de la liste
}
``` 
9. Définir une fonction :

```javascript
function functionName(parameter1, parameter2) {
  // Code à exécuter dans la fonction
}
``` 
10. Appeler une fonction :

```javascript
functionName(argument1, argument2);
```

## tableau de commandes utiles :

|commande|utilité |
|--------|--------|
|console.log|affiche le résulat du programme |
|