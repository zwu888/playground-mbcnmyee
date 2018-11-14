# Use 
/*
 * Function hasUniqueChars2
 * Args - std::string
 * Output:: True if string has all characters which are unique
 *          False if string has at least one repeated char.
 * Assumption:: string only contains (a..z), 26 chars.
 */
```C++ runnable
#include<iostream>
#include<string>

using namespace std;

bool hasUniqueChars2( std::string str)
{
    int check = 0;
    int len = str.length();
    for (int i = 0; i < len; ++i)
    {
        int c = (int)(str[i] - 'a');
        cout << c << endl;
        if ( check & ( 1 << c ) ) {
            return false;
        }
        check |= ( 1 << c);
    }
    return true;
}

int main()
{
    std::string in="abbc";
    cout << hasUniqueChars2(in) << endl;
}
