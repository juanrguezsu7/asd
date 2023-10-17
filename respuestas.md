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
### Pregunta 63: ¿Cuál es el resultado de cada una de estas operaciones?
- c = a | b -> [1, 2, 3, 4, 5]
- d = b | a -> [5, 4, 3, 2, 1]
- e = a & b -> [2, 3, 4]
- f = b & a -> [4, 3, 2]
******
### Pregunta 64: ¿Qué resultados dan las siguientes operaciones?
- a.to_a -> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
- b.to_a -> [1, 2, 3, 4, 5, 6, 7, 8, 9]
- b.include? 10 -> false
- b.include? 8 -> true
- b.step(2) {|x| print "#{x} " } -> 1 3 5 7 9 => 1...10
- 1..3.to_a -> NoMethodError: undefined method 'to_a' for 3:Integer (se arregla poniendo (1..3).to_a y devuelve [1, 2, 3])
******
### Pregunta 65: ¿Qué resultados dan las siguientes operaciones? 
- r.member? 50 -> true
- r.include? 99.9 -> true
- r.member? 99.9 -> true
******
### Pregunta 66: ¿Qué resultados dan las siguientes operaciones? 
- true.class -> TrueClass
- false.class -> FalseClass
- puts "hello" if 0 -> hello
- puts "hello" if nil -> (nada)
- puts "hello" if "" -> hello
******
### Pregunta 67: ¿Qué resultados dan las siguientes operaciones?
- x.class -> Symbol
- x == 'sym' -> false
- x == :sym -> true
- z.class -> Symbol
- x == 'sym'.to_sym -> true
- x.to_s == 'sym' -> true
******
### Pregunta 68: ¿Qué resultados se dan?
- t = s -> "Ruby"
- t[-1] = "" -> ""
- print s -> Rub
- t = "Java" -> "Java"
- print s, t -> RubJava
******
### Pregunta 69: ¿Cuál es el resultado?
- "%d %s" % [3, "rubies"] -> "3 rubies"
******
### Pregunta 70: ¿Cuáles son los resultados?
- x, y = 4, 5 -> [4, 5]
- z = x > y ? x : y -> 5
- x,y,z = [1,2,3] -> [1, 2, 3]
******
### Pregunta 71: ¿Qué resultados dan las siguientes operaciones?
- x.keys -> [:a, :b]
- x.values -> [1 ,2]
- x -> {:a=>1, :b=>2, :c=>3}
- x -> {:a=>1, :b=>2, :c=>3}
- x -> {:b=>2, :c=>3}
- x.delete_if { |k, v| v % 2 == 0 } -> {:a=>1}
- x -> {:a=>1}
******
### Pregunta 72: ¿Qué hace la siguiente sentencia? *counts = Hash.new(0)* ¿Qué diferencia hay con la asignación *counts = {}*?
Ambas son iguales y crean un hash asociativo vacío.
******
### Pregunta 73: ¿Qué retorna esta expresión regular? *'hello world, hello LPP'.scan /\w+/*
El metacaracter \w casa con todas las palabras usando como separadores los espacios, puntos y comas entre otros. Por tanto, devuelve *["hello", "world", "hello", "LPP"]*.
