# Detect_Capital

Given a word, you need to judge whether the usage of capitals in it is right or not.

We define the usage of capitals in a word to be right when one of the following cases holds:

All letters in this word are capitals, like "USA".
All letters in this word are not capitals, like "leetcode".
Only the first letter in this word is capital if it has more than one letter, like "Google".
Otherwise, we define that this word doesn't use capitals in a right way.


Example 1:
Input: "USA"
Output: True


Example 2:
Input: "FlaG"
Output: False
Note: The input will be a non-empty word consisting of uppercase and lowercase latin letters.



## submission solution

```c

bool detectCapitalUse(char* word) {
    int size = strlen(word);
    
    if(*(word) >= 'A' && *(word) <= 'Z'){
        if(*(word+1) >= 'A' && *(word+1) <= 'Z'){
            for(int i=1 ; i<size ; i++){
                if(*(word+i) >= 'a' && *(word+i) <= 'z'){
                    return false;
                }
            }
        }
        else{
            for(int i=1 ; i<size ; i++){
                if(*(word+i) >= 'A' && *(word+i) <= 'Z'){
                    return false;
                }
            }
        }
    }
    else{
        for(int i=0 ; i<size ; i++){
            if( *(word+i) >= 'A' && *(word+i) <= 'Z' ){
                return false;
            }
        }
    }
    return true;
}


```

![Detect_Capital.png](./Detect_Capital.png)