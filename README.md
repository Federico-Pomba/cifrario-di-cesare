#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#define first_letter 'A'
#define last_letter 'Z'
int main(int argc, char *argv[]){
    int lunghezza = strlen(argv[2]);
    char letter;
    int alfabeto = last_letter-first_letter + 1;
    if(argc!=3){
        printf("errore");
        return 0;
    }
    else {
    int chiave = atoi(argv[1]);
    for(int i=0; i<lunghezza; i++){
        letter = (argv[2][i]+ (alfabeto - chiave)) % (last_letter + 1);
    if(letter<first_letter)
        letter=letter+first_letter;
    printf("%c",letter);
    }
    }
}
