using System;
using System.Linq;
using System.Collections.Generic;
using System.Xml.Linq;
using System.Collections;

public class MainClass
{
    public static void Main()
    {
        List<Suspect> suspects = new List<Suspect>();
        for (int i = int.Parse(Console.ReadLine()); i > 0; i--)
        {
            var a = Console.ReadLine().Split(", ");
            suspects.Add(new Suspect(a[0], Convert.ToBoolean(a[1]), Convert.ToBoolean(a[2])));
        }
        suspects.MySingle();
    }
}

public class Suspect
{
    public string Name;
    public bool Alibi;
    public bool Motive;

    public Suspect(string name, bool alibi, bool motive)
    {
        Name = name;
        Alibi = alibi;
        Motive = motive;
    }
}

public static class Extension1
{
    public static IEnumerable<Suspect> Items { get; private set; }

    public static void MySingle(this IEnumerable<Suspect> items)
    {
        Items = items;
        bool flag = false;
        string name = null;
        foreach (Suspect b in items)
        {
            if (b.Alibi == false && b.Motive == true)
            {
                if (flag) { Console.Write("Тупик"); return; }
                name = b.Name;
            }
        }
        Console.Write(name);
    }
}
