# 3_lister_vejledning

## Slutresultat
https://user-images.githubusercontent.com/48329669/128570069-64627288-c9fa-4313-aa17-d727d279563e.mp4

## App.js
1. Opret et nyt expo projekt med `` expo init <projektNavn>`` i din mappe med opgaver

## components
1. Opret en ny mappe kaldt ``components `` som skal indeholde 3 filer kaldt ArrayListComponent.js, FetchListComponent.js og FlatListComponent.js.
2. I hver af filerne brug skabelonen fra hints
   1. Husk også at KomponentNavn skal være ens med filnavnet
   2. Husk at importere React
   3. Husk at importere Text fra react-native

## App.js
1. Opret først et View som wrapper applikationen i return
2. Tilføj i View'ets attributter en styling med container `` style={styles.container} ``
3. Opret et nyt stylesheet kaldt med skabelon 2, og eventuelt ændre baggrundsfarven
4. import nu de tre nyoprettet komponenter med hver deres komponentnavn som fx ``<ArrayListComponent/>``
5. Nu burde du have 3 tekster fra hver af de nyoprettet komponenter

## const.js
1. opret en såkaldt const.js i mappens rod, som skal bruges til indeholde alt vores "hardcoded data", som i dette tilfælde kommer til at være vores lande, biler og vores fetch url
2. opret nu hhv en const for CARS, COUNTRIES og GET_USERS_URL med dataen nede fra skabelon 3. Husk for at vi kan "bruge" vores data, så skal const'en blive eksporteret. Så hvis der skulle eksporteres en liste af OL-lege skal man skrive ``export const OL_LEGE = ['volleyball','basketball','spydkast']  ``
3. For at teste dine lister og url kan du eventuel console.log() dem i App.js, for at se om const'ene kan kaldes på ( husk at importere const'ene i toppen af App.js)

## ArrayListComponent.js
1. I return funktionen opret et `<View> </View>` som wrapper så der agerer som "forældren" til komponenterne herunder. For der kan kun være en "forældre" i return funktionen
2. Tilføj nu en styling til ``View`` elementet ligesom fra App.js, men her vil vi gerne have der bliver tilføjet alignItems: 'center', justifyContent: 'center' i containeren
3. Style nu ligeledes det nuværende `<Tekst> </Text>` element så det ligner en overskrift ( se evt referencer om styling)
4. Opret under Tekst elementet et `<ScrollView></ScrollView>` element ( læs mere på https://reactnative.dev/docs/scrollview )
5. Definer i ScrollViewet at den maks må mere 80 i højden med `` style={{height:80}}``
6. Tilføj nu følgende kodestykke: ![](Screenshot 2021-08-07 at 07.26.49.png)
   1. Det vi gør her er at loope igennem vores lande med en map funktion, som looper igennem arrays. Heri laver vi en funktion som først har værdien og dernæst index nummeret. Der bruger vi keyen til at definere pladsen på elementet og country til udprint af vores værdi
7. Tjek nu om der er en række lande udprintet på din telefon






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


## Referencer
https://reactnative.dev/docs/style
https://reactnative.dev/docs/statusbar
https://reactnative.dev/docs/flatlist
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map 
