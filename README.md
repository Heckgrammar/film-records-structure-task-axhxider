using System;
					
public class Program
{
	public static void Main()
	{
		Film hulk = new Film("Hulk", "12A" , 2005 , false);  
		Film ironMan = new Film("Iron Man" , "12A" , 2008 , true);
		Film antMan = new Film("Ant-Man","12A" , 2015 , false);
		Film[] filmCollection = new Film[]	{antMan, hulk, ironMan};
		int year = 0;
		int position = 0;
		
		Film newestFilm = filmCollection[0];
		
		for (int i = 1; i < filmCollection.Length; i++)
		{
			
			if (filmCollection[i].year > newestFilm.year)
			{
				newestFilm = filmCollection[i];
			}
		}
		
		Console.WriteLine(" The newest film is: " + newestFilm.title);
		
		for (int i = 0; i < filmCollection.Length; i++);
		{
			if (filmCollection[i].title == "Ant-Man")
			{
				filmCollection[i].beingShown = true;
			}
		
		}
		
		foreach (var film in filmCollection)
		{
			Console.WriteLine($"{film.title} - being shown: {film.beingShown}");
		}
		
		
	}
}
