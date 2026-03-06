package ProgramasParcial1;

import java.util.Scanner;

public class Programas {

    public static void main(String[] args) {
        Scanner teclado = new Scanner(System.in);
        int opcion = 0;

        // BUCLE PRINCIPAL
        while (opcion != 6) {
            System.out.println("\n===== MENÚ PRINCIPAL =====");
            System.out.println("1. Parte 1- Ciclos y operaciones numéricas");
            System.out.println("2. Parte 2- Condiciones y Divisibilidad");
            System.out.println("3. Parte 3- Uso de Switch");
            System.out.println("4. Parte 4- Análisis Numérico");
            System.out.println("5. Parte 5- Patrones y transformaciones");
            System.out.println("6. Salir");
            System.out.print("Seleccione una opción: ");

            if (teclado.hasNextInt()) {
                opcion = teclado.nextInt();
                teclado.nextLine();
            } else {
                System.out.println("Error: Ingrese un número.");
                teclado.next(); 
                continue;
            }
//================================================================================================================================================           
            // --- INICIO DEL SUBMENÚ ---
            switch (opcion) {
                case 1:
                    int subOpcion1 = 0;
                    while (subOpcion1 != 6) { 
                        System.out.println("\n--- Programas Parte 1 Ciclos y Operaciones Numericas ---");
                        System.out.println("1. Números Divisibles entre 4");
                        System.out.println("2. Factorial");
                        System.out.println("3. Cantidad de números -+0");
                        System.out.println("4. Promedio de números pares");
                        System.out.println("5. Suma de dígitos de una cantidad");
                        System.out.println("6. << PARA VOLVER AL MENÚ PRINCIPAL: Ingrese 6");
                        System.out.print("Seleccione: ");
                        
                        subOpcion1 = teclado.nextInt();
                        teclado.nextLine();

                        switch (subOpcion1) {
                            case 1: System.out.println("Ejecutando: Divisibles entre 4..."); numerosdivisiblesentre4(teclado); pausar(teclado); break;
                            case 2: System.out.println("Ejecutando: Factorial...");  Factorial(teclado); pausar(teclado);                        break;
                            case 3: System.out.println("Ejecutando: Cantidad -+0..."); cantidadPositivosNegativosCero(teclado); pausar(teclado);       break;
                            case 4: System.out.println("Ejecutando: Promedio pares..."); promedioPares(teclado); pausar(teclado);       break;
                            case 5: System.out.println("Ejecutando: Suma de dígitos...");sumadigitos(teclado); pausar(teclado);   break;
                            case 6: System.out.println("Regresando...");                      break; 
                            default: System.out.println("Opción no válida.");
                        }
                    } // Fin del while del submenú
                    break; // Fin del case 1 (esto te regresa al menú principal)
//_____________________________________________________________________________________________________________________________
                case 2: 
                int subOpcion2 = 0;
                while (subOpcion2 != 4) { 
                    System.out.println("\n--- Programas Parte 2 Condiciones y Divisibilidad---");
                    System.out.println("1. Multiplos de 7 o de 11");
                    System.out.println("2. Divisibles entre 3 pero no en 2");
                    System.out.println("3. Mañana, Tarde, Noche");
                    System.out.println("4. << PARA VOLVER AL MENÚ PRINCIPAL: ingrese 6");
                    System.out.print("Seleccione: ");
                    
                    subOpcion2 = teclado.nextInt();
                    teclado.nextLine();

                    switch (subOpcion2) {
                        case 1: System.out.println("Multiplos de 7 o de 11...");multiplos7u11(teclado);pausar(teclado);                     break;
                        case 2: System.out.println("Ejecutando: Divivibles entre 3 pero no en 2...");numerosdivisiblesentre3peronoen2(teclado);pausar(teclado);   break;
                        case 3: System.out.println("Ejecutando: Mañana, Tarde, noche..."); mañanatardenoche(teclado); pausar(teclado);           break;
                        case 4: System.out.println("Regresando...");                                  break; 
                        default: System.out.println("Opción no válida.");
                    }
                }
//___________________________________________________________________________________________________________________________
                case 3:
                int subOpcion3 = 0;
                while (subOpcion3 != 6) { 
                    System.out.println("\n--- Programas Parte 3 Uso de Switch---");
                    System.out.println("1. Numeros romanos del 1 al 5 ");
                    System.out.println("2. Opciones +-*");
                    System.out.println("3. << PARA VOLVER AL MENÚ PRINCIPAL: Ingrese 6");
                    System.out.print("Seleccione: ");
                         
                    subOpcion3 = teclado.nextInt();
                    teclado.nextLine();

                    switch (subOpcion3) {
                        case 1: System.out.println("Ejecutando: Numeros romanos..."); convertirARomanos(teclado);pausar(teclado);            break;
                        case 2: System.out.println("Ejecutando: Opciones..."); sumarrestarmultiplicar(teclado); pausar(teclado);                   break;
                        case 3: System.out.println("Regresando...");                              break; 
                        default: System.out.println("Opción no válida.");
                         }
                     }
                
//________________________________________________________________________________________________________________________
                case 4: 
                int subOpcion4 = 0;
                while (subOpcion4 != 6) { 
                   System.out.println("\n--- Programas Parte 4 Análisis Numérico---");
                   System.out.println("1. Numeros >< diferencia ");
                   System.out.println("2. Tabla de division del 1 al 10");
                   System.out.println("3. Cantidad de Digitos pares");
                   System.out.println("4. Triangular");
                   System.out.println("5. Promedio de números negativos");
                   System.out.println("6. << PARA VOLVER AL MENÚ PRINCIPAL: Ingrese 6");
                   System.out.print("Seleccione: ");
                              
                   subOpcion4 = teclado.nextInt();
                   teclado.nextLine();

                   switch (subOpcion4) {
                         case 1: System.out.println("Ejecutando: Numeros <> y diferencia..."); compararNumeros(teclado); pausar(teclado);              break;
                         case 2: System.out.println("Ejecutando: Tabla de division del 1 al 10..."); tablaDivision(teclado);pausar(teclado);       break;
                         case 3: System.out.println("Ejecutando: Cantidad de digitos pares..."); contarDigitosPares(teclado); pausar(teclado);          break;
                         case 4: System.out.println("Ejecutando: Triangular..."); esTriangular(teclado); pausar(teclado);                          break;
                         case 5: System.out.println("Ejecutando: Promedio de numeros negativos...");promedioNegativos(teclado);  pausar(teclado);        break;
                         case 6: System.out.println("Regresando...");                                      break; 
                         default: System.out.println("Opción no válida.");
                              }
                          }
                     
//___________________________________________________________________________________________________________________________
                case 5:
                int subOpcion5 = 0;
                while (subOpcion5 != 6) { 
                  System.out.println("\n--- Programas Parte 5 PAtrones y Transformaciones---");
                  System.out.println("1. Primeros multiplos de 6");
                  System.out.println("2. Numeros potencia de 2");
                  System.out.println("3. Numero Invertido");
                  System.out.println("4. Suma de los Numeros 1 al n par o impar");
                  System.out.println("5. Celsius a Fahrenheit");
                  System.out.println("6. << PARA VOLVER AL MENÚ PRINCIPAL: Ingrese 6");
                  System.out.print("Seleccione: ");
                                   
                        subOpcion5 = teclado.nextInt();
                        teclado.nextLine();

                        switch (subOpcion5) {
                              case 1: System.out.println("Ejecutando: Primeros multiplos de 6..."); mostrarMultiplosDe6(teclado); pausar(teclado);             break;
                              case 2: System.out.println("Ejecutando: Numeros potencia de 2..."); esPotenciaDeDos(teclado); pausar(teclado);                  break;
                              case 3: System.out.println("Ejecutando: Numero invertido...");  invertirNumero(teclado); pausar(teclado);                    break;
                              case 4: System.out.println("Ejecutando: Suma de los numeros 1 al n par o impar..."); verificarParSuma(teclado); pausar(teclado);   break;
                              case 5: System.out.println("Ejecutando: Celsius a Farenheit...");  convertirCelsiusAFahrenheit(teclado); pausar(teclado);                   break;
                              case 6: System.out.println("Regresando...");                                           break; 
                              default: System.out.println("Opción no válida.");
                                   }
                               }     
//___________________________________________________________________________________________________________________________
                case 6: System.out.println("Saliendo del programa..."); break;
                default: System.out.println("Opción inválida.");
            }
        }
        teclado.close(); // Se cierra al final de todo el programa
    }

    
//===================Fin del Submenu===============================================================================================================  
    
    
//_________________________________________________________________________________________________________________________________________________
    //================================Funciones y metodos==========================================================================================
//____________________________________________________________________________________________________________________
    public static void numerosdivisiblesentre4(Scanner entrada) {
        
        System.out.print("Introduce un número n: ");
        int n = entrada.nextInt();
        
        int suma = 0;
        for (int i = 4; i <= n; i += 4) {
            suma += i;
        }
        
        System.out.println("La suma de los números divisibles entre 4 hasta " + n + " es: " + suma);
        
    }
//_____________________________________________________________________________________________________________________
    public static void Factorial(Scanner entrada) {
        
        System.out.print("Introduce un número para calcular su factorial: ");
        int n = entrada.nextInt();
        
        long factorial= 1;
        
        if (n < 0) {
            System.out.println("El factorial no está definido para números negativos.");
        } else {
            for (int i = 1; i <= n; i++) {
                factorial *= i;
            }
            System.out.println("El factorial de " + n + " es: " + factorial);
        }
        
    }
//________________________________________________________________________________________________________________________
    public static void cantidadPositivosNegativosCero(Scanner entrada) {
        System.out.print("¿Cuántos números desea ingresar? (n): ");
        int n = entrada.nextInt();
      
        int positivos = 0;
        int negativos = 0;
        int ceros = 0;
        //Para ingresar n cantidad de numeros a evaluar
        for (int i = 1; i <= n; i++) {
            System.out.print("Ingrese el número " + i + ": ");
            int num = entrada.nextInt(); // <-- Leemos el número actual
            
            if (num > 0) {
                positivos++;
            } else if (num < 0) {
                negativos++;
            } else {
                ceros++;
            }
        }
        
        System.out.println("\n--- Resultados ---");
        System.out.println("Positivos: " + positivos);
        System.out.println("Negativos: " + negativos);
        System.out.println("Ceros: " + ceros);
        
        entrada.nextLine();
    }
//________________________________________________________________________________________________________________________________
    public static void promedioPares(Scanner entrada) {
        System.out.print("Introduce el límite (n): ");
        int n = entrada.nextInt();
        
        int suma = 0;
        int cantidad = 0;

        for (int i = 1; i <= n; i++) {
            if (i % 2 == 0) {
                suma += i;      
                cantidad++; 
            }
        }

        if (cantidad > 0) {
            double promedio = (double) suma / cantidad;
            System.out.println("\nResultados:");
            System.out.println("Cantidad de números pares: " + cantidad);
            System.out.println("El promedio de los numeros pares es: " + promedio);
        } else {
            System.out.println("No hay números pares en el rango de 1 a " + n);
        }

        entrada.nextLine();
    }
//___________________________________________________________________________________________________________________________________
    public static void sumadigitos(Scanner entrada) {
        System.out.print("Introduce un numero (n): ");
        int n = entrada.nextInt();
        
        int suma = 0;

        while (n > 0) {
            int digito = n % 10;    
            suma = suma + digito;   
            n = n / 10;             
        }

        System.out.println("La suma de los dígitos es: " + suma);
        entrada.nextLine(); 
    }
    

