# Teorema fundamental de la programación estructurada
### Pregunta 41: ¿Qué diferencia hay entre "\t\n" y '\t\n'?
La principal diferencia es que con las comillas dobles ("") el contenido es evaluable mientras que con las comillas simples ('') se interpreta el contenido literalmente. Es decir, si intentamos realizar *put "\t\n"* se imprimirá una tabulación y un salto de línea mientras que con *put '\t\n'* se imprimirá *\t\n* literalemente.
******
### Pregunta 42: ¿Cómo funciona %q? ¿Qué es %q{hello world\n}? ¿Qué es %q{'a' 'b' 'c'}?
%q transforma lo que esté en su interior a una string con comillas simples ('') no interpolable, es decir, una string donde todos los caracteres se interpretarán literalmente. Por tanto, *%q{hello world\n}* transformará la string de su interior a '"hello world\n"' literalmente sin interpretar el salto de línea ni las comillas dobles. Por último, *%q{'a' 'b' 'c'}* transformará la string de su interior a ''a' 'b' 'c'' literalmente sin interpretar las comillas simples.
******
### Pregunta 43: ¿Cómo funciona %Q? ¿Qué es %Q{hello world\n}? ¿Qué es %Q{"a" "b" "c"}?
%Q transforma lo que esté en su interior a una string con comillas dobles ("") interpolable, es decir, una string donde puede haber expresiones evaluables. Por tanto, *%Q{hello world\n}* transformará la string de su interior a ""hello world\n"" evaluando el salto de línea y dejando las últimas comillas dobles en una línea aparte. Por último, *%Q{"a" "b" "c"}* transformará la string de su interior a ""a" "b" "c"" donde no había ninguna expresión evaluable en su interior.
******
### Pregunta 44: ¿Qué queda en c?
Queda "--4--\n--2--\n". HERE incluye lo que introduzca el usuario y lo interpreta.
******
### Pregunta 45: ¿Qué queda en c?
Queda "--\#{a}--\n--\#{b}--\n". 'HERE' incluye lo que introduzca el usuario de forma literal.
******
### Pregunta 46: *s = "hello"*. ¿Cuál es el valor de la siguientes expresiones?
- s[0, 2] -> "he"
- s[-1, 1] -> "o"
- s[0, 10] -> "hello"
******
### Pregunta 47: ¿Qué queda en g?
Queda "hello world".
******
### Pregunta 48: ¿Qué queda en e?
Queda "...".
******
### Pregunta 49: ¿Cuál es el resultado?
Queda "2 2 2 ".
******
### Pregunta 50: ¿Qué es esto? *%w[this is a test]*
*%w* devuelve un array con strings evaluables pero con contenido literal (lo transforma a literal si la palabra fuese evaluable) de los elementos pasados como argumento separados por espacios. En este ejemplo, se devolvería un array *["this", "is", "a", "test"]*.
### Pregunta 51: ¿Qué es esto? *%w[\t \n]*
Lo mismo que la pregunta anterior pero aquí, como los elementos son evaluables, se transforman a literales empleando el carácter de escape. En este ejemplo, se devolvería un array *["\\t", "\\n"]*.
******
### Pregunta 52: ¿Qué es esto? *%W[\t \n]*
Lo mismo que *%w* pero no transforma los elementos a literales. En este ejemplo, se devolvería un array *["\t", "\n"]*.
******
### Pregunta 53: ¿Qué contiene nils? *nils = Array.new(3)*
Contiene tres elementos nil en un array.
******
### Pregunta 54: ¿Qué contiene zeros? zeros = Array.new(3, 0)
Contiene tres elementos con un valor entero de 0 en un array.
******
### Pregunta 55: ¿Qué queda en b?
Una copia del array de x.
******
### Pregunta 56: ¿Qué queda en c?
Queda un array de esta forma *[0, 2, 4]*.
******
### Pregunta 57: ¿Cuál es el resultado de cada una de estas operaciones?
- a[1, 1] -> Array con un solo elemento "b"
- a[-2, 2] -> Array con dos elementos "d" y "e"
- a[0..2] -> Array con tres elementos "a", "b" y "c"
- a[0...1] -> Array con un solo elemento "a"
- a[-2..-1] -> Array con dos elementos "d" y "e"
******
### Pregunta 58: ¿Cuál es el resultado de cada una de estas operaciones?
- 1º *a* -> ["A", "B", "c", "d", "e"]
- 2º *a* -> ["A", "B", "C", "D", "E"]
- 3º *a* -> [1, 2, 3, "A", "B", "c", "D", "E"]
- 4º *a* -> [3, "A", "B", "c", "D", "E"]
- 5º *a* -> [3, "A", "B", "c", "D", "Z"]
- 6º *a* -> [3, "A", "B", "c", nil]
******
### Pregunta 59: ¿Cuál es el resultado de cada una de estas operaciones?
- a = (1...4).to_a -> [1, 2, 3]
- a = a + [4, 5] -> [1, 2, 3, 4, 5]
- a += [[6, 7, 8]] -> [1, 2, 3, 4, 5, [6, 7, 8]]
- a = a + 9 -> TypeError: no implicit conversion of Integer into Array.
******
### Pregunta 60: ¿Cuál es el resultado de cada una de estas operaciones?
- x = %w{a b c b a} -> ["a", "b", "c", "b", "a"]
- x = x - %w{b c d} -> ["a", "a"]
******
### Pregunta 61: ¿Cuál es el resultado de cada una de estas operaciones?
- z = [0]\*8 -> [0, 0, 0, 0, 0, 0, 0, 0]
******
### Pregunta 62: ¿Cuál es el resultado de cada una de estas operaciones?
- a << 1 -> [1]
- a << 2 << 3 -> [1, 2, 3]
- a << [4, 5, 6] -> [1, 2, 3, [4, 5, 6]]
- a.concat [7, 8] -> [1, 2, 3, [4, 5, 6], 7, 8]
******
