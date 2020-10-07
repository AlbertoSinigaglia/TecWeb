Appunti TecWeb per il progetto 

# **1. XHTML**

## **1.1 Header**

#### 1.1.1 DOCTYPE

```html
// html5
<!DOCTYPE html>
// xhtml
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<html>
...
```
:x: Se manca, il browser è libero di interpretare la pagina come meglio crede (come se ci son errori nella sintassi [[`Quirks Mode`](https://it.wikipedia.org/wiki/Quirks_Mode)])

#### 1.1.2 Intestazione
```html
<html xmlns="..." xml:lang="it" lang="it">
...
```

#### 1.1.3 Content type
```html
<html>
  <head>
    // xhtml
    <meta http-equiv="content-type" content="text/html; charset=UTF-8">
    // html5
    <meta charset="UTF-8">
...
```
#### 1.1.4 Link
definisce un collegamento ad una risorsa esterna (`href`, `rel`)
```html
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="/file.css" />
    <link rel="shortcut icon" href="/img.ico" />
...
```

#### 1.1.5 Base
definisce la posizione di base per i collegamenti
```html
<html>
  <head>
    <base href="/cartella_base/" />
...
```

#### 1.1.6 Meta
suddivisi tra `http-equiv` (esempio `charset` o `refresh`) e `name` (`description`, `keywords`, `copyright`, `author`, `robots`, `rating`)
```html
<html>
  <head>
    <meta name="description" content="la mia descrizione" />
...
```

## **1.2 Body** 

#### 1.2.1 Attributi Core
Sono `class`, `id`, `title` (aggiunge informazioni a un elemento) e `style` (supportati da tutti i tag)

#### 1.2.2 Div
Elemento contenitore generico per l'associazione con fogli di stile e crea un nuovo blocco
```html
<html>
  ...
  <body>
    ...
    <div> ... </div>
...
```


#### 1.2.3 Span
Elemento con alcuna cratteristica se non di fare da supporto per stili o per dichiarare la presenza di vocaboli in altre lingue (elemento in linea)
```html
<html>
  ...
  <body>
    ...
    <p> foo <span>bar</span> </p>
...
```

#### 1.2.4 P
Elemento per l'inserimento di un paragrafo, per andare a capo si usa `<br/>`
```html
<html>
  ...
  <body>
    ...
    <p> foo <br/> bar </p>
...
```

#### 1.2.5 Headers
Elemento "gerarchico" per la definizione degli argomenti/topics principali
```html
<html>
  ...
  <body>
    ...
    <h1> Titolo principale </h1>
    <h2> Paragrafo del testo </h2>
...
```

#### 1.2.6 Quote
Si possono usare `quote` e `cite` per inserire citazioni 

#### 1.2.7 Pre
Usato per l'inserimento di testo preformattato (non fa il trim degli spazi)

#### 1.2.8 Elenchi non ordinati
Elenchi puntati (`ul`)  da utilizzare quando vogliamo dei punti per il nostro elenco senza un ordine ben preciso.  
Ogni elemento è un `li`
```html
<html>
  ...
  <body>
    ...
    <ul>
      <li> entry 1 </li>
      <li> entry 2 </li>
    </ul>
...
```

#### 1.2.8 Elenchi ordinati
Elenchi puntati (`ol`)  da utilizzare quando vogliamo dei punti per il nostro elenco con un ordine ben preciso.  
Ogni elemento è un `li`
```html
<html>
  ...
  <body>
    ...
    <ol>
      <li> entry 1 </li>
      <li> entry 2 </li>
    </ol>
...
```

#### 1.2.9 Elenchi di definizioni
Elenchi in cui non si utilizza ancun tipo di punto, utili soprattutto per definire dei termini.
`dl` è il tag generico, in cui `dt` è l'elemento da definire e `dd` la definizione.
```html
<html>
  ...
  <body>
    ...
    <dl>
      <dt> termine </dt>
      <dd> la definizione del termine </dd>
    </dl>
...
```

#### 1.2.10 Immagini
il tag è `img` con possibili attributi:
1. `alt` : testo alternativo (testo descrizione della foto da un punto di vista informativo/visivo)
2. `longdesc` : URI a una pagina con una descrizione dell'immagine

```html
<html>
  ...
  <body>
    ...
    <img src="nome.png" alt="descrizione">
...
```

#### 1.2.11 Link a
il tag è `a` con possibili attributi:
1. `href` : path a cui il link punta
2. `target` : attributo per specificare se si vuole aprire una nuova finestra
3. `title` : titolo del link che descrive la destinazione
4. `download` : attributo per la dichiarazione che la destinazione è da scaricare
5. `tabindex`, `accesskey` : indicano rispettivamente un carattere per portare il focus sul link e l'ordine di tabulazione (`accesskey` ha poco senso perchè ormai gli shortcut son già tutti occupati) 
```html
<html>
  ...
  <body>
    ...
    <a href="/altrapagina.php" target="_blank" title="titolo del link">
...
```

#### 1.2.12 Tabelle
il tag è `table` e supportano i seguenti tag:
1. `tr`: riga
2. `td`: elemento della riga
3. `th`: elemento della riga dell'header
4. `thead`: header della tabella
5. `tfoot`: footer della tabella
6. `tbody`: corpo della tabella
7. `summary`: descrizione della tabella
8. `caption`: didascalia della tabella

```html
<html>
  ...
  <body>
    ...
    <table>
      <thead>
        <tr>
          <th> prima colonna </th>
        </tr>
      </thead>
      <tfoot>
        <tr>
          <td> footer prima colonna </td>
        </tr>
      </tfoot>
      <tbody>
        <tr>
          <td>valore prima riga prima colonna</td>
        </tr>
      </tbody>
    </table>
...
```

#### 1.2.13 Form
Il tag è `form` e supporta i seguenti tag
1. `action`: pagina cui puntata
2. `method`: metodo da usare per la richiesta (`GET` o `POST`)
3. `enctype="multipart/form-data"`: metodo di criptazione nel caso nel form ci siano `input` con `type="file"`
Ogni elemento è un `li`
```html
<html>
  ...
  <body>
    ...
    <form action="registrati.php" method="post">
      ...
    </form>
...
```
si usano inoltre i campi `fieldset` (e relativa `legend`) e `div` per il suo contenuto

#### 1.2.14 Input, textarea
ognuno di questi elementi in un form deve avere l'attributo `name` per la richiesta
`input` può essere del tipo (`type`):
1. `text`: con relativo `maxlength` per dichiarare la dimensione di testo massimo
2. `password`: testo offuscato visivamente
3. `checkbox`: on/of
4. `radio`: "uno dei"
5. `submit`: invio
6. `reset`: reset del form
7. `hidden`: campo nascosto
8. `file`: per caricare un file
9. `button`: bottone ma non per il submit
10. `image`: come `button` ma con immagine
Ogni elemento è un `li`
```html
<html>
  ...
  <body>
    ...
    <form action="registrati.php" method="post">
      <fieldset>
        <legend> Inserimento dati personali </legend>
        <label for="campo_nome"> inserisci il tuo nome </label>
        <input type="text" name="nome" id="campo_nome"> 
        <label for="campo_storia"> inserisci la tua storia </label>
        <textarea type="text" name="storia" id="campo_storia"> la mia lunghissima storia </textarea>
      </fieldset>
    </form>
...
```
Gli si associa inoltre una `label` per associare il testo associato a un `input` (con l'attributo `for`)


#### 1.2.15 Select
Permette di creare un elenco di dati, che viene visualizzato come menù a tendina (può essere usato anche per la selezione multipla con tag `multiple`)
```html
<html>
  ...
  <body>
    ...
    <form action="registrati.php" method="post">
      <fieldset>
        <legend> legenda del settore del form </legend>
        <label for="select_nome"> seleziona il tuo nome </label>
        <select name="nome" id="select_nome">
          <optgroup label="Primo gruppo">
            <option value="1.1">prima scelta</option>
            <option value="1.2">seconda scelta</option>
          </optgroup>
          <optgroup label="Secondo gruppo">
            <option value="2.1">prima scelta</option>
            <option value="2.2">seconda scelta</option>
          </optgroup>
        </select>
      </fieldset>
    </form>
...
```

# **2. HTML5**

## **2.1 Header**

#### 2.1.1 Viewport
impostare il rapporto di visualizzazione:
```html
<html>
  <head>
  ...
    <meta name="viewport" content="width=device-width">
    ...
```
può avere nel `content` anche:
1. `initial-scale`
2. `minimum-scale`
3. `maximum-scale`
4. `user-scalable`

## **2.2 Body**

#### 2.2.1 Canvas
Area di disegno interativa

#### 2.2.2 Audio e video
Accesso e riproduzione di multimedia senza la necessità di plug-in

#### 2.2.2 Nuovi tag alternativi a div
HTML5 inserisce nuovi tag quali `section`, `article`, `header`, `footer`, `nav`, `aside`

#### 2.2.2 Nuovi tag semantivi
HTML5 inserisce nuovi tag semantici quali `time`, `figure`, `meter` (con attributi `max` e `min`), `progress`, `small`.  
In particolare `datalist`:
```html
<html>
  <head>
  ...
  </head>
  <body>
    <input list="lista">
    <datalist id="lista">
      <option value="valore1"> Valore 1 </option>
      <option value="valore2"> Valore 2 </option>
    </datalist>
  </body>
</html>
```

#### 2.2.3 Novità nei form
si aggiunge l'attributo `target`, `autocomplete` e `novalidate`, mentre a `input` si aggiungono tipi quali:
1. `number`
2. `color`
3. `email`, `url`, `tel`
4. `search`
5. `datetime`, `datetime-local`, `date`, `month`, `time`, `week`

Vengono inoltre aggiunti attributi a `input` come 
1. `required`
2. `formnovalidate`
3. `pattern`
4. `placeholder`
5. `autocomplete`
6. `autofocus`
7. `spellcheck`
8. `multiple`
9. `min`, `max`, `step`