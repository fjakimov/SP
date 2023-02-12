#include <stdio.h>
#include <ctype.h>
#include <string.h>

void writeToFile() {
    FILE *f = fopen("text.txt", "w");
    char c;
    while((c = getchar()) != '#') {
        fputc(c, f);
    }
    fclose(f);
}
int isVowel(char letter){
    return tolower(letter)=='a' || tolower(letter)=='i' || tolower(letter)=='o' || tolower(letter)=='u' || tolower(letter)=='e';
}

int main() {

    writeToFile();
    FILE *f = fopen("text.txt","r");
    char curr,other='$';
    int vowelCounter=0;
    while((curr= fgetc(f))!=EOF){
        isVowel(curr);
        isVowel(other);
        if(isVowel(curr)){
            if(isVowel(other)){
                vowelCounter++;
                printf("%c%c", tolower(other), tolower(curr));
            }
            other=curr;
        }
        else {
            other='$';
        }
    }
    printf("%d",vowelCounter);
    // Vasiot kod zapocnuva od tuka
    fclose(f);

    return 0;
}
