# Uebung-038  -- Reverse String

###### [Angabezettel (.pdf)](https://github.com/IxI-Enki/Uebung-038/blob/main/16%201%20StringReverse.pdf)

## Lernziele:  
 - Stringbearbeitung
   
## Aufgabenstellung:  
  Schreiben Sie ein Programm, welches vom Benutzer einen beliebigen Text einliest, diesen umkehrt und
  anschließend auf die Konsole ausgibt.

## Hinweis:
  Die Benutzereingaben dürfen im gesamten Programm nicht verändert werden und müssen erhalten bleiben.
  Zur Lösung dieser Aufgabe dürfen Sie nicht die Standard-Methoden von String verwenden!

## Beispiel:

> Eingabe: ```Hallo Max, wie geht’s?```

> Ausgabe: ```?s’theg eiw, xaM ollaH```

---

# **SPOILER**  

> [!TIP]
>
> *[C#] Visual Studio :*

 ```c#
namespace StringReverse     //  
{                           //
  public class Program      //
  {                         //
    static void Main()      //
    {
      ///*----------------------- console_settings ------------------------*///
      const int cWidth = 53;                     //  console width
      const int cHeight = 30;                    //  & height
      Console.SetWindowSize(cWidth, cHeight);    //
      Console.OutputEncoding = Encoding.UTF8;    //  Unicode Symbols

      /*----------------------------- VARIABLES -----------------------------*/
      string userInput;
      int index,
          lenght = 0;
      /*-------------------------------- HEAD -------------------------------*/
      Console.Clear();
      Console.Write("\n                  Reverse String                     " +
      /* cWidth: */ "\n=====================================================");

      /*---[in:]-------------------- PROMPT_USER ----------------------------*/
      Console.Write("\n Geben Sie einen Text ein.");    //  

      /*----------------------------- GET_INPUT -----------------------------*/
      userInput = Console.ReadLine();              //  get input + [enter]
                                                   //
      foreach (char letter in userInput)
      { lenght++; }
      Console.Write($"\n Länge:{lenght}\n\n");

      char[] charsInput = new char[lenght];

      for (int i = 0; i < lenght; i++)
      {
        char letter = userInput[i];
        charsInput[i] = letter;
      }

      /*---[out:]--------------------- SOLUTION -----------------------------*/
      index = lenght - 1;
      do
      {
        Console.Write($"{charsInput[index]}");
        index--;
      } while (index >= 0);

      /*-------------------------------- END --------------------------------*/
      Console.Write("\n Zum beenden Eingabetaste drücken..");
      Console.ReadLine();    //  wait for [enter]
      Console.Clear();       //
    }
  }
}
 ```
