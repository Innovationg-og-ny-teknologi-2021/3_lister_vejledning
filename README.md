# 3_lister_vejledning

## Slutresultat
https://user-images.githubusercontent.com/48329669/128570069-64627288-c9fa-4313-aa17-d727d279563e.mp4

## Introduktion
I dag skal vi arbejde med lister. Lister er især gode til at præsentere jeres data på screens.
F.eks. den mest brugte liste er FlatList, som er en liste der kan scrolles op og ned i.
Det den type liste som bl.a. bruges i Facebook, Instagram, Twitter og mange andre apps når
i sidder og doom-scroller til undervisningen.

Start med at læse dokumentationen på de relevante komponenter, som i skal bruge i dag.
I finder dem i bunden af denne guide. 

## App.js
<<<<<<< HEAD
1. Opret et nyt expo projekt med `` npx create-expo-app <projektNavn>`` i din mappe med opgaver
=======

## components
1. Opret en ny mappe kaldt ``components `` som skal indeholde 3 filer kaldt ArrayListComponent.js, FetchListComponent.js og FlatListComponent.js.
2. I hver af filerne bruges skabelonen fra skabelon 1 og 2
   1. Husk også at KomponentNavn skal være ens med filnavnet
   2. Husk at importere React
   3. Husk at importere Text og hvad i skal bruge fra react-native


## App.js
<<<<<<< HEAD
1. Opret først et View som wrapper applikation i return
2. Tilføj i View'ets attributter en styling med container `` style={styles.container} ``
3. Opret et nyt stylesheet, se skabelon 2, og eventuelt ændre baggrundsfarven
4. Importér nu de tre nyoprettet komponenter med hver deres komponentnavn som fx ``<ArrayListComponent/>``
5. Nu burde du have 3 tekster fra hver af de nyoprettede komponenter
=======
1. Opret et nyt stylesheet, se skabelon 2, og eventuelt ændre baggrundsfarven
2. importér nu de tre nyoprettet komponenter med hver deres komponentnavn som fx ``<ArrayListComponent/>``
3. Nu burde du have 3 tekster fra hver af de nyoprettede komponenter


### Hint:
``` 
export default function App() {
  return (
      <View style={styles.container}>
        <StatusBar style="auto" />
        // TODO: Tilføj komponenter her
      </View>
  );
}
```


**OBS**! - Ved standard expo opstilling vil der være `` alignItems: 'center'`` & `` justifyContent 'center'`` i jeres stylesheet container. Disse attributter kan drille jeres lister (især på Android). Prøv at udkommentere dem hvis ikke i kan se jeres 3 tekster fra jeres komponenter.  

## const.js
1. Opret en såkaldt const.js i mappens rod, som skal bruges til indeholde alt vores "hardcoded data", som i dette tilfælde kommer til at være vores lande, biler og vores fetch url
2. Opret nu hhv en const for CARS, COUNTRIES og GET_USERS_URL med dataen nede fra skabelon 3. Husk for at vi kan "bruge" vores data, så skal const'en blive eksporteret. Så hvis der skulle eksporteres en liste af OL-lege skal man skrive ``export const OL_LEGE = ['volleyball','basketball','spydkast']  ``
3. For at teste dine lister og url kan du eventuel console.log() dem i App.js, for at se om const'ene kan kaldes på ( husk at importere const og funktionerne i toppen af App.js)

### skabelon 3

``` 
["Audi","BMW","Tesla","Alfa oreo","Ford","Kia","Rover", "Saab", "Seat", "Skoda", "Smart", "SsangYong", "Subaru", "Suzuki"]

["Denmark","England","Spanien","Italien"];

'https://randomuser.me/api?results=';

```

