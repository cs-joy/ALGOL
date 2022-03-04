
![ALGOL20](https://github.com/cs-joy/ALGOL/blob/main/1965_ALGOL-20_A_Language_Manual%2C_Fierst_et_al_-_cover.jpg)


# ALGOL
ALGOL-'"Algorithmic Language" is a family of imperative computer programming languages originally developed in 1958

### Family tree of the Algol, Fortran and COBOL programming language dynasty

![Test](https://github.com/cs-joy/ALGOL/blob/main/Algol%26Fortran_family-by-Borkowski.svg.png)

<details><summary>Sample Programs</summary>
<p>
    ```
      // the main program (this is a comment)

      BEGIN
      FILE F (KIND=REMOTE);
      EBCDIC ARRAY E [0:11];
      REPLACE E BY "HELLO WORLD!";
      WHILE TRUE DO
        BEGIN
            WRITE (F, *, E);
        END;
      END.
    ```
> This program demonstrates the text output function of the ALGOL programming language by displaying the message "Hello world!". This code runs on a Unisys (Burroughs) A-series mainframe.
</p>
</details>

<details><summary>Compute the mean</summary>
> Description
This program computes the mean (average) of the absolute value of an array. Block structures, a dynamic array, and iterative statements are featured in this program. The bold type print represent keywords.
> Source Code
  
    ```
    // the main program (this is a comment)

    begin
      integer N;
      Read Int(N);

      begin
        real array Data[1:N];
        real sum, avg;
        integer i;
        sum:=0;

        for i:=1 step 1 until N do
          begin real val;
            Read Real(val);
            Data[i]:=if val<0 then -val else val
          end;

        for i:=1 step 1 until N do
          sum:=sum + Data[i];
        avg:=sum/N;
        Print Real(avg)
      end
    end	
    ```
> Program Notes
This program has NOT been tested due to the inability to locate the necessary compiler. It is posted here just to give you an example of what ALGOL source code looks like. Compare it to the other example listed to see the syntactic differences that exist in the language.
</p>
</details>

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
