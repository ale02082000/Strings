# Strings
Programma C# per lo studio delle stringhe ASCII 7 bit (non unicode).

Nel programma non si potranno utilizzare le seguenti classi/metodi di manipolazione delle stringhe tipiche del C#, C++, Python:

- StringBuilder
- ToUpper(), ToLower(), Count(), Lenght(), Replace(),
- IsLetter(), IsNumber()
 
 Il programma dovrà contenere queste richieste:
 
 - la sua versione Maiuscola
 
- la sua versione Minuscola
 
- se contiene solo caratteri Alfabetici
 
- di quante lettere è formata
 
- se contiene solo caratteri alfanumerici



 ``` 
 
    string ToUpperCase(string text)
    {
        char[] chars = text.ToCharArray();
        for (int i = 0; i < chars.Length; i++)
        {
            char c = chars[i];
            if (c >= 'a' && c <= 'z')
            {
                chars[i] = (char)(c - 32);
            }
        }
        return new string(chars);
    }
    
    ```
 In questo codice viene defiinito una funzione chiamata "ToUpperCase" che accetta una stringa in ingresso  e restituisce la versione in maiuscolo di quella stringa. 
La funzione controlla tutti i caratteri nella stringa e, se un carattere è una lettera minuscola, lo converte in maiuscolo sottraendo 32 dal valore ASCII del carattere. Infine, la funzione restituisce la versione in maiuscolo della stringa originale.

 tyde
  string ToLowerCase(string text)
    {
        char[] chars = text.ToCharArray();
        for (int i = 0; i < chars.Length; i++)
        {
            char c = chars[i];
            if (c >= 'A' && c <= 'Z')
            {
                chars[i] = (char)(c + 32);
            }
        }
        return new string(chars);
    }
    
       ```
   Il codice presentato utilizza una funzione chiamata "ToLowerCase"  che prende una stringa in ingresso  e restituisce la versione in minuscolo di quella stringa. 
La funzione controlla ogni carattere della stringa e converte eventuali lettere maiuscole in minuscole sottraendo 32 dal valore ASCII del carattere.
Il codice utilizza un array di caratteri per rappresentare la stringa e poi controlla ogni carattere utilizzando un ciclo for. Se il carattere è una lettera maiuscola, il codice lo converte in minuscolo sommando 32 al valore ASCII del carattere. Infine, la funzione restituisce una nuova stringa contenente i caratteri modificati.

``` 
string Reverse(string text)
    {
        char[] chars = text.ToCharArray();
        for (int i = 0, j = text.Length - 1; i < j; i++, j--)
        {
            char temp = chars[i];
            chars[i] = chars[j];
            chars[j] = temp;
        }
        return new string(chars);
    }
     ```
     Il codice prende una stringa in input e la inverte utilizzando  due puntatori. La stringa viene convertita in un array di caratteri, quindi i due puntatori partono dall'inizio e dalla fine dell'array e si muovono verso il centro dell'array scambiando i caratteri corrispondenti. Infine, viene creata una nuova stringa a partire dall'array invertito e restituita come output. 
     ``` 
       bool alfabetica(string text)
    {
        for (int i = 0; i < text.Length; i++)
        {
            char c = text[i];
            if (!((c >= 'a' && c <= 'z') || (c >= 'A' && c <= 'Z')))
            {
                return false;
            }
        }
        return true;
    }
    
     ```
     Il codice definisce una funzione chiamata "alfabetica" che prende in input una stringa "text" e restituisce un valore booleano. La funzione controlla ogni carattere nella stringa usando un  for, e se il carattere non appartiene all'alfabeto  (lettere minuscole o maiuscole), la funzione restituisce false. Se tutti i caratteri nella stringa appartengono all'alfabeto , la funzione restituisce true. 
     
     ```
       bool alfanumerica(string text)
    {
        for (int i = 0; i < text.Length; i++)
        {
            char c = text[i];
            if (!((c >= 'a' && c <= 'z') || (c >= 'A' && c <= 'Z') || (c >= '0' && c <= '9')))
            {
                return false;
            }
        }
        return true;
    }
     ```
     Questo codice utilizza una funzione chiamata "alfanumerica" che prende una stringa come input e restituisce un valore booleano. La funzione controlla se la stringa contiene solo caratteri alfanumerici (lettere e numeri) controllando attraverso ogni carattere della stringa e restituendo "false" se trova un carattere che non è alfanumerico. Se tutti i caratteri sono alfanumerici, la funzione restituisce "true".
  
    ```
    int NumeroLettere(string text)
    {
        int count = 0;
        for (int i = 0; i < text.Length; i++)
        {
            char c = text[i];
            if ((c >= 'a' && c <= 'z') || (c >= 'A' && c <= 'Z'))
            {
                count++;
            }
        }
        return count;
    }
    
      ```
      La funzione NumeroLettere prende in input una stringa text e restituisce il numero di lettere presenti al suo interno.
Per fare ciò, la funzione utilizza un ciclo for per scorrere tutti i caratteri della stringa, verificando se ciascun carattere è una lettera dell'alfabeto (sia maiuscola che minuscola) tramite una serie di condizioni, e incrementa il contatore count ogni volta che viene trovata una lettera.
      
     
     
    
     



    
