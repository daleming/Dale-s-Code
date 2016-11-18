# Dale-s-Code
//Just some of my code
//Try to reverse a string without library functions

#include <iostream>
#include <cstring>

char* revStr(char* ptrToString)
    {
        if (ptrToString == NULL)
            return NULL;

        char* ptrToBegin = ptrToString;
        char* ptrToEnd = ptrToBegin;

        for (;*ptrToEnd != '\0'; ++ptrToEnd);

        ptrToEnd -=1;

        while (ptrToBegin < ptrToEnd)
            {
                char temp = *ptrToBegin;
                *ptrToBegin = *ptrToEnd;
                *ptrToEnd = temp;
                ptrToBegin++;
                ptrToEnd--;
            }
        return ptrToString;
    }

int main()
    {
        char myStr[20] = "eduD olleH";
        std::cout << myStr << std::endl;
        std::cout << revStr(myStr);
        return 0;
    }