  //______________________________________________________________________________________________________________________________________
    public static void multiplos7u11(Scanner entrada) {
        System.out.print("Ingrese un número: ");
        int num = entrada.nextInt();

        // Verificamos si el residuo es 0 para el 7 O para el 11
        if (num % 7 == 0) {
            System.out.println(num + " es múltiplo de 7");
        if (num % 11 == 0) {
                System.out.println(num + " es múltiplo de 11");
        } else {
            System.out.println(num + " no es múltiplo de ninguno de los dos.");
        }

        entrada.nextLine(); // Limpiar el búfer para que la pausa funcione
    }   
    }
    //_______________________________________________________________________________________________________________________________________
    public static void numerosdivisiblesentre3peronoen2(Scanner entrada) {
        System.out.print("Introduce el límite (n): ");
        int n = entrada.nextInt();

        System.out.println("Números que son divisibles entre 3 pero no entre 2:");
        
        // Recorremos desde 1 hasta n
        for (int i = 1; i <= n; i++) {
            if (i % 3 == 0 && i % 2 != 0) {
                System.out.print(i + " ");
            }
        }
        
        System.out.println();
        entrada.nextLine();
    }
//_____________________________________________________________________________________________________________________________________________
    public static void mañanatardenoche(Scanner entrada) {
        System.out.print("Ingrese la hora (0-23): ");
        int hora = entrada.nextInt();

        if (hora >= 0 && hora < 12) {
            System.out.println("La hora " + hora + " corresponde a la MAÑANA (AM)");
        } 
        else if (hora >= 12 && hora < 18) {
            System.out.println("La hora " + hora + " corresponde a la TARDE (PM)");
        } 
        else if (hora >= 18 && hora <= 23) {
            System.out.println("La hora " + hora + " corresponde a la NOCHE (PM)");
        } 
        else {
            System.out.println("Hora no válida. Ingrese un valor entre 0 y 23.");
        }

        entrada.nextLine(); // Limpieza de búfer
    }
//________________________________________________________________________________________________________________________________________________
    public static void convertirARomanos(Scanner entrada) {
        System.out.print("Ingrese un número del 1 al 5: ");
        int num = entrada.nextInt();

        switch (num) {
            case 1:
                System.out.println("El número romano es: I");
                break;
            case 2:
                System.out.println("El número romano es: II");
                break;
            case 3:
                System.out.println("El número romano es: III");
                break;
            case 4:
                System.out.println("El número romano es: IV");
                break;
            case 5:
                System.out.println("El número romano es: V");
                break;
            default:
                System.out.println("Número fuera de rango. Solo se permiten del 1 al 5.");
                break;
        }
        
        entrada.nextLine(); // Limpieza de búfer
    }
//__________________________________________________________________________________________________________________________
    public static void sumarrestarmultiplicar(Scanner entrada) {
    	System.out.print("Elija una opcion 1:Suma, 2: Resta, 3: Multiplicacion ");
        int opcion = entrada.nextInt();
        
        System.out.print("Ingrese el primer numero numero : ");
        int num1 = entrada.nextInt();
        System.out.print("Ingrese el segundo numero número ");
        int num2 = entrada.nextInt();

        switch (opcion) {
            case 1:
                System.out.println("El resultado de la Suma:" + (num1+num2));
                break;
            case 2:
                System.out.println("El resultado de la Resta"+ (num1-num2));
                break;
            case 3:
                System.out.println(" El resultado de la Multiplicacion"+(num1*num2));
                break;
            default:
                System.out.println("Número fuera de rango. Solo se permiten del 1 al 3.");
                break;
        }
        
        entrada.nextLine(); // Limpieza de búfer
    }
//_______________________________________________________________________________________________________________________
    public static void compararNumeros(Scanner entrada) {
        System.out.print("Ingrese el primer número (a): ");
        int a = entrada.nextInt();
        System.out.print("Ingrese el segundo número (b): ");
        int b = entrada.nextInt();

        if (a > b) {
            System.out.println("El mayor es: " + a);
            System.out.println("El menor es: " + b);
        } else if (b > a) {
            System.out.println("El mayor es: " + b);
            System.out.println("El menor es: " + a);
        } else {
            System.out.println("Ambos números son iguales.");
        }

        int diferencia = Math.abs(a - b);
        System.out.println("La diferencia absoluta es: " + diferencia);

        entrada.nextLine();
    }
    
//________________________________________________________________________________________________________________________
    public static void tablaDivision(Scanner entrada) {
        System.out.print("¿De qué número desea la tabla de división?: ");
        double n = entrada.nextDouble();

        System.out.println("\n--- Tabla de división del " + n + " ---");

        // Recorremos del 1 al 10
        for (int i = 1; i <= 10; i++) {
            double resultado = n / i;
            
            // Usamos printf para mostrar solo 2 decimales y que se vea ordenado
            System.out.printf("%.0f / %d = %.2f %n", n, i, resultado);
        }

        entrada.nextLine();
    }
//_______________________________________________________________________________________________________________________
    public static void contarDigitosPares(Scanner entrada) {
        System.out.print("Ingrese un número entero: ");
        int n = entrada.nextInt();
        
        int numeroOriginal = n;
        int contadorPares = 0;

        // Usamos el valor absoluto por si el número es negativo
        int aux = Math.abs(n);

        // Si el usuario ingresa 0, el programa debería contar 1 par
        if (aux == 0) {
            contadorPares = 1;
        } else {
            while (aux > 0) {
                int digito = aux % 10; // Extraemos el último dígito
                
                if (digito % 2 == 0) {
                    contadorPares++;
                }
                
                aux = aux / 10; 
            }
        }

        System.out.println("El número " + numeroOriginal + " tiene " + contadorPares + " dígito(s) par(es).");
        
        entrada.nextLine();
    }
//_______________________________________________________________________________________________________________________
    public static void esTriangular(Scanner entrada) {
        System.out.print("Ingrese un número para verificar si es triangular: ");
        int n = entrada.nextInt();
        
        int suma = 0;
        int k = 1;

        while (suma < n) {
            suma += k;
            k++;
        }

        if (suma == n) {
            System.out.println(n + " ES un número triangular.");
            System.out.println("Se obtiene sumando de 1 hasta " + (k - 1));
        } else {
            System.out.println(n + " NO es un número triangular.");
        }
        entrada.nextLine(); 
    }
//_________________________________________________________________________________________________________________________
    public static void promedioNegativos(Scanner entrada) {
        System.out.print("¿Cuántos números desea ingresar? ");
        int n = entrada.nextInt();
        
        int sumaNegativos = 0;
        int contadorNegativos = 0;

        for (int i = 1; i <= n; i++) {
            System.out.print("Ingrese el número " + i + ": ");
            int num = entrada.nextInt();

            // Verificamos si el número es negativo
            if (num < 0) {
                sumaNegativos += num;
                contadorNegativos++;
            }
        }

        if (contadorNegativos > 0) {
            double promedio = (double) sumaNegativos / contadorNegativos;
            System.out.println("\n--- Resultados ---");
            System.out.println("Cantidad de negativos: " + contadorNegativos);
            System.out.println("El promedio de los negativos es: " + promedio);
        } else {
            System.out.println("\nNo hay negativos.");
        }

        entrada.nextLine();
    }
//________________________________________________________________________________________________________________________
    public static void mostrarMultiplosDe6(Scanner entrada) {
        System.out.print("¿Cuántos múltiplos de 6 desea ver?: ");
        int n = entrada.nextInt();

        System.out.println("Los primeros " + n + " múltiplos de 6 son:");

        for (int i = 1; i <= n; i++) {
            int multiplo = i * 6;
            
            System.out.print(multiplo + " ");
        }

        System.out.println(); // Salto de línea al finalizar
        entrada.nextLine();   // Limpiar búfer
    }
//________________________________________________________________________________________________________________________
    public static void esPotenciaDeDos(Scanner entrada) {
        System.out.print("Ingrese un número: ");
        int n = entrada.nextInt();
        
        if (n <= 0) {
            System.out.println(n + " NO es potencia de 2.");
        } else {
            int original = n;
            while (n % 2 == 0) {
                n = n / 2;
            }

            if (n == 1) {
                System.out.println(original + " SI es potencia de 2.");
            } else {
                System.out.println(original + " NO es potencia de 2.");
            }
        }
        
        entrada.nextLine();
    }
//______________________________________________________________________________________________________________________
    public static void invertirNumero(Scanner entrada) {
        System.out.print("Ingrese un número entero: ");
        int n = entrada.nextInt();
        
        int original = n;
        int invertido = 0;
     
        int aux = Math.abs(n);

        while (aux > 0) {
            int ultimoDigito = aux % 10;           // Extraemos el de la derecha
            invertido = (invertido * 10) + ultimoDigito; // Lo "empujamos" a la izquierda
            aux = aux / 10;                        // Quitamos el dígito procesado
        }

        if (original < 0) {
            invertido = invertido * -1;
        }

        System.out.println("El número invertido es: " + invertido);
        
        entrada.nextLine();
    }
 //___________________________________________________________________________________________________________________
    public static void verificarParSuma(Scanner entrada) {
        System.out.print("Ingrese un número n: ");
        int n = entrada.nextInt();
        
        int suma = 0;

        // Calculamos la suma de 1 hasta n
        for (int i = 1; i <= n; i++) {
            suma += i;
        }

        // Verificamos si la suma es par o impar
        if (suma % 2 == 0) {
            System.out.println("La suma de 1 hasta " + n + " es " + suma + ", la cual es PAR.");
        } else {
            System.out.println("La suma de 1 hasta " + n + " es " + suma + ", la cual es IMPAR.");
        }

        entrada.nextLine(); // Limpieza de búfer
    }
//______________________________________________________________________________________________________________________
    public static void convertirCelsiusAFahrenheit(Scanner entrada) {
        System.out.print("Ingrese la temperatura en grados Celsius: ");
        double celsius = entrada.nextDouble();

        // Aplicamos la fórmula matemática
        double fahrenheit = (celsius * 9 / 5) + 32;

        // Usamos printf para mostrar un formato limpio con 2 decimales
        System.out.printf("%.2f °C equivalen a %.2f °F %n", celsius, fahrenheit);
        
        entrada.nextLine(); // Limpiar el búfer
    }
//########################################################################    
    public static void pausar(Scanner entrada) {
        System.out.println("\n--> Presione ENTER para continuar...");
        try {
            System.in.read(); // Lee un solo carácter (el Enter)
        } catch (Exception e) {
            entrada.nextLine();
        }
    }
//_______________________________________________________________________________________________________________________
    //Fin de la clase main 
    }
