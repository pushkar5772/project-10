# project-10
Mini Library Management System
#include <stdio.h>

struct Book {
    int id;
    char name[50];
};

int main() {
    struct Book books[100];
    int count = 0, choice;

    while (1) {
        printf("\n1.Add Book\n2.Show Books\n3.Exit\nChoice: ");
        scanf("%d", &choice);

        if (choice == 1) {
            printf("Enter book id: ");
            scanf("%d", &books[count].id);
            printf("Enter name: ");
            scanf("%s", books[count].name);
            count++;
        }
        else if (choice == 2) {
            for (int i = 0; i < count; i++) {
                printf("%d - %s\n", books[i].id, books[i].name);
            }
        }
        else if (choice == 3) {
            return 0;
        }
    }
}