## ArrayListComponent.js
1. I return funktionen opret et `<View> </View>` som wrapper og derved fungerer som "parent" til komponenterne herunder. For der kan kun være en "parent " i return funktionen
2. Tilføj nu en styling til ``View`` elementet ligesom fra App.js, men her vil vi gerne have der bliver tilføjet ``alignItems: 'center', justifyContent: 'center'`` i containeren
3. Style nu ligeledes det nuværende `<Tekst> </Text>` element så det ligner en overskrift ( se evt referencer om styling)
4. Opret under Tekst elementet et `<ScrollView></ScrollView>` element ( læs mere på https://reactnative.dev/docs/scrollview )
5. Definer i ScrollViewet at den maks må mere 80 i højden med `` style={{height:80}}``
6. Tilføj nu følgende kodestykke: <img width="560" alt="Screenshot 2021-08-07 at 07 26 49" src="https://user-images.githubusercontent.com/48329669/133664027-a97b9de6-1e44-401d-8fc0-400c515cf4cc.png">
   1. Det vi gør her er at loope igennem vores lande med en map funktion, som looper igennem arrays. Heri laver vi en funktion som først har værdien og dernæst index nummeret. Der bruger vi key'en til at definere pladsen på elementet og country til udprint af vores værdi
7. Tjek nu om der er en række lande udprintet på din telefon

## FlatListComponent.js 
1. I return funktionen oprettes et `<View> </View>` som wrapper der fungerer som "parent" til komponenterne herunder. For der kan kun være en "parent" i return funktionen
2. Tilføj nu en styling til ``View`` elementet ligesom fra App.js, men her vil vi gerne have der bliver tilføjet alignItems: 'center', justifyContent: 'center' i containeren
3. Style nu ligeledes det nuværende `<Text> </Text>` element så det ligner en overskrift ( se evt referencer om styling)
4. Tilføj nu en `<FlatList />` med attributterne style, data, renderItem og keyExtractor.
   1. I style skal der være et objekt med height:80
   2. I data, skal vi have vores CARS fra const.js
   3. I renderItem skal vi have en funktion med props for Item som returnere en CarItem med attributterne item, som modtager et item argument ( se hint 4)
<<<<<<< HEAD
   4. Skriv følgende i `keyExtractoren={item => item}`
### Hint
```
return(
        <View style={styles.container}>
            {/* Title med styling*/ }
            <Text style={{ fontSize: 20, textAlign:'center',paddingTop:40 }}>
                1 Mine biler - Flatlist
            </Text>
            {/* FlatList komponent med title propertien og en værdi*/ }
            <FlatList
                style={{height:--}}
                data={"Jeres data"}
                renderItem={({item})=>{
                    {/*Render CarItem, her er det vigtigt at kalde et subkomponent*/}
                    return(
                        <CarItem
                            item={item}
                            msg={"Oh boy i love"}
                        />
                    )
                }}
                keyExtractor={item => item}
            />

        </View>
    )

```
=======
   4. Skriv følgende i `keyExtractor={item => item}`
>>>>>>> 2a51138660e67129ad8749893a5b10cbbd1ef63a
5. Opret nu en funktion kaldt CarItem som har i parametrene () ``{item,msg}``
   1. I funktionen laves en et return, som returnere et ``<Text> </Text>`` som har {item} `` i sig

### Hint
```
    const CarItem = ({item,msg}) => {
        return(
            <Text>
                {msg} "{item}"
            </Text>
        )
    }
```

6. Se nu i App.js om du har en liste af biler 
   1. Hvis du oplever problemer så husk at bruge console.log()

## FetchListComponent.js - useState og useEffect
1. opret nu 3 states, der kaldes; users, msg og amount. Disse states skal håndtere de data vi henter fra vores endpoint i vores const.js
   1. Tip: ``const [users,setUsers] = useState({});``
   2. Husk at sætte en initial state på hver af state-variablerne
2. Opret nu en useEffect, som kalder en funktion ved navn loadUsers(), og lav en dependency af amount
   1. Hint 5
3. Lav en async funktion kaldt loadUsers 
   1. `` const loadUsers = async () => {}``
   2. Deri laves en `try{} catch(error){}`hvor du først laver en fetch med GET_USERS_URL fra const.js. Dette fetch sættes ligmed en const response. 
   3. Derunder laves en const json = await response.json();
   4. Til sidst setUsers(json.result)
   5. Derefter laves en setMsg med error i catch'en

### Hint
```
    const loadUsers = async () => {
        try {
            const response = await fetch(***);
            const json = await response.json();
            setUsers(***);
        } catch (error) {
            setMsg(***)
        }
    }
```

4. Gå nu ned i return funktionen og "wrap" tekst elementet med en if else shorthand, hvor i if'et skal der stå users.length > 0
   1. Se evt hint 7
5. I if statementet laves samme struktur med View og overskrift-tekst som de andre komponenter
   1. Under `<Text> </Text>` elementet oprettes et `<TextInput/>` element som har tilhørende attributter: style, onChangeText, value, placeholder og keyboardType
   2. Stylen på feltet kan være `` {borderWidth:1,borderColor:"black",width:"70%",padding:4} ``
   3. onChangeText skal sættes med setAmount
   4. value skal være amount.toString()
   5. placeholder kan du selv bestemme, men det skal være en string
   6. keyboardType skal være numeric
   7. Se eventuelt textinput i referencer
6. Opret under TextInputtet et `<ScrollView> </ScrollView>` med følgende attributter: ` bounces={true} style={{height:350,width:"60%"}} `
   1. Herunder laves en map-funktion som looper igennem users. se Screenshot
   2. ![image](Screenshot 2021-08-07 at 09.19.03.png)<img width="755" alt="Screenshot 2021-08-07 at 09 19 03" src="https://user-images.githubusercontent.com/48329669/133664100-78192a09-ef65-469d-80d7-b1e528eed57b.png">
7. Under ScrollViewet tilføj følgende: `<Text> {msg ? msg :""} </Text>`
8. Tjek nu på din telefon om du kan skrive et antal og at viste brugere vil skifte
   1. Hvis du oplever problemer så HUSK console.log igennem dine objekter eller states + læs hvad react native brokker sig over.



## Hints

### skabelon 1
``` 
const KomponentNavn = (props) => { 
    return (
        <Text>Det er mit KomponentNavn</Text>
    )
}

export default KomponentNavn; 
```

### skabelon 2

```
const styles = StyleSheet.create({
  container: {
    backgroundColor: '#fff',
    flex:1
  }
});
```

### skabelon 3

``` 
["Audi","BMW","Tesla","Alfa oreo","Ford","Kia","Rover", "Saab", "Seat", "Skoda", "Smart", "SsangYong", "Subaru", "Suzuki"]

["Denmark","England","Spanien","Italien"];

'https://randomuser.me/api?results=';

```



### hint 4
```
renderItem={({item})=>{
  return(
      <CarItem
          item={item}
          msg={"Oh boy i love"}
      />
  )
}}

```

### Hint 5
```
useEffect( () => {
  loadUsers();
},[amount])
```

### Hint 6
```
const response = await fetch(GET_USERS_URL+amount);
const json = await response.json();
setUsers(json.results);

```

### Hint 7
```
return(
        users.length > 0 ? (
            <Text> så er der brugere </Text>
         ): (
            <Text> Loading... </Text>
         )        
)

```

## Referencer
https://reactnative.dev/docs/textinput <br>
https://reactnative.dev/docs/flatlist <br>
https://reactnative.dev/docs/style <br>
https://reactnative.dev/docs/statusbar <br>
https://reactnative.dev/docs/flatlist <br>
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map 
