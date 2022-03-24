#include<stdio.h>
#include<stdlib.h>
struct Patron{
    int id;
    char name[50];
    char email[100];
    char password[50];
};
struct Book{
    char name[50];
    char author[50];
    int pages;
    char genre[50];
};


void menu();
void add_patron();
void view_patron();
void add_book();
void view_book();




int main()
{
    char tittle[50]= "county library management";
    char name[10]= "kevin\n";
    printf("\t\t%s\n\t\t%s", tittle, name);
    menu();

}


void menu()
{
    int action;
    do {
          printf("\t\t 1.add patron\n");
          printf("\t\t 2.view patron\n");
          printf("\t\t 3.add book\n");
          printf("\t\t 4.view book\n");
          printf("\t\t 0.exit\n");
          printf("\t\t select one action: ");
          scanf("\t\t%d", &action);

          switch(action){

              case 1:
                add_patron();
                break;

              case 2:
                view_patron();
                break;

              case 3:
                add_book();
                break;

              case 4:
                view_book();
                break;

              case 0:
                exit(1);

              default:
                ("invalid action");
          }
          system("cls");
    } while (action!=0);

}
void add_patron()
{
    system("cls");
    struct Patron patron;
    printf("\t\t\tAdd new patron\n");
    printf("\t\t patron name: ");
    scanf("%s", patron.name);
    printf("\t\t patron email: ");
    scanf("%s", patron.email);
    printf("\t\t password\n");



}
void view_patron()
{
    system("cls");
    struct Patron patron;
    getchar();
    printf("patron %s.\n", patron.name);
    printf("email %s.\n", patron.email);
    printf("password %s.\n", patron.password);
    printf("ID %s.\n", patron.id);
    getchar();
}
void add_book()
{
    system("cls");
    struct Book book;

    printf("\t\t\tAdd New book: \n");
    printf("\t\t book name");
    scanf("%s.\n", book.name);
    printf("\t\t author name");
    scanf("%s.\n", book.author);
    printf("\t\t book genre");
    scanf("%s.\n", book.genre);
    printf("\t\t book pages");
    scanf("%d.\n", book.pages);

}
void view_book()
{
    struct Book book;
    getchar();
    printf("\t\t\t view book: \n" );
    printf("\t\t book %s.\n", book.name );
    printf("\t\t author %s.\n", book.author );
    printf("\t\t genre %s.\n", book.genre);
    printf("\t\t pages %d.\n", book.pages);
    getchar();
}
