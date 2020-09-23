<div align="center">

## AI\-Hanoi


</div>

### Description

Shows simple algorithm solving the Hanoi Towers. This is a very basic Artificial Intelligence example of how the computer can solve such problems.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Larry Bray](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/larry-bray.md)
**Level**          |Beginner
**User Rating**    |4.3 (13 globes from 3 users)
**Compatibility**  |C\#
**Category**       |[Algorithims](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/algorithims__10-29.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/larry-bray-ai-hanoi__10-3632/archive/master.zip)





### Source Code

```
using System;
namespace AI
{
	class Hanoi
	{
		[STAThread]
		static void solveTowers(int count, char source, char dest, char spare)
		{
			if (count == 1)
				Console.WriteLine("Move top disk from pole {0} to pole {1}", source, dest);
			else
			{
				solveTowers(count-1, source, spare, dest);
				solveTowers(1, source, dest, spare);
				solveTowers(count-1, spare, dest, source);
			}
		} //ends solveTowers
		static void Main(string[] args)
		{
			int myCount;
			char mySource, myDest, mySpare;
			Console.Write("Enter number of rings: ");
			myCount = Convert.ToInt16(Console.ReadLine());
			Console.Write("Enter letter of peg to put rings on: ");
			mySource = Convert.ToChar(Console.ReadLine());
			Console.Write("Enter letter of peg to move rings to: ");
			myDest = Convert.ToChar(Console.ReadLine());
			Console.Write("Enter letter of spare peg: ");
			mySpare = Convert.ToChar(Console.ReadLine());
			solveTowers(myCount, mySource, myDest, mySpare);
			Console.ReadLine();
		}
	} //ends Hanoi class
} //ends AI namespace
```

