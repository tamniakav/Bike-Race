using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Bike_Race
{
    class Program
    {
        static void Main(string[] args)
        {
            int j = int.Parse(Console.ReadLine());
            int s = int.Parse(Console.ReadLine());
            string route = Console.ReadLine();

            int allPlayers = j + s;
            decimal sum = 0;

            if (route == "cross-country")
            {
                sum = j * 8 + s * 9.50m;
                if (allPlayers >= 50)
                {
                    sum *= 0.75m;
                }
            }
            else if (route == "trail")
            {
                sum = j * 5.5m + s * 7;
            }
            else if (route == "downhill")
            {
                sum = j * 12.25m + s * 13.75m;
            }
            else if (route == "road")
            {
                sum = j * 20 + s * 21.50m;
            }

            sum *= 0.95m;

            Console.WriteLine($"{sum:f2}");
        }
    }
}
