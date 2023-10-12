using System;
using System.Linq;
using System.Numerics;
using System.Collections.Generic;
using System.Collections;
using System.Linq.Expressions;

namespace a
{
    class Program
    {
        delegate bool Predicate<T>(T a);

        private static bool Mypr<T>(T a)
        {
            if (a != null) return true;
            return false;
        }
        static void Main()
        {
            List<int> list = new List<int> { 1, 10, 17, 20, 3, 90 };
            List<string> list_2 = new List<string> { "abc" };
            List<int> b = new List<int> { 3, 2, 1 };
            b.MyWhere(x => Mypr(x)).ToList();
            Console.WriteLine(b);
        }
    }

    static class Publ
    {
        public static IEnumerable<T> MyWhere<T>(this IEnumerable<T> items, Func<T, bool> predicate)
        {
            foreach (var item in items)
            {
                if (predicate(item)) yield return item;
            }
        }
    }
}
