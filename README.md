# 1. XHTML & HTML5

Appunti TecWeb per il progetto 

## 1.1 Header 

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

## 1.2 Body 

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
