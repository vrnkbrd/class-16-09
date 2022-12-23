# class-16-09
### Task 1 7kyu
Given a string made up of letters a, b, and/or c, switch the position of letters a and b (change a to b and vice versa). Leave any incidence of c untouched.
Example:
'acb' --> 'bca'
'aabacbaa' --> 'bbabcabb'

### My solution
```Java
  public class Switch {
    public static String switcheroo(String x) {
      String[] Letters = x.split("");

          for (int i=0; i < Letters.length; i++){
              if (Letters[i].equals("a")) Letters[i] = "b";
              else if (Letters[i].equals("b")) Letters[i] = "a";
          }
          x = String.join("", Letters);
          return x;
    }
  }
```

Fav solution
```Java
  class Switch {

    public static String switcheroo(String x) {
      return x.replace('a','_').replace('b','a').replace('_','b');
    }

  }
  ```
I liked that they created additional letter what was enough for using a library method.

### Task 2 7kyu

Write a function to convert a name into initials. This kata strictly takes two words with one space in between them.
The output should be two capital letters with a dot separating them.
It should look like this:
Sam Harris => S.H
patrick feeney => P.F

### My solution
```Java
  public class AbbreviateTwoWords {

    public static String abbrevName(String name) {
          name = name.toUpperCase();
          String[] Letters = name.split(" ");
          char ch1 = Letters[0].charAt(0);
          char ch2 = Letters[1].charAt(0);

          return ch1 + "." + ch2;
    }
  }
```

### Fav solution
```Java
  public class AbbreviateTwoWords {

    public static String abbrevName(String name) {
      return name.toUpperCase().replaceAll("(.).*\\s(.).*", "$1.$2");
    }

  }
  ```
Just leave it here
