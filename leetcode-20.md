## leetcode 20题--C#

	public class Solution
    {
        public bool IsValid(string s)
        {
            Dictionary<char, char> parenth_dict = new Dictionary<char, char>();
            parenth_dict['('] = ')';
            parenth_dict['{'] = '}';
            parenth_dict['['] = ']';

            Stack<char> aux = new Stack<char>();

            for (int i = 0; i < s.Length; i++)
            {
                if (s[i] == '(' || s[i] == '{' || s[i] == '[')
                    aux.Push(s[i]);
                else if ( aux.Count()==0 || parenth_dict[aux.Peek()] != s[i])
                    return false;
                else
                    aux.Pop();
            }

            return aux.Count()==0;
        }
    }
