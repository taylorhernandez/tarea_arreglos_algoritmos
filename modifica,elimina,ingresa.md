using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
namespace Arrays
{
    class Array
    {
        static void Main()
        {
            string[] nombres;
            int indice;
            ushort num = 10;
            Console.Write(" -----Escribe 10 nombres------  \n ");
            nombres = new string[10];
            for (int i = 0; i < num; i++)
            {
                Console.Write("Escribe el nombre {0} ", i);
                nombres[i] = Console.ReadLine();
            }
            Console.WriteLine("Se han Ingresado los {0} nombres con exito !!! \n", num);
            string respuesta, nuevoNombre;
            Console.WriteLine("Desea modificar algún nombre:  ");
            respuesta = Console.ReadLine();
            respuesta = respuesta.ToUpper();
            if (respuesta.Equals("SI"))
            {
                Console.WriteLine("Ingrese el numero del listado que desea modificar;");
                indice = Convert.ToInt32(Console.ReadLine());
                
                if (indice > 0 && indice < nombres.Length)
                {
                    Console.Write("ingres el nuevo nombre de " + nombres[indice] + ": ");
                    nuevoNombre = Console.ReadLine();
                    nombres[indice] = nuevoNombre;
                }
                  else
                {
                    Console.WriteLine("el indice " + indice + "no existe en el vector ");
                }
                
            }

            Console.WriteLine("Pulsa INTRO para listarlos");
            string a = Console.ReadLine();
            for (int i = 0; i < num; i++)
            {
                Console.WriteLine("Elemento {0}: {1}", i, nombres[i]);
            }
            a = Console.ReadLine();
             {
                string delet = null; 
                Console.WriteLine("Desea eliminar algún nombre:  ");
                respuesta = Console.ReadLine();
                respuesta = respuesta.ToUpper();
                if (respuesta.Equals("SI"))
                {
                    Console.WriteLine("Ingrese el numero del listado que desea eliminar;");
                    indice = Convert.ToInt32(Console.ReadLine());
                    nombres[indice] = delet;
                    Console.ReadLine();
                        
                    }

                    Console.WriteLine("Pulsa INTRO para listarlos");
                    for (int i = 0; i < num; i++)
                    {
                        Console.WriteLine("Elemento {0}: {1}", i, nombres[i]);
                    }
                    a = Console.ReadLine();

                }

            }
        }
    }
