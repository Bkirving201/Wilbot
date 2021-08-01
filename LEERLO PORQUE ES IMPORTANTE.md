# Wilbot

Dentro de la carpeta c# encontraran mis archivos referentes al bot

Como no agarro, no abre no se porque motivo, y como ya me rendí aqui le dejo el codigo, nada mas pegan el codigo y ejecutar

using System;


    class Program
    {
        static void Main(string[] args)
        {
// Variables //
		string cliente = " ";
		String respuesta;
		String respuesta1;
		int menu;
		const int precioham = 70;
		const int preciopa = 30;
		const int preciorefr = 15;
		int pedidoham;
		int pedidopa;
		int pedidorefr;
		float totalcompra;
		
		
		//Saludo// 
		Random rnd = new Random();   //Inicia la instancia del random//
		string [] saludos = { 
		"Hola, mi nombre es Wilson, y el día de hoy seré su mesero virtual",
		"Que tal, mucho gusto, me llamo Wilson, y hoy los atendere como su mesero virtual",
		"Un gusto verle, soy Wilson, y sera un gusto ser su mesero virtual el día de hoy"};
		
		int aleatorio = rnd.Next(saludos.Length);   // Por medio de una variable guarda el random//
		
		
		Console.WriteLine("{0} \n \n",saludos[aleatorio]);
		Console.WriteLine("¿Le gustaria a usted que le llame de alguna forma especial? ");
		respuesta=Console.ReadLine();
		
			
		//Preguntar si desea el nombre o no//
		if (respuesta == "si" || respuesta == "Si")
		{
			Console.WriteLine("¿Por cual nombre quisiera que le llamara?");
			cliente=Console.ReadLine();
			Console.Clear(); 
			Console.WriteLine("Un gusto " + cliente + ", Enseguida le muestro la carta del menú \n");
			}
		else {
			Console.Clear(); 
			Console.WriteLine("Esta bien, Entiendo, un gusto atenderle ,Enseguida le muestro la carta del menú \n");
		}		
		//Acaba aqui la pedida de nombre//
		
			
		//Menu//
		Console.WriteLine("He aqui el menú del día \n");
		Console.WriteLine("-> Menú <- \n");
		Console.WriteLine("- Hamburguesa - $70 \n");
		Console.WriteLine("- Papas Individuales - $30 \n");
		Console.WriteLine("- Refresco - $15 \n");
		
		//Estructura de while para cerrar el menu y volver a la pedida de pedido//
		Console.WriteLine("Un gusto ser su mesero, psssss,disculpe, psss, ¿Quisiera que le contara un dato extra?");
		respuesta=Console.ReadLine();
		Console.Clear(); 
		
		while (respuesta == "Si" || respuesta == "si" )
	
			if (respuesta == "Si" || respuesta == "si"){
					 Console.WriteLine("jajaj sabría que iba querer, ¿Sobre que quisiera que le contara? \n");
					 Console.WriteLine("1 - Dialogo sobre quien es wilson ");
					 Console.WriteLine("2 - Acerca del restaurant ");
					 Console.WriteLine("3 - Ninguno, deseo ordenar ");
					 menu=int.Parse(Console.ReadLine());

					switch (menu) {
						case 1:
							Console.Clear(); 
							Console.WriteLine("1 - Dialogo sobre quien es wilson \n");
                            Console.WriteLine("Un gusto que te interes por mi, mi nombre es Wilson, soy un chatbot desarrollado en el lenguaje de c#  \n");
                            Console.WriteLine("Mi creador responde al nombre de Irving Noe y me ha dado una serie de funciones simples para servirle a usted \n \n");
                            Console.WriteLine("Mi nombre se encuentra inspirado de un personaje ubicado en el videojuego ´Dont Starve´ quien responde de igual forma al nombre de wilson \n");
							Console.WriteLine("¿Deseas saber algo mas?");
							respuesta=Console.ReadLine();
							Console.Clear();
							break;

						case 2:
							Console.Clear(); 
							Console.WriteLine("2 - Restaurant ");
                            Console.WriteLine("El restarant corresponde al nombre ´Rincon Azteca´ \n");
                            Console.WriteLine("Abrió sus puertas en octubre de 2001 con la finalidad de ofrecer");
                            Console.WriteLine("al público un sabor especial en la comida mexicana, en un ambiente agradable, limpio y accesible a todo presupuesto \n");
							Console.WriteLine("¿Deseas saber algo mas?");
							respuesta=Console.ReadLine();
							Console.Clear();
							break;

						case 3:
							Console.Clear();
							respuesta="No";
							break;
						default:
							//Console.WriteLine(" ");
							Console.Clear();
							break;
					}	
				
			}
		
		
		//Continuar con el pedido // 	
		
		Console.WriteLine("Entiendo, ¿Entonces digame cual sera su orden? \n");
		Console.WriteLine("¿Cuantas hamburguesas desea?");
		pedidoham = int.Parse(Console.ReadLine());
		Console.WriteLine(" ");
		Console.WriteLine("¿Cuantas Papas individuales desea?");
		pedidopa = int.Parse(Console.ReadLine());
		Console.WriteLine(" ");
		Console.WriteLine("¿Cuantos refrescos desea?");
		pedidorefr = int.Parse(Console.ReadLine());
		Console.WriteLine(" ");		
		Console.WriteLine("Un gusto atenderle, su pedido esta siendo procesado");
		

		//Hacer los calculos para los pedidos//
		pedidoham = pedidoham * precioham;
		pedidopa = pedidopa * preciopa;
		pedidorefr = pedidorefr * preciorefr;
		totalcompra = pedidoham + pedidopa + pedidorefr;
		
		//Respuesta del pedido y despedida//
		Console.Clear();
		Console.WriteLine("Ya he vuelto, su total es de $ " + totalcompra);
		Console.WriteLine(" ");
		Console.WriteLine("Espero disfrutara de su comida, permitame preguntarle, ¿He sido un buen mesero para usted?");
		respuesta1 = Console.ReadLine();
		
		if (respuesta1 == "Si" || respuesta1 == "si"){

			Console.WriteLine("Muchas gracias, he dado mi mayor esfuerzo"); }
		
		else {
		Console.WriteLine("Lamento oir eso, para la proxima pondré a trabajar mis transistores al máximo");	
		}
    Console.ReadKey();
        }
}
